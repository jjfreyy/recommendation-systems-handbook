# Recommendation Systems Handbook

Repositori ini berisi kumpulan implementasi algoritma **Sistem Rekomendasi** yang ditulis menggunakan Python (`3.12.13`) dan Jupyter Notebook. Proyek ini dirancang sebagai bahan pembelajaran dan referensi praktis dengan penjelasan konsep, notasi matematika, contoh perhitungan sederhana, serta visualisasi hasil.

> **Status Proyek:** 🚧 _Sedang dalam pengembangan aktif — algoritma baru akan terus ditambahkan secara bertahap._

---

## 📂 Struktur Proyek

```text
.
├── src/
│   ├── 01-popularity_based.ipynb
│   ├── 02-content_based_filtering.ipynb
│   └── 03-collaborative_filtering.ipynb
│   └── 04-matrix_factorization.ipynb
├── .gitignore
├── r.txt                                  # Daftar dependensi Python
└── README.md
```

---

## 🧠 Daftar Algoritma

1. **Popularity-Based Recommendation**: _Most Popular_, _Average Rating_, _Weighted Rating_, dan _Time-Decay Popularity_.
2. **Content-Based Filtering**: TF-IDF & _Cosine Similarity_.
3. **Collaborative Filtering**: _User-Based CF_ dan _Weighted Average_.
4. **Matrix Factorization**: _Funk SVD_ (SGD) & _NMF_ menggunakan _Pure NumPy_.

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
