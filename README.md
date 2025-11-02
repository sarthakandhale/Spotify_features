# 🎵 Feature Engineering and Data Preprocessing – Spotify Audio Features Dataset

## 📘 Overview

This project demonstrates **feature engineering** and **data preprocessing** using the **Spotify Audio Features Dataset**.
The goal is to prepare the dataset for **regression and classification modeling** to predict song characteristics such as **popularity, mood, or genre** based on various **audio and metadata features**.

---

## 📂 Dataset Information

* **Dataset Name:** Spotify Audio Features Dataset
* **Source:** [](https://www.kaggle.com/datasets?search=time)
* **Type:** Regression / Classification Problem
* **Target Variable:** `popularity` (integer values between 0–100) or custom target (e.g., `genre`, `mood`)
* **Number of Instances:** 10,000+ tracks (variable)
* **Number of Attributes:** 15+ (audio features + metadata)

### Key Features

| Feature            | Description                                   |
| ------------------ | --------------------------------------------- |
| `danceability`     | How suitable a track is for dancing (0.0–1.0) |
| `energy`           | Intensity and activity of a track             |
| `key`              | Estimated key of the track (0–11)             |
| `loudness`         | Overall loudness in decibels (dB)             |
| `mode`             | Modality (major = 1, minor = 0)               |
| `speechiness`      | Presence of spoken words                      |
| `acousticness`     | Confidence measure of acoustic sound          |
| `instrumentalness` | Likelihood of no vocals                       |
| `liveness`         | Presence of an audience in the recording      |
| `valence`          | Musical positiveness measure (0.0–1.0)        |
| `tempo`            | Beats per minute (BPM)                        |
| `duration_ms`      | Track length in milliseconds                  |
| `popularity`       | Target: Spotify popularity score (0–100)      |

---

## ⚙️ Steps Performed

1. **Data Loading & Exploration**

   * Loaded the dataset from CSV or API.
   * Checked missing values, data types, and summary statistics.
   * Visualized feature distributions and correlations.

2. **Missing Value Handling**

   * Verified and imputed missing numeric values using the **mean** or **median** strategy.

3. **Encoding Categorical Variables**

   * Encoded textual metadata such as `artist_name`, `genre`, and `track_name` using **LabelEncoder** and **OneHotEncoder**.

4. **Feature Scaling**

   * Standardized all numeric features using **StandardScaler** for balanced contribution.

5. **Feature Extraction (PCA)**

   * Applied **Principal Component Analysis (PCA)** to reduce dimensionality while retaining 95% variance.

6. **Feature Selection**

   * Used **SelectKBest (f_regression or chi2)** to identify top predictors of the target variable (e.g., popularity).

7. **Visualization**

   * Correlation heatmap to find feature relationships.
   * Boxplots and scatterplots to identify outliers and feature impact.

---

## 📊 Summary of Transformations

| Step              | Technique                    | Impact                             |
| ----------------- | ---------------------------- | ---------------------------------- |
| Missing Data      | Mean / Median Imputation     | Clean dataset without NaN values   |
| Encoding          | LabelEncoder / OneHotEncoder | Converted text to numeric values   |
| Scaling           | StandardScaler               | Standardized feature magnitudes    |
| PCA               | 2–3 Components               | Reduced dimensionality             |
| Feature Selection | SelectKBest                  | Identified top predictive features |
| Visualization     | Heatmap / Pairplot           | Improved data understanding        |

**Top Features Identified:**
`danceability`, `energy`, `valence`, `loudness`, `tempo`, `acousticness`

---

## 🧠 Observations

* Tracks with **high danceability** and **energy** tend to be more popular.
* **Valence** (positiveness) and **tempo** strongly influence listener preference.
* PCA reduced redundancy and helped visualize clusters by genre or mood.
* Dataset is now standardized and suitable for regression/classification models.

---

## ⚖️ Ethical Considerations

Even though Spotify data is public, it’s essential to:

* Follow **Spotify API usage policies** and rate limits.
* Ensure **no bias** in predicting popularity or genre based on incomplete metadata.
* Keep preprocessing steps transparent and reproducible.

---

## 🧩 Tools and Libraries Used

* Python 3
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn (PCA, StandardScaler, SelectKBest)
* Spotipy (Spotify API Client)

---

## 📁 Files in Repository

| File Name                           | Description                                                 |
| ----------------------------------- | ----------------------------------------------------------- |
| `Feature_Engineering_Spotify.ipynb` | Main Jupyter Notebook with preprocessing & feature analysis |
| `Spotify_Feature_Report.pdf`        | 1–2 page summary of feature engineering results             |
| `README.md`                         | Documentation and ethical considerations                    |

---

## 👨‍💻 How to Run

Run this notebook directly in Google Colab:
👉 [Open in Colab](https://colab.research.google.com/drive/1jqRrb_DQ2vq_z58XAfII_OOSfAcuIUXE)

---

## 🧑‍🎓 Author

**Name:** Andhale Sarthak Adinath
**Course:** Artificial Intelligence
**Instructor:** Mrs. ANITA SHINGADE
**Date:** 2 November 2025
