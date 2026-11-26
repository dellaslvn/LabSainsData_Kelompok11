# HARNESS – Instruksi Kerja AI untuk Proyek Kelompok 11

## 1. Tujuan proyek
Membantu penjual online menentukan aspek perbaikan yang perlu diprioritaskan berdasarkan ulasan pelanggan, dengan fokus awal pada ulasan produk perangkat handphone.

## 2. Keputusan bisnis yang didukung
Tentukan apakah penjual perlu memprioritaskan:
1. kualitas produk;
2. pengemasan/pengiriman; atau
3. pelayanan penjual.

Keputusan harus didukung oleh ringkasan frekuensi keluhan, rating, dan urgensi yang sudah diverifikasi manusia.

## 3. Empat pertanyaan analitik
- Deskriptif: kategori keluhan apa yang muncul dan seberapa sering?
- Diagnostik: pola apa yang tampak antara kategori keluhan dan rating pelanggan?
- Prediktif: apakah kategori keluhan pada ulasan baru dapat diperkirakan dari teks setelah tersedia data berlabel terverifikasi?
- Preskriptif: aspek perbaikan mana yang patut diprioritaskan berdasarkan frekuensi, rating, dan urgensi?

## 4. Sumber dan batas data
- Dataset utama: Tokopedia Product Reviews 2019, lihat `DATA-SOURCES.md` dan `DATA-CARD.md`.
- Jangan menggabungkan dataset pembanding tanpa persetujuan tim dan pemeriksaan skema.
- Jangan mengarang data, label, jumlah sampel, hasil pengujian, atau sumber.
- Data 2019 tidak boleh disebut sebagai gambaran kondisi marketplace saat ini.
- Rating tidak otomatis sama dengan sentimen atau kategori keluhan.

## 5. Aturan privasi dan keamanan
- Jangan memasukkan nama, nomor telepon, alamat, email, token, API key, password, atau informasi pribadi ke repository.
- Jangan mengunggah kredensial ke file, notebook, screenshot, atau log.
- Jangan melakukan scraping massal atau mengakses data di luar izin dan ketentuan sumber.
- Jika menemukan data pribadi, hentikan pemrosesan bagian tersebut dan laporkan kepada anggota tim.

## 6. Aturan penggunaan AI
- AI boleh membantu membuat kode, merangkum struktur data, menyarankan label awal, dan memeriksa konsistensi.
- AI tidak boleh menetapkan label final tanpa pemeriksaan manusia.
- Semua saran AI harus ditandai sebagai saran/draf sampai diperiksa.
- Catat prompt/tugas, hasil yang digunakan, perubahan manual, tanggal, dan pemeriksa di `LOG-AI.md`.
- Jangan menuliskan bahwa AI menjalankan proses atau menghasilkan angka tertentu jika proses tersebut belum benar-benar dilakukan.

## 7. Aturan analisis
- Pisahkan data mentah, data hasil pembersihan, sampel anotasi, dan data final.
- Simpan langkah transformasi agar dapat diulang.
- Catat jumlah baris sebelum dan sesudah filter/deduplikasi.
- Buat definisi operasional untuk setiap kategori label.
- Jika satu ulasan berisi lebih dari satu keluhan, tandai multi-aspek dan catat aspeknya.
- Jika isi ulasan tidak cukup jelas, gunakan label ambigu/tidak dapat ditentukan; jangan menebak.
- Evaluasi kesepakatan antar-anotator sebelum label digunakan untuk pemodelan.
- Untuk model prediktif, pisahkan data latih dan uji serta laporkan metrik yang relevan. Jangan menyatakan model akurat tanpa evaluasi.

## 8. Struktur folder yang disarankan
```text
data/raw/          # data sumber asli, tidak diedit
data/processed/    # data setelah pembersihan/filter
data/sample/       # sampel untuk anotasi
docs/              # data card, sumber, keputusan, pedoman anotasi
notebooks/         # analisis yang dapat diulang
```

## 9. Pemeriksaan sebelum commit
- [ ] Tidak ada data pribadi atau kredensial.
- [ ] Nama file dan folder jelas.
- [ ] Dataset mentah tidak tertimpa.
- [ ] Perubahan data dan kode dapat dijelaskan.
- [ ] Sumber dan lisensi dicantumkan.
- [ ] Hasil AI yang belum diperiksa diberi penanda.
- [ ] `LOG-AI.md` diperbarui.
- [ ] README mencerminkan status sebenarnya.

## 10. Prinsip pelaporan
Laporkan hanya hal yang sudah dikerjakan. Bedakan dengan tegas antara:
- selesai dan sudah diperiksa;
- disiapkan tetapi belum diverifikasi;
- rencana untuk tahap berikutnya.
