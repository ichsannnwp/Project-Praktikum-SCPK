# 💻 Sistem Pendukung Keputusan Pemilihan Laptop (Metode Weighted Product)

Aplikasi berbasis web interaktif ini dibangun menggunakan **Streamlit** untuk membantu pengguna menentukan pilihan laptop terbaik berdasarkan berbagai kriteria spesifikasi hardware. Sistem ini menggunakan algoritma *Multi-Criteria Decision Making* (MCDM) dengan **Metode Weighted Product (WP)**.

## ✨ Fitur Utama

- **🎛️ Pengaturan Bobot Dinamis:** Pengguna dapat menyesuaikan bobot tingkat kepentingan (skala 1-5) untuk masing-masing kriteria secara *real-time* melalui *sidebar*.
- **🔄 Integrasi & Pemetaan Data Otomatis:** Sistem secara otomatis memetakan spesifikasi prosesor dan kartu grafis dari data laptop dengan nilai benchmark global (CPU multiScore dan GPU 3DMark).
- **🧮 Transparansi Kalkulasi WP:** Menampilkan langkah-langkah matematis secara detail, mulai dari konversi tipe data, normalisasi bobot kriteria, perhitungan Vektor S, hingga hasil akhir Vektor V.
- **📊 Visualisasi Data Interaktif:** Menyajikan grafik peringkat Top 10 laptop, persentase kualitas kriteria untuk laptop peringkat pertama, dan grafik komparasi *bar chart* untuk Top 3 laptop.

## 📋 Kriteria Penilaian

Sistem ini mengevaluasi alternatif laptop berdasarkan 5 kriteria berikut:

| Kriteria | Sifat Atribut | Keterangan |
| :--- | :--- | :--- |
| **CPU** | Benefit | Diukur dari nilai *multiScore* benchmark CPU. |
| **GPU** | Benefit | Diukur dari skor *3DMark* grafis. |
| **RAM** | Benefit | Kapasitas memori dalam Gigabyte (GB). |
| **Storage** | Benefit | Kapasitas penyimpanan data dalam Gigabyte (GB). |
| **Harga** | Cost | Harga laptop dalam satuan USD (Semakin murah semakin baik). |

## 📂 Struktur Dataset

Aplikasi ini membutuhkan 3 file dataset berformat CSV yang harus diletakkan di dalam folder `dataset/`:
1. `laptop.csv`: Berisi daftar alternatif unit laptop beserta spesifikasi dasar dan harganya.
2. `CPU.csv`: Berisi database benchmark prosesor (membutuhkan kolom *manufacturer*, *namaCPU*, dan *multiScore*).
3. `GPU.csv`: Berisi database benchmark kartu grafis (membutuhkan kolom *gpuName* dan *G3Dmark*).

## 🚀 Cara Instalasi dan Menjalankan Aplikasi

1. **Pastikan Python sudah terinstal** (Disarankan versi 3.8 atau lebih baru).
2. **Clone repositori ini** ke komputer lokal kamu:
```bash
   git clone [https://github.com/username-kamu/nama-repo.git](https://github.com/username-kamu/nama-repo.git)
   cd nama-repo