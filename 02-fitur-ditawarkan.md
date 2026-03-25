# Fitur yang Ditawarkan

Dokumen ini merangkum kemampuan utama sistem per area bisnis.

## 1. Website Publik (Marketing)

- Beranda dengan konten dinamis dari CMS.
- Katalog produk dengan filter kategori dan pencarian.
- Detail produk dengan informasi deskripsi, gambar, dan kategori.
- Halaman tentang perusahaan dan profil sekutu aktif.
- Halaman kontak dengan form inquiry.
- Perlindungan form: validasi, honeypot anti-spam, rate limit.

## 2. CMS Konten Website

- Edit konten website langsung dari admin.
- Tipe konten fleksibel: text, textarea, richtext, image.
- Pengelompokan konten per grup (beranda, tentang, kontak).

## 3. Master Data

- Produk, kategori, gudang.
- Customer.
- Supplier.
- Sekutu.
- Site content.

## 4. Manajemen Stok

- Stok per produk per gudang.
- Riwayat pergerakan stok (masuk, keluar, adjustment, transfer).
- Alert stok kritis otomatis.
- Stok masuk cepat dari modul gudang.

## 5. Penjualan End-to-End

- Quotation dengan item, diskon, dan PPN.
- Konversi quotation ke sales order.
- Sales order dengan progres status operasional.
- Pembuatan invoice dari sales order.
- Pencatatan pembayaran parsial atau lunas.
- Aksi cepat lunasi invoice.

## 6. Procurement dan Purchase Order

- Procurement request dengan approval dan penerimaan barang.
- Purchase order ke supplier dengan approval dan receive.
- Otomatis menambah stok saat barang diterima.

## 7. Keuangan dan Laporan

- Pencatatan pengeluaran.
- Ringkasan penjualan periode.
- Ringkasan laba rugi periode.
- Distribusi laba sekutu berbasis persentase.
- Halaman Financial Report Center.
- Export PDF pada dokumen dan laporan.

## 8. Integrasi Dokumen dan Komunikasi

- Upload lampiran untuk quotation, sales order, invoice, purchase order.
- Quick action kirim WhatsApp dari transaksi utama.
- Generate PDF invoice/quotation/laporan.

## 9. API Internal

- Endpoint produk, customer, invoice, dashboard, dan report.
- Dilindungi Sanctum.
- Cocok untuk integrasi frontend eksternal atau aplikasi mobile internal.

## 10. Keamanan dan Governance

- Role-based access control dengan Spatie Permission.
- Policy authorization pada model penting.
- Audit activity log.
- Proteksi form inquiry terhadap spam dan input berbahaya.
