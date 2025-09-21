# World Happiness Report Analysis (2020–2024)

## Deskripsi

Project ini merupakan bagian dari **Capstone Project - Data Classification & Summarization**.  
Dataset yang digunakan adalah **World Happiness Report (2020–2024)** yang mencakup 156 negara,  
dengan berbagai indikator sosial dan ekonomi yang berhubungan dengan tingkat kebahagiaan.

Fokus analisis:

1. **Klasifikasi** negara berdasarkan tingkat kebahagiaan (`Low`, `Medium`, `High`).
2. **Identifikasi faktor utama** yang memengaruhi kebahagiaan.
3. **Summarization otomatis** menggunakan **IBM Granite (via Replicate)**.
4. **Insight & rekomendasi kebijakan** berbasis data.

---

## Struktur Project

```
world-happiness-analysis/
│
├── pone.0322287.s001.xlsx      # Dataset utama (2020–2024)
├── notebook.ipynb              # Notebook utama analisis
├── README.md                   # Dokumentasi project
└── requirements.txt            # Library Python yang digunakan
```

---

## Teknologi yang Digunakan

- **Python 3.12**
- **Pandas, Numpy** : Data wrangling
- **Matplotlib, Seaborn, Plotly** : Visualisasi data
- **Scikit-learn** : Preprocessing & Modeling (Random Forest)
- **Replicate API + LangChain** : Summarization dengan **IBM Granite**

---

## Proses Analisis

1. **Load Dataset**

   - Dataset 2020–2024 terdiri dari 5 sheet berbeda : dinormalisasi menjadi 1 dataframe.
   - Variabel utama: _Happiness Score_, _GDP per capita_, _Social support_, _Health expectancy_, dll.

2. **EDA (Exploratory Data Analysis)**

   - Distribusi _Happiness Score_ per tahun.
   - Top 5 & Bottom 5 negara per tahun.
   - Korelasi antar variabel (heatmap).

3. **Preprocessing**

   - Imputasi missing values.
   - Scaling (StandardScaler).
   - Pembuatan label `happiness_level` (`Low`, `Medium`, `High`).

4. **Modeling (Random Forest)**

   - Train-test split 80:20.
   - Evaluasi dengan classification report & confusion matrix.
   - Feature importance untuk identifikasi faktor utama.
   - 5-Fold Cross Validation untuk validasi stabilitas model.

5. **Summarization dengan IBM Granite**
   - Insight otomatis berdasarkan feature importance & tren global.
   - Menghasilkan narasi faktor dominan, tren 2020–2024, serta rekomendasi kebijakan.

---

## Hasil Utama

- **Faktor utama kebahagiaan**:

  1. GDP per Capita
  2. Social Support (Family)
  3. Health (Life Expectancy)
  4. Freedom
  5. Trust (Government Corruption)
  6. Generosity

- **Tren global**:

  - 2020–2021 : penurunan skor akibat pandemi COVID-19.
  - 2022–2024 : mulai rebound, terutama di negara maju.
  - Negara Nordik konsisten menduduki posisi tertinggi.

- **Kinerja model Random Forest**:
  - F1-score rata-rata cross-validation: **0.81** (stabil antar fold).
  - Medium class paling akurat, Low vs Medium kadang tertukar.

---

## Rekomendasi Kebijakan

1. **Ekonomi Berkelanjutan** : dorong pertumbuhan GDP berbasis inovasi & inklusi.
2. **Kesehatan Publik** : perkuat layanan preventif & akses kesehatan merata.
3. **Dukungan Sosial** : kebijakan jaminan sosial & program berbasis keluarga.
4. **Transparansi Pemerintah** : perangi korupsi & tingkatkan trust publik.
5. **Solidaritas Sosial** : kampanye nasional kepedulian & filantropi.

---

## Cara Menjalankan Project

1. Clone repository ini:

   ```bash
   git clone https://github.com/NurAlif125/IBM-world-happiness-analysis
   cd world-happiness-analysis
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Jalankan notebook:

   ```bash
   jupyter notebook notebook.ipynb
   ```

4. (Opsional) Set API Key Replicate:
   ```bash
   export REPLICATE_API_TOKEN=your_api_token_here
   ```

---

## Catatan

- Dataset asli berasal dari **World Happiness Report (2020–2024)**.
- Summarization menggunakan **IBM Granite 3.3 8B Instruct** via **Replicate API**.
- Notebook ini dapat digunakan untuk eksplorasi ulang dengan model lain (SVM, Logistic Regression, dsb).

---

## Author

- **Nama:** Muhammad Nur Alif Ramadhan
- **Capstone Project** — Data Classification & Summarization
- **Tahun:** 2025
=======
# IBM-world-happiness-analysis
>>>>>>> 9e7f241312c9a6b188c2408c2582ba63220bf42e
