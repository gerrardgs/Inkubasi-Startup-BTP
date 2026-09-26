# 📁 Folder 05: Laporan Data Crawling, Sintesis Laporan Final & 2 Referensi Pendukung Utama

> **Hub Dokumentasi Intelijen Data, Audit Bukti Ilmiah Stunting Nasional, dan Fondasi Algoritmik Platform Geny StuntCare**  
> Disusun untuk: **Inkubasi Startup Batch 24 Bandung Techno Park (BTP) : Telkom University**  
> Penulis / Peneliti Utama: **Gerrard Sebastian** (Informatika Telkom University Surabaya)  
> Tanggal Pembaruan Terakhir: **26 September 2026**

---

## 📌 Ringkasan Eksekutif & Gambaran Umum

Folder ini merupakan **pilar intelijen data dan validasi saintifik paling komprehensif** dalam repositori `Projects21`. Modul ini mendokumentasikan proses *data crawling* multi-sumber, dekonstruksi bukti sekunder, audit silang (*cross-audit*) file historis proyek, serta integrasi metodologis dari **2 referensi pendukung utama**:
1. **Paper GENY (IBITeC 2026)**: *Predicting Childhood Stunting Risk from Field-Recordable Survey Variables Using Decision Tree Learning* (Gerrard Sebastian dkk., 2026).
2. **Buku Tugas Akhir (TA) Stunting**: *Monitoring Stunting pada Balita di Kalimantan Tengah Menggunakan Fuzzy Logic (Studi Kasus Data SKI 2023)* (Gerrard Sebastian, NIM 1203220018, 2026).

Dokumentasi ini membuktikan secara ilmiah mengapa startup **Geny StuntCare** bertransisi dari sekadar "aplikasi edukasi stunting generik" menjadi **platform operasional triase cerdas berbasis lapangan (*field-deployable decision support system*)** yang ditargetkan pada program nasional (Posyandu ILP dan MBG 3B).

```
                            ARSITEKTUR INTELIJEN RISET & MODELING
 ┌────────────────────────────────────────────────────────────────────────────────────────┐
 │ 1. DATA CRAWLING MULTI-SUMBER                                                          │
 │    ├─ Consensus AI Export (102 Halaman, 22 Pertanyaan PECO/PICO Unik)                  │
 │    ├─ Dataset 20 Paper UCD & mHealth Stunting (SJR Analysis, Usability Metrics)        │
 │    ├─ Survei Nasional: SKI 2023 (n=306.281 Balita) & SSGI 2024 (n=294.538 Ibu/Balita)  │
 │    └─ NotebookLM Corpus & AI Synthesis (10 Laporan Audit & 13 Visualisasi Data)        │
 └──────────────────────────────────────────┬─────────────────────────────────────────────┘
                                            │ (Penyaringan & Verifikasi Kritis)
                                            ▼
 ┌────────────────────────────────────────────────────────────────────────────────────────┐
 │ 2. SINTESIS LAPORAN FINAL: DETERMINAN STUNTING (27 HALAMAN, 26 SEP 2026)               │
 │    ├─ Bukti Kuantitatif Terverifikasi: BBLR aOR 2.55; Finansial aOR 0.47 (Q5 vs Q1)     │
 │    ├─ Jalur Pendidikan Ibu: OR 1.2–1.9 (bekerja via Pengetahuan Terapan aOR 1.6)       │
 │    ├─ Bukti Kontra: Faltering Seluruh Populasi (Roth), Meta-analisis Kerawanan Pangan │
 │    ├─ Audit Silang: Menggugurkan 13 Klaim Usang/Halusinasi (DALY Rp275 Jt, MARS lama) │
 │    └─ Rencana Lapangan: 16 Minggu Riset Operasional & Matriks Purposif Sel A–E         │
 └─────────────────────┬──────────────────────────────────────────────┬───────────────────┘
                       │                                              │
                       ▼                                              ▼
 ┌──────────────────────────────────────────┐   ┌─────────────────────────────────────────┐
 │ 3. REFERENSI UTAMA 1: PAPER GENY (2026)  │   │ 4. REFERENSI UTAMA 2: BUKU TA (2026)    │
 │    ├─ Model: CART Decision Tree          │   │    ├─ Model: Sugeno Fuzzy + GA Tuning   │
 │    ├─ Dataset: SKI 2023 (n=304.193)      │   │    ├─ Dataset: SKI 2023 Kalteng (n=389) │
 │    ├─ Akurasi: 75.57%, Macro F1 0.7373   │   │    ├─ Inovasi: Dual Ground Truth HAZ    │
 │    ├─ Screening PPV: 92.76%, Sens: 73.97%│   │    │  (Baseline Lahir vs Pengukuran)    │
 │    ├─ Temuan Inti: TB & Usia = 98.23%    │   │    ├─ Dinamika Trayektori Pertumbuhan   │
 │    │  Feature Importance (Batas WHO)     │   │    └─ Audit Data: Koreksi Tautan Ibu    │
 │    └─ Tanpa TB/Usia: Macro F1 = 0.3565   │   │       (E1) & Bias Bulan Penuh (E3)      │
 └─────────────────────┬────────────────────┘   └─────────────────────┬───────────────────┘
                       │                                              │
                       └──────────────────────┬───────────────────────┘
                                              │
                                              ▼
 ┌────────────────────────────────────────────────────────────────────────────────────────┐
 │ 5. STRATEGI STARTUP GENY STUNTCARE (BTP BATCH 24)                                      │
 │    ├─ Produk: Alat Triase Kader Offline-First (Tanpa Perlu Tabel LMS WHO Manual)       │
 │    ├─ Validasi Lapangan: Pilot Kemitraan Desa Siwalanpanji, Sidoarjo, Jawa Timur       │
 │    └─ Target Pasar: Integrasi B2G/B2B2C dengan Posyandu ILP Kemenkes & SPPG MBG 3B     │
 └────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## 📂 Struktur Berkas dalam Modul Ini

Folder ini dibagi secara sistematis ke dalam 5 dokumen panduan utama serta subdirektori arsip referensi dan aset visual:

| Dokumen | Deskripsi & Fokus Isi | Tautan Langsung |
| :--- | :--- | :--- |
| **01. Laporan Data Crawling** | Hasil *crawling* 102 halaman Consensus, analisis 20 paper UCD, audit korpus NotebookLM, dan statistik makro. | [01_laporan_data_crawling_consensus_dan_ucd.md](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/01_laporan_data_crawling_consensus_dan_ucd.md) |
| **02. Sintesis Laporan Final** | Bedah tuntas 27 halaman Laporan Final: determinan stunting, bukti kontra, audit 13 klaim, dan roadmap 16 minggu. | [02_sintesis_laporan_final_determinan_stunting.md](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/02_sintesis_laporan_final_determinan_stunting.md) |
| **03. Referensi Utama 1 (Paper GENY)** | Analisis saintifik Paper IBITeC 2026: Decision Tree pada 304.193 balita SKI 2023, dominasi TB/usia (98.23%), dan trade-off auditability. | [03_referensi_utama_1_paper_geny.md](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/03_referensi_utama_1_paper_geny.md) |
| **04. Referensi Utama 2 (Buku TA)** | Bedah buku Tugas Akhir (160 halaman): Monitoring Stunting Kalteng dengan Fuzzy Takagi-Sugeno & GA, evaluasi dual HAZ, dan temuan audit. | [04_referensi_utama_2_buku_ta_stunting.md](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/04_referensi_utama_2_buku_ta_stunting.md) |
| **05. Alur Kerja & Integrasi Flow** | Master flow triangulasi data, pipeline preprocessing data mikro, evolusi machine learning, dan operational execution flow. | [05_alur_kerja_dan_integrasi_flow.md](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/05_alur_kerja_dan_integrasi_flow.md) |

---

## 📚 Akses Langsung ke Berkas Referensi Asli (*Direct Reference Files*)

Seluruh berkas dokumen sumber, naskah publikasi, dataset crawling, dan draf audit telah diarsipkan secara lokal dalam subfolder [`references/`](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references) dan dapat diakses langsung melalui tautan di bawah ini:

### 1. Naskah Riset Utama & Buku Tugas Akhir (Tersedia Langsung di Folder Ini)
- 📘 **Buku TA Stunting (Gerrard Sebastian, 160 Halaman)**:  
  [1203220018_GERRARDSEBASTIAN_BUKU_TA_FIXs.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/1203220018_GERRARDSEBASTIAN_BUKU_TA_FIXs.pdf)  
  *(Salinan Arsip: [references/1203220018_GERRARDSEBASTIAN_BUKU_TA_FIXs.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/1203220018_GERRARDSEBASTIAN_BUKU_TA_FIXs.pdf))*
- 📄 **Paper GENY (Draf IEEE IBITeC 2026, 6 Halaman)**:  
  [PaperGeny.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/PaperGeny.pdf)  
  *(Salinan Arsip: [references/PaperGeny.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/PaperGeny.pdf))*
- 📑 **Laporan Final Determinan Stunting Indonesia (27 Halaman, 26 Sep 2026)**:  
  [Laporan_Final_Determinan_Stunting_Indonesia_UPDATE2_26Sep2026.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/Laporan_Final_Determinan_Stunting_Indonesia_UPDATE2_26Sep2026.pdf)  
  *(Salinan Arsip: [references/Laporan_Final_Determinan_Stunting_Indonesia_UPDATE2_26Sep2026.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Laporan_Final_Determinan_Stunting_Indonesia_UPDATE2_26Sep2026.pdf))*
- 🌐 **Ekspor Sesi Consensus AI (102 Halaman, 22 Topik Sintesis)**:  
  [Faktor Faktor Stunting Indonesia - Consensus.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/Faktor%20Faktor%20Stunting%20Indonesia%20-%20Consensus.pdf)  
  *(Salinan Arsip: [references/Faktor Faktor Stunting Indonesia - Consensus.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Faktor%20Faktor%20Stunting%20Indonesia%20-%20Consensus.pdf))*
- 📝 **Laporan Audit & Koreksi Naskah Paper GENY**:  
  [Audit_Paper_GENY_draf_19Agu2026.docx](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Audit_Paper_GENY_draf_19Agu2026.docx)

### 2. Dataset & Seluruh Laporan Crawling NotebookLM (di Subfolder `references/`)
- 📊 **Dataset CSV 20 Paper UCD & Stunting App Adoption**:  
  [Does user-centered design improve stunting app uptake in Indonesian caregivers - 26 Sep 2026.csv](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Does%20user-centered%20design%20improve%20stunting%20app%20uptake%20in%20Indonesian%20caregivers%20-%2026%20Sep%202026.csv)
- 📑 **Dokumen Sintesis & Audit Digital NotebookLM Lengkap (PDF & DOCX)**:  
  - [Audit_Inovasi_Digital_Stunting_Nasional.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Audit_Inovasi_Digital_Stunting_Nasional.pdf) *(15 MB)*
  - [Cetak_Biru_Digitalisasi_Penanganan_Stunting_Indonesia.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Cetak_Biru_Digitalisasi_Penanganan_Stunting_Indonesia.pdf) *(11 MB)*
  - [Dekonstruksi_Krisis_Stunting_Dan_Cetak_Biru_Inovasi_mHealth.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Dekonstruksi_Krisis_Stunting_Dan_Cetak_Biru_Inovasi_mHealth.pdf) *(16 MB)*
  - [Indonesia_Digital_Stunting_Blueprint.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Indonesia_Digital_Stunting_Blueprint.pdf) *(9 MB)*
  - [Strategic_Digital_Stunting_Audit.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Strategic_Digital_Stunting_Audit.pdf) *(18 MB)*
  - [Analisis Komprehensif Faktor Stunting, Kontradiksi Literatur, dan Peluang Pasar Solusi Digital.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Analisis%20Komprehensif%20Faktor%20Stunting,%20Kontradiksi%20Literatur,%20dan%20Peluang%20Pasar%20Solusi%20Digital.pdf)
  - [Digital Solutions for Stunting Prevention and Child Growth Monitoring.pdf](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Digital%20Solutions%20for%20Stunting%20Prevention%20and%20Child%20Growth%20Monitoring.pdf)
  - [Laporan_Audit_Inovasi_Digital_Stunting_v3.docx](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/references/Laporan_Audit_Inovasi_Digital_Stunting_v3.docx)

---

## 🖼️ Galeri Visual & Audit Aset Grafik

Aset grafik historis (`chart1` s.d. `chart7`) dan diagram metodologis telah diaudit dan disimpan dalam [`assets/`](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/assets):
- [chart1_trend_publikasi_v3.png](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/assets/chart1_trend_publikasi_v3.png): Tren publikasi aplikasi stunting di Indonesia (2019–2026).
- [chart2_distribusi_sasaran_v2.png](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/assets/chart2_distribusi_sasaran_v2.png): Proporsi target pengguna aplikasi stunting (Kader vs Pengasuh vs Nakes).
- [chart3_mars_benchmarking_v3.png](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/assets/chart3_mars_benchmarking_v3.png): Benchmark kualitas aplikasi pediatrik berdasarkan skala MARS terverifikasi (Irawan dkk., 2025).
- [chart4_odds_ratio_stunting_v3.png](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/assets/chart4_odds_ratio_stunting_v3.png): Forest plot ringkasan Odds Ratio determinan stunting nasional.
- [chart5_efisiensi_operasional_kader_v3.png](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/assets/chart5_efisiensi_operasional_kader_v3.png): Bukti efisiensi input data kader (SI-MASTING: 7,1 mnt ➔ 2,4 mnt, galat 15,4% ➔ 2,1%).
- [stunting_mhealth_impact_and_risk_matrix.png](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/assets/stunting_mhealth_impact_and_risk_matrix.png): Matriks dampak klinis versus risiko adopsi solusi digital stunting.

---

## 🎯 Hubungan Strategis dengan Inkubasi BTP Batch 24

Seluruh bukti empiris dalam modul ini menjadi dasar pertanggungjawaban dalam modul **Startup Readiness Level (SRL)** BTP:
1. **SRL 0 (Competencies & Market Analysis)**: Memetakan keunggulan kompetitif tim di bidang komputasi biomedis cerdas (Fuzzy Logic & Decision Tree) dan pemahaman mendalam tentang data survei kesehatan skala besar (SKI 2023).
2. **SRL 1 (Problem Validation)**: Membuktikan bahwa masalah stunting di Indonesia telah bergeser dari sekadar *"masalah ketidaktahuan"* menjadi *"masalah ketidakmampuan daya beli, lambatnya diagnosis dini di posyandu, dan rendahnya kualitas input antropometri"*.
3. **SRL 2 (Solution Validation & Value Proposition)**: Mengembangkan proposisi nilai **Geny StuntCare**: alat bantu kerja kader Posyandu offline-first yang mampu menghitung Z-score WHO secara otomatis tanpa perlu membuka tabel LMS fisik, tervalidasi dengan sensitivitas triase 73,97% dan PPV 92,76%.
4. **SRL 3 (MVP Development & Pilot)**: Mengarahkan arsitektur prototipe mobile berbasis aturan keputusan transparan yang telah diujicobakan bersama mitra komunitas di Desa Siwalanpanji, Sidoarjo.

---
*Buka dokumen pertama untuk memulai eksplorasi teknis:*  
👉 **[Lanjut ke 01. Laporan Data Crawling Consensus & UCD Papers ➔](file:///Users/sinitygs/Projects21/05-laporan-data-crawling/01_laporan_data_crawling_consensus_dan_ucd.md)**
