# Spesifikasi Arsitektur API Platform: Geny StuntCare
## Standar Kontrak Endpoint RESTful, Deteksi Stunting WHO, Integrasi Posyandu, dan Interoperabilitas SatuSehat

Dokumen ini mendefinisikan spesifikasi arsitektur antarmuka pemrograman aplikasi (Application Programming Interface / API) untuk platform **Geny StuntCare** (`genystuntcare.com`). Spesifikasi ini menjadi acuan tunggal dalam pengembangan modul backend, aplikasi web, dashboard kader posyandu, serta integrasi data surveilans faskes tingkat puskesmas dan dinas kesehatan.

---

## 1. Metadata & Prinsip Arsitektur API

| Parameter | Keterangan Detail |
| :--- | :--- |
| **Nama Sistem** | **Geny StuntCare Core API** |
| **Domain Platform** | `genystuntcare.com` |
| **Base URL Produksi** | `https://api.genystuntcare.com/v1` |
| **Base URL Staging** | `https://staging-api.genystuntcare.com/v1` |
| **Protokol** | HTTPS / TLS 1.3 (Wajib Terenkripsi) |
| **Format Pertukaran Data** | JSON (`application/json; charset=utf-8`) |
| **Format Tanggal & Waktu** | ISO 8601 UTC (`YYYY-MM-DDTHH:mm:ssZ`) |
| **Penyelaras Standar Gizi** | Kurva Pertumbuhan WHO Child Growth Standards (MGRS) & Permenkes No. 2 Tahun 2020 |
| **Interoperabilitas Faskes** | Format HL7 FHIR (Fast Healthcare Interoperability Resources) Kemenkes SatuSehat |
| **Penyusun & Penanggung Jawab** | **Gerrard Sebastian** (Anggota Tim Geny StuntCare) |

```
+---------------------------------------------------------------------------------------------------+
|                              TOPOLOGI & ALUR KOMUNIKASI API GENY STUNTCARE                        |
+---------------------------------------------------------------------------------------------------+
|                                                                                                   |
|  [Ibu Balita / Web Mobile]    [Kader Posyandu / Tablet]    [Puskesmas & Dinkes / Dashboard B2G]   |
|               \                           |                           /                           |
|                \                          |                          /                            |
|                 +-------------------------+-------------------------+                             |
|                                           |                                                       |
|                                           v                                                       |
|                          [Cloudflare WAF & Edge Cache]                                            |
|                                           |                                                       |
|                                           v                                                       |
|                     [API Gateway: api.genystuntcare.com/v1]                                       |
|                                           |                                                       |
|                     +---------------------+---------------------+                                 |
|                     |                     |                     |                                 |
|                     v                     v                     v                                 |
|             [Layanan Auth]       [Mesin Z-Score WHO]    [Modul Laporan Posyandu]                  |
|             [JWT & RBAC]         [Deteksi Stunting]     [Export Agregat Faskes]                   |
|                     |                     |                     |                                 |
|                     +---------------------+---------------------+                                 |
|                                           |                                                       |
|                                           v                                                       |
|                        [Basis Data Relasional & Cache Redis]                                      |
|                                           |                                                       |
|                                           v                                                       |
|                   [Layanan Eksternal: SatuSehat Kemenkes (FHIR)]                                  |
|                                                                                                   |
+---------------------------------------------------------------------------------------------------+
```

---

## 2. Autentikasi, Otorisasi, & Hak Akses (RBAC)

API Geny StuntCare menerapkan otorisasi berbasis peran (*Role-Based Access Control* / RBAC). Kredensial dikirimkan melalui header HTTP standar:  
`Authorization: Bearer <access_token>`

### Matriks Peran Pengguna:
1. `parent` (Orang Tua / Ibu Balita): Akses riwayat pertumbuhan anak pribadi, rekomendasi menu MPASI, dan konsultasi.
2. `cadre` (Kader Posyandu): Input data antropometri massal di hari buka posyandu, rekapitulasi data balita satu RW/desa.
3. `faskes_admin` (Tenaga Kesehatan / Puskesmas): Monitoring prevalensi stunting tingkat kecamatan, verifikasi rujukan gizi.
4. `superadmin` (Tim Pengembang Geny StuntCare): Konfigurasi sistem global, audit log, dan integrasi API SatuSehat.

---

## 3. Spesifikasi Kelompok Endpoint API

### A. Layanan Autentikasi Pengguna (`/auth`)

#### 1. Registrasi Akun Pengguna Baru
* **Endpoint:** `POST /auth/register`
* **Hak Akses:** Publik
* **Payload Request:**
  ```json
  {
    "full_name": "Rina Kartika",
    "email": "rina.kartika@example.com",
    "phone_number": "081234567890",
    "password": "PasswordKuat123!",
    "role": "parent",
    "city_code": "35.07",
    "subdistrict_name": "Kepanjen",
    "posyandu_id": "pos-malang-042"
  }
  ```
* **Format Response Sukses (`201 Created`):**
  ```json
  {
    "success": true,
    "message": "Registrasi berhasil. Silakan verifikasi nomor ponsel Anda.",
    "data": {
      "user_id": "usr-889102",
      "full_name": "Rina Kartika",
      "email": "rina.kartika@example.com",
      "role": "parent",
      "created_at": "2026-09-25T10:00:00Z"
    }
  }
  ```

#### 2. Masuk Akun (Login)
* **Endpoint:** `POST /auth/login`
* **Hak Akses:** Publik
* **Payload Request:**
  ```json
  {
    "identifier": "081234567890",
    "password": "PasswordKuat123!"
  }
  ```
* **Format Response Sukses (`200 OK`):**
  ```json
  {
    "success": true,
    "data": {
      "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
      "refresh_token": "def5020038910a...",
      "expires_in": 3600,
      "token_type": "Bearer",
      "user": {
        "user_id": "usr-889102",
        "full_name": "Rina Kartika",
        "role": "parent"
      }
    }
  }
  ```

---

### B. Manajemen Data Profil Balita (`/children`)

#### 1. Mendaftarkan Profil Balita Baru
* **Endpoint:** `POST /children`
* **Hak Akses:** `parent`, `cadre`, `faskes_admin`
* **Payload Request:**
  ```json
  {
    "full_name": "Aisyah Putri",
    "nik": "3507123456780001",
    "gender": "female",
    "birth_date": "2025-03-15",
    "birth_weight_kg": 3.1,
    "birth_length_cm": 49.0,
    "head_circumference_birth_cm": 34.0,
    "is_premature": false,
    "gestational_age_weeks": 39,
    "parent_user_id": "usr-889102",
    "posyandu_id": "pos-malang-042"
  }
  ```
* **Format Response Sukses (`201 Created`):**
  ```json
  {
    "success": true,
    "data": {
      "child_id": "chd-771204",
      "full_name": "Aisyah Putri",
      "nik": "3507123456780001",
      "gender": "female",
      "birth_date": "2025-03-15",
      "age_in_months": 18,
      "created_at": "2026-09-25T10:05:00Z"
    }
  }
  ```

#### 2. Mengambil Profil Balita dan Ringkasan Status
* **Endpoint:** `GET /children/{id}`
* **Hak Akses:** Pemilik profil (`parent`), kader wilayah, nakes faskes
* **Format Response Sukses (`200 OK`):**
  ```json
  {
    "success": true,
    "data": {
      "child_id": "chd-771204",
      "full_name": "Aisyah Putri",
      "gender": "female",
      "birth_date": "2025-03-15",
      "age_in_months": 18,
      "latest_measurement": {
        "date": "2026-09-20",
        "weight_kg": 8.9,
        "height_cm": 78.5,
        "head_circumference_cm": 46.0,
        "nutrition_status": "Gizi Baik",
        "stunting_status": "Normal",
        "stunting_risk_level": "LOW"
      }
    }
  }
  ```

---

### C. Modul Antropometri & Kalkulator Z-Score WHO (`/anthropometry`)

#### 1. Input Data Pengukuran Antropometri Rutin
* **Endpoint:** `POST /anthropometry/records`
* **Hak Akses:** `parent`, `cadre`, `faskes_admin`
* **Payload Request:**
  ```json
  {
    "child_id": "chd-771204",
    "measurement_date": "2026-09-20",
    "weight_kg": 8.9,
    "height_cm": 78.5,
    "head_circumference_cm": 46.0,
    "measurement_posture": "standing",
    "lila_cm": 14.5,
    "notes": "Anak aktif, baru sembuh batuk 3 hari lalu"
  }
  ```
* **Format Response Sukses (`201 Created`):**
  ```json
  {
    "success": true,
    "message": "Data pengukuran berhasil disimpan dan dikalkulasi terhadap kurva WHO.",
    "data": {
      "record_id": "rec-994120",
      "child_id": "chd-771204",
      "measurement_date": "2026-09-20",
      "age_months_calculated": 18,
      "z_scores": {
        "wfa_zscore": -0.85,
        "hfa_zscore": -0.62,
        "wfh_zscore": -0.74,
        "bfa_zscore": -0.58
      },
      "classifications": {
        "weight_for_age": "Berat Badan Normal",
        "height_for_age": "Normal",
        "weight_for_height": "Gizi Baik (Normal)",
        "bmi_for_age": "Gizi Baik"
      }
    }
  }
  ```

#### 2. Mengambil Data Grafik Pertumbuhan Balita (*Growth Chart*)
* **Endpoint:** `GET /anthropometry/growth-chart/{child_id}?indicator=hfa`
* **Parameter Query:**
  - `indicator`: Pilihan indikator kurva: `wfa` (BB/U), `hfa` (TB/U), `wfh` (BB/TB), atau `all`.
* **Format Response Sukses (`200 OK`):**
  ```json
  {
    "success": true,
    "data": {
      "child_id": "chd-771204",
      "indicator": "hfa",
      "who_reference_curves": {
        "sd_minus_3": [45.4, 53.2, 57.1, 60.0, 62.5, 65.0, 67.2, 69.1, 71.0, 72.8, 74.5, 76.1],
        "sd_minus_2": [47.3, 55.6, 59.6, 62.7, 65.3, 67.8, 70.0, 72.0, 74.0, 75.8, 77.5, 79.2],
        "sd_median": [49.1, 57.7, 61.9, 65.3, 68.0, 70.6, 72.8, 74.9, 77.0, 78.9, 80.7, 82.5],
        "sd_plus_2": [51.0, 59.9, 64.3, 67.9, 70.7, 73.4, 75.6, 77.8, 80.0, 82.0, 83.9, 85.8]
      },
      "actual_measurements": [
        { "month": 0, "height_cm": 49.0, "zscore": -0.05 },
        { "month": 6, "height_cm": 67.5, "zscore": -0.12 },
        { "month": 12, "height_cm": 74.2, "zscore": -0.35 },
        { "month": 18, "height_cm": 78.5, "zscore": -0.62 }
      ]
    }
  }
  ```

---

### D. Mesin Deteksi Dini & Peringatan Risiko Stunting (`/stunting-warning`)

#### 1. Evaluasi Risiko Stunting Otomatis (*Early Warning Evaluation*)
* **Endpoint:** `POST /stunting-warning/evaluate/{child_id}`
* **Logika Deteksi:**
  1. *Faltering Growth Check:* Memeriksa apakah bobot badan anak tidak mengalami kenaikan selama 2 kali penimbangan berurutan.
  2. *Z-Score Trend Check:* Memeriksa apakah terjadi deviasi tajam kurva TB/U mendekati batas ambang `-2 SD`.
* **Format Response Sukses (`200 OK`):**
  ```json
  {
    "success": true,
    "data": {
      "child_id": "chd-771204",
      "risk_level": "MODERATE",
      "risk_score": 65,
      "detected_anomalies": [
        {
          "type": "GROWTH_FALTERING",
          "severity": "WARNING",
          "description": "Kenaikan berat badan bulan ini (100 gram) di bawah Kenaikan Berat Badan Minimal (KBM: 200 gram)."
        }
      ],
      "action_recommendations": [
        "Tingkatkan asupan protein hewani minimal 2 porsi sehari (telur ayam dan hati ayam).",
        "Jadwalkan kunjungan konseling gizi bersama nakes di Puskesmas terdekat dalam 7 hari.",
        "Pantau berat badan ulang pada 14 hari ke depan."
      ],
      "notification_dispatched": {
        "parent_sms": true,
        "cadre_alert": true
      }
    }
  }
  ```

---

### E. Rekomendasi Menu MPASI & Pangan Lokal Terjangkau (`/nutrition`)

#### 1. Rekomendasi Menu MPASI Personalisasi
* **Endpoint:** `GET /nutrition/mpasi-plans?age_months=18&cost_tier=budget`
* **Format Response Sukses (`200 OK`):**
  ```json
  {
    "success": true,
    "data": {
      "age_category": "12-23 bulan",
      "texture_recommendation": "Makanan keluarga yang dicincang atau diiris halus",
      "frequency_per_day": "3-4 kali makan utama + 1-2 kali selingan",
      "daily_menu_suggestion": {
        "pagi": {
          "title": "Nasi Tim Hati Ayam Cincang & Wortel",
          "primary_protein": "Hati Ayam (30 gram)",
          "cost_estimate_idr": 4500
        },
        "siang": {
          "title": "Nasi Sup Ikan Kembung Kuah Bening",
          "primary_protein": "Ikan Kembung Lokal (40 gram)",
          "cost_estimate_idr": 6000
        },
        "malam": {
          "title": "Nasi Telur Puyuh Orak-Arik Bayam",
          "primary_protein": "Telur Puyuh (3 butir) / Telur Ayam (1 butir)",
          "cost_estimate_idr": 4000
        }
      },
      "estimated_daily_protein_gram": 18.5,
      "estimated_total_cost_idr": 14500
    }
  }
  ```

---

### F. Posyandu Digital Hub & Laporan Surveilans Faskes (`/posyandu`)

#### 1. Input Data Pengukuran Massal Hari Buka Posyandu (*Batch Record*)
* **Endpoint:** `POST /posyandu/sessions/{session_id}/batch-records`
* **Hak Akses:** `cadre`, `faskes_admin`
* **Payload Request:**
  ```json
  {
    "session_date": "2026-09-20",
    "posyandu_id": "pos-malang-042",
    "measurements": [
      {
        "child_id": "chd-771204",
        "weight_kg": 8.9,
        "height_cm": 78.5,
        "head_circumference_cm": 46.0,
        "posture": "standing"
      },
      {
        "child_id": "chd-771205",
        "weight_kg": 11.2,
        "height_cm": 85.0,
        "head_circumference_cm": 48.0,
        "posture": "standing"
      }
    ]
  }
  ```
* **Format Response Sukses (`200 OK`):**
  ```json
  {
    "success": true,
    "message": "2 data pengukuran berhasil diverifikasi dan disimpan.",
    "data": {
      "processed_count": 2,
      "alerts_generated": 1,
      "sync_timestamp": "2026-09-20T11:45:00Z"
    }
  }
  ```

#### 2. Dashboard Agregat Prevalensi Stunting Wilayah (B2G Endpoint)
* **Endpoint:** `GET /posyandu/analytics/district-summary?subdistrict_id=sub-kepanjen`
* **Hak Akses:** `faskes_admin`, `superadmin`
* **Format Response Sukses (`200 OK`):**
  ```json
  {
    "success": true,
    "data": {
      "subdistrict_name": "Kepanjen",
      "reporting_period": "2026-09",
      "total_target_toddlers": 1420,
      "total_measured_toddlers": 1280,
      "coverage_rate_percentage": 90.14,
      "stunting_summary": {
        "very_short_count": 48,
        "short_count": 182,
        "normal_count": 1020,
        "tall_count": 30,
        "stunting_prevalence_percentage": 17.97
      },
      "who_target_met": true,
      "national_rpjmn_target_gap_percentage": 3.97
    }
  }
  ```

---

### G. Interoperabilitas SatuSehat Kemenkes (HL7 FHIR Mapping)

Geny StuntCare menyediakan adapter otomatis untuk mentransformasikan data penimbangan lokal ke dalam struktur standar **FHIR Observation** SatuSehat Kemenkes RI:

* **Endpoint Integrasi:** `POST /integration/satusehat/fhir-sync/{record_id}`
* **Pemetaan Resource FHIR:**
  - `subject`: `Patient/{ihs_number}` (Nomor IHS Anak di SatuSehat).
  - `code`: `LOINC 8302-2` (Body height) dan `LOINC 29463-7` (Body weight).
  - `valueQuantity`: Nilai numerik dalam satuan `cm` dan `kg`.
  - `interpretation`: Kode SNOMED CT status gizi anak.

---

## 4. Format Respons Standar & Penanganan Kesalahan (Error Handling)

Setiap respons error dari API Geny StuntCare mengikuti standar **RFC 7807 (Problem Details for HTTP APIs)**:

```json
{
  "type": "https://genystuntcare.com/errors/growth-faltering-detected",
  "title": "Data Pengukuran Memerlukan Verifikasi",
  "status": 422,
  "detail": "Tinggi badan anak tercatat lebih rendah 2 cm dibanding pengukuran bulan sebelumnya. Mohon periksa kembali posisi ukur.",
  "instance": "/v1/anthropometry/records/chd-771204",
  "code": "MEASUREMENT_REGRESSION_ERROR",
  "timestamp": "2026-09-25T10:10:00Z"
}
```

### Tabel Status Kode HTTP:
| Kode Status | Kategori | Arti & Skenario Penggunaan |
| :---: | :--- | :--- |
| **200 OK** | Sukses | Permintaan GET, PUT, atau POST evaluasi berhasil diproses. |
| **201 Created** | Sukses | Data profil balita atau record pengukuran baru berhasil disimpan. |
| **400 Bad Request** | Kesalahan Klien | Format JSON tidak valid atau parameter wajib tidak disertakan. |
| **401 Unauthorized** | Autentikasi | Token akses JWT tidak disertakan atau telah kedaluwarsa. |
| **403 Forbidden** | Otorisasi | Pengguna tidak memiliki hak akses pada data anak atau wilayah tersebut. |
| **404 Not Found** | Sumber Daya | Balita, data antropometri, atau akun posyandu tidak ditemukan. |
| **422 Unprocessable** | Validasi Domain | Nilai pengukuran tidak realistis (misal: berat badan negatif atau deviasi ekstrem). |
| **429 Too Many Req** | Batas Laju | Melebihi ambang batas pemanggilan API (Rate limit: 120 req/menit). |
| **500 Internal Error**| Kesalahan Server | Kegagalan koneksi basis data atau mesin kalkulasi WHO. |

---

## 5. Keamanan Data Medis & Kepatuhan Perlindungan Data Pribadi (UU PDP)

1. **Enkripsi End-to-End & At-Rest:** Seluruh NIK anak, identitas orang tua, dan rekam medis tumbuh kembang dienkripsi menggunakan algoritma **AES-256-GCM** pada level basis data.
2. **Sanitasi Data Agregat:** Endpoint analitik untuk pihak eksternal (Dinas Kesehatan, CSR, peneliti) hanya menyajikan data agregasi tanpa identitas personal (*anonymized & aggregated data*).
3. **Audit Trail Lengkap:** Setiap aktivitas baca (*read*), ubah (*update*), dan hapus (*delete*) pada data medis balita dicatat di tabel audit yang tidak dapat diubah (*append-only log*).

---
<p align="center">
  <em>Dokumen spesifikasi API resmi ini disusun dan dipelihara untuk platform Geny StuntCare : Program Inkubasi Startup Batch 24 Bandung Techno Park (Telkom University).</em>
</p>
