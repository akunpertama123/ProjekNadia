# Laporan Alur Kerja dan Fungsi Tools dalam Proyek Template Marketplace

## 1. Node.js
Node.js adalah platform runtime yang memungkinkan menjalankan kode JavaScript di luar browser, khususnya di server. Dalam proyek ini, Node.js digunakan untuk menjalankan backend server yang menangani API dan melayani file frontend.

## 2. npm (Node Package Manager)
npm adalah alat manajemen paket yang digunakan untuk mengelola dependensi (library/paket) yang dibutuhkan oleh proyek. Dengan menjalankan perintah `npm install`, npm akan mengunduh dan menyimpan paket-paket tersebut di folder `node_modules`.

## 3. Folder node_modules
Folder ini berisi semua paket yang diunduh oleh npm. Paket-paket ini menyediakan berbagai fungsi yang digunakan oleh aplikasi, seperti:
- **express**: Framework web untuk membuat server dan API.
- **bcryptjs**: Library untuk enkripsi password.
- **multer**: Middleware untuk menangani upload file.
- **cors**: Middleware untuk mengatur kebijakan Cross-Origin Resource Sharing.
- Dan lain-lain sesuai kebutuhan proyek.

## 4. Struktur Folder dan File Proyek

### Backend Folder
- **package.json**: File konfigurasi utama proyek Node.js yang berisi metadata proyek, daftar dependensi, dan skrip untuk menjalankan aplikasi (misalnya `start`).
- **server_new_clean.mjs**: File utama backend yang menjalankan server Express. Mengatur middleware, API endpoint, dan melayani file frontend.
- **backend/data/**: Folder yang berisi data JSON seperti:
  - `users.json`: Data pengguna aplikasi.
  - `templates.json`: Data template yang tersedia.
  - `payments.json`: Data transaksi pembayaran.
- **utils/**: Folder berisi helper functions, misalnya `payments.js` yang mengelola fungsi terkait pembayaran.
- **node_modules/**: Folder yang berisi semua paket npm yang diinstal.

### Marketplace Folder (Frontend)
- Berisi file HTML, CSS, dan JavaScript yang membentuk tampilan dan interaksi pengguna.
- Contoh file penting:
  - `index.html`: Halaman utama aplikasi.
  - `login.html`, `register.html`: Halaman autentikasi pengguna.
  - `admin/dashboard.html`: Halaman dashboard admin.
  - Folder `js/`: Berisi skrip JavaScript untuk interaksi frontend.
  - Folder `css/`: Berisi file stylesheet untuk tampilan.

## 5. Alur Kerja Proyek
1. **Instalasi Dependensi**: Jalankan `npm install` di folder backend untuk mengunduh semua paket yang dibutuhkan.
2. **Menjalankan Server**: Jalankan `npm start` di folder backend untuk memulai server Express.
3. **Akses Aplikasi**: Buka browser dan akses `http://localhost:8002` untuk menggunakan aplikasi.
4. **Interaksi Pengguna**: Frontend berinteraksi dengan backend melalui API yang disediakan.
5. **Pengelolaan Data**: Backend mengelola data pengguna, template, dan pembayaran menggunakan file JSON dan penyimpanan file upload.

## 6. Penjelasan Singkat Per File Penting Backend

- **server_new_clean.mjs**: 
  - Menginisialisasi server Express.
  - Mengatur middleware seperti CORS, body-parser, multer untuk upload file.
  - Mendefinisikan API endpoint untuk login, registrasi, pengelolaan template, pembayaran, dan download file.
  - Melayani file statis frontend dari folder `marketplace`.
  - Menjalankan server pada port 8002.

- **utils/payments.js**:
  - Berisi fungsi untuk memuat dan menyimpan data pembayaran dari/ke file `payments.json`.

- **backend/data/users.json, templates.json, payments.json**:
  - File JSON yang menyimpan data aplikasi secara persisten.

## 7. Penjelasan Singkat Per Folder Frontend

- **marketplace/**:
  - Berisi halaman HTML yang diakses pengguna.
  - Folder `js/` berisi skrip untuk autentikasi, pengelolaan keranjang, pembayaran, dan interaksi lainnya.
  - Folder `css/` berisi stylesheet untuk mempercantik tampilan halaman.

---
