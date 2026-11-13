# Laporan UTS Web Software Tools

**Nama:*Elton Tri Hartoni Sanjaya*
**Nomor Induk Mahasiswa:_12522015_
**Kelas:*TI-B*
**Tanggal:_13-11-2026_

## A. Bukti pemeriksaan masalah

| Masalah          | Alat yang digunakan | Bukti pemeriksaan | Perkiraan penyebab | Perbaikan | Hasil setelah perbaikan |
| ---------------- | ------------------- | ----------------- | ------------------ | --------- | ----------------------- |
| Produk           |                     |                   |                    |           |                         |
| Tombol keranjang |                     |                   |                    |           |                         |
| Total belanja    |                     |                   |                    |           |                         |

## B. Hasil pengujian

- Jumlah pengujian sebelum perbaikan:
- Jumlah pengujian berhasil setelah perbaikan:
- Catatan perubahan pada fungsi yang diperiksa:

## C. Kualitas kode

- Temuan sebelum perbaikan:
- Perbaikan yang dilakukan:
- Hasil pemeriksaan ulang:

## D. Git

- Branch (jika membuat):
- Ringkasan commit:
- Hasil pemeriksaan `git status`:

## E. Pemakaian kecerdasan buatan (jika digunakan)

- Nama alat:
- Pertanyaan/instruksi yang diberikan:
- Bagian jawaban yang diterapkan:
- Cara memeriksa apakah saran tersebut benar:

## F. Refleksi singkat

- Satu pelajaran paling penting dari ujian ini:

A. Bukti pemeriksaan masalah

1. Masalah Daftar Produk

Alat yang digunakan: Browser Console, Network

Bukti pemeriksaan: Permintaan ke /api/barang mengembalikan status 404 Not Found.

Perkiraan penyebab: Ketidaksesuaian endpoint antara klien (/api/barang) dan server (/api/products).

Perbaikan: Mengubah URL fetch pada app.js dari /api/barang menjadi /api/products.

Hasil setelah perbaikan: Produk berhasil dimuat dan tampil di halaman toko.

2. Masalah Tombol Keranjang

Alat yang digunakan: Browser Elements, Console

Bukti pemeriksaan: Klik pada tombol tidak memicu fungsi penambahan karena elemen tidak merespons.

Perkiraan penyebab: Selektor kelas di event listener (.add-to-cart) tidak cocok dengan kelas tombol HTML (.add-button).

Perbaikan: Memperbarui selektor pada app.js dari .add-to-cart menjadi .add-button.

Hasil setelah perbaikan: Tombol keranjang berfungsi normal dan produk masuk ke keranjang saat diklik.

3. Masalah Total Belanja

Alat yang digunakan: Code Review, Unit Testing

Bukti pemeriksaan: Perhitungan total harga salah karena nilai kuantitas tidak dikalikan, serta ada typo syntax pada perenderan baris keranjang.

Perkiraan penyebab: Fungsi calculateTotal hanya menjumlahkan harga satuan tanpa mengalikan kuantitas, dan ada operator perkalian yang hilang di app.js.

Perbaikan: Memperbarui rumus item.price \* item.quantity pada src/cart.js dan memperbaiki syntax di app.js.

Hasil setelah perbaikan: Total belanja dihitung secara akurat sesuai jumlah barang yang dibeli.

B. Hasil pengujian

Jumlah pengujian sebelum perbaikan: Gagal / Beberapa tes gagal akibat error logika dan endpoint.

Jumlah pengujian berhasil setelah perbaikan: 7 dari 7 pengujian berhasil (100% passed).

Catatan perubahan pada fungsi yang diperiksa: Memperbaiki endpoint fetch produk, mencocokkan event listener tombol keranjang, serta menyempurnakan kalkulasi reduce total harga dengan kuantitas item.

C. Kualitas kode

Temuan sebelum perbaikan: Terdapat error linting/format dan kesalahan logika pada fungsi kalkulasi keranjang serta ketidakcocokan endpoint.

Perbaikan yang dilakukan: Menyesuaikan penulisan kode sesuai standar Biome, memperbaiki syntax error pada template string, dan merapikan struktur fungsi.

Hasil pemeriksaan ulang: Perintah npm run lint dan npm run format:check bersih tanpa error.

D. Git

Branch (jika membuat): main (default)

Ringkasan commit:

chore: initial exam (commit awal kondisi ujian)

Hasil pemeriksaan git status: Berkas sudah di-commit dan working tree bersih.

E. Pemakaian kecerdasan buatan (jika digunakan)

Nama alat: Gemini (Google)

Pertanyaan/instruksi yang diberikan: Meminta analisis permasalahan pada berkas app.js, server.mjs, dan src/cart.js, serta panduan mengatasi kendala Git.

Bagian jawaban yang diterapkan: Penyesuaian endpoint API produk, perbaikan selektor tombol keranjang, perbaikan logika perkalian kuantitas pada fungsi total keranjang, dan panduan perintah Git.

Cara memeriksa apakah saran tersebut benar: Menjalankan aplikasi di browser, mengecek interaksi keranjang, menjalankan pengujian otomatis (npm run test:once), dan memastikan seluruh tes lulus.

F. Refleksi singkat

Satu pelajaran paling penting dari ujian ini: Pentingnya memeriksa bukti nyata dari Browser DevTools dan pengujian otomatis sebelum melakukan modifikasi, serta memastikan keselarasan antara endpoint server dan permintaan sisi klien.
