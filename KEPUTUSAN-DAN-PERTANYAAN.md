# Lembar Rencana Data: Keputusan dan Pertanyaan Analitik

## Keputusan bisnis
**Aspek apa yang perlu diprioritaskan oleh penjual online untuk diperbaiki—kualitas produk, pengemasan/pengiriman, atau pelayanan penjual—berdasarkan pola keluhan pelanggan?**

## Alternatif keputusan
- A. Memprioritaskan perbaikan kualitas produk.
- B. Memprioritaskan perbaikan pengemasan dan pengiriman.
- C. Memprioritaskan peningkatan pelayanan pelanggan.

## Empat pertanyaan analitik
| Jenis analitik | Pertanyaan | Data yang dibutuhkan | Hasil yang diharapkan |
|---|---|---|---|
| Deskriptif | Kategori keluhan apa yang paling sering muncul pada ulasan produk perangkat handphone? | Teks ulasan dan label kategori keluhan yang telah diverifikasi | Jumlah dan proporsi tiap kategori keluhan |
| Diagnostik | Bagaimana pola rating pada masing-masing kategori keluhan? | Teks ulasan, kategori keluhan final, rating | Tabel silang kategori keluhan dan rating; pola asosiasi, bukan klaim sebab-akibat |
| Prediktif | Dapatkah kategori keluhan ulasan baru diperkirakan dari teksnya? | Teks ulasan berlabel final yang cukup dan representatif | Prediksi kategori pada data uji beserta metrik evaluasi |
| Preskriptif | Aspek perbaikan mana yang sebaiknya diprioritaskan? | Frekuensi keluhan, rating, urgensi final, dan pertimbangan bisnis | Urutan prioritas perbaikan dengan alasan dan keterbatasan |

## Ambang perhatian awal
Kategori yang mencapai 30% dari keluhan dapat ditandai untuk ditinjau sebagai perhatian utama. Angka 30% adalah ambang kerja awal, bukan standar universal dan bukan aturan keputusan otomatis. Keluhan berdampak serius tetap perlu ditinjau meskipun frekuensinya lebih kecil.

## Sumber data
Dataset utama: Tokopedia Product Reviews 2019. Rincian sumber dan pembanding tersedia di `DATA-SOURCES.md`.

## Batasan interpretasi
- Jangan menyamakan rating rendah dengan satu kategori keluhan tertentu.
- Jangan menyimpulkan sebab-akibat hanya dari hubungan antara rating dan teks ulasan.
- Jangan membuat prediksi sebelum label final manusia tersedia dan model diuji.
- Rekomendasi akhir belum dapat dibuat sebelum hasil analisis tersedia.
