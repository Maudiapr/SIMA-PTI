## Fungsi file
- `config/database.php`: koneksi MySQL melalui PDO.
- `includes/auth.php`: memulai session dan melindungi halaman.
- `includes/functions.php`: terjemahan, escaping output, token CSRF, dan helper redirect.
- `includes/header.php` / `footer.php`: layout yang dipakai bersama.
- `login.php` / `logout.php`: login dan logout.
- `register.php`: membuat akun baru dengan validasi dan password hash.
- `index.php`: daftar seluruh mahasiswa.
- `create.php`: tambah mahasiswa.
- `edit.php`: ubah data berdasarkan ID unik.
- `delete.php`: hapus data melalui POST.
- `language.php`: menyimpan pilihan bahasa di session.
- `database.sql`: membuat database dan tabel.

## Catatan keamanan
- Query dengan input pengguna menggunakan prepared statements.
- Semua nilai yang ditampilkan dalam HTML di-escape dengan `htmlspecialchars()`.
- Password disimpan menggunakan `password_hash()` dan diverifikasi dengan `password_verify()`.
- Operasi perubahan data memakai POST dan token CSRF.
- Session ID diregenerasi saat login.
- Jangan gunakan akun awal atau konfigurasi database default untuk server publik.
