# PROYEK LAB SAINS DATA — KELOMPOK 11

## Analisis Ulasan Pelanggan Tokopedia untuk Penentuan Prioritas Perbaikan Produk

Repositori ini digunakan untuk mendokumentasikan seluruh perkembangan proyek kelompok pada mata kuliah **Lab Sains Data**, Program Studi Bisnis Digital, Fakultas Ekonomika dan Bisnis, Universitas Diponegoro.

Proyek ini berangkat dari permasalahan bisnis penjual online yang mengalami kesulitan dalam mengidentifikasi dan menentukan prioritas keluhan pelanggan berdasarkan ulasan yang diberikan. Melalui pendekatan analisis data, kelompok berupaya mengolah informasi berupa teks ulasan dan rating pelanggan menjadi informasi yang dapat mendukung pengambilan keputusan bisnis.

---

## Identitas Proyek

| Keterangan | Informasi |
|---|---|
| Mata Kuliah | Lab Sains Data |
| Dosen Pengampu | Nana Varian Januardi, S.E., MBA |
| Program Studi | Bisnis Digital |
| Fakultas | Ekonomika dan Bisnis |
| Universitas | Universitas Diponegoro |
| Kelompok | 11 |
| Tahun Akademik | 2026 |

### Anggota Kelompok

1. Della Selviana
2. Keyra Anantasya P
3. Augustinus Giovanni

---

## 1. Latar Belakang dan Identifikasi Permasalahan

Pada tahap awal proyek, kelompok melakukan identifikasi terhadap berbagai permasalahan yang ditemukan di lingkungan mahasiswa, kegiatan UMKM, dan aktivitas bisnis digital.

Sebanyak **30 permasalahan** berhasil dihimpun dan kemudian diseleksi menjadi tiga calon permasalahan yang dinilai berpotensi dikembangkan melalui pendekatan analisis data.

Tiga permasalahan yang dipertimbangkan adalah:

1. Mahasiswa kesulitan memilih kos sesuai anggaran, lokasi, dan fasilitas.
2. Usaha makanan kesulitan menentukan jumlah porsi yang perlu disiapkan.
3. Penjual online kesulitan menentukan keluhan pelanggan yang perlu diprioritaskan.

Berdasarkan pertimbangan awal, kelompok memilih permasalahan ketiga sebagai fokus utama proyek, yaitu kesulitan penjual online dalam menentukan prioritas keluhan pelanggan.

Permasalahan tersebut dipilih karena ulasan pelanggan mengandung informasi mengenai pengalaman pembelian, penilaian produk, dan kemungkinan permasalahan yang perlu ditindaklanjuti oleh penjual.

## 2. Keputusan Bisnis

Keputusan bisnis yang ingin didukung melalui proyek ini adalah:

**Menentukan jenis permasalahan pelanggan yang perlu diprioritaskan untuk diperbaiki oleh penjual online berdasarkan informasi dalam ulasan pelanggan.**

Pada tahap analisis awal, ruang lingkup proyek difokuskan pada ulasan produk perangkat handphone di Tokopedia, terutama aspek kualitas produk.

Aspek pengemasan, pengiriman, dan pelayanan penjual tetap dapat dicatat apabila ditemukan dalam ulasan, tetapi tidak menjadi fokus utama pemodelan pada tahap ini.

## 3. Empat Jenis Analitik dan Pertanyaan Analitik

Proyek ini menggunakan empat pendekatan analitik sebagai dasar pengolahan dan interpretasi data.

| Jenis Analitik | Pertanyaan Analitik |
|---|---|
| Descriptive Analytics | Bagaimana distribusi rating dan tema keluhan kualitas produk yang ditemukan dalam ulasan perangkat handphone? |
| Diagnostic Analytics | Pola masalah kualitas produk apa yang lebih sering ditemukan pada ulasan dengan rating rendah setelah teks diperiksa dan diberi label secara manual? |
| Predictive Analytics | Seberapa baik model klasifikasi teks dapat mengidentifikasi kategori masalah kualitas produk pada ulasan baru berdasarkan data berlabel yang telah diverifikasi? |
| Prescriptive Analytics | Jenis masalah kualitas produk apa yang sebaiknya diprioritaskan berdasarkan frekuensi temuan terverifikasi, rating, dan tingkat dampak atau urgensi? |

## 4. Sumber dan Karakteristik Data

Dataset utama yang digunakan adalah **Tokopedia Product Reviews 2019**.

Sumber dataset:
https://huggingface.co/datasets/farhamu/tokopedia-product-reviews-2019

Karakteristik dataset sumber:

- Jumlah data: 40.607 ulasan.
- Jumlah atribut: 8 kolom.
- Kategori produk: 5 kategori.
- Format: CSV.
- Bahasa ulasan: Indonesia.
- Lisensi yang dicantumkan pada dataset card: Apache 2.0.

Dataset memiliki beberapa atribut utama, yaitu:

- `text`: isi ulasan pelanggan.
- `rating`: penilaian pelanggan dari 1 sampai 5.
- `category`: kategori produk.
- `product_name`: nama produk.
- `product_id`: identitas produk.
- `sold`: informasi jumlah produk terjual.
- `shop_id`: identitas toko.
- `product_url`: tautan produk.

## 5. Hasil Pemeriksaan dan Seleksi Data

Kategori handphone pada dataset sumber memiliki 6.136 ulasan. Namun, kategori tersebut juga dapat mencakup aksesori dan komponen produk.

Untuk meningkatkan relevansi data, kelompok melakukan penyaringan berdasarkan nama dan karakteristik produk.

Hasil pemeriksaan awal:

| Keterangan | Jumlah |
|---|---:|
| Ulasan kategori handphone pada sumber | 6.136 |
| Kandidat setelah penyaringan produk | 1.279 |
| Pasangan duplikat produk dan teks yang dihapus | 2 |
| Subset operasional setelah penyaringan | 1.277 |
| Produk unik | 18 |
| Toko unik | 7 |

Subset tersebut digunakan sebagai dasar analisis deskriptif awal dan persiapan anotasi.

### Distribusi Rating

Distribusi rating pada 1.277 ulasan yang telah disaring:

| Rating | Jumlah |
|---|---:|
| 1 | 14 |
| 2 | 101 |
| 3 | 191 |
| 4 | 335 |
| 5 | 636 |
| **Total** | **1.277** |

Rating 5 merupakan kategori terbanyak dalam subset. Namun, rating tidak secara otomatis menunjukkan jenis keluhan atau sentimen dalam teks. Oleh karena itu, pemeriksaan isi ulasan tetap diperlukan.

## 6. Tahapan dan Progress Proyek

Tabel berikut menunjukkan kesinambungan pengerjaan proyek berdasarkan tahapan perkuliahan dan hasil yang benar-benar telah disiapkan.

| Tahap | Kegiatan | Status |
|---|---|:---:|
| Week 1 | Mengidentifikasi 30 permasalahan bisnis | Selesai |
| Week 1 | Menyeleksi 3 calon permasalahan | Selesai |
| Week 1 | Menyusun rancangan empat jenis analitik | Selesai |
| P8 | Menetapkan masalah utama dan keputusan bisnis | Selesai |
| P8 | Memilih sumber data dan melakukan pemeriksaan awal | Selesai |
| P8 | Menyaring dataset berdasarkan relevansi produk | Selesai |
| P8 | Menyusun kamus data dan dokumentasi sumber | Selesai |
| P9 | Menyiapkan sampel 300 ulasan untuk anotasi | Disiapkan |
| P9 | Melakukan pelabelan dan verifikasi manual | Belum |
| P10 | Melakukan pembersihan lanjutan dan analisis SQL menggunakan DuckDB | Belum |
| P11 | Memeriksa klaim dan hasil analisis terhadap data | Belum |
| P12 | Membandingkan alternatif dan menyusun memo keputusan | Belum |
| P13 | Membuat dashboard dan notebook analisis | Belum |
| P14 | Menyusun keputusan akhir dan portofolio proyek | Belum |

**Keterangan status:**

- **Selesai:** pekerjaan telah dilakukan dan memiliki hasil yang dapat diperiksa.
- **Disiapkan:** perangkat atau bahan kerja telah tersedia, tetapi belum seluruh prosesnya dilaksanakan.
- **Belum:** kegiatan belum dilaksanakan dan belum diklaim sebagai hasil proyek.

Status akan diperbarui secara berkala berdasarkan perkembangan pekerjaan kelompok.

## 7. Struktur Repository

Repository ini disusun berdasarkan fungsi dokumentasi dan tahapan pengolahan data.

```text
LabSainsData_Kelompok11/
│
├── README.md
├── .gitignore
├── LOG-PENGGUNAAN-AI.md
│
├── 01-dokumentasi/
│   ├── README.md
│   ├── Laporan_Progress_Week_1.pdf
│   └── Laporan_Lanjutan_Progress_Week_1.docx
│
├── 02-data/
│   ├── README.md
│   ├── dataset_ulasan_perangkat_handphone.csv
│   ├── sampel_anotasi_ulasan_300.csv
│   └── kamus_data.csv
│
├── 03-visualisasi/
│   ├── README.md
│   ├── distribusi_kategori_dataset.png
│   └── distribusi_rating_handphone.png
│
├── 04-analisis/
│   └── README.md
│
└── 05-referensi/
    └── README.md
```

## 8. Dokumentasi Penggunaan AI

Dalam proses pengerjaan, kelompok menggunakan bantuan AI sebagai pendukung eksplorasi ide, penyusunan rancangan analisis, dan persiapan pengolahan data.

Setiap penggunaan AI akan didokumentasikan, termasuk:

- Tujuan penggunaan AI.
- Pertanyaan atau instruksi yang diberikan.
- Hasil yang dihasilkan AI.
- Proses pemeriksaan dan verifikasi.
- Koreksi apabila terdapat informasi yang tidak sesuai.

Hasil AI tidak langsung dianggap benar dan tetap harus diperiksa berdasarkan sumber data serta kebutuhan akademik.

## 9. Referensi dan Sumber Data

1. Farhamu. (2019). *Tokopedia Product Reviews 2019*. Hugging Face Dataset.  
   https://huggingface.co/datasets/farhamu/tokopedia-product-reviews-2019

2. Materi perkuliahan Lab Sains Data, Pertemuan 8: Dari Keputusan ke Data.

3. Panduan Tugas Kecil 1: Paket Dasar, Keputusan, dan Sumber Data.

4. Dokumentasi Hugging Face Datasets:  
   https://huggingface.co/docs/datasets

## 10. Dokumen Laporan Proyek

Dokumen laporan disusun secara bertahap mengikuti perkembangan proyek.

- **Progress Week 1:** Identifikasi dan pemilihan permasalahan bisnis.
- **Laporan Lanjutan:** Pemilihan sumber data, pemeriksaan kualitas data, penyaringan dataset, dan analisis deskriptif awal.

Laporan lengkap dan berkas pendukung dapat ditemukan pada folder `01-dokumentasi/` dan `02-data/`.

## 11. Rencana Pengembangan Selanjutnya

Setelah tahap pemeriksaan dan persiapan data, kelompok akan melanjutkan proses anotasi manual, validasi label, analisis diagnostik, pengembangan model prediktif, serta penyusunan rekomendasi preskriptif.

Seluruh proses akan didokumentasikan secara bertahap agar repository ini dapat menjadi rekam jejak pengerjaan sekaligus portofolio proyek analisis data kelompok.

---

**Kelompok 11 | Lab Sains Data**  
Program Studi Bisnis Digital  
Fakultas Ekonomika dan Bisnis  
Universitas Diponegoro  
2026
