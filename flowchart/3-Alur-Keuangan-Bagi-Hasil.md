# Modul 3: Alur Laporan Keuangan & Bagi Hasil

Modul ini adalah pusat muara dari seluruh transaksi yang terjadi di Modul Penjualan dan Modul Pembelian. Di sini, Manajer dan Pemodal (Sekutu) bisa memantau dengan tepat kemana perginya uang dan seberapa besar keuntungan CV.

## 📊 Flowchart Laporan & Bagi Hasil (Profit Distribution)

```mermaid
graph TD
    INV_LUNAS["Uang Masuk\nInvoice Pelanggan Lunas"] --> PNL
    PO_LUNAS["Uang Keluar\nPembelian Barang / PO"] --> ARUS_KAS
    EXP["Uang Keluar\nPengeluaran Operasional / Expense"] --> PNL
    EXP --> ARUS_KAS

    PNL(("Laporan Laba Rugi\nAccrual Basis"))
    ARUS_KAS(("Laporan Arus Kas\nCash Basis"))

    PNL --> LABA_BERSIH{"Ada\nLaba Bersih?"}

    LABA_BERSIH -->|Rugi| STOP([Tahan Bagi Hasil])

    LABA_BERSIH -->|Laba| PROFIT_DIST["1. Profit Distribution\nBagi Hasil Dibuat"]

    PROFIT_DIST --> SEKUTU_1["2. Porsi\nPemodal A (40%)"]
    PROFIT_DIST --> SEKUTU_2["2. Porsi\nPemodal B (60%)"]

    SEKUTU_1 --> DIVIDEN["3. Pencatatan Dividen"]
    SEKUTU_2 --> DIVIDEN

    DIVIDEN --> END(("Selesai"))

    style PNL fill:#f9f,stroke:#333,stroke-width:2px
    style ARUS_KAS fill:#f9f,stroke:#333,stroke-width:2px
    style PROFIT_DIST fill:#bbf,stroke:#333,stroke-width:2px
    style DIVIDEN fill:#bfb,stroke:#333,stroke-width:2px
```

## 📝 Panduan Penggunaan Langkah-demi-Langkah (Step-by-Step)

### Tahap 1: Pencatatan Pengeluaran Operasional Tambahan (Expense)

**Kapan digunakan:** Selain berbelanja barang (yang sudah tercatat otomatis lewat Purchase Order), perusahaan pasti memiliki biaya harian seperti Listrik, Gaji Karyawan, Transport Sales, Kopi, Pajak, dll. Anda harus mencatatnya secara manual di sini.

1. Buka _Sidebar_ kiri, klik menu **Keuangan > Pengeluaran**.
2. Klik tombol **+ New Expense**.
3. **Isi Formulir:**
   - **Kategori:** Pilih jenis pengeluaran (misal: Operasional, Gaji, Utilitas).
   - **Tanggal:** Pilih tanggal pengeluaran terjadi.
   - **Jumlah:** Masukkan nominal uang yang keluar (misal: Rp5.000.000).
   - **Deskripsi:** Tulis rinciannya, contoh: "Gaji 2 staff gudang bulan Juli".
   - **Bukti Struk:** Anda bisa mengambil foto struk / nota pembayaran dan meng-uploadnya (opsional).
4. Klik **Create** (Simpan). Uang kas perusahaan akan otomatis berkurang senilai jumlah yang Anda masukkan.

### Tahap 2: Membaca Laporan Keuangan

**Kapan digunakan:** Manajer atau Owner ingin memonitor apakah perusahaan sedang profit atau tidak.

1. Buka menu **Keuangan > Financial Report Center**.
2. Di atas halaman, terdapat rentang _Filter Tanggal_. Pilih rentang yang ingin Anda lihat (Misal: 1 Juli - 31 Juli), lalu klik tombol **Terapkan Filter**.
3. **Cara Membaca Dasbor:**
   - **Tabel P&L (Laba Rugi - Kiri Kaca):** Menunjukkan profitabilitas murni. Diambil dari total nominal Penjualan yang sudah jadi Sales Order, dikurangi HPP (Modal Barang), dikurangi Total Expense. Hasil akhirnya adalah **Laba Bersih**.
   - **Tabel Arus Kas (Kanan Kaca):** Menunjukkan uang _cash/tunai_ nyata. Diambil dari uang yang benar-benar ditransfer pelanggan (Payment Invoice Lunas), dikurangi uang yang dibayarkan untuk Supplier (PO) dan Expense.
   - **Tabel Piutang & Hutang (Bawah):** Memantau "Siapa pelanggan yang ngutang ke CV kita?" (Piutang) dan "CV kita ngutang ke Supplier mana saja?" (Hutang).
4. Di bagian form filter, ada juga tombol **Export PDF**. Klik tombol tersebut untuk mengunduh laporan berformat cantik yang siap diprint dan dibawa saat rapat pemegang saham/sekutu.

### Tahap 3: Master Data Sekutu / Pemodal

**Kapan digunakan:** Anda memiliki pemodal baru atau ingin mengubah susunan saham CV.

1. Buka menu **Master Data > Sekutu**.
2. Klik **+ New Sekutu**.
3. Masukkan **Nama**, **Alamat**, **No Telepon**, dan **Persentase Kepemilikan (Porsi Saham)**.
4. Total persentase seluruh sekutu diusahakan harus 100% (Misal: Pak Budi 40%, Pak Andi 60%).

### Tahap 4: Membagikan Laba (Profit Distribution)

**Kapan digunakan:** Biasanya dilakukan di akhir tahun, atau saat uang kas surplus dan Owner setuju untuk membagikan deviden kepada para Sekutu.

1. Buka Dasbor _Financial Report Center_, lihat berapakah angka **Laba Bersih** Anda di periode ini. Misal Laba Bersih = Rp100.000.000.
2. Buka menu **Keuangan > Profit Distributions**.
3. Klik **+ New Profit Distribution**.
4. **Isi Formulir:**
   - **Bulan & Tahun:** Pilih periode pembukuan yang sedang akan dibagi hasilkan.
   - **Total Laba:** Masukkan nominal Rp100.000.000 (sesuai yang disepakati manajer).
5. Klik **Create**.
6. **EFEK SISTEM:**
   - Anda tidak perlu memecah uang satu per satu! Sistem akan otomatis memecah 100 Juta tersebut menjadi Rp40jt untuk Pak Budi dan Rp60jt untuk Pak Andi.
   - Anda bisa mengklik dokumen _Profit Distribution_ tersebut untuk melihat rincian jatah uang masing-masing pemodal.
   - Gunakan dokumen tersebut sebagai landasan untuk mentransfer uang ke rekening masing-masing sekutu secara manual via m-Banking.

## ⚠️ Edge Cases (Kasus Khusus / Masalah Umum)

- **Kasus 1: Mengapa angka Laba Bersih saya miliaran (Positif), tapi angka Arus Kas saya minus?**
  - **Penjelasan:** Ini fenomena sangat wajar di bisnis B2B (Alat Pabrik Berat). Artinya Anda punya banyak Sales Order (Transaksi jalan terus, Laba Kertas tinggi), NAMUN para pelanggan tersebut belum mentransfer pembayarannya alias Invoicenya pada masih ngutang (_Piutang membengkak_). Sementara itu, Anda sudah mengeluarkan banyak uang kas tunai ke Supplier untuk kulakan barang (_PO Lunas_).
  - **Solusi:** Buka _Financial Report Center_, gulir ke bawah ke tabel **Piutang Pelanggan**. Segera hubungi dan tagih pelanggan-pelanggan tersebut agar mentransfer uangnya ke CV, sehingga Arus Kas Anda kembali Positif!
- **Kasus 2: Total Bagi Hasil ternyata salah ketik nominalnya.**
  - **Solusi:** Selama dokumen _Profit Distribution_ belum disahkan/dicetak untuk dibagikan secara final, Anda masih dapat membatalkan dan mengedit/menghapusnya dari menu, lalu membuat dokumen baru yang nominalnya benar.

---

**[⬅️ Kembali ke Alur Pembelian](2-Alur-Pembelian-Stok.md)** | **[🏠 Kembali ke Daftar Isi Utama](../Buku-Panduan-Sistem.md)**
