# Algerian Forest Fire Predictor

Proyek ini adalah aplikasi berbasis web yang memprediksi **Fire Weather Index (FWI)** berdasarkan data meteorologi menggunakan teknik *Machine Learning*. Proyek ini dibangun dengan **Flask** sebagai kerangka kerja web dan menggunakan algoritma **Ridge Regression** untuk prediksi.

## 📌 Deskripsi Proyek

Aplikasi ini bertujuan untuk membantu memprediksi risiko cuaca kebakaran hutan di wilayah Aljazair. Model dilatih menggunakan dataset **Algerian Forest Fires**, yang mencakup data cuaca dari dua wilayah: Bejaia (timur laut) dan Sidi Bel-abbes (barat laut).

Sistem melakukan langkah-langkah berikut:
1.  Menerima input parameter cuaca dari pengguna melalui antarmuka web.
2.  Memproses data menggunakan *scaler* yang telah dilatih sebelumnya.
3.  Memprediksi nilai **FWI** (Fire Weather Index) menggunakan model Regresi Ridge.

## 📂 Dataset

Dataset yang digunakan dalam proyek ini adalah `Algerian_forest_fires_cleaned_dataset.csv`. Dataset ini telah melalui proses pembersihan (*cleaning*) dan *Feature Engineering* (FE) yang mencakup:
* Pembersihan data (menangani nilai kosong, *header* ganda).
* Konversi tipe data.
* Encoding fitur kategorikal (`Classes` dan `Region`).
* Analisis Korelasi untuk seleksi fitur.

## 🛠 Teknologi yang Digunakan

* **Python 3.x**: Bahasa pemrograman utama.
* **Flask**: Framework web untuk membuat API dan antarmuka pengguna.
* **Scikit-Learn**: Untuk pembuatan model (Ridge Regression) dan *preprocessing* data (StandardScaler).
* **Pandas & NumPy**: Untuk manipulasi dan analisis data.
* **Matplotlib & Seaborn**: Untuk visualisasi data selama tahap analisis (EDA).
* **Pickle**: Untuk menyimpan dan memuat model yang telah dilatih.

## 📁 Struktur Proyek

```bash
├── application.py          # File utama aplikasi Flask (Entry point)
├── requirement.txt         # Daftar dependensi library Python
├── models/                 # Folder penyimpanan model ML
│   ├── ridge.pkl           # Model Ridge Regression yang sudah dilatih
│   └── scaler.pkl          # Standard Scaler untuk normalisasi data
├── templates/              # Template HTML untuk antarmuka web
│   ├── index.html          # Halaman utama
│   └── home.html           # Halaman prediksi
├── Notebook/               # Jupyter Notebooks untuk eksperimen
│   ├── 2.0-EDA And FE...   # Exploratory Data Analysis & Feature Engineering
│   ├── 3.0-Model Training..# Proses pelatihan dan evaluasi model
│   └── Algerian_forest...  # File dataset CSV
└── .ebextensions/          # Konfigurasi untuk deployment (AWS Elastic Beanstalk)


## 🚀 Cara Instalasi dan Menjalankan

Ikuti langkah-langkah berikut untuk menjalankan proyek ini di komputer lokal Anda:

1. **Clone Repositori**
```bash
git clone [https://github.com/username-anda/nama-repo-anda.git](https://github.com/username-anda/nama-repo-anda.git)
cd nama-repo-anda

```


2. **Buat Virtual Environment (Opsional tapi Disarankan)**
```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate

```


3. **Install Dependensi**
Pastikan Anda berada di direktori yang sama dengan `requirement.txt`.
```bash
pip install -r requirement.txt

```


4. **Jalankan Aplikasi**
```bash
python application.py

```


5. **Akses Aplikasi**
Buka browser dan kunjungi alamat lokal yang muncul di terminal, biasanya:
`http://127.0.0.1:5000/`

## 📊 Fitur Input

Aplikasi memprediksi FWI berdasarkan parameter input berikut:

* **Temperature**: Suhu dalam derajat Celsius.
* **RH (Relative Humidity)**: Kelembaban relatif (%).
* **Ws (Wind Speed)**: Kecepatan angin (km/h).
* **Rain**: Curah hujan (mm).
* **FFMC (Fine Fuel Moisture Code)**.
* **DMC (Duff Moisture Code)**.
* **ISI (Initial Spread Index)**.
* **Classes**: Klasifikasi awal (Fire/Not Fire).
* **Region**: Kode wilayah (0 untuk Bejaia, 1 untuk Sidi Bel-abbes).

## 📈 Pengembangan Model

Proses pengembangan model didokumentasikan dalam folder `Notebook/`:

1. **EDA (Exploratory Data Analysis)**: Memahami distribusi data, mendeteksi *outlier*, dan melihat korelasi antar fitur.
2. **Preprocessing**: Membersihkan data dan melakukan *train-test split*.
3. **Model Training**: Melatih model Regresi Linear, Lasso, Ridge, dan ElasticNet. Model **Ridge** dipilih karena performanya yang optimal.

## 🤝 Kontribusi

Kontribusi selalu diterima! Silakan buat *Pull Request* atau buka *Issue* jika Anda menemukan *bug* atau memiliki saran perbaikan.


**Dibuat oleh Farhan kamil hermansyah - 152024150**
'''

```

```
