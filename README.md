# Recommendation Systems Handbook

Repositori ini berisi kumpulan implementasi algoritma **Sistem Rekomendasi** yang ditulis menggunakan Python (`3.12.13`) dan Jupyter Notebook. Proyek ini dirancang sebagai bahan pembelajaran dan referensi praktis dengan penjelasan konsep, notasi matematika, contoh perhitungan sederhana, serta visualisasi hasil.

> **Status Proyek:** 🚧 _Sedang dalam pengembangan aktif — algoritma baru akan terus ditambahkan secara bertahap._

---

## 📂 Struktur Proyek

<pre style="font-size: 16px; line-height: 1.6;">
├── <a href="src/">src/</a>
│   ├── <a href="src/01-popularity_based.ipynb">01-popularity_based.ipynb</a>
│   ├── <a href="src/02-content_based_filtering.ipynb">02-content_based_filtering.ipynb</a>
│   ├── <a href="src/03-collaborative_filtering.ipynb">03-collaborative_filtering.ipynb</a>
│   ├── <a href="src/04-matrix_factorization.ipynb">04-matrix_factorization.ipynb</a>
│   ├── <a href="src/05-implicit_feedback_recommendation.ipynb">05-implicit_feedback_recommendation.ipynb</a>
│   ├── <a href="src/06-advanced_factorization_models.ipynb">06-advanced_factorization_models.ipynb</a>
│   └── <a href="src/07-deep_learning_based_recommendation.ipynb">07-deep_learning_based_recommendation.ipynb</a>
├── <a href=".gitignore">.gitignore</a>
├── <a href="r.txt">r.txt</a> # Daftar dependensi Python
└── <a href="README.md">README.md</a>
</pre>

---

## 🧠 Daftar Algoritma

1. **[Popularity-Based Recommendation](src/01-popularity_based.ipynb)**: _Most Popular_, _Average Rating_, _Weighted Rating_, dan _Time-Decay Popularity_.
2. **[Content-Based Filtering](src/02-content_based_filtering.ipynb)**: TF-IDF & _Cosine Similarity_.
3. **[Collaborative Filtering](src/03-collaborative_filtering.ipynb)**: _User-Based CF_ dan _Weighted Average_.
4. **[Matrix Factorization](src/04-matrix_factorization.ipynb)**: _Funk SVD_ (SGD) & _NMF_ menggunakan _Pure NumPy_.
5. **[Implicit Feedback Recommendation](src/05-implicit_feedback_recommendation.ipynb)**: _Weighted Alternating Least Squares (ALS)_ & _Bayesian Personalized Ranking (BPR)_ menggunakan _Pure NumPy_.
6. **[Advanced Factorization Models](src/06-advanced_factorization_models.ipynb)**: _Factorization Machines (FM)_ & _Field-aware Factorization Machines (FFM)_ menggunakan _Pure NumPy_.
7. **[Deep Learning-Based Recommendation](src/07-deep_learning_based_recommendation.ipynb)**: _Neural Collaborative Filtering (NCF)_ dengan arsitektur _Neural Matrix Factorization (NeuMF)_ & _Deep Factorization Machine (DeepFM)_.

---

## 🚀 Cara Menjalankan Proyek

### 1. Kloning Repositori

```bash
git clone https://github.com/jjfreyy/recommendation-systems-handbook.git
cd recommendation-systems-handbook
```

### 2. Instal Miniconda & Buat _Environment_ (Python 3.12.13)

Pastikan **Miniconda** sudah terinstal di sistem Anda (unduh melalui [dokumentasi resmi Miniconda](https://www.anaconda.com/docs/getting-started/miniconda/main) jika belum terpasang), lalu jalankan perintah berikut untuk membuat dan mengaktifkan _environment_:

```bash
conda create -n recsys python=3.12.13 -y
conda activate recsys
```

### 3. Instal Dependensi

```bash
python -m pip install -r r.txt
```

### 4. Instal PyTorch dengan CUDA (Direkomendasikan)

Untuk komputer dengan **GPU NVIDIA** dan driver yang kompatibel, instal PyTorch dengan dukungan **CUDA 13.2**:

```bash
python -m pip install torch==2.15.0 --index-url https://download.pytorch.org/whl/cu132
```

Sebagai alternatif, PyTorch 2.15.0 juga menyediakan build **CUDA 13.4**:

```bash
python -m pip install torch==2.15.0 --index-url https://download.pytorch.org/whl/cu134
```

Pilih **salah satu** perintah di atas. Periksa opsi yang sesuai untuk sistem lain melalui [panduan instalasi resmi PyTorch](https://pytorch.org/get-started/locally/). Pastikan driver GPU NVIDIA mendukung runtime CUDA yang dipilih.

Verifikasi apakah PyTorch mendeteksi GPU:

```bash
python -c "import torch; print('PyTorch:', torch.__version__); print('CUDA:', torch.version.cuda); print('GPU available:', torch.cuda.is_available()); print('GPU:', torch.cuda.get_device_name(0) if torch.cuda.is_available() else 'Tidak tersedia')"
```

Jika `GPU available: True`, notebook dapat menjalankan model pada GPU melalui `device = 'cuda'`.

### 5. Buka Jupyter Notebook

Buka folder `src/` menggunakan VS Code, JupyterLab, atau Jupyter Notebook, lalu pilih kernel Python **`recsys`** sebelum menjalankan sel kode.

### 6. Alternatif GPU Cloud: Google Colab atau Kaggle

> **Catatan:** Pelatihan model _deep learning_ seperti NeuMF dapat dijalankan di CPU, tetapi penggunaan **GPU direkomendasikan**, terutama untuk dataset yang lebih besar atau eksperimen berulang. Jika tidak memiliki GPU NVIDIA yang kompatibel, gunakan layanan notebook berbasis cloud berikut.

- **[Google Colab](https://colab.research.google.com/)**: Buka atau impor notebook dari GitHub, kemudian pilih **Runtime → Change runtime type → Hardware accelerator → GPU**.
- **[Kaggle Notebooks](https://www.kaggle.com/code)**: Buat atau impor notebook, kemudian pilih **Settings → Accelerator → GPU**.

Kedua layanan menyediakan opsi GPU sesuai ketersediaan dan batas pemakaian. Lingkungan cloud biasanya sudah memiliki PyTorch; jalankan pemeriksaan `torch.cuda.is_available()` terlebih dahulu sebelum menginstal ulang paket.
