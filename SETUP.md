# Setup Guide untuk GitHub Profile

Sesuai dengan referensi gambar yang kamu berikan, GitHub profile tersebut menggunakan kombinasi dari **Activity Graph**, **PageSpeed Insights** dari metrics, dan **Snake Animation** pada graf kontribusi GitHub.

Aku sudah menyalin dan menyiapkan konfigurasi yang kamu butuhkan. Berikut adalah langkah-langkah yang perlu kamu ikuti agar tampilannya bisa berjalan dan terlihat persis seperti di gambar.

## Langkah-langkah:

### 1. Ubah URL PageSpeed Insights
Aku telah menambahkan GitHub Actions untuk _PageSpeed Insights_.
1. Buka file `.github/workflows/pagespeed.yml`
2. Pada bagian `plugin_pagespeed_url:`, ganti `https://your-website.com` dengan URL website aslimu (misalnya website portofolio).

### 2. Push ke GitHub
Karena ini menggunakan **GitHub Actions** untuk men-generate gambar PageSpeed dan animasi Snake, maka kamu harus meng-upload (*push*) repository ini ke GitHub milikmu.
Pastikan nama repository-nya **sama persis dengan username GitHub kamu** (misal: `MuhammadFeryantoPratama`).

### 3. Aktifkan Permissions untuk GitHub Actions
Secara default, GitHub Actions butuh izin (permission) untuk menulis (push) file _generated_ (seperti `pagespeed.svg` dan file snake) kembali ke dalam repository kamu.
1. Buka repository GitHub-mu di browser.
2. Masuk ke tab **Settings** > **Actions** > **General**.
3. Scroll ke bawah ke bagian **Workflow permissions**.
4. Pilih **Read and write permissions**.
5. Centang **"Allow GitHub Actions to create and approve pull requests"**.
6. Klik **Save**.

### 4. Jalankan GitHub Actions secara Manual (Pertama Kali)
Agar gambarnya langsung muncul di profile kamu tanpa perlu menunggu jadwal (*schedule*), kamu bisa jalankan *Action*-nya secara manual.
1. Masuk ke tab **Actions** di repository kamu.
2. Di sebelah kiri, pilih **Metrics** (untuk PageSpeed), klik tombol **Run workflow** -> **Run workflow**.
3. Di sebelah kiri, pilih **Generate Snake Animation**, klik tombol **Run workflow** -> **Run workflow**.

Setelah proses _workflow_ selesai (ditandai dengan centang hijau), gambar PageSpeed dan Snake Animation akan otomatis muncul di GitHub Profile kamu! 🚀
