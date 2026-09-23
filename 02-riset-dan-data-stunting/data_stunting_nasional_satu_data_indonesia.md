# Data Stunting Nasional — Portal Satu Data Indonesia (data.go.id)
## Referensi Riset & Validasi Baseline Masalah Stunting Balita di Indonesia

Dokumen ini mendokumentasikan dataset resmi prevalensi stunting nasional dari portal Satu Data Indonesia (Kementerian Perencanaan Pembangunan Nasional / Bappenas & Kementerian Kesehatan RI) yang menjadi landasan problem statement startup **Geny StuntCare**.

---

## 1. Tautan Dataset Resmi Pemerintah

### Dataset 1: Prevalensi Stunting (Pendek dan Sangat Pendek) pada Anak Balita
* **Tautan Sumber:** [Portal Satu Data Indonesia - Dataset 1](https://data.go.id/dataset/dataset/prevalesi-stunting-pendek-dan-sangat-pendek-pada-anak-balita)
* **Organisasi Pembuat Data:** Kementerian Kesehatan Republik Indonesia
* **Definisi Indikator:**
  * Persentase anak usia di bawah lima tahun (balita 0–59 bulan) yang memiliki indeks Tinggi Badan menurut Umur (TB/U) atau Panjang Badan menurut Umur (PB/U) kurang dari **-2 Standar Deviasi (-2 SD)** dari standar kurva pertumbuhan WHO.
  * Kategori:
    * **Pendek (*stunted*):** Z-score antara -2 SD sampai dengan -3 SD.
    * **Sangat Pendek (*severely stunted*):** Z-score kurang dari -3 SD.

### Dataset 2: Prevalensi Stunting pada Balita
* **Tautan Sumber:** [Portal Satu Data Indonesia - Dataset 2](https://data.go.id/dataset/dataset/prevalensi-stunting-pada-balita)
* **Frekuensi Pembaruan:** Tahunan / Survei Status Gizi Indonesia (SSGI) & Survei Kesehatan Indonesia (SKI)
* **Cakupan Wilayah:** 38 Provinsi di Indonesia, mencakup agregat tingkat Nasional, Provinsi, dan Kabupaten/Kota.

---

## 2. Analisis Tren & Urgensi Masalah

### A. Target Penurunan Nasional (RPJMN & SDGs)
1. **Target RPJMN 2020–2024:** Pemerintah Indonesia menargetkan penurunan prevalensi stunting balita menjadi **14%**.
2. **Kondisi Riil:** Meskipun tren prevalensi stunting mengalami penurunan bertahap (dari ~30.8% pada Riskesdas 2018 menjadi 21.6% pada SSGI 2022 dan ~21.5% pada SKI 2023), penurunan ini belum merata di seluruh kabupaten/kota dan masih menyisakan kesenjangan disparitas wilayah yang signifikan.
3. **Standar WHO:** Batas ambang (*threshold*) batas toleransi kesehatan masyarakat dari WHO untuk stunting adalah **< 20%**. Indonesia saat ini masih berada di sekitar batas kritis tersebut.

### B. Faktor Penyebab Utama (Akar Masalah)
1. **Periode Kritis 1000 Hari Pertama Kehidupan (HPK):**
   * Mulai dari konsepsi dalam kandungan (270 hari kehamilan) hingga anak berusia 2 tahun (730 hari).
   * Kerusakan perkembangan fisik dan kognitif akibat stunting pada fase ini bersifat **irreversibel** (tidak dapat diperbaiki sempurna setelah usia 2 tahun).
2. **Intervensi Spesifik (Penyebab Langsung):**
   * Asupan gizi mikro dan makro ibu hamil (anemia, Kurang Energi Kronis / KEK).
   * Praktik Inisiasi Menyusu Dini (IMD) dan ASI Eksklusif 6 bulan pertama yang belum optimal.
   * Kualitas dan ketepatan Makanan Pendamping ASI (MPASI) yang kaya protein hewani (telur, ikan, daging, ayam).
   * Status imunisasi dasar lengkap dan penanganan infeksi berulang (diare, ISPA, kecacingan).
3. **Intervensi Sensitif (Penyebab Tidak Langsung):**
   * Akses air minum layak dan sanitasi keluarga (Jamban Sehat / ODF).
   * Tingkat literasi gizi orang tua dan ibu muda.
   * Jarak dan aksesibilitas geografis menuju fasilitas pelayanan posyandu/puskesmas.
   * Faktor pengasuhan dan perhatian orang tua terhadap pemantauan kurva KMS (Kartu Menuju Sehat).

---

## 3. Relevansi Data dengan Value Proposition Geny StuntCare

Berdasarkan dataset nasional di atas, startup **Geny StuntCare** hadir untuk mengatasi bottleneck pada pemantauan dan intervensi dini:

| Bottleneck Lapangan | Data Pendukung | Solusi Geny StuntCare (`genystuntcare.com`) |
| :--- | :--- | :--- |
| **Keterlambatan Deteksi** | Balita baru teridentifikasi stunting saat usia > 24 bulan | Modul deteksi dini risiko stunting berbasis input antropometri digital dan machine learning |
| **Absensi Posyandu** | Banyak balita tidak dipantau pertumbuhannya secara rutin setiap bulan | Pemantauan mandiri oleh orang tua lewat web platform + notifikasi reminder jadwal tumbuh kembang |
| **Literasi MPASI Rendah** | Asupan protein hewani rendah pada keluarga muda | Rekomendasi nutrisi personal berbasis pangan lokal yang terjangkau |
| **Disparitas Wilayah** | Data posyandu di daerah pelosok lambat terintegrasi ke faskes | Sistem agregasi data real-time untuk kader posyandu dan puskesmas |
