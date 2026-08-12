# Prediksi Nilai Indeks Standar Pencemar Udara (ISPU) DKI Jakarta Menggunakan Algoritma XGBoost

Laporan Proyek Data Science — Kelompok 4  
Program Studi Teknik Informatika  
Fakultas Teknologi Informatika  
Universitas Bale Bandung  
2026

## 👥 Anggota Kelompok
| Nama | NIM |
|---|---|
| Atsaal Najwan | 301240012 |
| Muhammad Fajar Ramadhan | 301240036 |
| Najib Fadhil Akbar | 301240019 |

## 📌 Deskripsi Proyek
Proyek ini bertujuan untuk memprediksi nilai **Indeks Standar Pencemar Udara (ISPU)** di DKI Jakarta menggunakan algoritma **XGBoost (Extreme Gradient Boosting) Regressor**. Analisis dilakukan menggunakan metode **CRISP-DM**, mulai dari *business understanding*, *data understanding*, *data preprocessing*, *exploratory data analysis (EDA)*, *modeling*, hingga *evaluation*.

## 📊 Dataset
Dataset yang digunakan adalah data historis kualitas udara DKI Jakarta (`ispu_dki_all.csv`) yang memuat hasil pemantauan konsentrasi polutan harian dari beberapa stasiun pemantauan, dengan rincian:
- **5.538 baris data**
- **11 kolom fitur**: tanggal, stasiun, pm25, pm10, so2, co, o3, no2, max, critical, categori

Target prediksi adalah kolom `max`, yaitu nilai indeks pencemar tertinggi dari seluruh parameter yang diukur pada hari tersebut.

## 🛠️ Tools & Library
- Google Colab, Python
- Pandas, NumPy, Matplotlib, Seaborn
- Scikit-learn, XGBoost

## 🔍 Alur Analisis (CRISP-DM)
1. **Business Understanding** — merumuskan masalah prediksi kualitas udara
2. **Data Understanding** — eksplorasi struktur, informasi, dan permasalahan data
3. **Data Preprocessing** — penanganan missing value, deteksi outlier, encoding data kategorikal, feature engineering (ekstraksi tahun & bulan)
4. **Exploratory Data Analysis (EDA)** — statistik deskriptif dan insight data
5. **Modeling** — training model XGBoost Regressor
6. **Evaluation** — evaluasi performa model menggunakan MAE, MSE, RMSE, dan R²

## 📈 Hasil Model
| Metrik | Nilai |
|---|---|
| MAE | 1,2281 |
| MSE | 4,4082 |
| RMSE | 2,0996 |
| R² | 0,9975 |

Model XGBoost Regressor berhasil menjelaskan **99,75% variasi data**, jauh lebih unggul dibandingkan model Regresi Linear pada laporan sebelumnya (R² = 0,7759).

### Feature Importance
| Fitur | Importance |
|---|---|
| o3 | 0,6797 |
| pm25 | 0,1322 |
| tahun | 0,0688 |
| pm10 | 0,0648 |
| bulan | 0,0174 |
| no2 | 0,0148 |
| so2 | 0,0138 |
| co | 0,0085 |

Fitur **O3 (ozon)** dan **PM2.5** merupakan faktor paling berpengaruh terhadap nilai ISPU harian.

## ✅ Kesimpulan
Algoritma XGBoost Regressor sangat efektif digunakan untuk memprediksi nilai ISPU di DKI Jakarta, mampu menangani missing value secara otomatis tanpa perlu imputasi maupun feature scaling, serta memberikan performa yang jauh lebih akurat dibandingkan model Regresi Linear.

## 📎 Link Google Colab
[Buka Notebook di Google Colab](https://colab.research.google.com/drive/1PcPNLbg0FsTMtrUCVI6gcMT0QK4YzysY?usp=sharing)
