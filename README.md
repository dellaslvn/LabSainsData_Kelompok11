# Lab Sains Data – Kelompok 11
## Paket Dasar: Keputusan dan Sumber Data

### Fokus proyek
Proyek ini membantu penjual online menentukan aspek perbaikan yang perlu diprioritaskan berdasarkan ulasan pelanggan. Fokus awal dibatasi pada ulasan produk perangkat handphone berbahasa Indonesia dari dataset Tokopedia Product Reviews 2019.

### Keputusan bisnis
**Aspek apa yang perlu diprioritaskan oleh penjual online untuk diperbaiki—kualitas produk, pengemasan/pengiriman, atau pelayanan penjual—berdasarkan pola keluhan pelanggan?**

### Empat pertanyaan analitik
1. **Deskriptif – Apa yang terjadi?** Berapa jumlah dan proporsi ulasan yang menunjukkan keluhan kualitas produk, pengemasan/pengiriman, dan pelayanan penjual?
2. **Diagnostik – Mengapa/pola apa yang berkaitan?** Bagaimana kategori keluhan berhubungan dengan rating pelanggan, dan pola apa yang tampak pada ulasan dengan rating rendah?
3. **Prediktif – Apa yang mungkin terjadi?** Dapatkah kategori keluhan pada ulasan baru diperkirakan berdasarkan teks ulasannya setelah tersedia data berlabel yang diverifikasi manusia?
4. **Preskriptif – Apa yang sebaiknya dilakukan?** Aspek perbaikan mana yang sebaiknya diprioritaskan dengan mempertimbangkan frekuensi keluhan, rating, dan tingkat urgensi yang telah diverifikasi?

### Sumber data
Lihat [`DATA-SOURCES.md`](DATA-SOURCES.md) untuk tiga sumber yang sudah diperiksa. Dataset utama yang saat ini tersedia di folder kerja adalah `tokopedia-product-reviews-2019.csv`. Dua sumber lain merupakan pembanding/alternatif dan tidak otomatis digabungkan ke dataset utama.


### Status saat ini
| Komponen | Status |
|---|---|
| Satu keputusan bisnis | Disusun |
| Empat pertanyaan analitik | Disusun |
| Tiga sumber data diperiksa pada tingkat metadata/kesesuaian | Selesai |
| Dataset utama tersedia dan diperiksa secara awal | Selesai |
| Sampel untuk verifikasi/anotasi manual | Disiapkan; perlu validasi anggota |
| Pelabelan final manusia | Belum selesai |
| Pemodelan dan evaluasi | Belum dimulai |

### Catatan penting
- Dataset utama berasal dari tahun 2019, sehingga tidak mewakili kondisi pasar terkini.
- Rating bintang tidak boleh langsung dianggap sebagai label sentimen atau bukti kategori keluhan.
- Saran label otomatis hanya membantu penyaringan awal. Label final harus ditetapkan melalui pemeriksaan manusia.
- Jangan mengklaim hasil prediksi, hubungan sebab-akibat, atau rekomendasi final sebelum analisis dan evaluasi dilakukan.
- Simpan atribusi sumber dan patuhi lisensi dataset.
