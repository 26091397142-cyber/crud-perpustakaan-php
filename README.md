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
![1 (Buka Halaman Buku)](Hasil/1%20(Buka%20Halaman%20Buku).png)

### 2. Pencarian Data
![2 (Pencarian Data)](Hasil/2%20(Pencarian%20Data).png)

### 3. Tambah Buku Baru
![3 (Tambah Buku Baru)](Hasil/3%20(Tambah%20Buku%20Baru).png)

### 4. Tes Error ID Duplikat
![4 (Tes Error ID Duplikat)](Hasil/4%20(Tes%20Error%20ID%20Duplikat).png)

### 5. Tes Error Format ID
![5 (Tes Error Format ID)](Hasil/5%20(Tes%20Error%20Format%20ID).png)

### 6. Edit Buku
![6 (Edit Buku)](Hasil/6%20(Edit%20Buku).png)

### 7. Hapus Buku yang Belum Pernah Dipinjam
![7 (Hapus Buku yang Belum Pernah Dipinjam)](Hasil/7%20(Hapus%20Buku%20yang%20Belum%20Pernah%20Dipinjam).png)

### 8. Tes Error Hapus Buku yang Memiliki Riwayat Pinjam
![8 (Tes Error Hapus Buku yang Memiliki Riwayat Pinjam)](Hasil/8%20(Tes%20Error%20Hapus%20Buku%20yang%20Memiliki%20Riwayat%20Pinjam).png)

### 9. Buka Halaman Peminjaman
![9 (Buka Halaman Peminjaman)](Hasil/9%20(Buka%20Halaman%20Peminjaman).png)

### 10. Filter Status
![10 (Filter Status)](Hasil/10%20(Filter%20Status).png)

### 11. Catat Peminjaman Baru
![11 (Catat Peminjaman Baru)](Hasil/11%20(Catat%20Peminjaman%20Baru).png)

### 12. Pengembalian Buku
![12 (Pengembalian Buku)](Hasil/12%20(Pengembalian%20Buku).png)

### 13. Pinjam Buku Sampai Stok Habis
![13 (Pinjam Buku Sampai Stok Habis)](Hasil/13%20(Pinjam%20Buku%20Sampai%20Stok%20Habis).png)

### 14. Hapus Transaksi yang Masih Dipinjam
![14 (Hapus Transaksi yang Masih Dipinjam)](Hasil/14%20(Hapus%20Transaksi%20yang%20Masih%20Dipinjam).png)

### 15. Verifikasi Hasil Langsung di phpMyAdmin
![Verifikasi hasil langsung di PHPMyAdmin](Hasil/Verifikasi%20hasil%20langsung%20di%20PHPMyAdmin.png)
