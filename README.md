# Hands-On 1 — Data Scraping & Eksplorasi Data

Repositori pengumpulan tugas praktikum **Penambangan Data (Data Mining)**
Program Studi Rekayasa Kecerdasan Artifisial — Departemen Teknik Informatika, ITS.

| | |
|---|---|
| **Nama** | Rayyan Muhtar Ali |
| **NRP** | 5054251051 |
| **Materi** | 1 — Data Scraping & Eksplorasi Data (EDA) |
| **Semester** | 3 |

---

## Isi Repositori

| Berkas | Keterangan |
|---|---|
| `1a - Eksplorasi Data.ipynb` | Eksplorasi data: statistik deskriptif, visualisasi distribusi, dan ukuran proximity (lampiran Section 2.3). |
| `1b - Template_Web_Scraping.ipynb` | Web scraping dengan `requests` + Beautiful Soup: parsing HTML, ekstraksi & pembersihan data, penyimpanan ke CSV, serta latihan pada situs `quotes.toscrape.com`. |
| `data/pelanggan_toko_online.csv` | Dataset yang digunakan pada notebook eksplorasi data. |
| `hasil_buku.csv` | Luaran (output) dari notebook scraping — hasil ekstraksi katalog buku. |
| `requirements.txt` | Daftar dependensi Python. |

```
.
├── 1a - Eksplorasi Data.ipynb
├── 1b - Template_Web_Scraping.ipynb
├── data/
│   └── pelanggan_toko_online.csv
├── hasil_buku.csv
├── requirements.txt
└── README.md
```

## Cara Menjalankan

```bash
# 1. Buat dan aktifkan virtual environment
python -m venv .venv
.venv\Scripts\activate        # Windows
# source .venv/bin/activate   # macOS / Linux

# 2. Pasang dependensi
pip install -r requirements.txt

# 3. Jalankan Jupyter
jupyter notebook
```

Kedua notebook membaca berkas dengan **path relatif** (`data/pelanggan_toko_online.csv` dan
`hasil_buku.csv`), sehingga notebook harus dijalankan dari direktori root repositori ini.

> Seluruh sel pada notebook sudah dijalankan, jadi output dapat langsung dilihat lewat
> pratinjau GitHub tanpa perlu menjalankan ulang.

## Catatan Etika

Bagian scraping pada modul ini hanya mengakses HTML contoh yang dibuat sendiri dan
[quotes.toscrape.com](https://quotes.toscrape.com/) — sebuah situs yang memang disediakan
untuk latihan scraping. Permintaan dibatasi dengan `timeout`, `User-Agent` yang jelas, jeda
antar-permintaan, dan pemeriksaan `robots.txt` sesuai pedoman etika pada modul praktikum.
