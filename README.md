# 📘 Laporan Praktikum Pertemuan Ke - 6

🧑‍🎓 Kholil Irsyad Marwan - 4524210110

# 📚 Book Management System (AuthBook)

Aplikasi manajemen buku dan penulis berbasis web yang dibangun menggunakan Laravel 11 dan Filament v3 Admin Panel untuk Praktikum 6 Pemrograman Berbasis Web.

<p align="center">
  <img src="https://img.shields.io/badge/PHP-8.2-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP 8.2">
  <img src="https://img.shields.io/badge/Laravel-11.x-FF2D20?style=for-the-badge&logo=laravel&logoColor=white" alt="Laravel 11">
  <img src="https://img.shields.io/badge/Filament-v3-FDAE4B?style=for-the-badge&logo=filament&logoColor=black" alt="Filament v3">
  <img src="https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite">
</p>

📋 Daftar Isi
Instalasi & Penggunaan

Soal & Jawaban Tugas 1

Halaman yang Tersedia

Tentang Aplikasi

Tujuan Praktikum

Fitur Utama

Tech Stack

Struktur Database

📸 Hasil Screenshot Tampilan Aplikasi
---

### 1. Clone Repository

Buka terminal dan jalankan perintah clone untuk mengunduh repositori:

```bash
git clone [https://github.com/KholilIrsyadMarwan/4524210110_KHOLILIRSYADMARWAN_PBW-A-Praktikum6.git](https://github.com/KholilIrsyadMarwan/4524210110_KHOLILIRSYADMARWAN_PBW-A-Praktikum6.git)

cd 4524210110_KHOLILIRSYADMARWAN_PBW-A/authbook

```
### 2. Install PHP Dependencies
Instal seluruh pustaka PHP yang dibutuhkan (termasuk Filament v3): <br>


``` bash
composer install
```

### 3. Setup Environment (.env)

Salin file .env.example menjadi .env lalu generate application key:

``` bash
cp .env.example .env
php artisan key:generate
```
Catatan Konfigurasi Database (SQLite):

Pastikan di dalam file .env variabel database sudah terkonfigurasi ke SQLite:

Ini, TOML 
DB_CONNECTION=sqlite

### 4. Setup Database & Seeding Data Dummy
Jalankan migrasi database untuk membuat tabel authors & books, sekaligus mengisi data dummy (10 Author & 50 Book): <br>

```bash
php artisan migrate:fresh --seed
```

### 5. Membuat Account Admin Filament
Buat akun pengguna agar bisa masuk ke dalam Filament Admin Panel: <br>

```bash
php artisan make:filament-user
```

Input data akun: <br>

Name: Admin<br>

Email address: admin@example.com<br>

Password: password<br>

### 6. Jalankan Local Development Server
Jalankan server bawaan Laravel: <br>

```bash
php artisan serve
```
## 📋 Daftar Isi

- [🚀 Instalasi & Penggunaan](#-instalasi--penggunaan)
- [📌 Soal & Jawaban Tugas 1](#-soal--jawaban-tugas-1)
- [🎯 Tentang Aplikasi](#-tentang-aplikasi)
- [🎯 Tujuan Praktikum](#-tujuan-praktikum)
- [✨ Fitur Utama](#-fitur-utama)
- [🛠️ Tech Stack](#️-tech-stack)
- [🗄️ Struktur Database](#️-struktur-database)
- [📸 Hasil Screenshot Tampilan Aplikasi](#-hasil-screenshot-tampilan-aplikasi)

 ### 📌 Soal & Jawaban Tugas 1
Tugas 1: Implementasi Dasar (Nilai: 40)

Implementasikan semua langkah di atas dan buktikan dengan:

### 1. Screenshot admin panel yang berhasil login


### 2. Screenshot list books dengan data yang terseed

### 3. Screenshot form create book

### 4. Screenshot hasil pencarian

### 5. Screenshot filter aktif
### 💡 Jawaban Bukti Implementasi (Screenshot):
###  1. Screenshot Admin Panel yang Berhasil Login
![Dashboard](screenshot/dashboard.jpeg)
###  2. Screenshot List Books dengan Data yang Terseed (50 Books)
   ![List Books](screenshot/list_books.jpeg)
###  3. Screenshot Form Create Book
   ![Form Create Book](screenshot/create_book.jpeg)
###  4. Screenshot Hasil Pencarian
   ![Hasil Pencarian](screenshot/hasil_pencarian.jpeg)
###  5. Screenshot Filter Aktif
   ![Filter Aktif](screenshot/filter_aktif.jpeg)

### 🎯 Tentang Aplikasi
AuthBook adalah aplikasi pengelolaan katalog pustaka digital berbasis admin panel yang responsif dan interaktif. Dikelola menggunakan framework Laravel 11 dan Filament v3, sistem ini memungkinkan administrator untuk mengelola data penulis (author) serta koleksi buku secara terstruktur.

### 🎯 Tujuan Praktikum
Memahami pembuatan admin panel modern dengan Filament v3.

Mengimplementasikan skema database relasional (Relationship HasMany & BelongsTo) antara Model Author dan Book.

Menerapkan pengisian data otomatis (Data Seeding & Factory) untuk 10 Penulis dan 50 Buku.

Menyiapkan otorisasi hak akses menggunakan Laravel Policy untuk mengamankan data.

### ✨ Fitur Utama
✅ Authentication Admin Panel - Proteksi login khusus user administrator.

✅ Manajemen Author (Penulis) - Fitur CRUD lengkap untuk data penulis.

✅ Manajemen Book (Buku) - Fitur CRUD koleksi buku lengkap dengan ISBN, Cover, Tahun, dan Status.

✅ Search & Filter Table - Pencarian instan dan penyaringan data interaktif pada tabel buku.

✅ Automated Seeding - Pengisian 10 data Author dan 50 data Buku instan saat migrasi.

✅ Authorization Policy - Pengaturan izin akses aksi CRUD berbasis Policy.

### 🛠️ Tech Stack
Backend
Laravel 11.x - PHP Framework

PHP ^8.2 - Programming Language

SQLite - Database Storage

Eloquent ORM - Database Management

Admin Panel & Frontend
Filament v3 - Admin Panel Framework

Tailwind CSS - UI Styling Framework

### 🗄️ Struktur Database
authors: id, name, timestamps

books: id, isbn, title, author_id, publisher, year, cover, status, timestamps

### 📸 Hasil Screenshot Tampilan Aplikasi
### 1. Halaman Login Admin
### 2. Dashboard Utama Admin Panel
### 3. Daftar Buku (Seeded 50 Data Books)
### 4. Form Tambah Buku (Create Book)
### 5. Detail Informasi Buku (View Book)
### 6. Fitur Pencarian Data Buku (Search)
### 7. Fitur Filtering Aktif pada Tabel
### 8. Kelola Data Penulis (Author List)
