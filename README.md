# Sistem Kategori Buku

## Nama dan NIM
Nama  : Muhammad Hamdi Yahya 
NIM   : 60324035

## Deskripsi Singkat Aplikasi
Aplikasi ini merupakan sistem berbasis web yang digunakan untuk mengelola data kategori buku. Pengguna dapat melakukan operasi CRUD (Create, Read, Update, Delete) dengan tampilan sederhana dan mudah digunakan.

Fitur utama:
- Menampilkan daftar kategori buku
- Menambahkan kategori baru
- Mengedit kategori
- Menghapus kategori
- Validasi input data
- Notifikasi sukses dan error

Teknologi yang digunakan:
- PHP Native (tanpa framework)
- MySQL
- Bootstrap

## Cara Instalasi dan Menjalankan Aplikasi
1. Download / Clone project dan simpan ke folder:
   - htdocs (XAMPP)
   - www (Laragon)

2. Buat database di phpMyAdmin dengan nama:
   uts_perpustakaan_60324035

3. Jalankan query berikut untuk membuat tabel:
```sql
   CREATE TABLE kategori (
       id_kategori INT AUTO_INCREMENT PRIMARY KEY,
       kode_kategori VARCHAR(10) NOT NULL,
       nama_kategori VARCHAR(50) NOT NULL,
       deskripsi TEXT,
       status ENUM('Aktif','Nonaktif') DEFAULT 'Aktif',
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );
   ```

4. Tambahkan sample data:
```sql
   INSERT INTO `kategori` (`id_kategori`, `kode_kategori`, `nama_kategori`, `deskripsi`, `status`, `created_at`) VALUES
   (1, 'KAT-001', 'Pemrograman', 'Buku-buku tentang bahasa pemrograman', 'Aktif', '2026-05-04 11:42:22'),
   (2, 'KAT-002', 'Database', 'Buku-buku tentang sistem basis data', 'Aktif', '2026-05-04 11:42:22'),
   (3, 'KAT-003', 'Jaringan', 'Buku-buku tentang jaringan komputer', 'Aktif', '2026-05-04 11:42:22'),
   (4, 'KAT-004', 'Keamanan', 'Buku-buku tentang sistem keamanan', 'Nonaktif', '2026-05-04 11:42:22'),
   (5, 'KAT-005', 'Analisis Data', 'Buku-buku tentang analisis data', 'Aktif', '2026-05-04 11:42:22'),
   (6, 'KAT-006', 'Multimedia', 'Buku-buku tentang desain grafis dan multimedia', 'Nonaktif', '2026-05-04 12:18:19');
   ```

5. Buka file config/database.php lalu sesuaikan:
   - host: localhost
   - username: root
   - password: (kosong jika default)
   - database: uts_perpustakaan_60324035

6. Jalankan aplikasi di browser:
   http://localhost/nama-folder-project/index.php

## Struktur Folder
```text
project-folder/
│
├── config/
│   └── database.php
│
├── index.php
├── create.php
├── edit.php
├── delete.php
├── test_connection.php
│
└── README.md
```