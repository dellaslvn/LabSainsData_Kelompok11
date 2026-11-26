# Data Card: Tokopedia Product Reviews 2019

## Identitas
- Nama dataset: Tokopedia Product Reviews 2019
- Nama file kerja: `tokopedia-product-reviews-2019.csv`
- Sumber: https://huggingface.co/datasets/farhamu/tokopedia-product-reviews-2019
- Pengunggah/pengelola dataset card: farhamu
- Tahun data yang dinyatakan: 2019
- Jumlah baris pada dataset card: 40.607 ulasan
- Format: CSV
- Lisensi yang tercantum: Apache-2.0
- Bahasa: terutama Bahasa Indonesia

## Variabel
| Kolom | Keterangan | Penggunaan dalam proyek |
|---|---|---|
| `text` | Teks ulasan pelanggan | Bahan identifikasi aspek/keluhan |
| `rating` | Rating 1–5 | Pembanding penilaian pelanggan |
| `category` | Kategori produk | Penyaringan kategori produk |
| `product_name` | Nama produk | Pemeriksaan relevansi unit analisis |
| `product_id` | Identitas produk | Pengelompokan/deduplikasi dalam produk |
| `sold` | Informasi jumlah terjual | Tidak digunakan sebelum tipe dan nilai diperiksa |
| `shop_id` | Identitas toko | Metadata; bukan identitas pribadi pembeli |
| `product_url` | Tautan halaman produk | Metadata sumber; tidak perlu dipublikasikan ulang bila tidak dibutuhkan |

## Unit analisis dan batas proyek
Unit analisis yang direncanakan adalah satu ulasan pelanggan untuk produk perangkat handphone. Baris dalam kategori `handphone` perlu disaring berdasarkan nama produk agar aksesori/komponen tidak otomatis masuk sebagai perangkat handphone.

## Variabel hasil anotasi
Kategori keluhan:
- `kualitas_produk`
- `pengemasan_pengiriman`
- `pelayanan_penjual`
- `multi_aspek`
- `tidak_ada_keluhan_teridentifikasi`
- `netral_atau_ambigu`
- `keluhan_aspek_belum_jelas`

Sentimen teks:
- `positif`
- `negatif`
- `netral_atau_ambigu`
- `campuran`

Urgensi:
- `rendah`
- `sedang`
- `tinggi`
- `belum_dapat_ditentukan`

Kategori di atas merupakan rancangan kerja. Definisi operasional dan contoh anotasi harus disepakati tim sebelum label final dibuat.

## Risiko bias dan keterbatasan
1. Data bersifat historis dan hanya menggambarkan ulasan pada periode sumber.
2. Ulasan yang tersedia tidak selalu mewakili seluruh pelanggan.
3. Rating bintang dapat berbeda dari sentimen yang dinyatakan dalam teks.
4. Ulasan singkat atau ambigu dapat menyulitkan klasifikasi.
5. Pemilihan satu kategori produk dan penyaringan nama produk dapat menimbulkan bias seleksi.
6. Label otomatis berbasis kata kunci bukan label kebenaran (ground truth).

## Privasi dan etika
- Jangan mencoba mengidentifikasi pembeli atau pemilik akun.
- Jangan menambahkan data pribadi ke repository.
- Batasi penggunaan metadata pada kebutuhan analisis.
- Pertahankan atribusi dan ikuti lisensi Apache-2.0.
- Periksa kembali apakah file yang akan dipublikasikan memang boleh didistribusikan sesuai lisensi dan ketentuan platform.

## Status pemeriksaan
Dataset utama tersedia di lingkungan kerja dan telah diperiksa secara awal. Angka statistik dan hasil filter pada laporan kerja harus tetap diselaraskan dengan versi file yang benar-benar digunakan. Setiap perubahan data harus dicatat.
