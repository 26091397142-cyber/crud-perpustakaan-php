# Sistem Informasi Perpustakaan (CRUD PHP Native)

Implementasi Studi Kasus 1 Mata Kuliah Basis Data untuk mengelola data buku dan transaksi peminjaman perpustakaan menggunakan arsitektur *Server-Side Rendering*.

## Teknologi yang Digunakan
* **Bahasa Pemrograman:** PHP Native (PHP 8+)
* **Database:** MySQL / MariaDB (`db_perpustakaan`) dengan ekstensi PDO
* **Frontend:** HTML5, CSS3, dan Bootstrap 5 (CDN)
* **Server Lokal:** XAMPP / Laragon

## Fitur Utama
1. **Modul Buku (CRUD):** Menampilkan daftar buku, pencarian berdasarkan judul/pengarang, menambah buku dengan validasi format ID (`Bxxx`), mengubah data buku (ID terkunci), dan menghapus buku (dilindungi *foreign key* jika memiliki riwayat peminjaman).
2. **Modul Peminjaman (CRUD + Transaksi):** Menampilkan daftar peminjaman dengan `INNER JOIN`, filter status (`dipinjam` / `kembali`), penanda otomatis keterlambatan (> 7 hari), pencatatan peminjaman baru yang otomatis mengurangi stok, serta pengembalian buku yang otomatis menambah stok.

## Cara Menjalankan Project
1. Clone atau unduh repository ini, lalu letakkan folder project di dalam direktori `htdocs` (XAMPP) atau `www` (Laragon).
2. Jalankan modul **Apache** dan **MySQL**.
3. Buka `http://localhost/phpmyadmin`, buat/impor database menggunakan file `db_perpustakaan.sql`.
4. Buka browser dan akses `http://localhost/perpus-php/`.

---

## Tampilan Hasil Pengujian (Skenario CRUD)

### 1. Buka Halaman Buku
[1 (Buka Halaman Buku)](Hasil/1%20(Buka%20Halaman%20Buku).png)
<img width="1368" height="768" alt="1 (Buka Halaman Buku)" src="https://github.com/user-attachments/assets/e52b70bf-e4d1-4a18-9baa-edbd2d5d3ab8" />

### 2. Pencarian Data
[2 (Pencarian Data)](Hasil/2%20(Pencarian%20Data).png)
<img width="1368" height="768" alt="2 (Pencarian Data)" src="https://github.com/user-attachments/assets/c56b952b-747c-41e7-b844-7a1af54f9eae" />

### 3. Tambah Buku Baru
[3 (Tambah Buku Baru)](Hasil/3%20(Tambah%20Buku%20Baru).png)
<img width="1368" height="768" alt="3 (Tambah Buku Baru)" src="https://github.com/user-attachments/assets/68b507e7-83e9-4686-a16f-ab9b098b4e99" />

### 4. Tes Error ID Duplikat
[4 (Tes Error ID Duplikat)](Hasil/4%20(Tes%20Error%20ID%20Duplikat).png)
<img width="1368" height="768" alt="4 (Tes Error ID Duplikat)" src="https://github.com/user-attachments/assets/20d20679-0c41-410f-849f-630f3832ea3c" />

### 5. Tes Error Format ID
[5 (Tes Error Format ID)](Hasil/5%20(Tes%20Error%20Format%20ID).png)
<img width="1368" height="768" alt="5 (Tes Error Format ID)" src="https://github.com/user-attachments/assets/945014a7-5ce9-403c-9d76-414f0b78a2d0" />

### 6. Edit Buku
[6 (Edit Buku)](Hasil/6%20(Edit%20Buku).png)
<img width="1368" height="768" alt="6 (Edit Buku)" src="https://github.com/user-attachments/assets/75755261-860e-49d0-a990-773bf08f9206" />

### 7. Hapus Buku yang Belum Pernah Dipinjam
[7 (Hapus Buku yang Belum Pernah Dipinjam)](Hasil/7%20(Hapus%20Buku%20yang%20Belum%20Pernah%20Dipinjam).png)
<img width="1368" height="768" alt="7 (Hapus Buku yang Belum Pernah Dipinjam)" src="https://github.com/user-attachments/assets/ba0fa749-fbb4-40c2-b22e-4f1eec995fd7" />

### 8. Tes Error Hapus Buku yang Memiliki Riwayat Pinjam
[8 (Tes Error Hapus Buku yang Memiliki Riwayat Pinjam)](Hasil/8%20(Tes%20Error%20Hapus%20Buku%20yang%20Memiliki%20Riwayat%20Pinjam).png)
<img width="1368" height="768" alt="8 (Tes Error Hapus Buku yang Memiliki Riwayat Pinjam)" src="https://github.com/user-attachments/assets/c31d992f-21d6-4dc1-a8c4-fe3ee3b0ceca" />

### 9. Buka Halaman Peminjaman
[9 (Buka Halaman Peminjaman)](Hasil/9%20(Buka%20Halaman%20Peminjaman).png)
<img width="1368" height="768" alt="9 (Buka Halaman Peminjaman)" src="https://github.com/user-attachments/assets/12a822e7-6ab7-49c4-823c-5224986498f0" />

### 10. Filter Status
[10 (Filter Status)](Hasil/10%20(Filter%20Status).png)
<img width="1368" height="768" alt="10 (Filter Status)" src="https://github.com/user-attachments/assets/d47a3290-cbdf-4c5d-8f05-e004176cf0d3" />

### 11. Catat Peminjaman Baru
[11 (Catat Peminjaman Baru)](Hasil/11%20(Catat%20Peminjaman%20Baru).png)
<img width="2728" height="768" alt="11 (Catat Peminjaman Baru)" src="https://github.com/user-attachments/assets/84fee739-b218-4a41-993b-2d4c6fc3a298" />

### 12. Pengembalian Buku
[12 (Pengembalian Buku)](Hasil/12%20(Pengembalian%20Buku).png)
<img width="2736" height="768" alt="12 (Pengembalian Buku)" src="https://github.com/user-attachments/assets/a1975419-360c-4cc4-98fa-fdc3d4e2c3b7" />

### 13. Pinjam Buku Sampai Stok Habis
[13 (Pinjam Buku Sampai Stok Habis)](Hasil/13%20(Pinjam%20Buku%20Sampai%20Stok%20Habis).png)
<img width="2736" height="768" alt="13 (Pinjam Buku Sampai Stok Habis)" src="https://github.com/user-attachments/assets/9f8c4049-2b73-4179-9cbd-b68b970cd87b" />

### 14. Hapus Transaksi yang Masih Dipinjam
[14 (Hapus Transaksi yang Masih Dipinjam)](Hasil/14%20(Hapus%20Transaksi%20yang%20Masih%20Dipinjam).png)
<img width="2736" height="768" alt="14 (Hapus Transaksi yang Masih Dipinjam)" src="https://github.com/user-attachments/assets/67d75070-f9bf-4f64-9c6b-cb322ef26941" />

### 15. Verifikasi Hasil Langsung di phpMyAdmin
![Verifikasi hasil langsung di PHPMyAdmin](Hasil/Verifikasi%20hasil%20langsung%20di%20PHPMyAdmin.png)
<img width="1368" height="768" alt="Verifikasi hasil langsung di PHPMyAdmin" src="https://github.com/user-attachments/assets/37844046-fbbd-4ed8-82c4-dfb10ff914bb" />
