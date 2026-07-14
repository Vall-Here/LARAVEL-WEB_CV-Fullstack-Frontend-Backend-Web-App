# Modul 4: Alur Manajemen Dokumen (Document Management System - DMS)

Modul Document Management System (DMS) berfungsi sebagai brankas digital (arsip terpusat) bagi seluruh dokumen legal dan operasional CV. Di sini Anda bisa menyimpan, mengatur versi, dan mengatur hak akses dokumen-dokumen penting seperti Akta Pendirian, NPWP, Surat Izin Usaha, hingga Kontrak Kerja.

## 💡 Konsep Dasar yang Wajib Dipahami

1. **Struktur Folder (Direktori)**
   DMS tidak sekadar menumpuk file. Anda wajib membuat struktur folder (Direktori) terlebih dahulu, mirip seperti struktur di Windows Explorer atau Google Drive. Contoh direktori: `Legalitas`, `Keuangan`, `Kontrak Sales`.
2. **Pengendalian Versi (Versioning)**
   Dokumen legal seringkali mengalami pembaruan (misal: perpanjangan SIUP tiap tahun). DMS mendukung fitur *Version Control*. Anda tidak perlu menghapus file SIUP yang lama; cukup upload versi barunya di atas dokumen yang sama. Sistem akan menyimpan kedua versinya, namun versi terbaru-lah yang akan disajikan secara default.
3. **Keamanan & Hak Akses (Permissions)**
   Dokumen tertentu bersifat rahasia (contoh: Laporan Audit Eksternal) dan tidak boleh dilihat oleh staf Gudang. DMS memungkinkan Anda untuk mengatur *Hak Akses* pada setiap dokumen: siapa role yang boleh mengunduhnya, dan siapa role yang tidak boleh.

---

## 🎬 Contoh Kasus Penggunaan (Skenario Dunia Nyata)

Mari kita bayangkan skenario ketika HRD ingin mengarsipkan perpanjangan Kontrak Sewa Ruko:

- **Bulan Lalu:** HRD telah membuat direktori `Legal & Aset` dan mengunggah dokumen "Kontrak Sewa Ruko 2024.pdf". 
- **Bulan Ini (Perpanjangan):** Masa sewa ruko diperpanjang, dan CV menerima "Kontrak Sewa Ruko 2025.pdf" yang baru.
- **Tindakan Admin:** Alih-alih membuat entri dokumen baru dan membuat daftar berantakan, HRD membuka data "Kontrak Sewa Ruko" yang sudah ada, lalu mengklik tab **Version History**. Di sana, ia mengklik *Upload New Version*, lalu mengunggah file PDF versi 2025 dengan catatan "Perpanjangan tahun kedua".
- **Efek Sistem:** File lama (2024) otomatis diarsipkan, dan ketika orang lain mendownload "Kontrak Sewa Ruko" keesokan harinya, mereka otomatis mendapatkan file versi 2025 (terbaru).

---

## 📝 Panduan Penggunaan Langkah-demi-Langkah (Step-by-Step)

### Tahap 1: Membuat Folder (Direktori Dokumen)
1. Buka *Sidebar* kiri, klik menu **DMS > Direktori Dokumen**.
2. Klik tombol **+ New Document Directory**.
3. Isi nama folder (misal: "Dokumen Legal Perusahaan") dan deskripsinya.
4. Klik **Create**.

### Tahap 2: Mengunggah Dokumen Baru
1. Buka menu **DMS > Dokumen Terpusat**.
2. Klik tombol **+ New Document**.
3. **Isi Formulir:**
   - **Judul Dokumen:** Beri nama yang jelas (misal: "NPWP Perusahaan").
   - **Nomor Registrasi/Dokumen:** Isi jika ada (misal: "02.xxx.xxx.x-xxx.000").
   - **Direktori:** Pilih folder yang baru Anda buat di Tahap 1.
   - **File & Tipe:** Upload file PDF/Gambar, lalu tentukan tipe mime-nya.
   - **Tanggal Kadaluarsa:** Jika dokumen punya masa berlaku (seperti SIUP), masukkan tanggal matinya. Sistem bisa memantau dokumen mana yang hampir expired.
4. Klik **Create** (Simpan).

### Tahap 3: Mengelola Versi Baru (Version Control)
1. Buka detail salah satu dokumen di menu **DMS > Dokumen Terpusat**.
2. Di bagian bawah layar, terdapat tab bernama **Version History**.
3. Klik tombol **Upload New Version**.
4. Unggah file dokumen terbarunya, isikan kolom *Catatan Versi* (misal: "Revisi pasal 3"), lalu klik Submit.
5. Versi baru akan tertumpuk di atas dan ditandai sebagai versi aktif (terbaru).

### Tahap 4: Mengatur Hak Akses Spesifik
Jika Anda tidak ingin dokumen tertentu dibaca oleh sembarang pegawai:
1. Buka menu **User Management > Roles**.
2. Edit role yang ingin dibatasi (misal: `Kasir`).
3. Cari *permissions* yang berkaitan dengan DMS (contoh: `view_any_document` atau `download_document`) dan pastikan checkbox-nya tidak tercentang untuk role tersebut.
4. Untuk batasan per-dokumen secara individual, akan dikembangkan melalui kebijakan folder di masa mendatang, saat ini hak akses diatur melalui *Role Permissions*.

---
**[🏠 Kembali ke Daftar Isi Utama](../Buku-Panduan-Sistem.md)**
