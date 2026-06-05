# Analisis Data Penjualan

## Deskripsi Proyek

Proyek ini bertujuan untuk melakukan analisis data penjualan menggunakan Python. Analisis dilakukan untuk memahami tren penjualan, perilaku pelanggan, pengaruh anggaran iklan terhadap penjualan, serta performa produk.

Dataset dianalisis menggunakan beberapa teknik data analysis seperti:

* Data Wrangling
* Visualisasi Data
* Analisis RFM
* Regresi Linear

---

# Business Question

Penelitian ini dilakukan untuk menjawab beberapa pertanyaan bisnis berikut:

1. Bagaimana tren penjualan produk pada setiap bulan?
2. Apakah anggaran iklan (Advertising Budget) berpengaruh terhadap total penjualan?
3. Produk kategori apa yang memiliki performa penjualan terbaik dan terendah?
4. Siapa pelanggan terbaik berdasarkan analisis RFM (Recency, Frequency, Monetary)?

---

# Tools dan Library

Proyek ini menggunakan beberapa library Python berikut:

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import datetime as dt
from sklearn.linear_model import LinearRegression
```

---

# Data Wrangling

Tahap data wrangling dilakukan sebelum proses analisis data.

## 1. Membaca Dataset

```python
df = pd.read_csv(nama_file)
```

## 2. Konversi Format Tanggal

```python
df['Order_Date'] = pd.to_datetime(df['Order_Date'])
```

## 3. Menghitung Total Penjualan

```python
df['Total_Sales'] = df['Quantity'] * df['Price_Per_Unit']
```

## 4. Membuat Kolom Bulan

```python
df['Month'] = df['Order_Date'].dt.to_period('M').astype(str)
```

---

# Visualisasi dan Analisis Data

## 1. Tren Penjualan Bulanan

Analisis dilakukan menggunakan line chart untuk melihat perubahan total penjualan setiap bulan.

### Insight

* Penjualan mengalami fluktuasi setiap bulan.
* Beberapa bulan menunjukkan peningkatan penjualan yang cukup signifikan.
* Faktor promosi dan musim penjualan kemungkinan mempengaruhi hasil penjualan.

---

## 2. Analisis Produk

Visualisasi scatter plot digunakan untuk melihat hubungan antara harga produk dan jumlah produk terjual.

### Insight

* Produk dengan harga lebih rendah cenderung memiliki jumlah penjualan lebih tinggi.
* Beberapa kategori produk memiliki performa lebih baik dibanding kategori lainnya.

---

## 3. Analisis RFM

Analisis RFM digunakan untuk mengelompokkan pelanggan berdasarkan:

* Recency
* Frequency
* Monetary

### Insight

* Pelanggan dengan frequency dan monetary tinggi merupakan pelanggan loyal.
* Pelanggan aktif memiliki potensi memberikan kontribusi besar terhadap pendapatan perusahaan.

---

## 4. Regresi Linear

Analisis regresi linear digunakan untuk mengetahui hubungan antara anggaran iklan dan total penjualan.

### Insight

* Anggaran iklan memiliki pengaruh positif terhadap penjualan.
* Semakin besar anggaran iklan, penjualan cenderung meningkat.

---

# Recommendation

Berdasarkan hasil analisis data, berikut beberapa rekomendasi yang dapat diterapkan perusahaan:

1. Mempertahankan pelanggan loyal melalui program membership atau reward.
2. Mengoptimalkan strategi pemasaran dan anggaran iklan.
3. Mengevaluasi produk dengan performa penjualan rendah.
4. Memanfaatkan tren penjualan bulanan untuk strategi stok dan promosi.

---

# Kesimpulan

Berdasarkan hasil analisis data penjualan, dapat disimpulkan bahwa tren penjualan mengalami perubahan pada setiap bulan dan anggaran iklan memiliki pengaruh terhadap peningkatan penjualan.

Analisis RFM menunjukkan adanya pelanggan loyal yang memberikan kontribusi besar terhadap perusahaan. Oleh karena itu, perusahaan dapat memanfaatkan hasil analisis data ini untuk membantu pengambilan keputusan bisnis yang lebih efektif.

---

# Cara Menjalankan Project

1. Upload dataset CSV ke Google Colab atau Jupyter Notebook.
2. Install library yang dibutuhkan.
3. Jalankan seluruh kode Python.
4. Visualisasi dan hasil analisis akan tampil otomatis.

---

# Author

Nama: Aryadani Santoso
