# Deliverable 1: Data Collection, Cleaning, and Exploration

## 📊 Dataset Summary

This project uses a modified version of the UCI Heart Disease dataset. The dataset consists of **1,035 records** with **14 attributes** including age, sex, chest pain type, cholesterol, and other health-related features. The target variable `target` indicates the presence or absence of heart disease (1 = disease, 0 = no disease).

---

## 🧹 Data Cleaning Steps

### 1. Handling Missing Values
- Introduced missing values were found in `chol`, `thalach`, and `oldpeak`.
- Filled them using **median imputation** to avoid data loss and maintain the distribution.

### 2. Removing Duplicates
- Identified and removed duplicate rows using `df.drop_duplicates()` to ensure uniqueness and avoid data bias.

### 3. Addressing Noisy Data (Outliers)
- Unrealistically high values like `chol = 1000` and `trestbps = 300` were identified.
- Applied the **IQR method** to cap outliers in columns like `chol`, `trestbps`, `thalach`, and `oldpeak`.

---

## 📈 Exploratory Data Analysis (EDA)

### Feature Distributions
- Most features follow expected distributions.
- Binary features like `sex`, `fbs`, and `exang` are clearly distinguishable.

### Correlation Heatmap
- Positive correlation between `cp` and `target`
- Negative correlation between `thalach`, `oldpeak`, and `target`
- These features will be key in modeling stages.

### Boxplots
- Confirmed outliers were effectively capped and distributions are now controlled.

---

## 💡 Key Insights

- Data is clean, complete, and ready for modeling.
- Key predictive features identified: `cp`, `thalach`, `oldpeak`, `exang`.
- Dataset supports multiple modeling types (regression, classification, clustering).

---

## ⚙️ Challenges Encountered

- Simulating realistic issues like missing values, duplicates, and noise
- Understanding and applying correct methods (IQR, imputation) to handle them

---

✅ Dataset is now fully preprocessed and EDA is complete — ready for Deliverable 2 (Regression Modeling).
