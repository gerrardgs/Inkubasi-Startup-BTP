# SLR 1 GENY STUNTCARE : Problem Validation & Action Plan
## Rencana Aksi Validasi Masalah, Riset Lapangan, dan Uji Ahli (Stage 1 Inkubasi BTP)

Dokumen ini merupakan transkripsi resmi, elaborasi sistematis, dan rencana kerja operasional yang dikembangkan dari catatan lapangan **SLR 1 Geny StuntCare** (Gambar 1).

---

## 1. Fondasi Problem Validation (Framework 5 Pertanyaan Kunci)

Sesuai metodologi *Startup Readiness Level 1 (SRL 1)* BTP, sebelum membangun atau memodifikasi fitur teknologi pada platform `genystuntcare.com`, tim wajib memvalidasi 5 pertanyaan inti:

1. **Siapa Customer?**
   - Pihak yang memiliki anggaran atau kewenangan membeli/mengadopsi solusi (Dinas Kesehatan, Puskesmas, Yayasan Kesehatan Telkom/Yakes, Program CSR korporat, atau orang tua yang membayar paket premium konsultasi gizi).
2. **Siapa User?**
   - Pihak yang berinteraksi langsung dengan antarmuka aplikasi/web setiap hari (Ibu muda, ibu pekerja, kader posyandu, bidan desa, dan calon pengantin/catin).
3. **Apa Aktivitas Mereka?**
   - Mengasuh anak, memasak MPASI, menimbang balita di posyandu sebulan sekali, bekerja di kantor/pabrik/sawah, mengakses ponsel pintar (media sosial, chat WhatsApp), dan mencatat KMS buku KIA.
4. **Apa Kebutuhan Mereka?**
   - Kepastian bahwa anak tumbuh normal dan tidak stunting.
   - Cara praktis memantau status gizi tanpa harus mengantre lama di posyandu.
   - Panduan menu gizi seimbang yang tidak mahal dan mudah diolah.
   - Peringatan dini (*early alert*) bila anak mengalami keterlambatan pertumbuhan.
5. **Di Mana Mereka Berkumpul?**
   - **Offline:** Meja Posyandu, Puskesmas Pembantu, Balai Desa, Arisan RT/RW, Pengajian Ibu-Ibu, Ruang Laktasi Kantor/Pabrik, KUA/Gereja (kursus pranikah).
   - **Online:** WhatsApp Group RT/RW/Posyandu, Grup Facebook Komunitas Ibu & Balita, Akun Instagram/TikTok parenting dan resep MPASI.

---

## 2. Metode & Instrumen Riset (*Tools*)

Untuk memperoleh data empiris yang objektif dan terhindar dari bias asumsi, validasi dilakukan melalui 3 instrumen:
* **Interview (Wawancara Mendalam):** Menggali cerita pengalaman riil, kebiasaan, emosi, dan *Jobs to be Done* (JTBD) customer.
* **Survey (Kuesioner Terstruktur):** Mengukur frekuensi kejadian, persentase perilaku, dan pola skala besar (*pattern recognition*).
* **Observasi Langsung:** Mengamati secara objektif perilaku riil di lapangan tanpa mendikte subjek (misal: waktu antre posyandu, cara ibu mengukur tinggi badan, interaksi dengan gadget).

---

## 3. Rencana Aksi Audit Internal Platform (`genystuntcare.com`)

Sebelum terjun ke lapangan, tim melakukan audit metrik internal terhadap data pengguna platform saat ini:

* [ ] **Cek Jumlah Akun Sekarang:**
  - Melakukan rekapitulasi total pengguna terdaftar di basis data `genystuntcare.com`.
* [ ] **Cek Sebaran User (Geographical Distribution):**
  - Memetakan asal kota/kabupaten dan provinsi dari pengguna terdaftar (Jawa Timur, Jawa Tengah, Jawa Barat, atau luar Jawa).
* [ ] **Cek Profil Pengguna (User vs Customer Breakdown):**
  - Mengelompokkan profil akun: berapa persen ibu balita, kader posyandu, tenaga medis, atau masyarakat umum.
* [ ] **Cek Retensi & Recurring Active Users (Berapa yang Login Ulang):**
  - Mengukur *Retention Rate* 7 hari dan 30 hari: berapa persen pengguna yang kembali membuka web untuk input data pertumbuhan bulan kedua/ketiga.

---

## 4. Rencana Wawancara Pengguna (User Interview Plan)

### A. Target Segmen Eksisting
1. **Ibu Muda (Milenial / Gen Z):**
   - Menggali pemahaman mereka mengenai stunting, cara mereka mencari informasi gizi anak, dan preferensi penggunaan aplikasi smartphone vs buku KIA fisik.
2. **Ibu Bekerja (*Working Mothers*):**
   - Menggali kendala waktu menghadiri posyandu bulanan (karena jam kerja berbenturan), pola delegasi pengasuhan ke nenek/daycare, dan cara memantau menu harian anak dari jarak jauh.
3. **Kader Posyandu & Bidan:**
   - Menggali beban kerja pencatatan manual di buku register posyandu, kendala memasukkan data ke e-PPGBM, serta kesulitan memanggil ibu balita agar hadir rutin.

### B. Target Segmen Baru (Edukasi Hulu 1000 HPK)
1. **Calon Pengantin (Catin):**
   - Menilai tingkat kesadaran calon pengantin tentang pencegahan stunting sebelum kehamilan (lingkar lengan atas/LILA, kadar hemoglobin/anemia, konsumsi tablet tambah darah).
2. **Mbak-Mbak / Remaja Putri Pranikah:**
   - Menguji apakah topik stunting relevan bagi mereka, atau materi apa yang perlu dikemas agar menarik minat belajar kesehatan reproduksi sejak dini.

---

## 5. Rencana Survei Lapangan (Hypothesis Testing)

Survei dirancang untuk menguji validitas 3 hipotesis masalah utama yang diajukan tim:

| No | Hipotesis Masalah yang Diajukan | Pertanyaan Validasi Kuesioner | Kriteria Sukses Validasi |
| :---: | :--- | :--- | :--- |
| **H1** | **Posyandu jarang didatangi oleh ibu-ibu muda** | *"Dalam 6 bulan terakhir, berapa kali Ibu datang langsung ke posyandu untuk menimbang balita? Apa alasan utama jika tidak hadir?"* | > 40% responden ibu muda hadir < 4 kali dalam 6 bulan terakhir karena bentrok waktu atau merasa tidak praktis. |
| **H2** | **Banyak kasus stunting di daerah yang jarak ke posyandunya jauh/terpencil** | *"Berapa jarak tempuh dan waktu yang dibutuhkan dari rumah Ibu menuju lokasi posyandu terdekat? Apakah ada kendala transportasi?"* | Korelasi positif antara jarak > 2 km dengan penurunan frekuensi penimbangan balita dan peningkatan risiko gizi kurang. |
| **H3** | **Banyak ibu-ibu yang terlalu fokus main HP sehingga perhatian pengasuhan gizi terdistraksi / preferensi media digital sangat tinggi** | *"Berapa jam sehari Ibu menggunakan HP untuk bermedia sosial? Dari mana Ibu paling sering mendapatkan tips MPASI dan kesehatan anak?"* | > 70% ibu mengakses HP > 3 jam/hari dan lebih menyukai tips video/infografis singkat dibanding buku bacaan tebal. |

---

## 6. Observasi Kuantitatif Lapangan

Tim tidak hanya mengandalkan wawancara lisan, melainkan melakukan pengukuran kuantitatif langsung saat pelaksanaan posyandu:
* **Waktu Tunggu:** Menghitung menit rata-rata dari kedatangan ibu hingga selesai penimbangan & pencatatan.
* **Tingkat Partisipasi (D/S):** Menghitung rasio balita yang ditimbang (D) dibandingkan total balita yang ada di wilayah posyandu (S).
* **Kepatuhan Jadwal:** Menghitung persentase ibu yang rutin datang setiap bulan berturut-turut.
* **Durasi Skrining:** Mengukur waktu yang dihabiskan kader untuk menjelaskan grafik status pertumbuhan ke ibu balita.

---

## 7. Rencana Pengujian oleh Ahli (*Expert Evaluation*)

Platform web `genystuntcare.com` yang telah berjalan akan dievaluasi secara komprehensif oleh panel ahli lintas disiplin:

1. **Aspek yang Dievaluasi:**
   - **User Interface (UI):** Kerapian visual, keterbacaan tipografi, kejelasan tombol aksi (*Call to Action*), dan daya tarik tampilan di layar mobile.
   - **User Experience (UX):** Kemudahan alur pengisian data antropometri (*user flow*), kecepatan navigasi, dan kemudahan bagi ibu awam/kader senior dalam memahami grafik status stunting.
   - **Model Algoritma & Akurasi Medis:** Validitas rumus perhitungan Z-score WHO, klasifikasi stunting/wasting/underweight, serta ketepatan rekomendasi gizi yang dimunculkan sistem.
2. **Panel Ahli yang Dilibatkan:**
   - **Akademisi / Researcher:** Dosen Telkom University (Pakar Rekayasa Perangkat Lunak, Human-Computer Interaction, dan Data Science).
   - **Praktisi Medis Lapangan:** Tim Medis & Ahli Gizi **Yakes Telkom** (Yayasan Kesehatan Telkom) serta praktisi kesehatan masyarakat.

---

## 8. Cakupan Wilayah Lapangan (*Fieldwork Geographical Scope*)

Aktivitas survei, wawancara, dan observasi langsung akan dijalankan di 8 titik wilayah strategis:

```
[Wilayah Sasaran Lapangan Geny StuntCare]
├── 1. Kota Malang (Area Urban / Perkotaan)
├── 2. Kabupaten Banyuwangi (Area Pesisir & Program Stunting Inovatif)
├── 3. Siwalanpanji, Kabupaten Sidoarjo (Area Pemukiman Semi-Urban & Komunitas)
├── 4. Turen, Kabupaten Malang (Area Rural / Kabupaten Malang Selatan)
├── 5. Kabupaten Magetan (Area Agrikultur / Pegunungan)
├── 6. Gondanglegi, Kabupaten Malang (Area Padat Penduduk Kabupaten Malang)
├── 7. Kota Surabaya (Metropolitan / Disparitas Urban Slum)
└── 8. Kota Jember (Area Perkebunan & Tapal Kuda Jawa Timur)
```

---

## 9. Target Progres Data & Integrasi Sekunder

* **Target Data Primer Awal:** Mengumpulkan minimal **21 data responden valid** (kombinasi ibu balita, ibu hamil, catin, dan kader posyandu) sebagai *baseline sample* pertama.
* **Target Data Sekunder:** Mengunduh dan menelaah publikasi data resmi **Badan Pusat Statistik (BPS)** untuk memperkuat data pembanding demografi wilayah di 8 lokasi tersebut.
