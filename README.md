# 🌊 Hybridization of SVM-Based Undersampling dan Safe-Level SMOTE untuk Peningkatan Klasifikasi pada Dataset Gelombang Oseanografi yang Tidak Seimbang

Kelompok 05

## 👥 Anggota Kelompok

| NIM | Nama |
| --- | --- |
| 123140074 | Mekar Cendra Narwastu |
| 123140076 | Mei Disti Ayuningtias |
| 123140103 | Ribka Hana Josephine Situmorang |
| 123140111 | Abel Fortino |
| 123140116 | Diwan Ramadhani Dwi Putra |
| 123140120 | M. Zahran Dhiyaul Haq |

---

## 📌 Deskripsi Project

Project ini bertujuan untuk menguji keandalan metode **Hybrid Oversampling and Undersampling Method (HOUM)** guna mengatasi masalah ketidakseimbangan kelas (*imbalanced dataset*) yang signifikan pada data oseanografi gelombang laut di Indonesia serta data curah hujan di Australia.

Empat pendekatan penanganan data tidak seimbang dibandingkan dalam studi ini:

| Metode | Deskripsi |
| :--- | :--- |
| **Baseline** | Penggunaan dataset asli tanpa menerapkan teknik penanganan imbalanced. |
| **Random Undersampling (RUS)** | Pengurangan jumlah sampel kelas mayoritas secara acak hingga seimbang. |
| **NearMiss-1** | Teknik undersampling selektif berbasis jarak keputusan terdekat (*distance-based*). |
| **HOUM** | Metode hibrida adaptif yang mengintegrasikan *SVM-Based Undersampling* dengan *Safe-Level SMOTE*. |

Model yang digunakan: **Random Forest Classifier**

---

## 📂 Struktur Folder

```text
Daming_Oseanografi/
├── data/
│   ├── Gelombang (1).xlsx
│   ├── Gelombang (2).xlsx
│   ├── Gelombang (3).xlsx
│   ├── Gelombang (4).xlsx
│   ├── Gelombang (5).xlsx
│   ├── Gelombang (6).xlsx
│   └── weatherAUS.csv
├── docs/
│   ├── Logbook Penambangan Data.pdf
│   ├── Tubes_DM_Kelompok5_Imbalanced.pdf
│   └── Tubes_DM_Kelompok8_HOUM_Final.pdf
├── kelompok5_houm_imbalanced.ipynb
└── README.md
```
---

## 📊 Dataset

### 1. Dataset Gelombang Laut Indonesia
* **Sumber:** Data observasi stasiun pengukuran gelombang di 6 lokasi perairan Indonesia.
* **File:** Terdiri dari 6 file Excel (`data/Gelombang (1).xlsx` s.d. `data/Gelombang (6).xlsx`).
* **Jumlah baris:** 61.230 Baris.
* **Target:** `Hsig(Scale)` (*Smooth*, *Slight*, *Moderate*) dengan rasio ketimpangan ekstrem mencapai ~13:1.

### 2. Dataset Rain in Australia
* **Sumber:** [Kaggle - Weather Dataset Rattle Package](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package)
* **File:** `data/weatherAUS.csv`.
* **Jumlah baris:** 145.460 Baris.
* **Target:** `RainClass` (*No Rain*, *Light Rain*, *Heavy Rain*) dengan rasio ketimpangan ~9,82:1.

---

## 📈 Metrik Evaluasi

Guna menghindari bias estimasi akibat *accuracy paradox*, performa model dievaluasi menggunakan metrik yang representatif untuk data tidak seimbang:
* **Accuracy, Precision (macro), Recall (macro), F1-Score (macro), G-Mean,** dan **AUC-ROC**.
* **Confusion Matrix** untuk memetakan performa klasifikasi tiap skenario resampling.
* **Visualisasi Perbandingan** metrik evaluasi antarmetode dalam bentuk grafik batang guna mempermudah analisis performa.

---
