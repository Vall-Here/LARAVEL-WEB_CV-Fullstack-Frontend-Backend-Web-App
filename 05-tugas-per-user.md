# Tugas Per User

Dokumen ini menjabarkan tanggung jawab inti per role agar operasional tim terstandar.

## 1. Matriks Tanggung Jawab

| Area Tugas | super_admin | owner | admin | kasir | gudang |
|---|---|---|---|---|---|
| Setup user dan role | Utama | Monitoring | - | - | - |
| Kelola master produk/kategori | Utama | Approve kebijakan | Eksekusi | - | Input data pendukung |
| Kelola warehouse dan stok | Monitoring | Monitoring | Koordinasi | - | Utama |
| Proses inquiry website | Monitoring | Monitoring | Utama | Bantuan follow-up | - |
| Quotation dan sales order | Monitoring | Monitoring | Utama | Bantuan administrasi | Koordinasi stok |
| Invoice dan pembayaran | Monitoring | Monitoring KPI | Koordinasi | Utama | - |
| Expense dan laporan keuangan | Monitoring | Utama review | Input operasional | Input terkait kas | - |
| Procurement dan purchase order | Monitoring | Approve kebijakan | Utama proses | - | Utama penerimaan |
| CMS website | Monitoring | Approve konten | Utama | - | - |
| Audit log dan compliance | Utama | Review | Support data | Support data | Support data |

## 2. Detail Tugas per Role

## super_admin

- Menetapkan role dan permission.
- Menjamin konfigurasi sistem berjalan (queue, scheduler, storage, env).
- Mengawasi konsistensi data lintas modul.
- Menangani insiden akses, bug kritikal, dan audit trail.

## owner

- Meninjau performa penjualan dan laba rugi.
- Menentukan keputusan bisnis strategis (harga, procurement besar, prioritas produk).
- Meninjau piutang dan status invoice jatuh tempo.
- Menyetujui arah konten website dan positioning bisnis.

## admin

- Mengelola alur inquiry -> quotation -> sales order -> invoice.
- Mengelola data customer, produk, supplier, procurement, dan dokumen pendukung.
- Menjaga kualitas data transaksi dan status dokumen.
- Menangani update konten website via CMS.

## kasir

- Mencatat pembayaran invoice dengan bukti dan metode yang benar.
- Menjaga akurasi saldo pembayaran dan status invoice.
- Memantau invoice belum lunas dan overdue untuk follow-up.
- Menyediakan data transaksi kas untuk kebutuhan laporan.

## gudang

- Menjaga akurasi stok per gudang.
- Melakukan pencatatan stok masuk/keluar/adjustment sesuai bukti.
- Menangani penerimaan barang dari procurement/purchase order approved.
- Berkoordinasi dengan admin saat proses order selesai.

## 3. SOP Singkat Harian

## Pembukaan Hari

1. Cek dashboard alert.
2. Cek task prioritas per role.
3. Validasi data transaksi belum selesai.

## Penutupan Hari

1. Pastikan seluruh pembayaran hari itu sudah tercatat.
2. Pastikan stok mutasi hari itu sudah sinkron.
3. Pastikan status dokumen utama sudah diperbarui.
4. Simpan bukti dokumen/lampiran yang belum lengkap.
