# Pemeriksaan Sumber Data

**Tujuan:** memenuhi persyaratan minimal tiga sumber data yang diperiksa, sekaligus menentukan sumber yang paling sesuai dengan keputusan bisnis proyek.

## Ringkasan pemeriksaan

| No. | Sumber | Isi dan cakupan yang dinyatakan penerbit | Lisensi yang tercantum | Kesesuaian | Keputusan |
|---|---|---|---|---|---|
| 1 | [Tokopedia Product Reviews 2019 – Hugging Face](https://huggingface.co/datasets/farhamu/tokopedia-product-reviews-2019) | 40.607 ulasan Tokopedia; kolom utama `text`, `rating`, `category`, `product_name`, `product_id`, `sold`, `shop_id`, dan `product_url`; data dikumpulkan tahun 2019. | Apache-2.0 pada dataset card | Sangat sesuai: memuat teks ulasan berbahasa Indonesia dan rating serta metadata produk. | **Dataset utama.** File CSV tersedia di lingkungan kerja dan telah diperiksa secara awal. Gunakan subset produk perangkat handphone yang telah diseleksi, dengan verifikasi manual. |
| 2 | [PRDECT-ID – Mendeley Data](https://data.mendeley.com/datasets/574v66hf2v/1) | 5.400 ulasan produk Tokopedia dari 29 kategori; memiliki anotasi emosi (love, happiness, anger, fear, sadness) serta atribut rating dan metadata produk. | CC BY 4.0 | Sesuai untuk pembanding struktur ulasan dan referensi anotasi sentimen/emosi. Tidak identik dengan kategori dan cakupan dataset utama. | **Sumber pembanding.** Jangan digabungkan langsung dengan dataset utama; gunakan untuk membandingkan pendekatan dan memahami kemungkinan label. |
| 3 | [Dataset Costumer Review Indonesia – Mendeley Data](https://data.mendeley.com/datasets/74xrbd4vxy/1) | 203.786 ulasan berbahasa Indonesia dari platform e-commerce publik, mencakup 4.422 produk; tersedia versi raw dan processed dengan rating serta label sentimen hasil model IndoBERT. | CC BY 4.0 | Relevan untuk pembanding data ulasan e-commerce Indonesia dan evaluasi keterbatasan label otomatis. Platform dan cakupan produk perlu diperiksa lebih lanjut sebelum digunakan. | **Sumber pembanding/alternatif.** Jangan digabungkan ke dataset utama sebelum memeriksa berkas, struktur kolom, periode, dan kesesuaian unit analisis. |

## Hasil verifikasi dan batas penggunaan

### Sumber 1 – dataset utama
- Nama file yang tersedia: `tokopedia-product-reviews-2019.csv`.
- Format: CSV.
- Kolom yang tersedia: `text`, `rating`, `category`, `product_name`, `product_id`, `sold`, `shop_id`, `product_url`.
- Dataset card menyebut 40.607 baris ulasan.
- Data bersifat historis (2019); hasil analisis hanya menggambarkan data pada periode tersebut.
- Kategori `handphone` pada dataset mentah tidak otomatis berarti semua produknya adalah telepon genggam. Pemeriksaan nama produk diperlukan untuk mengeluarkan aksesori/komponen yang tidak sesuai dengan batas proyek.
- Jangan menganggap `rating` sebagai label keluhan. Kategori keluhan harus ditentukan dari isi teks dan diverifikasi manusia.

### Sumber 2 – PRDECT-ID
- Penerbit mencantumkan 5.400 ulasan Tokopedia dan 29 kategori produk.
- Memiliki label emosi yang dibuat melalui proses anotasi.
- Lisensi tercantum CC BY 4.0; atribusi wajib dipertahankan.
- Cocok sebagai bahan pembanding metode/label, bukan pengganti dataset utama.

### Sumber 3 – Dataset Costumer Review Indonesia
- Penerbit mencantumkan 203.786 ulasan dan 4.422 produk.
- Memiliki versi data mentah serta data olahan dengan label sentimen.
- Lisensi tercantum CC BY 4.0; atribusi wajib dipertahankan.
- Label sentimen pada versi olahan dihasilkan menggunakan model, sehingga bukan ground truth manusia dan tidak boleh diperlakukan sebagai label benar tanpa evaluasi.
- Perlu mengunduh dan memeriksa file serta struktur kolom sebelum memutuskan apakah dataset layak dipakai dalam analisis.

## Kesimpulan pemilihan
Dataset Tokopedia Product Reviews 2019 dipilih sebagai sumber utama karena file CSV-nya sudah tersedia dan memiliki teks ulasan, rating, kategori, serta metadata produk. PRDECT-ID dan Dataset Costumer Review Indonesia telah diperiksa pada tingkat informasi dataset dan lisensi sebagai sumber pembanding. Ketiganya **tidak digabungkan** karena perbedaan periode, platform/cakupan, skema kolom, dan metode pelabelan dapat menghasilkan bias.

## Catatan pemeriksaan
Pemeriksaan sumber 2 dan 3 pada dokumen ini merupakan pemeriksaan halaman metadata, deskripsi, cakupan, dan lisensi. Berkas mentah kedua sumber tersebut belum dinyatakan telah diunduh atau diaudit baris per baris. Pemeriksaan isi file tetap diperlukan sebelum keduanya dipakai untuk pemodelan.

## Referensi
1. Farhan, M. (2025). *Tokopedia Product Reviews 2019*. Hugging Face Datasets. https://huggingface.co/datasets/farhamu/tokopedia-product-reviews-2019
2. Sutoyo, R., Chowanda, A., Achmad, S., Andangsari, E. W., Isa, S. M., Soetandar, J. P., Andres, J. R., Richard, R., Hadiwijaya, M. A., Andrews, M. H., & Pirdaus, F. P. (2022). *Product Reviews Dataset for Emotions Classification Tasks - Indonesian (PRDECT-ID) Dataset*. Mendeley Data. https://doi.org/10.17632/574v66hf2v.1
3. Sari, A. C. (2026). *Dataset Costumer Review Indonesia*. Mendeley Data. https://doi.org/10.17632/74xrbd4vxy.1
