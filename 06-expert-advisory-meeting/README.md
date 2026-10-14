# 🎯 Master Panduan Strategis & Matriks Pertanyaan Rapat Dewan Pakar
## Konsultasi Tingkat Tinggi: Validasi Saintifik, Kebijakan Dinas Kesehatan & Scale-Up Korporat
### Startup Geny StuntCare — Program Inkubasi Bisnis Startup Batch 24 Bandung Techno Park (Telkom University)

---

<p align="center">
  <img src="https://img.shields.io/badge/Dokumen-Master%20Advisory%20Guide-red?style=for-the-badge&logo=googledocs" alt="Master Guide" />
  <img src="https://img.shields.io/badge/Tahap-SRL--1%20Problem%20Validation-orange?style=for-the-badge" alt="SRL-1" />
  <img src="https://img.shields.io/badge/Institusi-Bandung%20Techno%20Park-blue?style=for-the-badge&logo=telkom" alt="BTP" />
  <img src="https://img.shields.io/badge/Lokus%20Pakar-Palangka%20Raya%2C%20Kalteng-emerald?style=for-the-badge" alt="Palangka Raya" />
  <img src="https://img.shields.io/badge/Platform-genystuntcare.com-blueviolet?style=for-the-badge&logo=googlechrome" alt="Website" />
</p>

---

## 🗺️ 1. Peta Perjalanan & Riwayat Progres Proyek (*Project Trajectory Tracker*)

Sebelum melangkah ke sesi konsultasi dewan pakar, berikut adalah rekapitulasi komprehensif perjalanan riset, validasi, dan pengembangan teknologi **Geny StuntCare** sejak awal pembentukan hingga titik saat ini:

```mermaid
timeline
    title PETA PERJALANAN DAN PROGRES STARTUP GENY STUNTCARE (2025 - 2026)
    section Fondasi Riset Saintifik (2025 - Pertengahan 2026)
        Inisiasi dan Riset Lapangan : Program Innovillage 2025 di Desa Siwalanpanji Sidoarjo
        Paper GENY (IEEE IBITeC 2026) : Pengolahan Data Mikro SKI 2023 (304.193 balita) dengan Decision Tree CART (Akurasi 75,57%)
        Buku Tugas Akhir 160 Hlm : Sistem Monitoring Stunting 14 Kab/Kota Kalteng berbasis Fuzzy Sugeno dan Genetic Algorithm (Gerrard Sebastian)
        Audit dan Crawling Konsensus : Ekstraksi 102 hlm Consensus AI, telaah 20 paper UCD, sintesis determinan stunting (Laporan Final 27 hlm)
    section Inkubasi BTP Stage 1 (September 2026)
        Bootcamp Pembukaan BTP : Seleksi resmi Inkubasi Startup Batch 24 Bandung Techno Park
        Masterclass Sesi 1 dan 2 : Customer Discovery (Indra Purnama) dan Design Thinking (Dr. Iwan Iwut Tritoasmoro)
        Masterclass Sesi 3 : Problem Validation dan VPC (Muhammad Nur Awaludin / Kak Mumu)
        Spesifikasi Arsitektur API : Perancangan RESTful API Z-Score WHO, modul deteksi prediktif, dan integrasi SatuSehat
    section Penajaman Validasi Lapangan (Awal Oktober 2026)
        Instrumen Wawancara 76 Soal : Penyusunan pedoman wawancara 4 persona dan matriks sampling purposif 5 Sel (8 titik Jatim)
        Mentoring 1 BTP (8 Okt 2026) : Evaluasi kritis Mentor Wulan Fitriani (Pivot fokus ke balita faltering 6-24 bln, diferensiasi MPASI, zero-burden nakes)
        Rapat Dewan Pakar (13 Okt 2026) : Triangulasi 3 Pakar Palangka Raya Kalteng (Prof. Heti, dr. Dewi Rama Dewa, Bpk. Setyohadi)
```

### Rekapitulasi Status Kesiapan Startup Saat Ini:
* **Status SRL (Startup Readiness Level):** Memasuki gerbang akhir **SRL-1 (Problem Validation)** menuju pengujian prototipe **SRL-2 (Solution Validation)**.
* **Aset Teknologi Aktif:** Platform web purwarupa ([genystuntcare.com](https://genystuntcare.com)), model komputasi CART Decision Tree (Paper IBITeC 2026), model Fuzzy Sugeno (Buku TA Kalteng), dan dokumen spesifikasi API.
* **Tantangan Validasi yang Sedang Diselesaikan:** Mengonfirmasi batasan klinis fenomena *weight faltering* balita usia 6–24 bulan, merumuskan formula intervensi gizi MPASI lokal, memastikan arsitektur *zero data-entry burden* bagi nakes, serta mengunci dukungan kemitraan pemerintah (Dinkes) dan korporasi (Telkom Group).

> 🎬 **Pembaruan Hasil Eksekusi Wawancara Dewan Pakar (14 Oktober 2026):**  
> Sesi konsultasi mendalam bersama **dr. Dewi Rama Dewa, M.Kes.** dan **Bapak Setyohadi** telah tuntas dilaksanakan (Durasi: ~1 Jam 3 Menit).  
> * 📹 **Tautan Rekaman YouTube:** [https://youtu.be/-jGlQGCjEwI](https://youtu.be/-jGlQGCjEwI)  
> * 📘 **README Terstruktur Notulensi Resmi:** [notulensi-wawancara-dr-dewi-dan-bpk-setyohadi/README.md](file:///Users/sinitygs/Projects21/06-expert-advisory-meeting/notulensi-wawancara-dr-dewi-dan-bpk-setyohadi/README.md)  
> * 📄 **Salinan Berkas Markdown:** [hasil-wawancara-dr-dewi-dan-bpk-setyohadi-14-oktober-2026.md](file:///Users/sinitygs/Projects21/06-expert-advisory-meeting/hasil-wawancara-dr-dewi-dan-bpk-setyohadi-14-oktober-2026.md)

---

## 📌 2. Profil Mendalam & Rekam Jejak (*Track Record Dossier*) 3 Pakar Kunci

Pertemuan strategis pada **Selasa, 13 Oktober 2026** mempertemukan tim pendiri Geny StuntCare dengan tiga figur berpengaruh di **Kota Palangka Raya, Provinsi Kalimantan Tengah**. Ketiganya memiliki irisan riset, jabatan birokrasi, dan kepemimpinan industri yang sangat relevan:

```
┌────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                              DOSIR REKAM JEJAK & DINAMIKA STRATEGIS PANEL PAKAR                        │
├───────────────────────────────────┬───────────────────────────────────┬────────────────────────────────┤
│ Prof. / Dr. Heti Ira Ayue, S.ST., │ dr. Dewi Rama Dewa, M.Kes.        │ Bapak Setyohadi                │
│ M.Keb.                            │ (Istri dari Bapak Setyohadi)      │ (Suami dari dr. Dewi Rama D.)  │
├───────────────────────────────────┼───────────────────────────────────┼────────────────────────────────┤
│ JABATAN & INSTITUSI:              │ JABATAN & INSTITUSI:              │ JABATAN & INSTITUSI:           │
│ • Dosen Jurusan Kebidanan,        │ • Kepala Bidang Kesehatan         │ • Eksekutif Senior / Mantan    │
│   Poltekkes Kemenkes Palangka Raya│   Masyarakat (Kabid Kesmas),      │   Manager Marketing Telkom     │
│ • Lulusan Program Doktor (S3)     │   Dinas Kesehatan Kota Palangka   │   Kalimantan Timur & Tengah    │
│   Ilmu Kedokteran, Universitas    │   Raya                            │ • Tokoh Senior Manajemen Bisnis│
│   Brawijaya (UB) Malang           │ • Dokter Praktik Mandiri / Klinik │   & Kemitraan Telkom Group     │
│ • Pemohon Resmi Akses Data Mikro  │ • Tim Surveyor Akreditasi         │   Palangka Raya                │
│   SKI 2023 Kemenkes RI (Surat FK  │   Puskesmas Kemenkes RI           │                                │
│   UB No. 06361/2024)              │                                   │                                │
├───────────────────────────────────┼───────────────────────────────────┼────────────────────────────────┤
│ REKAM JEJAK RISET & KEPAKARAN:    │ REKAM JEJAK RISET & KEPAKARAN:    │ REKAM JEJAK RISET & KEPAKARAN: │
│ • Penulis Utama Paper Bereputasi  │ • Pemegang otoritas teknis &      │ • Berpengalaman puluhan tahun  │
│   Internasional (PubMed/Scopus):  │   anggaran program percepatan     │   dalam penetrasi pasar B2B &  │
│   "Exploring the multifactorial   │   penurunan stunting di seluruh   │   B2G telco/enterprise Kalteng │
│   predictors of stunting in       │   Puskesmas Kota Palangka Raya    │ • Paham struktur pendanaan     │
│   children under five" (2024)     │ • Menguasai sistem Posyandu ILP,  │   TJSL/CSR BUMN penanganan     │
│ • Pelopor program Kelompok        │   distribusi PMT, & alur rujukan  │   stunting serta ekosistem BTP │
│   Pendukung ASI (KP-ASI) & KIE    │ • Berhadapan langsung dengan ibu  │ • Menguasai tantangan jaringan │
│   Digital maternal di Kalteng     │   balita GTM di meja periksa      │   telekomunikasi 3T Kalteng    │
└───────────────────────────────────┴───────────────────────────────────┴────────────────────────────────┘
```

### 💡 Analisis Dinamika Khusus Pasangan Suami-Istri (dr. Dewi Rama Dewa & Bpk. Setyohadi):
Hubungan pernikahan antara **dr. Dewi Rama Dewa (Kabid Kesmas Dinkes Palangka Raya)** dan **Bapak Setyohadi (Senior Executive Telkom Group)** merupakan **kekuatan strategis luar biasa (*power-couple synergy*)** bagi Geny StuntCare:
1. **Sinergi Kebijakan Publik & Anggaran Korporat:** dr. Dewi memegang lokus masalah, data balita posyandu, dan kebutuhan faskes di lapangan, sementara Bapak Setyohadi memahami bagaimana korporasi telekomunikasi (Telkom TJSL/CSR) dapat mendanai program intervensi sosial melalui skema kemitraan resmi.
2. **Kredibilitas Ganda:** Rekomendasi medis dari dr. Dewi menjamin kepatuhan klinis Kemenkes, sedangkan restu bisnis dari Bapak Setyohadi memastikan arsitektur cloud, skalabilitas enterprise, dan keamanan data anak sesuai standar BUMN Telkom.
3. **Pintu Masuk Pilot Project:** Pasangan ini memiliki akses langsung untuk memfasilitasi dan menyetujui uji coba di puskesmas-puskesmas Kota Palangka Raya.

---

### 🌏 2.1. Rekam Jejak Mobilitas Nasional (Jawa $\leftrightarrow$ Kalimantan $\leftrightarrow$ Lintas Pulau) & Strategi "Jawa Timur First"

Salah satu aset intelijen paling berharga dari ketiga pakar ini adalah **jam terbang penugasan dan mobilitas geografis yang sangat tinggi di tingkat nasional**:
* **Mobilitas Lintas Pulau:** Ketiganya memiliki riwayat berpindah-pindah domisili dan penugasan strategis antara **Kalimantan** dan **Jawa**, bahkan beberapa kali dipercaya mengemban amanah di berbagai **pulau lain di Indonesia** (seperti penugasan surveyor faskes Kemenkes oleh dr. Dewi, penugasan rotasi manajemen Telkom Group oleh Bpk. Setyohadi, dan studi doktoral Prof. Heti di UB Malang), sebelum akhirnya saat ini menetap dan berdomisili di **Palangka Raya, Kalimantan Tengah**.
* **Fokus Proyek Saat Ini: Validasi Lapangan di JAWA TIMUR DULU (Fase 1):**  
  Meskipun ketiga pakar saat ini menetap di Palangka Raya, **fokus riset dan pengujian empiris Geny StuntCare pada Stage 1 Inkubasi BTP berpusat secara mutlak di JAWA TIMUR DULU** (mencakup 8 titik wilayah: Kota Surabaya, Kota Malang, Siwalanpanji Sidoarjo, Turen Kab. Malang, Gondanglegi Kab. Malang, Kabupaten Banyuwangi, Kota Jember, dan Kabupaten Magetan).
* **Keunggulan Perspektif Komparatif (*The Dual-Lens Advantage*):**  
  Pengalaman hidup dan kerja ketiga pakar di Jawa dan luar Jawa memberikan sudut pandang komparatif yang sangat tajam:
  1. Mereka memahami betul karakteristik kultural, pola konsumsi gizi, daya beli, dan kepadatan faskes di **Jawa Timur** (yang menjadi lokus validasi awal tim).
  2. Mereka mampu menguji apakah solusi yang berhasil divalidasi di Jawa Timur memiliki ketahanan model untuk nantinya di-scale up (*direplikasi*) ke daerah luar Jawa (seperti Kalimantan Tengah) yang memiliki tantangan geografis sungai, keterbatasan sinyal, dan rantai pasok pangan yang berbeda.

---

## 🧭 3. Arsitektur Triangulasi Strategis: "Segitiga Emas Palangka Raya"

```mermaid
graph TD
    subgraph Segitiga_Emas ["SEGITIGA EMAS PALANGKA RAYA (KALTENG)"]
        A["<b>Prof./Dr. Heti Ira Ayue</b><br>(Poltekkes Kemenkes / S3 UB)<br>- Validasi Saintifik Model AI<br>- Prediktor Multifaktorial Stunting<br>- Pangan Lokal dan Ethical Clearance"]
        B["<b>dr. Dewi Rama Dewa, M.Kes.</b><br>(Kabid Kesmas Dinkes Palangka Raya)<br>- Kebijakan Intervensi Stunting Kota<br>- Realitas Pasien GTM dan Rujukan<br>- Zero-Burden Data Nakes Posyandu"]
        C["<b>Bapak Setyohadi</b><br>(Eksekutif Senior Telkom Group)<br>- Pendanaan TJSL/CSR BUMN Stunting<br>- Sinergi Yakes dan Telkomsel IoT<br>- Keamanan Data Anak dan Skalabilitas"]
    end

    subgraph Solusi_Geny ["PLATFORM GENY STUNTCARE"]
        D["<b>Problem-Solution Fit Tervalidasi</b><br>1. AI Triase Hand-Executable (SKI 2023)<br>2. Action Plan Menu MPASI Lokal Padat Kalori<br>3. Pilot Project Puskesmas Kota Palangka Raya<br>4. Dewan Penasihat Medis dan Bisnis Resmi"]
    end

    A ---|"Kolaborasi Riset Klinis dan Etik"| B
    B ---|"Sinergi Suami-Istri: Dinkes x CSR Telkom"| C
    A ---|"Pemanfaatan Data Mikro dan Komputasi"| C
    A --> D
    B --> D
    C --> D
```

---

## 🔬 4. Panduan Pertanyaan untuk Prof. / Dr. Heti Ira Ayue
*(POV: Akademisi Keperawatan Anak, Peneliti Utama Disertasi S3 UB, & Pakar Prediktor Multifaktorial Stunting)*

---

### KLASTER A: Validasi Saintifik Model Decision Tree (Paper GENY) & Data SKI 2023

#### ❓ Pertanyaan A.1: Resolusi Bobot Fitur vs Konsep Prediktor Multifaktorial
* **Redaksi Pertanyaan:**  
  *"Prof. Heti, dalam publikasi terbaru Ibu di Journal of Public Health Research (2024) yang mengulas 'Multifactorial predictors of stunting in children under five', Ibu menegaskan bahwa stunting dipicu oleh interaksi kompleks gizi, sanitasi, infeksi, dan pengasuhan. Namun, pada [Paper GENY](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/03_referensi_utama_1_paper_geny.md) kami berbasis data mikro SKI 2023 yang Ibu ajukan ke Kemenkes, model Decision Tree CART kami menemukan bahwa tinggi/panjang badan dan usia mendominasi 98,23% feature importance. Dari sudut pandang metodologi penelitian kedokteran, bagaimana kami harus menyandingkan temuan pohon biner ini dengan teori multifaktorial Ibu agar sistem triase kami tidak dianggap menyederhanakan determinan biologis anak?"*
* **Rasionalitas Data:** Mempertahankan keabsahan Paper IBITeC 2026 dan menyelaraskannya dengan disertasi S3 Prof. Heti di UB.
* **Target Insight:** Justifikasi bahwa model CART berfungsi sebagai *alat skrining cepat tingkat pertama (first-line triage)*, sementara determinan multifaktorial berfungsi sebagai *penentu intervensi tingkat kedua (second-line intervention)*.
* **Probing:** *"Jika anak terdeteksi berada di ambang batas z-score -1.9 SD (hampir stunting), prediktor non-antropometri apa dari kuesioner SKI yang menurut Ibu paling mendesak dihitung sebagai skor risiko pendukung?"*

#### ❓ Pertanyaan A.2: Evaluasi Trayektori Ganda Dinamis (Buku TA Fuzzy Kalteng)
* **Redaksi Pertanyaan:**  
  *"Dalam [Buku Tugas Akhir](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/04_referensi_utama_2_buku_ta_stunting.md) kami mengenai stunting di 14 Kabupaten/Kota Kalimantan Tengah, kami menemukan kelemahan mendasar posyandu yang hanya mendiagnosis secara statis pada satu titik waktu. Kami merancang logika Fuzzy Sugeno yang membandingkan Panjang Badan Lahir (PBL) dengan kondisi saat pengukuran untuk membedakan balita 'catch-up growth' vs 'growth faltering'. Berdasarkan pengamatan klinis Ibu di Kalimantan Tengah, seberapa besar proporsi balita yang lahir dengan panjang normal namun mengalami 'growth faltering' drastis setelah memasuki usia MPASI (6–12 bulan)?"*
* **Target Insight:** Konfirmasi klinis bahwa keterlambatan tumbuh di Kalteng mayoritas terjadi pada fase MPASI akibat kesalahan pola asuh/asupan, bukan murni faktor genetik bawaan.

---

### KLASTER B: Validasi Klinis Fokus Tunggal Balita Faltering 6–24 Bulan & GTM

#### ❓ Pertanyaan B.3: Menjustifikasi Arahan Mentor BTP (Wulan Fitriani)
* **Redaksi Pertanyaan:**  
  *"Mentor BTP kami menginstruksikan agar Geny StuntCare berhenti melebar ke calon pengantin dan ibu hamil, melainkan fokus 100% pada satu persona: Ibu balita usia 6–24 bulan yang mengalami weight faltering (berat badan seret/tidak naik) atau garis kuning KMS. Apakah pembatasan segmen ini selaras dengan fokus intervensi keperawatan anak, dan mengapa periode 6–24 bulan ini disebut sebagai 'last golden window' sebelum kerusakan fisik stunting menjadi ireversibel?"*
* **Target Insight:** Dasar teori patofisiologi untuk mempertahankan fokus produk pada Stage 1 Inkubasi.
* **Probing:** *"Berapa bulan toleransi berat badan stagnan pada anak usia 6–12 bulan sebelum terjadi perlambatan laju panjang badan (linier growth arrest) yang memicu stunting?"*

#### ❓ Pertanyaan B.4: Akar Penyebab Gerakan Tutup Mulut (GTM) Balita Kalteng
* **Redaksi Pertanyaan:**  
  *"Dalam riset dan pengabdian masyarakat Ibu terkait Kelompok Pendukung ASI (KP-ASI) di Palangka Raya, apa faktor pemicu utama balita mengalami GTM parah saat masa transisi MPASI? Apakah lebih dominan akibat defisiensi zat besi subklinis (anemia), tekstur yang tidak sesuai tahapan usia, atau menu yang monoton tanpa protein hewani yang memadai?"*
* **Target Insight:** Variabel skrining tambahan pada platform untuk membedakan GTM psikologis biasa vs GTM patologis akibat penyakit.

---

### KLASTER C: Intervensi Menu MPASI Berbasis Pangan Lokal Kalimantan Tengah

#### ❓ Pertanyaan C.5: Pemanfaatan Ikan Sungai & Pangan Lokal Kalteng untuk Catch-Up Growth
* **Redaksi Pertanyaan:**  
  *"Diferensiasi utama Geny StuntCare adalah menyediakan 'Personalized Action Plan MPASI Padat Kalori'. Di Kalimantan Tengah dengan kekayaan daerah aliran sungai (DAS Kahayan, Kapuas, Barito), komoditas ikan air tawar lokal apa (seperti ikan gabus/haruan, seluang, baung, atau patin) yang memiliki densitas albumin, protein, dan bioavailabilitas tertinggi untuk memulihkan balita faltering? Bagaimana formulasi takaran lemak tambahan lokal yang aman agar tidak memicu gangguan pencernaan pada balita?"*
* **Target Insight:** Resep terstandar berbasis kearifan lokal Kalteng yang dapat langsung dimasukkan ke dalam basis data aplikasi.

#### ❓ Pertanyaan C.6: Komparasi Epidemiologi Stunting Jawa Timur vs Kalimantan Tengah
* **Redaksi Pertanyaan:**  
  *"Prof. Heti, mengingat Ibu menempuh pendidikan doktoral (S3) di Universitas Brawijaya Malang dan mendalami data balita Kalteng, sementara fokus riset validasi lapangan Geny StuntCare saat ini berfokus di Jawa Timur (8 titik: Surabaya, Sidoarjo, Malang, Banyuwangi, Magetan, Jember): bagaimana perbandingan pola determinan stunting antara Jawa Timur dan Kalimantan? Apakah model intervensi menu MPASI yang kami validasi di Jawa Timur nantinya dapat langsung diadaptasi ke Kalimantan Tengah dengan penyesuaian komoditas lokal, ataukah ada perbedaan mendasar dalam pola perilaku makan keluarga?"*
* **Konteks & Rasionalitas:** Menjembatani riset Jawa Timur saat ini dengan rencana ekspansi masa depan ke Kalimantan Tengah.
* **Target Insight:** Peta komparasi faktor risiko: Jawa Timur lebih dipengaruhi disparitas *urban slum*, sanitasi padat, dan pola asuh ibu pekerja pabrik; sementara Kalimantan lebih dipengaruhi keterisolasian geografis, akses air bersih DAS, dan variasi pangan sungai.

---

### KLASTER D: Kelaikan Etik (Ethical Clearance) & Permohonan Sebagai Advisor

#### ❓ Pertanyaan D.6: Prosedur Ethical Clearance di KEPK Poltekkes Palangka Raya
* **Redaksi Pertanyaan:**  
  *"Untuk memastikan platform kami memenuhi standar etika medis sebelum diuji coba pada keluarga balita dan dipublikasikan secara internasional, kami membutuhkan Ethical Clearance. Bagaimana alur pengajuan persetujuan etik melalui KEPK di Poltekkes Kemenkes Palangka Raya atau FK UB untuk aplikasi intervensi gizi mHealth seperti Geny StuntCare?"*
* **Target Insight:** Jadwal sidang etik, syarat berkas, dan estimasi waktu terbitnya sertifikat etik.

#### ❓ Pertanyaan D.7: Permohonan Resmi Bergabung Sebagai Scientific & Clinical Advisor
* **Redaksi Pertanyaan:**  
  *"Prof. Heti, riset ini berakar dari data mikro yang Ibu perjuangkan aksesnya dan penelitian Tugas Akhir balita Kalteng. Dalam proses inkubasi di Bandung Techno Park, kami sangat memohon kesediaan Ibu untuk menjadi Scientific & Clinical Advisor resmi Geny StuntCare guna mengawal integritas ilmiah produk ini. Apakah Ibu berkenan mendampingi kami?"*
* **Target Output:** Komitmen kesediaan menjadi penasihat ilmiah resmi startup.

---

### KLASTER E: Rekomendasi Relasi Pakar Gizi Klinis, Kriteria Sampel Balita, & Metodologi Populasi Riset

#### ❓ Pertanyaan E.8: Rekomendasi Jaringan Ahli Gizi Klinis / Dietisien (AsDI/PERSAGI) & Kolega Riset UB Malang
* **Redaksi Pertanyaan:**  
  *"Prof. Heti, untuk memvalidasi algoritma penyusunan MPASI padat kalori dan substitusi bahan pangan lokal secara klinis, kami memerlukan review berkala dari Ahli Gizi Klinis (Registered Dietitian / AsDI) dan akademisi gizi anak. Apakah Ibu memiliki rekomendasi kolega pakar gizi di Universitas Brawijaya Malang, Poltekkes Malang/Surabaya, atau Poltekkes Kemenkes Palangka Raya yang bereputasi dan terbuka untuk kami jadikan validator ahli, mitra riset, atau co-author publikasi ilmiah bersama?"*
* **Konteks & Rasionalitas:** Membuka pintu ke jaringan dietisien akademis di Jawa Timur (Fase 1) dan Kalimantan Tengah (Fase 2).
* **Target Insight:** Nama kontak spesifik pakar gizi klinis, afiliasi kampus, dan kesediaan introduksi (*warm introduction*).

#### ❓ Pertanyaan E.9: Purifikasi Data Sampel: Kriteria Inklusi & Eksklusi Balita Faltering
* **Redaksi Pertanyaan:**  
  *"Tantangan metodologis terbesar dalam intervensi gizi balita usia 6–24 bulan adalah memisahkan antara balita faltering primer (murni karena defisit asupan & pola asuh) dengan faltering sekunder akibat penyakit organik (seperti TB anak, penyakit jantung bawaan/PJB, atau infeksi saluran kemih kronis). Menurut kaidah epidemiologi klinis Ibu, bagaimana kriteria inklusi dan eksklusi populasi yang harus kami kunci di aplikasi agar data hasil evaluasi intervensi kami murni dan tidak bias oleh penyakit penyerta?"*
* **Target Insight:** Checklist variabel penyaring medis pada tahap *onboarding* profil balita.

#### ❓ Pertanyaan E.10: Desain Besar Sampel (Power Sample) & Koordinasi Komite Etik Multi-Center
* **Redaksi Pertanyaan:**  
  *"Karena validasi empiris kami dimulai di Jawa Timur lalu direplikasi di Kalimantan Tengah, berapa jumlah sampel minimal balita faltering (*power sample size*) per klaster posyandu yang Ibu rekomendasikan agar data kami memiliki signifikansi statistik (*p-value < 0.05*) yang kuat saat dipublikasikan di jurnal internasional? Apakah pengurusan kelaikan etik sebaiknya dipusatkan di satu KEPK induk atau perlu kerja sama etik multi-center?"*
* **Target Insight:** Formula penentuan ukuran sampel riset intervensi gizi dan strategi clearance etik lintas provinsi.

---

## 🩺 5. Panduan Pertanyaan untuk dr. Dewi Rama Dewa, M.Kes.
*(POV: Kabid Kesmas Dinkes Kota Palangka Raya, Surveyor Akreditasi Puskesmas, & Praktisi Dokter)*

---

### KLASTER A: Realitas Kebijakan Stunting Kota Palangka Raya & Ruang Periksa

#### ❓ Pertanyaan A.1: Peta Riil Stunting & Pencapaian D/S di Kota Palangka Raya
* **Redaksi Pertanyaan:**  
  *"Dokter Dewi, selaku Kepala Bidang Kesmas Dinas Kesehatan Kota Palangka Raya, bagaimana potret riil situasi stunting di wilayah Palangka Raya saat ini (antara data survei SKI dengan data pencatatan rutin e-PPGBM Puskesmas)? Puskesmas mana di Palangka Raya (misal Pahandut, Jekan Raya, Menteng, atau Kereng Bangkirai) yang memiliki tantangan angka stunting atau tingkat partisipasi penimbangan posyandu (D/S) paling menantang?"*
* **Konteks & Rasionalitas:** Mengidentifikasi calon lokus *pilot project* di Kota Palangka Raya.
* **Target Insight:** Data baseline riil kecamatan sasaran dan peta masalah operasional posyandu kota.

#### ❓ Pertanyaan A.2: Psikologi Orang Tua & Stigma Menghadiri Posyandu
* **Redaksi Pertanyaan:**  
  *"Di ruang periksa dokter maupun saat monev posyandu, mengapa masih banyak ibu balita di perkotaan Palangka Raya yang enggan membawa anaknya ke posyandu atau merasa malu saat anaknya dinyatakan kurang gizi / garis kuning KMS? Bagaimana dokter mengomunikasikan diagnosis gagal tumbuh agar ibu tidak merasa dihakimi, dan bagaimana antarmuka aplikasi Geny StuntCare harus menyusun kata-kata notifikasi agar memotivasi ibu tanpa menimbulkan stigma?"*
* **Target Insight:** Standar bahasa komunikasi medis (*empathic clinical phrasing*) untuk teks UI/UX aplikasi.

#### ❓ Pertanyaan A.3: Kesiapan Faskes Primer: Komparasi Jawa Timur vs Luar Jawa
* **Redaksi Pertanyaan:**  
  *"Sebagai seorang Surveyor Akreditasi Puskesmas Kemenkes yang berpengalaman mengaudit faskes di berbagai pulau di Indonesia, bagaimana pandangan Dokter mengenai disparitas kesiapan faskes dan kader posyandu antara Jawa Timur (lokus validasi awal kami saat ini) dibandingkan wilayah luar Jawa seperti Kalimantan? Mengapa keberhasilan membuktikan Problem-Solution Fit di Jawa Timur terlebih dahulu dinilai sebagai fondasi metodologis yang paling kokoh sebelum mereplikasinya ke Palangka Raya?"*
* **Target Insight:** Justifikasi strategis metodologi bertahap: Jawa Timur sebagai *stress-test* volume tinggi dan literasi digital tinggi, disusul Kalimantan Tengah sebagai adaptasi geografis dan ketahanan logistik.

---

### KLASTER B: Alur Rujukan Resmi Stunting di Lapangan & Titik Sumbatan (Bottleneck)

#### ❓ Pertanyaan B.3: Di Mana Titik Putus Rujukan Balita Berisiko di Faskes Palangka Raya?
* **Redaksi Pertanyaan:**  
  *"Bagaimana SOP alur resmi rujukan penanganan balita faltering/stunting di Kota Palangka Raya: mulai dari penemuan kader di Posyandu ➔ pemeriksaan Bidan Kelurahan ➔ evaluasi Dokter di Puskesmas ➔ pemberian PMT Pemulihan/PKMK ➔ rujukan ke Dokter Spesialis Anak (Sp.A) di RSUD Doris Sylvanus atau RSUD Kota Palangka Raya? Di mana titik sumbatan (bottleneck) terbesar yang sering membuat penanganan balita terlambat?"*
* **Target Insight:** Pemetaan titik rujukan yang putus (misal: orang tua menolak rujukan RS karena kendala transportasi/biaya hidup, stok pangan olahan untuk keperluan medis khusus / PKMK di puskesmas kosong).
* **Probing:** *"Bagaimana Geny StuntCare dapat menjadi 'jembatan pengingat' bagi ibu agar patuh menyelesaikan rujukan puskesmas hingga tuntas?"*

---

### KLASTER C: Zero Data-Entry Burden untuk Tenaga Kesehatan & Integrasi Puskesmas

#### ❓ Pertanyaan C.4: Menghilangkan Beban Tambahan Nakes dan Kader Posyandu
* **Redaksi Pertanyaan:**  
  *"Mentor inkubasi kami menekankan bahwa nakes menolak aplikasi baru karena sudah sangat kelelahan menginput data ke e-PPGBM, ASIK Kemenkes, dan Simpus. Selaku Kabid Kesmas, bagaimana kami harus mendesain Geny StuntCare agar sama sekali TIDAK MEMBEBANI nakes? Jika aplikasi kami fokus digunakan mandiri oleh ibu balita di rumah, lalu menyediakan tombol 'Ekspor Rekap Laporan Bulanan' yang format tabelnya sudah persis sesuai kolom e-PPGBM Puskesmas, apakah inovasi ini akan sangat membantu meringankan kerja kader dan bidan?"*
* **Target Insight:** Validasi prinsip *Zero Data-Entry Burden*: nakes hanya sebagai penerima manfaat data terstruktur, bukan operator penginput data.

#### ❓ Pertanyaan C.5: Sudut Pandang Surveyor Akreditasi Puskesmas Kemenkes
* **Redaksi Pertanyaan:**  
  *"Sebagai seorang Surveyor Akreditasi Puskesmas Kemenkes, instrumen penilaian akreditasi pada bab Upaya Kesehatan Masyarakat (UKM) sangat menekankan inovasi penurunan stunting dan kepuasan masyarakat. Apakah kehadiran inovasi mHealth seperti Geny StuntCare di wilayah kerja puskesmas dapat menjadi nilai tambah (poin inovasi) yang mendongkrak penilaian akreditasi Puskesmas menjadi Paripurna?"*
* **Target Insight:** Nilai jual strategis (*selling point*) bagi Kepala Puskesmas untuk mau mengadopsi Geny StuntCare.

---

### KLASTER D: Peluang Pilot Project & Kemitraan Dinas Kesehatan Kota Palangka Raya

#### ❓ Pertanyaan D.6: Skema Pilot Project Kemitraan Dinkes Palangka Raya
* **Redaksi Pertanyaan:**  
  *"Dokter Dewi, jika kami ingin mengajukan Kota Palangka Raya sebagai Lokus Pilot Project Resmi Geny StuntCare (misal di 1 kelurahan atau 1 wilayah kerja puskesmas terpadat), bagaimana mekanisme birokrasi dan administrasi yang harus kami tempuh di Dinas Kesehatan? Apakah memungkinkan dibuatkan Perjanjian Kerja Sama (PKS) atau uji coba inovasi daerah?"*
* **Target Insight:** Prosedur audiensi resmi, dokumen proposal inovasi, dan syarat persetujuan Kepala Dinas Kesehatan.

---

### KLASTER E: Rekomendasi Dokter Spesialis Anak (IDAI), Nutrisionis Lapangan, Lokasi Faskes, & Akses Populasi Sasaran

#### ❓ Pertanyaan E.7: Rekomendasi Dokter Spesialis Anak (IDAI) & Nutrisionis Puskesmas Teladan
* **Redaksi Pertanyaan:**  
  *"Dokter Dewi, dalam penanganan klinis stunting dan faltering, Dokter Spesialis Anak (Sp.A) konsultan nutrisi & penyakit metabolik memegang peranan krusial dalam mendiagnosis red-flag dan meresepkan PKMK (Pangan Olahan untuk Keperluan Medis Khusus). Apakah Dokter memiliki rekomendasi kolega Sp.A (anggota IDAI di RSUD Palangka Raya maupun koneksi Dokter di Jawa Timur) yang berpikiran terbuka terhadap digital health dan bersedia kami wawancarai? Serta siapa Tenaga Pelaksana Gizi (TPG / Nutrisionis Puskesmas) teladan yang paling menguasai dinamika konseling MPASI di lapangan?"*
* **Konteks & Rasionalitas:** Mengamankan jejaring klinis spesialis anak dan praktisi gizi puskesmas untuk memvalidasi algoritma rujukan aplikasi.
* **Target Insight:** Kontak nama Sp.A konsultan nutrisi dan nutrisionis teladan untuk wawancara ahli lanjutan.

#### ❓ Pertanyaan E.8: Rekomendasi Lokasi Faskes: Wilayah Beban Tinggi (*High Burden*) vs Kesiapan Tinggi (*High Readiness*)
* **Redaksi Pertanyaan:**  
  *"Sebagai pejabat Dinkes sekaligus surveyor akreditasi puskesmas yang memahami karakter berbagai faskes: saat menentukan lokus riset percontohan, apakah tim kami sebaiknya menguji coba di wilayah puskesmas dengan prevalensi stunting tertinggi (high-burden, umumnya warga marginal dengan tantangan kepatuhan tinggi) ataukah wilayah dengan kader posyandu yang paling tertib dan melek teknologi (high-readiness)? Menurut Dokter, puskesmas dan kelurahan mana di Palangka Raya yang paling representatif untuk kedua profil tersebut?"*
* **Target Insight:** Rekomendasi nama puskesmas spesifik (misal Puskesmas Pahandut vs Puskesmas Menteng) beserta pertimbangan demografisnya.

#### ❓ Pertanyaan E.9: Strategi Humanis Mendekati Populasi Ibu Balita Garis Kuning KMS (Bypass Stigma)
* **Redaksi Pertanyaan:**  
  *"Di lapangan, banyak ibu balita yang anaknya mengalami garis kuning KMS merasa takut, malu, atau defensif didatangi petugas karena khawatir dicap 'tidak becus mengurus anak'. Dari pengalaman Dokter, bagaimana strategi pendekatan yang paling humanis dan dipercaya agar kami dapat merekrut ibu-ibu tersebut menjadi responden riset tanpa menimbulkan rasa rendah diri? Apakah merangkul Ketua Tim Penggerak PKK lingkungan atau tokoh masyarakat lokal lebih efektif daripada surat resmi kedinasan?"*
* **Target Insight:** Protokol pendekatan etis (*human-centered recruitment strategy*) untuk menjangkau kelompok rentan.

#### ❓ Pertanyaan E.10: Rekomendasi Relasi ke TPPS (Tim Percepatan Penurunan Stunting) & Bappeda Kota
* **Redaksi Pertanyaan:**  
  *"Penanganan stunting terpadu berada di bawah komando TPPS (Tim Percepatan Penurunan Stunting) yang diketuai Wakil Walikota dan beranggotakan lintas dinas (Dinkes, Bappeda, DP3AP2KB/BKKBN). Siapa tokoh atau sekretariat TPPS di Kota Palangka Raya yang paling tepat kami mintai arahan agar inovasi Geny StuntCare ini dapat diselaraskan dengan Rencana Aksi Daerah (RAD) penanganan stunting kota?"*
* **Target Insight:** Akses jalur advokasi kebijakan publik tingkat kota dan pintu masuk Bappeda.

---

## 💼 6. Panduan Pertanyaan untuk Bapak Setyohadi
*(POV: Senior Executive Telkom Group, Pakar Enterprise Sales, CSR Scaling, Rekam Jejak Penugasan Lintas Pulau di Indonesia, & Suami dr. Dewi Rama Dewa)*

---

### KLASTER A: Sinergi CSR BUMN & Solusi Finansial Keluarga Menengah-Bawah

#### ❓ Pertanyaan A.1: Skema Pendanaan TJSL/CSR BUMN untuk Pilot Project Stunting
* **Redaksi Pertanyaan:**  
  *"Pak Setyohadi, hasil riset kami menemukan paradoks bahwa keluarga berisiko stunting terbanyak berada di kalangan menengah-bawah yang tidak sanggup membayar biaya langganan aplikasi bulanan (B2C paywall). Sebagai eksekutif Telkom Group, bagaimana mekanisme mengawinkan kebutuhan Dinkes Kota Palangka Raya (yang dipimpin dr. Dewi) dengan program Tanggung Jawab Sosial dan Lingkungan (TJSL/CSR) Telkom atau BUMN Peduli Stunting? Format proposal dan KPI seperti apa yang dicari oleh unit TJSL Telkom agar bersedia membiayai pengadaan lisensi/paket intervensi Geny StuntCare bagi warga miskin?"*
* **Konteks & Rasionalitas:** Memanfaatkan posisi unik pasangan suami-istri untuk merancang pilot project terpadu: **Dinkes menyediakan lokus & nakes, Telkom TJSL mendanai operasional/gawai/pangan, Geny StuntCare menyediakan sistem monitoring AI**.
* **Target Insight:** Skema penganggaran CSR BUMN, metrik *Social Return on Investment (SROI)*, dan alur disposisi proposal ke Telkom Community Development Center (CDC).

#### ❓ Pertanyaan A.2: Pintu Masuk Kolaborasi dengan Yakes Telkom
* **Redaksi Pertanyaan:**  
  *"Di action plan SLR-1, kami merencanakan pengujian ahli dengan Yayasan Kesehatan Telkom (Yakes). Bagaimana tata kelola kemitraan korporat di Telkom Group untuk menguji coba platform ini pada klinik Yakes Telkom (khususnya memantau balita karyawan Telkom di Kalimantan atau Jawa Timur)? Siapa pejabat kunci di Yakes yang paling tepat kami mintai audiensi awal?"*
* **Target Insight:** Kontak atau jalur disposisi ke pimpinan Yakes Telkom untuk validasi B2B corporate wellness.

#### ❓ Pertanyaan A.3: Sinergi Enterprise & CSR Lintas Regional: Telkom Regional V (Jatim) ke Regional VI (Kalimantan)
* **Redaksi Pertanyaan:**  
  *"Mengingat pengalaman Bapak bertugas di berbagai wilayah pulau di Indonesia (Jawa, Kalimantan, dan wilayah lainnya): fokus validasi lapangan Geny StuntCare saat ini ditargetkan tuntas terlebih dahulu di Jawa Timur (Fase 1 bersama Telkom University Surabaya & Innovillage Sidoarjo) sebelum nantinya berekspansi ke Palangka Raya Kalimantan Tengah (Fase 2). Bagaimana strategi membangun sinergi antara Telkom Regional V (Jawa Timur) dan Telkom Regional VI (Kalimantan) agar portofolio validasi B2G/CSR yang kami rintis di Jawa Timur dapat langsung di-leverage secara mulus ketika kami mengajukan pilot di Palangka Raya?"*
* **Konteks & Rasionalitas:** Mengoptimalkan jaringan networking korporat Telkom di Jawa Timur untuk mendukung validasi saat ini, lalu membukakan jalan menuju Kalimantan.
* **Target Insight:** Jalur koordinasi antar-Regional Telkom (TR-5 Jatim ke TR-6 Kalimantan) dan skema program inkubasi/TJSL terintegrasi.

---

### KLASTER B: Infrastruktur Jaringan Pedalaman Kalteng & Keamanan Data (UU PDP)

#### ❓ Pertanyaan B.4: Arsitektur Offline-First Menghadapi Blank Spot Luar Jawa
* **Redaksi Pertanyaan:**  
  *"Berdasarkan pengalaman Bapak memimpin pemasaran dan operasional Telkom di berbagai daerah kepulauan Indonesia, terdapat kesenjangan tajam infrastruktur digital antara Jawa Timur (yang surplus serat optik dan BTS 4G/5G) dengan pedalaman luar Jawa seperti pinggiran sungai dan perkebunan Kalimantan. Bagaimana platform kami harus mempersiapkan arsitektur teknologi agar tetap tangguh: apakah arsitektur offline-first dengan database lokal di ponsel kader/ibu yang otomatis tersinkronisasi saat mendeteksi sinyal Telkomsel merupakan arsitektur yang paling direkomendasikan standar IT Telkom?"*
* **Target Insight:** Validasi kebutuhan teknis arsitektur *offline-first sync* untuk implementasi luar Jawa.

#### ❓ Pertanyaan B.5: Standar Keamanan Data Anak & Kepatuhan UU PDP No. 27/2022
* **Redaksi Pertanyaan:**  
  *"Platform Geny StuntCare mengelola data rekam pertumbuhan balita dan profil keluarga rentan. Dari standar enterprise Telkom dan regulasi UU Pelindungan Data Pribadi (UU PDP), sertifikasi keamanan data, enkripsi, dan tata kelola cloud lokal (seperti NeuCentrIX Telkom) apa yang wajib kami siapkan sejak tahap awal agar tidak tersandung masalah hukum saat scaling skala nasional?"*
* **Target Insight:** Checklist kepatuhan UU PDP untuk data medis anak balita dan rekomendasi fasilitas inkubasi cloud Telkom.

---

### KLASTER C: Navigasi Inkubasi BTP & Permohonan Sebagai Business Advisor

#### ❓ Pertanyaan C.6: Standar Pembuktian Traction di Mata Reviewer Inkubasi BTP
* **Redaksi Pertanyaan:**  
  *"Sebagai bagian dari keluarga besar Telkom Group dan ekosistem Telkom University, menurut Bapak, bukti traksi dan validasi seperti apa yang paling dicari oleh komite reviewer Bandung Techno Park di akhir Stage 1? Apakah Letter of Intent (LoI) kerja sama dari Dinas Kesehatan Kota Palangka Raya sudah cukup menjadi bukti validasi pasar yang sangat kuat untuk meloloskan kami ke Stage 2?"*
* **Target Insight:** Strategi memenangkan evaluasi reviewer inkubasi BTP dan kriteria penilaian kelayakan investasi lanjutan.

#### ❓ Pertanyaan C.7: Permohonan Kesediaan Menjadi Business & Strategic Advisor
* **Redaksi Pertanyaan:**  
  *"Pak Setyohadi, kami sangat membutuhkan arahan bisnis dan bimbingan kepemimpinan dari sosok senior Telkom Group seperti Bapak yang memahami dinamika bisnis di Jawa maupun luar pulau. Apakah Bapak berkenan menjadi Business & Strategic Advisor resmi bagi Geny StuntCare untuk mendampingi kami mematangkan model enterprise B2G dan scaling korporat?"*
* **Target Output:** Komitmen kesediaan menjadi penasihat bisnis resmi startup.

---

### KLASTER D: Rekomendasi Ekosistem Digital Health BUMN, Mitra Hardware Antropometri IoT, & Forum CSR Lintas Sektor

#### ❓ Pertanyaan D.8: Rekomendasi Jaringan Ekosistem Digital Health Telkom (Mediv, Yakes, DBT, Indigo)
* **Redaksi Pertanyaan:**  
  *"Pak Setyohadi, Telkom Group memiliki unit inovasi dan digital health seperti Telkom Health (Mediv), Yakes Telkom, divisi Digital Business & Technology (DBT), serta program inkubasi Indigo. Apakah Bapak memiliki rekomendasi kontak pimpinan unit atau principal product manager di lingkungan Telkom yang mengawal vertikal kesehatan digital (healthtech) agar Geny StuntCare dapat kami eksplorasi sinergi teknologinya dengan ekosistem BUMN?"*
* **Konteks & Rasionalitas:** Membuka pintu ke ekosistem corporate venture & digital health Telkom Group.
* **Target Insight:** Kontak person kunci di Telkom Health / Indigo / DBT untuk pembinaan dan sinergi teknologi.

#### ❓ Pertanyaan D.9: Rekomendasi Jaringan Forum TJSL BUMN Lintas Sektor (Jawa Timur & Kalimantan)
* **Redaksi Pertanyaan:**  
  *"Kementerian BUMN memiliki mandat prioritas penanganan stunting. Di Jawa Timur terdapat klaster BUMN besar (seperti Pelindo Regional 3 Surabaya, Semen Indonesia Group Gresik/Tuban, Petrokimia Gresik, dan Telkom TR-5), sementara di Kalimantan terdapat BUMN perkebunan (PTPN) dan pertambangan. Apakah Bapak memiliki relasi di Forum TJSL BUMN atau koordinator CSR kewilayahan yang dapat kami jajaki untuk pendanaan program intervensi balita faltering berbasis CSR?"*
* **Target Insight:** Jalur pengajuan proposal program TJSL terpadu BUMN peduli stunting.

#### ❓ Pertanyaan D.10: Rekomendasi Mitra Penyedia Hardware Antropometri Kit Berbasis IoT / Bluetooth
* **Redaksi Pertanyaan:**  
  *"Untuk menjamin akurasi penimbangan balita dan menghilangkan kesalahan input manual oleh kader posyandu (*zero human error*), roadmap teknologi kami merencanakan integrasi timbangan digital dan alat ukur panjang badan ber-Bluetooth (IoT). Dari jaringan kemitraan Telkom IoT atau ekosistem vendor perangkat keras lokal, apakah ada mitra penyedia antropometri kit terstandar Kemenkes yang dapat kami ajak kolaborasi Proof-of-Concept (PoC)?"*
* **Target Insight:** Rekomendasi mitra produsen/distributor antropometri kit bersertifikasi Kemenkes untuk integrasi IoT.

---

## 🌟 7. Skenario Emas Forum Terbuka: Kemitraan Tripartit & Blueprint Dua Fase ("Jawa Timur First ➔ Palangka Raya Grand Pilot")

Pada sesi diskusi bersama (15 menit terakhir), ajukan **Pertanyaan Kunci Tripartit** berikut yang menyatukan peran ketiga pakar dengan peta jalan proyek bertahap:

> 💬 **Pertanyaan Emas Forum Bersama (The Two-Phase Grand Pilot Blueprint):**  
> *"Ibu Heti, Dokter Dewi, dan Pak Setyohadi—kami sangat bersyukur dapat berdiskusi dengan tiga tokoh yang tidak hanya memiliki otoritas tertinggi di bidangnya masing-masing, namun juga memiliki pemahaman mendalam tentang realitas lapangan di Jawa maupun di luar Jawa:  
> 
> * **Fase 1 (Saat Ini - Jawa Timur First):** Riset lapangan dan pembuktian *Problem-Solution Fit* Geny StuntCare difokuskan secara ketat di **Jawa Timur** (Surabaya, Sidoarjo, Malang, Banyuwangi, Magetan, Jember) untuk menguji algoritma AI, kepatuhan MPASI, dan validasi kader posyandu di bawah inkubasi BTP Telkom University.  
> * **Fase 2 (Skalabilitas - Palangka Raya Grand Pilot):** Setelah model di Jawa Timur terbukti solid, kita melangkah bersama mereplikasikannya ke **Kota Palangka Raya, Kalimantan Tengah** sebagai *showcase* percontohan nasional pertama hasil sinergi tripartit:  
>   1. **Prof. Heti (Poltekkes Kemenkes / UB):** Mengawal protokol klinis gizi lokal dan rekomendasi komparasi epidemiologi;  
>   2. **dr. Dewi (Dinkes Kota Palangka Raya):** Membuka lokus Puskesmas percontohan dan integrasi alur rujukan faskes;  
>   3. **Pak Setyohadi (Telkom Group):** Menjembatani dukungan cloud NeuCentrIX dan pendanaan program CSR/TJSL BUMN;  
> 
> **Apakah rancangan blueprint dua fase (Jawa Timur First ➔ Palangka Raya Grand Pilot) ini menurut Bapak dan Ibu merupakan strategi yang paling realistis dan meyakinkan untuk memenangkan inkubasi BTP sekaligus memberikan dampak nyata bagi penurunan stunting nasional?** Langkah konkret apa yang harus kami siapkan dalam 2 minggu ke depan untuk mengunci komitmen bersama ini?"*

---

## ⏱️ 8. Rundown Waktu & Manajemen Pertemuan (Timeboxing 80 Menit)

| Waktu | Durasi | Agenda Utama Pertemuan | Sasaran Output (*Key Deliverable*) |
| :---: | :---: | :--- | :--- |
| **00.00 – 00.05** | 5 Menit | **Pembukaan & Apresiasi:** Menyampaikan rasa hormat dan mengutarakan maksud konsultasi ahli (mendengarkan arahan, bukan berjualan). | Tercipta suasana hangat, santun, dan cair (*rapport building*). |
| **00.05 – 00.12** | 7 Menit | **Elevator Pitch Masalah (Anti-Pitching):** Memaparkan temuan Paper GENY, Buku TA Kalteng, masukan Mentor Wulan Fitriani, dan fokus ke balita *faltering* 6–24 bulan. | Ketiga pakar memahami konteks posisi startup saat ini. |
| **00.12 – 00.35** | 23 Menit | **Sesi Mendalam 1 — Prof. Heti Ira Ayue:** Validasi model SKI, mekanisme biologis faltering, pangan lokal Kalteng, dan kelaikan etik (KEPK). | Catatan validasi saintifik, nama komoditas pangan lokal, & alur etik. |
| **00.35 – 00.58** | 23 Menit | **Sesi Mendalam 2 — dr. Dewi Rama Dewa:** Realitas stunting Palangka Raya, alur rujukan, puskesmas akreditasi, & zero-burden nakes. | Pemetaan birokrasi Dinkes, bahasa UI non-stigma, & peluang lokus puskesmas. |
| **00.58 – 01.15** | 17 Menit | **Sesi Mendalam 3 — Bapak Setyohadi:** Monetisasi B2G/CSR, arsitektur offline Kalimantan, UU PDP, & navigasi BTP. | Strategi proposal CSR Telkom & checklist kepatuhan data anak. |
| **01.15 – 01.25** | 10 Menit | **Diskusi Forum Bersama & Skenario Grand Pilot:** Mengajukan pertanyaan kemitraan tripartit dan permohonan resmi dewan penasihat (*Advisory Board*). | **Kesediaan 3 pakar menjadi Dewan Penasihat Resmi & komitmen tindak lanjut pilot project.** |

---

## 📋 9. Lembar Kendali Pasca-Pertemuan (*Deliverables Checklist*)

Pastikan seluruh butir di bawah ini terisi lengkap dalam transkrip catatan pasca-rapat:

### A. Validasi Ilmiah, Gizi Klinis, & Metodologi Riset (Prof. Heti Ira Ayue)
- [ ] Catatan rekomendasi penyesuaian bobot prediktor CART Decision Tree (Paper GENY).
- [ ] Daftar 3 komoditas ikan air tawar / pangan lokal bernutrisi tinggi untuk MPASI padat kalori.
- [ ] Kontak/rekomendasi nama Ahli Gizi Klinis (AsDI/PERSAGI) atau periset gizi anak (UB/Poltekkes) untuk validasi formula menu.
- [ ] Kriteria inklusi dan eksklusi balita faltering (screening TB anak / PJB) untuk purifikasi data sampel.
- [ ] Estimasi besar sampel minimal (*power sample size*) balita per klaster posyandu untuk signifikansi riset intervensi.
- [ ] Kontak Sekretariat KEPK Poltekkes Palangka Raya dan strategi pengurusan kelaikan etik (*Ethical Clearance*) multi-center.
- [ ] Kesediaan lisan Prof. Heti Ira Ayue sebagai **Scientific & Clinical Advisor** Geny StuntCare.

### B. Kebijakan Faskes, Rujukan Klinis, & Populasi Sasaran (dr. Dewi Rama Dewa) — *VERIFIED 14 OKT 2026*
- [x] **Format Integrasi e-PPGBM & Zero Burden:** Disepakati wajib integrasi 1-pintu ke e-PPGBM/SatuSehat; hindari aplikasi terpisah yang memaksa nakes mengetik ulang.
- [x] **Panduan Komunikasi Klinis Empati:** Tidak boleh langsung melabeli "stunting"; gunakan pertanyaan skrining empati (asupan harian, kebiasaan pentol/mie/sosis, ASI vs sufor, dan paparan asap rokok ayah).
- [x] **Kontak Dokter Spesialis Anak & Gizi:** Terbuka rekomendasi langsung ke **dr. Made, Sp.A (Ketua IDAI Kalimantan Tengah)** dan pengurus **PERSAGI Palangka Raya**.
- [x] **Lokus Faskes Percontohan:** Direkomendasikan **Puskesmas Menteng, Bukit Hindu, dan Kayon** (ASN/terdidik); Wajib hindari **Puskesmas Pahandut & Panarung** (pedagang pasar/fluktuatif).
- [x] **Protokol Pendekatan Komunitas:** Masuk langsung melalui **Bidan Kelurahan & Kader Posyandu ILP**; hindari birokrasi berbelit Ketua TP-PKK Kota.
- [x] **Pintu Masuk Advokasi Anggaran:** Menjadikan **BAPPEDA Kota** sebagai *leading sector* advokasi (pemegang 70% anggaran stunting lintas dinas) disusul Dinkes (30%).
- [x] **Komitmen Pendampingan:** dr. Dewi bersedia memfasilitasi audiensi ke staf/mantan anak buah di Dinkes Kota Palangka Raya dan mengawal rujukan ke Ketua IDAI Kalteng.

### C. Enterprise B2B/B2G, Infrastruktur IoT, & Sinergi Telkom (Bapak Setyohadi) — *VERIFIED 14 OKT 2026*
- [x] **Inisiatif Stunting Telkom:** Konfirmasi keberadaan platform **Stunting Action Hub** berbasis web milik Telkom untuk potensi kolaborasi data training AI.
- [x] **Tata Kelola CSR/TJSL BUMN:** Konfirmasi sistem CSR Telkom tersentralisasi (*one-door*) di kantor pusat dengan prioritas pada *digital capability / digital field*.
- [x] **Pemetaan Yakes Telkom:** Konfirmasi Yakes Telkom sudah tidak aktif di Palangka Raya; validasi corporate wellness diarahkan ke Telkom Regional V Jawa Timur.
- [ ] Kontak person pimpinan atau PIC strategis di unit Digital Health Telkom (Mediv / Yakes / DBT / Indigo).
- [ ] Akses penjajakan kemitraan ke Forum TJSL BUMN wilayah Jawa Timur (Telkom TR-5, Pelindo, SIG) dan Kalimantan.
- [ ] Rekomendasi rekanan vendor perangkat antropometri kit terstandar Kemenkes berbasis IoT / Bluetooth untuk PoC.
- [ ] Checklist kepatuhan standar keamanan enkripsi dan utilisasi cloud NeuCentrIX Telkom (UU PDP No. 27/2022).
- [x] **Kesediaan Arahan Bisnis:** Bpk. Setyohadi memberikan supervisi mengenai lanskap CSR tersentralisasi dan ekosistem data stunting Telkom.

---

<p align="center">
  <em>Disusun dengan standar integritas ilmiah kedokteran, metodologi riset human-centered design, dan tata kelola startup inkubasi Bandung Techno Park (Telkom University).</em>
</p>
