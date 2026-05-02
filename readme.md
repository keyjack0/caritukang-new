# Cari-Tukang

Aplikasi simulasi pemesanan tukang yang dibuat dengan PHP, CodeIgniter, dan MySQL. Proyek ini menyediakan antarmuka admin dan pengguna untuk mengelola layanan tukang, booking, pelanggan, dan ulasan.

## Teknologi

- PHP 8
- CodeIgniter3
- JavaScript
- Bootstrap 5
- MySQL

## Fitur Utama

- Halaman register dan login pengguna
- Admin dashboard untuk manajemen data
- CRUD untuk informasi mitra tukang, keahlian, booking, dan ulasan
- Tampilan daftar mitra dan detail layanan
- Sistem autentikasi admin dan pengguna

## Struktur Proyek

- `admin/` – aplikasi admin
  - `application/controllers/` – controller admin
  - `application/models/` – model database admin
  - `application/views/` – tampilan admin
- `pengguna/` – aplikasi pengguna
  - `application/controllers/` – controller pengguna
  - `application/models/` – model database pengguna
  - `application/views/` – tampilan pengguna
- `assets/` – file asset proyek seperti gambar dan CSS
- `database/` – file SQL untuk import database

## Instalasi

1. Salin seluruh folder proyek `cari-tukang` ke dalam direktori web server, misalnya `htdocs` di XAMPP.
2. Buat database baru di MySQL, misalnya `cari_tukang`.
3. Import file SQL yang tersedia:
   - `database/caritukang.sql`
4. Sesuaikan konfigurasi database di:
   - `admin/application/config/database.php`
   - `pengguna/application/config/database.php`
5. Jalankan aplikasi melalui browser:
   - Admin: `http://localhost/cari-tukang/admin`
   - Pengguna: `http://localhost/cari-tukang/pengguna`

## Hosting di InfinityFree dengan FileZilla

1. Daftar atau masuk ke akun InfinityFree di `https://www.infinityfree.net/`.
2. Buat akun hosting baru dan catat detail FTP yang diberikan.
3. Buka FileZilla dan sambungkan ke server FTP InfinityFree dengan:
   - Host: nama host FTP dari InfinityFree
   - Username: username FTP
   - Password: password FTP
   - Port: 21
4. Di panel lokal FileZilla, buka folder `cari-tukang` pada komputer Anda.
5. Di panel server FileZilla, buka folder `htdocs` pada akun InfinityFree.
6. Upload semua file dan folder dari `cari-tukang` ke `htdocs`.
7. Import database MySQL di panel kontrol InfinityFree:
   - Buat database baru di cPanel InfinityFree.
   - Import file `database/caritukang.sql` melalui phpMyAdmin.
  
8. Sesuaikan konfigurasi database di file proyek:
   - `admin/application/config/database.php`
   - `pengguna/application/config/database.php`
   - Gunakan hostname, nama database, username, dan password dari InfinityFree.
9. Jika perlu, sesuaikan `base_url` di `admin/application/config/config.php` dan `pengguna/application/config/config.php` sesuai domain atau subdomain InfinityFree.
10. Akses aplikasi melalui URL hosting InfinityFree Anda, misalnya `http://namadomain.infinityfree.app/admin` untuk admin.

## Penggunaan

- Untuk pengguna baru: daftar terlebih dahulu di halaman register.
- Untuk pengguna yang sudah ada: login langsung menggunakan akun yang tersedia.
- Admin dapat mengakses panel khusus untuk mengelola data aplikasi.

## Akun Default

### Pengguna
- Username: `dzaky`
- Password: `dzaky`

### Admin
- Username: `admin`
- Password: `admin`

## Catatan

- Pastikan server XAMPP berjalan dengan modul Apache dan MySQL aktif.
- Jika menggunakan URL berbeda, sesuaikan konfigurasi base URL di `application/config/config.php`.
- Periksa izin folder `assets/` bila ada masalah memuat file CSS atau gambar.
