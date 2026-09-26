# 🔄 Alur Kerja Terintegrasi & Master Architecture Flow

> **Arsitektur Alur Kerja Menyeluruh: Dari Data Crawling Multi-Sumber, Triangulasi Bukti Ilmiah, Rekayasa Data Mikro SKI 2023, Pemodelan AI (Fuzzy & Decision Tree), hingga Eksekusi Lapangan Startup Geny StuntCare**  
> Bagian dari Modul: **[05-laporan-data-crawling](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/README.md)**  
> Disusun oleh: **Gerrard Sebastian** | Tanggal: **26 September 2026**

---

## 1. Master Architecture Overview

Alur kerja riset dan pengembangan teknologi dalam proyek **Geny StuntCare** menggabungkan empat subsistem yang saling mengunci (*interlocking pipelines*):
1. **Pipeline Triangulasi Ilmiah**: Memvalidasi hipotesis determinan melalui konvergensi literatur, data kuantitatif lapangan, dan wawancara kasus negatif.
2. **Pipeline Rekayasa Data Mikro Survei Nasional**: Membersihkan dan memvalidasi data mikro SKI 2023 berskala 304.193 balita.
3. **Pipeline Evolusi Algoritma Kecerdasan Buatan**: Mengembangkan pemodelan dari *Fuzzy Inference System* + *Genetic Algorithm* (Buku TA) menjadi *CART Decision Tree* (Paper GENY).
4. **Pipeline Validasi Pasar & Inkubasi Startup BTP**: Menerapkan model ke dalam produk kerja kader *offline-first* yang terintegrasi dengan Posyandu ILP dan Program Makan Bergizi Gratis (MBG 3B).

```mermaid
graph TB
    subgraph S1 ["1. Data Crawling & Literature Extraction"]
        C1["Consensus AI (102 Hlm, 22 PECO/PICO)"]
        C2["Dataset 20 Paper UCD & mHealth (CSV)"]
        C3["Survei Nasional SKI 2023 & SSGI 2024"]
        C4["Korpus NotebookLM & 13 Visualisasi"]
    end

    subgraph S2 ["2. Audit Forensik & Laporan Final (27 Hlm)"]
        A1["Eliminasi 13 Klaim Usang / Halusinasi"]
        A2["Sintesis Kuantitatif: BBLR aOR 2.55; Finansial aOR 0.47"]
        A3["Sintesis Kualitatif: 6 Tema Hambatan Lapangan"]
        A4["Triangulasi 3 Sumber & Kriteria Gugur H1-H6"]
    end

    subgraph S3 ["3. Pemodelan AI & Validasi Saintifik"]
        M1["Buku TA: Fuzzy Sugeno + GA (Kalteng n=389)<br>• Dual HAZ Baseline Lahir vs Saat Ini<br>• Koreksi Tautan Ibu & Bias Umur"]
        M2["Paper GENY: Decision Tree CART (Nasional n=304.193)<br>• Akurasi 75.57%, Screening PPV 92.76%<br>• Bukti Dominasi TB/Usia 98.23% (Batas WHO)<br>• Hand-executable 1 Lembar di Posyandu"]
    end

    subgraph S4 ["4. Deployment Produk & Inkubasi BTP Batch 24"]
        P1["Geny StuntCare Mobile App (Offline-First)"]
        P2["Pilot Lapangan: Desa Siwalanpanji, Sidoarjo"]
        P3["Integrasi B2G: Kader Posyandu ILP & SPPG MBG 3B"]
    end

    S1 --> S2
    S2 --> S3
    S3 --> S4
```

---

## 2. Flow 1: Triangulasi Bukti Ilmiah (Revisi Laporan Final)

Salah satu kelemahan umum riset stunting adalah menarik kesimpulan kausal hanya dari wawancara kualitatif beberapa informan atau studi *cross-sectional* kecil dengan nilai OR ekstrem. Flow triangulasi Laporan Final memastikan bahwa klaim hanya dibuat setelah terkonfirmasi oleh minimal 2 dari 3 sumber independen:

```mermaid
sequenceDiagram
    autonumber
    actor Peneliti as Tim Riset Geny
    participant Lit as Literatur Sekunder (Consensus & PubMed)
    participant FieldQ as Data Lapangan Kuantitatif (Antropometri, HFIAS, MDD)
    participant FieldQual as Wawancara Purposif (Sel A-E & Posyandu)
    participant Decision as Gerbang Validasi Triangulasi

    Peneliti->>Lit: Ekstraksi bukti sekunder & meta-analisis
    Lit-->>Peneliti: Odds Ratio, confidence interval, dan bukti kontra
    Peneliti->>Peneliti: Susun Draft Hipotesis H1-H6 + Kriteria Gugur
    
    par Pengumpulan Bukti Lapangan
        Peneliti->>FieldQ: Ukur TB/U (papan standar WHO), HFIAS 9-item, MDD 8 kelompok pangan
        FieldQ-->>Peneliti: Dataset numerik berstandar z-score WHO Anthro
    and
        Peneliti->>FieldQual: Wawancara mendalam kasus positif deviance & kasus negatif
        FieldQual-->>Peneliti: Transkrip tema T1-T6 (hambatan daya beli, stigma, otonomi ibu)
    end

    Peneliti->>Decision: Uji silang pola data vs kriteria gugur
    alt Terbukti konsisten di minimal 2 sumber
        Decision-->>Peneliti: VALID: Diterima sebagai dasar fitur & proposisi nilai startup
    else Terdapat kontradiksi atau tidak konsisten
        Decision-->>Peneliti: REVISI / GUGUR: Catat terbuka sebagai keterbatasan riset
    end
```

### 6 Hipotesis Riset & Kriteria Gugur (Laporan Final Bagian 9):
- **H1 (Finansial Lewat Pangan)**: Efek finansial disalurkan lewat ketahanan pangan dan kualitas MP-ASI. *(Kriteria Gugur: Asosiasi pendapatan dan stunting tidak melemah setelah ketahanan pangan dikontrol)*.
- **H2 (Pendidikan Lewat Pengetahuan)**: Efek pendidikan ibu dimediasi oleh pengetahuan terapan dan pemanfaatan ANC. *(Kriteria Gugur: Mediator pengetahuan tidak berbeda antarjenjang pendidikan)*.
- **H3 (Pengetahuan Tanpa Daya Beli)**: Pengetahuan tanpa daya beli tidak menurunkan risiko stunting. *(Kriteria Gugur: Pengetahuan terbukti protektif setara di semua strata pendapatan)*.
- **H4 (Jajanan Keluarga Mampu)**: Pada keluarga mampu, pola konsumsi jajanan ultra-proses menjadi pendorong stunting. *(Kriteria Gugur: Pola jajan sama antara balita stunting dan normal di kelompok mampu)*.
- **H5 (Status Kerja Ibu)**: Dampak kerja ibu bergantung pada jenis kerja dan kualitas pengasuh pengganti. *(Kriteria Gugur: Tidak ada perbedaan menurut jenis pekerjaan)*.
- **H6 (Positive Deviance)**: Keluarga miskin dengan anak sehat memiliki praktik belanja dan jejaring yang dapat direplikasi. *(Kriteria Gugur: Tidak ditemukan praktik pembeda)*.

---

## 3. Flow 2: Pipeline Rekayasa Data Mikro Survei Nasional SKI 2023

Pipeline data mikro yang digunakan pada Paper GENY dan Laporan Final Addendum 12 menangani 304.193 balita melalui protokol pembersihan ketat:

```mermaid
flowchart TD
    subgraph Ingestion ["1. Data Ingestion & Key Normalization"]
        F1["balita.csv<br>(306.281 baris x 33 kolom)<br>Kunci: IDRT 'R000001'"]
        F2["rumahtangga.csv<br>(315.646 baris x 16 kolom)<br>Kunci: IDRT Bilangan Bulat"]
        F3["individu.csv<br>(877.531 baris x 413 kolom)<br>Kunci: IDRT & NO_IBU"]
        
        F1 --> K1["Normalisasi IDRT menjadi Bilangan Bulat Standar"]
        F2 --> K1
        F3 --> K1
    end

    subgraph Merging ["2. Multi-Level Relational Join"]
        K1 --> J1["Join Balita + Rumah Tangga (100% Match via IDRT)"]
        K1 --> J2["Join Balita + Individu Ibu (75.2% Match via IDRT)"]
        J1 & J2 --> J3["Dataset Mentah Tergabung: 306.281 Baris"]
    end

    subgraph Preprocessing ["3. Forensic Cleaning & Imputation"]
        J3 --> P1["Parsing Koma-Desimal Indonesia menjadi Float"]
        P1 --> P2["Substitusi Non-Response Codes Sesuai Buku Kode:<br>• Usia Kehamilan: 88 -> NaN<br>• Berat Lahir: 888 / 8888 -> NaN<br>• Tinggi Badan & Usia: Tidak Ada Kode Non-Response"]
        P2 --> P3["Imputasi Numerik Terarah:<br>• Berat Lahir -> Median 3.100 g<br>• Tinggi Badan -> Median 88.10 cm<br>• Usia Kehamilan -> Median 39.0 Minggu<br>• Kategori -> 'Missing' Explicit Token"]
        P3 --> P4["Deduplikasi Vektor 9 Dimensi:<br>2.088 baris identik (0,68%) dihapus"]
        P4 --> P5["Dataset Analitik Final: 304.193 Balita"]
    end

    subgraph Splitting ["4. Partisi & Pemodelan"]
        P5 --> S1["Stratified Split 80/20 (Random State 42)"]
        S1 --> S2["Train Set: 243.354 Balita"]
        S1 --> S3["Test Hold-out: 60.839 Balita"]
        S2 --> M1["Pelatihan CART Decision Tree (Depth 8, 179 Daun)"]
        S3 --> M2["Evaluasi Screening: Akurasi 75.57%, PPV 92.76%"]
    end
```

---

## 4. Flow 3: Evolusi Pemodelan AI (Dari Buku TA ke Paper GENY & Startup)

Perjalanan pemodelan kecerdasan buatan tim berkembang secara terukur dari studi kasus regional menuju standarisasi skrining nasional:

```mermaid
stateDiagram-v2
    [*] --> Tahap_1_Buku_TA
    
    state Tahap_1_Buku_TA {
        [*] --> Subsample_Kalteng: 1.679 Data Balita SKI 2023
        Subsample_Kalteng --> Listwise_Clean: Filter 389 Balita Lengkap (0-23 Bulan)
        Listwise_Clean --> Fuzzy_Sugeno: 6 Variabel Input + Pre-filter Jenis Kelamin/Usia
        Fuzzy_Sugeno --> GA_Tuning: Optimasi Batas Fungsi Keanggotaan via GA
        GA_Tuning --> Dual_HAZ_Output: Evaluasi Trayektori Pertumbuhan (Baseline vs Sekarang)
    }

    Tahap_1_Buku_TA --> Audit_Silang_Metodologi: Pelajaran Berharga Temuan E1-E4
    
    state Audit_Silang_Metodologi {
        E1: Tautan B4K3=2 keliru 95.8% (wajib NO_IBU)
        E3: Umur bulan penuh geser z-score (wajib WHO Anthro)
        E4: Koreksi bobot populasi (W_BALITA)
    }

    Audit_Silang_Metodologi --> Tahap_2_Paper_GENY

    state Tahap_2_Paper_GENY {
        [*] --> Skala_Nasional: 304.193 Balita dari 38 Provinsi
        Skala_Nasional --> Decision_Tree_CART: Max Depth 8, 179 Daun, Entropy
        Decision_Tree_CART --> Temuan_Dominasi: TB dan Usia = 98.23% Importance
        Temuan_Dominasi --> Model_Pembanding: Model Tanpa TB/Usia Macro F1 0.3565
        Model_Pembanding --> Nilai_Klinis: Rekonstruksi Batas WHO yang Hand-Executable
    }

    Tahap_2_Paper_GENY --> Tahap_3_Geny_StuntCare

    state Tahap_3_Geny_StuntCare {
        [*] --> Mobile_MVP: Aplikasi Android Offline-First
        Mobile_MVP --> Pilot_Sidoarjo: Implementasi Mitra Komunitas Siwalanpanji
        Pilot_Sidoarjo --> Integrasi_Nasional: Sinergi dengan Posyandu ILP & MBG 3B
    }
```

### Komparasi Metodologis Antar-Tahap:

| Fitur / Parameter | Tahap 1: Buku Tugas Akhir | Tahap 2: Paper GENY (IBITeC) | Tahap 3: Platform Geny StuntCare |
| :--- | :--- | :--- | :--- |
| **Penyusun Utama** | Gerrard Sebastian (1203220018) | Gerrard Sebastian dkk. | Tim Startup Geny StuntCare |
| **Metode AI** | Takagi-Sugeno Fuzzy Logic + GA | CART Decision Tree (Depth 8) | Decision Engine Teroptimasi + Rule Base |
| **Cakupan Wilayah** | 1 Provinsi (Kalimantan Tengah) | 38 Provinsi (Nasional Indonesia) | Komunitas Jawa Timur (Pilot) ➔ Nasional |
| **Ukuran Sampel** | 389 Balita (0–23 bulan) | 304.193 Balita (0–59 bulan) | Seluruh balita terdata di Posyandu sasaran |
| **Daya Eksekusi** | Komputasi fuzzy berbasis skrip web | **Dapat dieksekusi manual (1 lembar)** | Mobile App Offline-First & Cloud Sync |
| **Evaluasi Kritis** | Analisis trayektori dinamik lahir-kini | Skrining sensitivitas biner (PPV 92,76%) | Efisiensi kader (-66% waktu) & pemantauan MBG |

---

## 5. Flow 4: Implementasi Validasi Lapangan & Inkubasi BTP Batch 24

Dalam konteks program inkubasi di Bandung Techno Park (Telkom University), seluruh aset riset ini dialirkan ke dalam rencana operasional tahap **SRL 1 (Problem Validation)** dan **SRL 2 (Solution Validation)**:

```mermaid
flowchart LR
    subgraph Masalah_Riil ["1. Validasi Masalah Lapangan (SRL 1)"]
        P1["Data antropometri posyandu sering tidak akurat<br>(Galat input manual mencapai 15.4%)"]
        P2["Kader terbebani 25 kompetensi ILP Kemenkes"]
        P3["Distribusi bantuan makanan MBG 3B rawan salah sasaran"]
        P4["Penolakan keluarga akibat stigma kata 'stunting'"]
    end

    subgraph Solusi_Geny ["2. Validasi Solusi Produk (SRL 2)"]
        S1["Kalkulasi Z-score WHO Otomatis & Terverifikasi"]
        S2["Alat Kerja Kader Offline-First (Hemat Waktu 66%)"]
        S3["Modul Verifikasi & Bukti Distribusi Menu MBG 3B"]
        S4["Komunikasi Kurva Pertumbuhan Berbasis Empati"]
    end

    subgraph Model_Bisnis ["3. Rencana B2G & B2B2C (SRL 4-5)"]
        B1["Dinas Kesehatan / Pemda (Pengadaan Alat Posyandu ILP)"]
        B2["Mitra SPPG Badan Gizi Nasional (Monitoring MBG 3B)"]
        B3["Program CSR Kesehatan & Dana Desa"]
    end

    P1 --> S1
    P2 --> S2
    P3 --> S3
    P4 --> S4

    S1 & S2 & S3 & S4 --> Model_Bisnis
```

---

## 6. Matriks Akses Cepat Berkas Penunjang (*Direct File Cross-Reference*)

Semua komponen dokumen dan aset dalam workflow ini dapat diakses secara langsung melalui tabel direktori berikut:

| Tahapan Workflow | Berkas Dokumen Terkait | Tautan Langsung Workspace | Path Sistem Operasi Lokal |
| :--- | :--- | :--- | :--- |
| **Kompilasi Crawling** | Ekspor Sesi Consensus (102 Halaman) | [Consensus PDF](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Faktor%20Faktor%20Stunting%20Indonesia%20-%20Consensus.pdf) | `/Users/sinitygs/Downloads/GENY/Faktor Faktor Stunting Indonesia - Consensus.pdf` |
| **Kompilasi Crawling** | Dataset 20 Paper UCD Stunting | [20 UCD Papers CSV](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Does%20user-centered%20design%20improve%20stunting%20app%20uptake%20in%20Indonesian%20caregivers%20-%2026%20Sep%202026.csv) | `/Users/sinitygs/Downloads/GENY/Does user-centered design improve stunting app uptake in Indonesian caregivers - 26 Sep 2026.csv` |
| **Sintesis Bukti** | Laporan Final Determinan (27 Halaman) | [Laporan Final PDF](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Laporan_Final_Determinan_Stunting_Indonesia_UPDATE2_26Sep2026.pdf) | `/Users/sinitygs/Downloads/Laporan_Final_Determinan_Stunting_Indonesia_UPDATE2_26Sep2026.pdf` |
| **Referensi Utama 1** | Paper GENY (IEEE IBITeC 2026) | [Paper GENY PDF](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/PaperGeny.pdf) | `/Users/sinitygs/Downloads/PaperGeny.pdf` |
| **Referensi Utama 1** | Audit Forensik Naskah Paper GENY | [Audit Paper DOCX](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Audit_Paper_GENY_draf_19Agu2026.docx) | `/Users/sinitygs/Downloads/Audit_Paper_GENY_draf_19Agu2026.docx` |
| **Referensi Utama 2** | Buku Tugas Akhir Stunting (160 Hlm) | [Buku TA PDF](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/1203220018_GERRARDSEBASTIAN_BUKU_TA_FIXs.pdf) | `/Users/sinitygs/Downloads/1203220018_GERRARDSEBASTIAN_BUKU_TA_FIXs.pdf` |
| **Visualisasi Aset** | Benchmark MARS Terverifikasi | [MARS Chart](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/assets/chart3_mars_benchmarking_v3.png) | `/Users/sinitygs/Projects21/05-laporan-data-crawling/assets/chart3_mars_benchmarking_v3.png` |
| **Visualisasi Aset** | Efisiensi Kader Posyandu | [Efisiensi Chart](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/assets/chart5_efisiensi_operasional_kader_v3.png) | `/Users/sinitygs/Projects21/05-laporan-data-crawling/assets/chart5_efisiensi_operasional_kader_v3.png` |
| **Visualisasi Aset** | Forest Plot Odds Ratio Terverifikasi | [Odds Ratio Chart](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/assets/chart4_odds_ratio_stunting_v3.png) | `/Users/sinitygs/Projects21/05-laporan-data-crawling/assets/chart4_odds_ratio_stunting_v3.png` |

---
*Kembali ke indeks utama:*  
👉 **[Kembali ke 📁 README.md Indeks Folder 05 ➔](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/README.md)**
