# 📖 Buku Panduan Sistem (User Manual)
**Sistem Informasi & Manajemen Operasional CV Alat Pabrik Berat**

Selamat datang di Panduan Penggunaan Sistem. Dokumen ini dibuat khusus untuk memandu staf, admin, kasir, maupun manajer dalam menggunakan sistem ini sehari-hari. Sistem ini merangkum seluruh operasional CV mulai dari pencatatan ketersediaan barang, penjualan ke pelanggan, hingga memantau keuntungan finansial.

---

## 📑 Daftar Isi Modul Pembelajaran

Berikut adalah modul proses bisnis utama beserta tata cara pengerjaannya. Silakan klik tautan di bawah ini untuk melihat *Flowchart* (Diagram Alur) visual dari masing-masing proses:

1. **[Alur Penjualan (Sales) & Kas Masuk](flowchart/1-Alur-Penjualan.md)**
   Pelajari bagaimana melayani pelanggan mulai dari menjawab *Inquiry*, memberikan Penawaran Harga (*Quotation*), menerbitkan *Sales Order*, hingga menagih pembayaran (*Invoice*) dan mengirim barang dari Gudang.

2. **[Alur Pembelian (Purchasing) & Kas Keluar](flowchart/2-Alur-Pembelian-Stok.md)**
   Pelajari prosedur yang tepat ketika stok di Gudang habis. Mulai dari mengajukan permohonan pengadaan (*Procurement*), meresmikan ke Supplier (*Purchase Order*), hingga mencatat tagihan/Hutang Supplier.

3. **[Alur Laporan Keuangan & Bagi Hasil](flowchart/3-Alur-Keuangan-Bagi-Hasil.md)**
   Pelajari cara membaca kondisi kesehatan perusahaan di *Financial Report Center*. Modul ini juga akan menjelaskan bagaimana keuntungan bulanan dibagi kepada para pemodal/sekutu.

---

## 💡 Konsep Dasar yang Wajib Dipahami

Sebelum masuk ke detail, ada beberapa "aturan main" (*business logic*) yang tertanam kuat di sistem ini:

### A. Konsep Stok Barang (Inventory)
- **Barang tidak bisa dijual jika stok tidak mencukupi**. Sistem akan memblokir pembuatan *Invoice* jika *Quantity* melebihi stok yang ada di gudang yang dipilih.
- **Setiap Pergerakan Dilacak**. Menambah stok lewat PO, atau mengurangi stok karena penjualan, semuanya akan otomatis masuk ke tabel **Riwayat Stok (Stock Movement)**. Anda bisa mengecek di halaman detail produk, lalu tab "Mutasi Stok".

### B. Konsep Hak Akses (Roles & Permissions)
- Sistem memiliki manajemen akses yang ketat. Tidak semua menu bisa dilihat oleh sembarang staf.
- **Admin Gudang** biasanya hanya bisa melihat *Procurement* dan *Purchase Order*.
- **Admin Sales** hanya bisa mengelola *Quotation* dan *Sales Order*.
- **Manajer / Owner** bisa melihat laporan laba rugi dan menyetujui dokumen penting.

### C. Pentingnya Status Dokumen
Setiap dokumen transaksi memiliki **Status**. Perhatikan perpindahan status ini:
- `Draft`: Masih bisa diedit bebas, belum memiliki efek hukum/finansial di sistem.
- `Approved`: Sudah disahkan atasan, tidak bisa diedit sembarangan lagi.
- `Lunas` / `Received`: Transaksi sudah final, stok sudah berpindah, dan uang sudah berpindah.

---
*Siap untuk belajar? Silakan mulai dengan membuka modul **Alur Penjualan** pada daftar isi di atas.*
