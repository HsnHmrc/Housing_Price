# 🏡 Housing Price Prediction

This project aims to predict **house prices** using **feature engineering, encoding techniques, and machine learning models**. The dataset is from the **Kaggle Housing Price Competition**, and the objective is to develop a high-performing model to estimate property prices based on various features.

---

## 📂 Dataset Overview

The dataset consists of:  
- `tr.csv` → Training dataset (includes `SalePrice`)  
- `ts.csv` → Test dataset (without `SalePrice`, to be predicted)  

During the **exploratory data analysis (EDA)**:
- Examined **data types**, **missing values**, and **unique values** for each column.
- Removed **irrelevant** or **highly missing** columns.
- Retained **columns that could be derived from other features** while dropping redundant ones.

---

## 📌 Data Preprocessing & Feature Engineering

### 🔹 Handling Missing Values
- **Numerical Features:** Filled using `RandomForestRegressor`.  
- **Categorical Features:**  
  - Initially replaced missing values with `-999`.  
  - Applied **Ordinal Encoding** for naturally ordered categories.  
  - Used **One-Hot Encoding** for unordered categorical features.  
  - Converted `-999` back to `NaN` and imputed missing values using `RandomForestRegressor`.

### 🔹 Encoding the Test Dataset
- Ensured the **same encoding transformations** were applied to the test set.  
- Synchronized features for consistency between training and test sets.  

---

## 🚀 Model Training & Evaluation

### 🔹 Model Used: `XGBRegressor`
- **Defined independent (`X`) and dependent (`y`) variables**.
- **Trained the model** using `XGBRegressor` and made predictions.

### 🔹 Model Performance
- **MAE Score:** `16888.90`  
- **Average Sale Price:** `180,921.20`  
- **Average Sale Price / MAE Ratio:** `10.71`

This is the **first version** of my model, and I plan to refine it further.

---

## 🔍 Future Improvements

- **Compare multiple models** (e.g., `LightGBM`, `CatBoost`, `Stacking Regressors`) to find the best performer.  
- **Optimize hyperparameters** to enhance model accuracy.  
- **Feature Engineering Enhancements** to improve predictive power.  

I am confident that I will achieve even **better results** as I continue to develop my skills. Future model comparisons and optimizations will be added to this repository.
