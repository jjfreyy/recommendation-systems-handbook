# Recommendation Systems Handbook

Repositori ini berisi kumpulan implementasi algoritma **Sistem Rekomendasi** yang ditulis menggunakan Python (`3.12.13`) dan Jupyter Notebook. Proyek ini dirancang sebagai bahan pembelajaran dan referensi praktis dengan penjelasan konsep, notasi matematika, contoh perhitungan sederhana, serta visualisasi hasil.

> **Status Proyek:** 🚧 _Sedang dalam pengembangan aktif — algoritma baru akan terus ditambahkan secara bertahap._

---

## 📂 Struktur Proyek

```text
.
├── src/
│   ├── 01-popularity_based.ipynb          # Rekomendasi berbasis popularitas (Most Popular, Weighted Rating, Time-Decay)
│   ├── 02-content_based_filtering.ipynb   # Rekomendasi berbasis kemiripan konten (TF-IDF & Cosine Similarity)
│   └── 03-collaborative_filtering.ipynb   # Rekomendasi berbasis kemiripan perilaku pengguna (User-Based CF)
├── .gitignore
├── r.txt                                  # Daftar dependensi Python
└── README.md
```

---

## 🧠 Daftar Algoritma

### 1. Popularity-Based Recommendation (`01-popularity_based.ipynb`)

Memberikan rekomendasi item berdasarkan tren dan popularitas secara umum tanpa memerlukan riwayat profil pengguna.

- **Metode:** _Most Popular_, _Average Rating_, _Weighted Rating (Bayesian Average)_, dan _Time-Decay Popularity_.
- **Visualisasi:** Grafik batang perbandingan 2×2 untuk melihat perbedaan peringkat skor dari keempat metode.

### 2. Content-Based Filtering (`02-content_based_filtering.ipynb`)

Merekomendasikan item yang memiliki kemiripan atribut atau deskripsi konten dengan item yang disukai pengguna sebelumnya.

- **Metode:** Pembobotan kata **TF-IDF** dan pengukuran sudut vektor **Cosine Similarity**.
- **Visualisasi:** _Heatmap_ matriks kemiripan antar item dan grafik batang peringkat rekomendasi teratas.

### 3. Collaborative Filtering (`03-collaborative_filtering.ipynb`)

Merekomendasikan item kepada seorang pengguna berdasarkan pola penilaian (_rating_) dari pengguna lain yang memiliki preferensi serupa (_User-Based_).

- **Metode:** _User-to-User Cosine Similarity_ dan prediksi skor _rating_ menggunakan _Weighted Average_.
- **Visualisasi:** _Heatmap_ kemiripan antar pengguna dan grafik batang skor prediksi _rating_.

---

## 🚀 Cara Menjalankan Proyek

### 1. Kloning Repositori

```bash
git clone https://github.com/jjfreyy/recommendation-systems-handbook.git
cd recommendation-systems-handbook
```

### 2. Instal Miniconda & Buat _Environment_ (Python 3.12.13)

Pastikan **Miniconda** sudah terinstal di sistem Anda (unduh melalui [dokumentasi resmi Miniconda](https://anaconda.com) jika belum terpasang), lalu jalankan perintah berikut untuk membuat dan mengaktifkan _environment_:

```bash
conda create -n recsys python=3.12.13 -y
conda activate recsys
```

### 3. Instal Dependensi

```bash
pip install -r r.txt
```

### 4. Buka Jupyter Notebook

Buka folder `src/` menggunakan VS Code, JupyterLab, atau Jupyter Notebook, lalu pilih kernel Python **`recsys`** sebelum menjalankan sel kode.
