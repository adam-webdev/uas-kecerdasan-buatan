# Analisis Kritis & Peningkatan Akurasi Prediksi Harga Rumah Jakarta Selatan 

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Sklearn](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-green)

Proyek ini merupakan tugas **UAS Kecerdasan Buatan** yang bertujuan untuk membedah jurnal nasional, mereplikasi modelnya, dan melakukan *improvement* (peningkatan) akurasi menggunakan algoritma Machine Learning yang lebih modern.

---

##  Link Penting
- **Video Presentasi (YouTube):** [Tonton di sini](https://youtu.be/R5I2QS6wO-E) 
- **Source Code (Google Colab):** [Buka Notebook](https://colab.research.google.com/drive/1EH6nPzQm-Bfg8qIrv4oU7N7IEJTCh4Kn#scrollTo=_CUR5BkwQTJp) 

---

##  Identitas Jurnal Referensi
Proyek ini mengacu pada jurnal berikut sebagai *baseline*:
* **Judul:** Analisis Prediksi Harga Rumah Sesuai Spesifikasi Menggunakan Multiple Linear Regression
* **Metode:** Multiple Linear Regression (MLR)
* **Hasil Akurasi (R2) di Jurnal:** 66%
* **Kasus Studi:** Prediksi harga rumah di Jakarta Selatan dengan spesifikasi tertentu.

---

##  Metodologi & Peningkatan (Improvement)

Dalam proyek ini, dilakukan dua tahap eksperimen:

### 1. Replikasi (Baseline)
Mencoba meniru hasil jurnal menggunakan metode yang sama (**Multiple Linear Regression**) dan dataset yang sama untuk memvalidasi klaim akurasi jurnal.

### 2. Improvement (Usulan Baru) 
Melakukan serangkaian teknik Data Science untuk meningkatkan akurasi model di atas 66%:
* **Data Cleaning Lanjutan:** Menggunakan metode **IQR (Interquartile Range)** untuk membuang *outliers* (data harga ekstrem) yang mengganggu model.
* **Feature Engineering:** Menambahkan fitur logaritma pada target harga (`Log Transformation`) untuk menstabilkan variansi data harga properti yang sangat lebar.
* **Algoritma Canggih:** Mengganti Linear Regression dengan **XGBoost (Extreme Gradient Boosting)** dan **Random Forest** yang lebih tangguh terhadap data non-linear.

---

##  Hasil Komparasi

Berikut adalah perbandingan performa antara metode Jurnal (Linear Regression) dengan metode Improvement (XGBoost) yang telah dikembangkan:

| Metrik Evaluasi | Jurnal (Linear Regression) | Improvement (XGBoost)  |
| :--- | :---: | :---: |
| **Akurasi (R2 Score)** | **66.40%** | **~70.25%** |
| **Handling Data** | Raw Data | Log Transform + Outlier Removal |
| **Prediksi Studi Kasus*** | Rp 18,9 Milyar | **Rp 15,6 Milyar** |

> *) Studi Kasus: Rumah LT 500m², LB 625m², Jaksel. Rata-rata harga pasar untuk spesifikasi ini adalah ~Rp 15,2 Milyar. Prediksi Improvement jauh lebih realistis mendekati harga pasar dibandingkan model Jurnal (Rp 19,4 M).

---

##  Struktur Dataset
Dataset yang digunakan adalah `HARGA RUMAH JAKSEL.xlsx` yang berisi 1001 data rumah dengan fitur:
1.  **HARGA:** Harga rumah (Target).
2.  **LT:** Luas Tanah ($m^2$).
3.  **LB:** Luas Bangunan ($m^2$).
4.  **JKT:** Jumlah Kamar Tidur.
5.  **JKM:** Jumlah Kamar Mandi.
6.  **GRS:** Garasi (Ada/Tidak).

---

##  Cara Menjalankan Project

1.  Buka link Google Colab di atas.
2.  Pastikan file dataset `HARGA RUMAH JAKSEL.xlsx` sudah diupload ke sesi Colab atau ditarik dari GitHub.
3.  Jalankan setiap sel kode dari atas ke bawah (Runtime -> Run all).
4.  Hasil perbandingan akurasi dan grafik akan muncul di bagian bawah notebook.

---

##  Author
**ADAM DWI MAULANA**
*NIM: 312210242*
*Kelas/Kelompok: TI.22.S.E.B1 - KELOMPOK 6*

---
*Dibuat untuk memenuhi tugas UAS Mata Kuliah Kecerdasan Buatan.*
