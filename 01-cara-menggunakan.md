# Cara Menggunakan Sistem

Dokumen ini menjelaskan langkah dari instalasi sampai penggunaan harian aplikasi.

## 1. Persiapan Awal

## Kebutuhan Minimum

- PHP 8.2+
- Composer 2+
- Node.js 18+
- MySQL 8+

## Setup Cepat

```bash
composer setup
php artisan db:seed
php artisan storage:link
composer dev
```

Aplikasi akan berjalan di URL lokal default:

- Website publik: http://localhost:8000
- Dashboard admin: http://localhost:8000/admin

## Akun Default Login

Semua akun menggunakan password: password

- superadmin@cvniki.test
- owner@cvniki.test
- admin@cvniki.test
- kasir@cvniki.test
- gudang@cvniki.test

## 2. Cara Menggunakan Website Publik

## Halaman Utama

1. Buka beranda.
2. Lihat produk unggulan dan kategori.
3. Klik produk untuk melihat detail.

## Halaman Produk

1. Buka halaman katalog produk.
2. Gunakan filter kategori.
3. Gunakan pencarian kata kunci nama/deskripsi.
4. Buka detail produk berdasarkan slug.

## Halaman Kontak

1. Isi form inquiry.
2. Masukkan data nama, email, pesan, dan optional telepon/perusahaan.
3. Submit form.
4. Data inquiry masuk ke dashboard admin modul Inquiry.

## 3. Cara Menggunakan Dashboard Admin

## Login

1. Akses halaman admin.
2. Login menggunakan akun sesuai role.

## Penggunaan Harian Umum

1. Cek widget dashboard (KPI, alert overdue, stok kritis).
2. Proses inquiry baru dan follow-up.
3. Kelola transaksi penjualan dari quotation sampai invoice.
4. Catat pembayaran dan monitor piutang.
5. Kelola stok masuk/keluar dan mutasi gudang.
6. Cetak/ekspor dokumen saat dibutuhkan.

## 4. Menjalankan Job Otomatis

Agar reminder berjalan, pastikan scheduler dan queue aktif:

```bash
php artisan schedule:work
php artisan queue:work
```

Task otomatis yang dijalankan sistem:

- Cek stok kritis harian.
- Cek invoice jatuh tempo harian.
- Generate laporan bulanan.

## 5. Penggunaan API Internal

Semua endpoint API memerlukan token Sanctum.

Contoh endpoint:

- GET /api/products
- GET /api/customers
- GET /api/invoices
- POST /api/invoices/{id}/pay
- GET /api/dashboard/stats
- GET /api/reports/sales

Contoh penggunaan token di header:

```text
Authorization: Bearer <TOKEN_SANCTUM>
```

## 6. Troubleshooting Singkat

## Asset frontend tidak muncul

- Jalankan npm install
- Jalankan npm run dev atau npm run build

## File upload tidak bisa dibuka

- Jalankan php artisan storage:link

## Notifikasi/job tidak jalan

- Pastikan queue worker aktif
- Pastikan scheduler aktif

## 7. Checklist Operasional Harian

- Login sesuai role.
- Cek dashboard alert.
- Proses item prioritas hari itu.
- Sinkronkan status transaksi (draft, approved, selesai, lunas).
- Verifikasi data laporan sebelum tutup hari.
