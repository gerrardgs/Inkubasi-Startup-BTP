# SRL 3 — MVP Readiness

**Core Question:** Can we implement the solution as an MVP and generate real learning from users?

## What — Apa yang divalidasi?

Apakah solusi yang sudah divalidasi sebelumnya **sudah cukup matang untuk dibuat menjadi MVP**, lalu digunakan oleh real user untuk menghasilkan data dan pembelajaran?

MVP bukan produk final dan bukan sekadar versi kecil dari produk. MVP adalah **versi minimum yang sudah mampu menyelesaikan core problem dan menghasilkan data nyata dari user.**

## Why — Kenapa?

Karena tujuan MVP bukan hanya _“produk sudah jadi”_, tetapi:

1. **Solve a meaningful problem**, menyelesaikan masalah utama yang penting bagi user.

2. **Generate measurable data**, menghasilkan data yang bisa diukur untuk mengambil keputusan.

`MVP = Core Problem + Real User + Measurable Learning`

Jadi, MVP digunakan untuk menjawab:

`“Apakah solusi kita benar-benar bekerja ketika digunakan oleh user?”`

## How — Bagaimana caranya?

### 1. Tentukan Core Problem

Jangan mencoba menyelesaikan semua masalah user sekaligus.

Misalnya user memiliki 5 masalah:

- A → **core problem**
- B → non-core
- C → non-core
- D → non-core
- E → non-core

MVP cukup fokus menyelesaikan A, sementara B–E boleh tetap menggunakan existing solution yang sudah dimiliki user.

**MVP bukan smaller version, tetapi core version.**

### 2. Buat Functional MVP

MVP harus benar-benar bisa digunakan, bukan hanya prototype.

Pertanyaan:

`“Fitur minimum apa yang dibutuhkan agar user bisa mendapatkan solusi terhadap core problem?”`

### 3. Gunakan dengan Early Adopters

Berikan MVP kepada user yang memang mengalami masalah tersebut.

Yang dicari bukan sekadar:

`“Apakah mereka suka produknya?”`

Tetapi:

`“Apa yang mereka lakukan ketika menggunakan produk?”`

Karena **behavior lebih valuable daripada sekadar opinion.**

### 4. Buat Feedback Mechanism

Setiap penggunaan harus menghasilkan feedback/data.

Contoh:

- penggunaan fitur
- completion rate
- jumlah user aktif
- waktu penyelesaian task
- error
- feedback langsung
- interview
- retention
- conversion

### 5. Masukkan Learning ke Product Backlog

Temuan dari user → diterjemahkan menjadi backlog.

Contoh:

**User Feedback**

`“Saya bingung menentukan status risiko anak.”`

↓

**Learning**

`User membutuhkan interpretasi hasil yang lebih sederhana.`

↓

**Backlog**

`Tambahkan penjelasan status risiko.`

## Evidence — Bukti yang harus tersedia

| Evidence                      | Yang dibuktikan                                 |
| ----------------------------- | ----------------------------------------------- |
| **1. Functional MVP**         | MVP benar-benar dapat digunakan                 |
| **2. Early Adopter Data**     | Ada data dari pengguna awal                     |
| **3. User Testing**           | MVP sudah dites oleh real user                  |
| **4. Feedback Mechanism**     | Ada cara sistematis mengambil feedback          |
| **5. Product Backlog**        | Learning diterjemahkan menjadi pekerjaan produk |
| **6. Iteration History**      | Ada bukti perubahan berdasarkan learning        |
| **7. Version Change**         | Ada perubahan antar-versi MVP                   |
| **8. MVP Validation Results** | Ada kesimpulan berdasarkan data                 |

### Iteration — Bagian paling penting

#### The Iteration Loop

**Hypothesis → Experiment → Data → Learning → Adapt → Retest**

Contoh:

**Hypothesis**

`Ibu akan menggunakan fitur monitoring pertumbuhan anak jika hasilnya mudah dipahami.`

↓

**Experiment**

`Berikan MVP kepada 10 ibu.`

↓

**Data**

`8 menggunakan fitur, tetapi 5 meminta penjelasan tambahan.`

↓

**Learning**

`Fitur digunakan, tetapi interpretasi hasil belum cukup jelas.`

↓

**Adapt**

`Sederhanakan hasil dan tambahkan penjelasan.`

↓

**Retest**

`Berikan versi berikutnya kepada user.`

**Untuk Software: Iteration = Backlog → Release → Feedback → Backlog**

Jadi iteration bukan sekadar **“kami update aplikasi”**.

Yang penting adalah:

`Ada perubahan produk yang berasal dari learning user.`

Contoh:

→**MVP v0.1**
→ Testing user
→ Feedback
→ Backlog
→ **MVP v0.2**
→ Testing lagi
→ Feedback
→ Backlog
→ **MVP v0.3**

Minimal harus ada 1 iteration, sehingga bisa menunjukkan:

**v0.1 → user feedback → perubahan → v0.2**

### Pivot — Kapan dilakukan?

Pivot **bukan dilakukan karena feeling.**

Gunakan prinsip:

`“Datanya bilang apa?”`

Misalnya:

**Hypothesis**:
`User membutuhkan AI prediction.`

**Data**:
`User ternyata lebih sering menggunakan fitur monitoring dan hampir tidak menggunakan AI prediction.`

**Learning:**
`Core value mungkin bukan prediction, tetapi monitoring.`

Maka tim bisa mempertimbangkan perubahan arah berdasarkan **evidence**, bukan asumsi.

## Next — Apa yang harus dilakukan di SRL 3?

Untuk GENY–StuntCare, kamu bisa mulai dengan membuat:

- Define Core Problem MVP
- Tentukan fitur minimum
- Tentukan Early Adopter
- Buat Functional MVP
- Tentukan metrik yang diukur
- Test ke real user
- Kumpulkan feedback
- Masukkan hasil ke backlog
- Buat Version 2
- Bandingkan data sebelum vs sesudah
- Tentukan: Continue / Adapt / Pivot

Inti SRL 3:

`Bukan “Apakah kita sudah punya aplikasi?”
tetapi “Apakah kita punya MVP yang menyelesaikan core problem dan menghasilkan cukup evidence untuk menentukan langkah berikutnya?”`
