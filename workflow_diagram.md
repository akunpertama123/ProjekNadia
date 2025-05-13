# Diagram Alur Kerja Proyek Template Marketplace

```mermaid
graph TD
    A[Mulai] --> B[Instalasi Dependensi]
    B --> C[Jalankan Server Backend]
    C --> D[Akses Aplikasi di Browser]
    D --> E[Frontend Menampilkan Halaman]
    E --> F[Pengguna Berinteraksi dengan UI]
    F --> G[Frontend Mengirim Permintaan API ke Backend]
    G --> H[Backend Memproses Permintaan]
    H --> I[Backend Mengakses Data JSON / File Upload]
    I --> J[Backend Mengirimkan Respon ke Frontend]
    J --> E
    F --> K[Pengguna Melakukan Login / Registrasi]
    K --> G
    F --> L[Pengguna Mengelola Template dan Pembayaran]
    L --> G
    C --> M[Backend Melayani File Statis Frontend]
```

Diagram ini menggambarkan alur utama dari instalasi, menjalankan server, interaksi pengguna dengan frontend, komunikasi antara frontend dan backend, serta pengelolaan data di backend.
