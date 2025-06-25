
# 🫀 Heart Disease Prediction

## 📌 Objective

Build a binary classification model to predict whether an individual is at risk of heart disease based on their medical attributes. This task involves data cleaning, exploratory analysis, model training, and evaluation.

---

## 📂 Dataset

* **Name**: Heart Disease UCI Dataset
* **Source**: [Kaggle - UCI Heart Disease Dataset](https://www.kaggle.com/ronitf/heart-disease-uci)
* **Description**: Contains medical and demographic data of patients, with features like age, cholesterol level, chest pain type, maximum heart rate, etc.

---

## 🛠️ Tasks Performed

* ✅ Cleaned dataset and handled missing values
* ✅ Conducted extensive Exploratory Data Analysis (EDA)
* ✅ Built two classification models: **Logistic Regression** and **Decision Tree**
* ✅ Evaluated models using **Accuracy**, **Confusion Matrix**, and **ROC Curve**
* ✅ Identified important predictive features

---

## 📊 Exploratory Data Analysis (EDA) – Key Findings

### 🔹 1. Heart Disease Presence (Target: `num`)

* Majority of patients show some level of heart disease (num > 0).
* Converted into binary target:

  * `1` → presence of heart disease
  * `0` → no disease

---

### 🔹 2. Correlation Matrix

* **Positively correlated with disease**: `oldpeak`, `exang`
* **Negatively correlated**: `thalch` (max heart rate)
* **Weak predictors**: `chol`, `trestbps`

---

### 🔹 3. Feature Distributions

* *Skewed distributions* in `chol`, `thalch`, and `oldpeak`
* Some features (e.g. `oldpeak`) are *right-skewed*
* Outliers present, especially in `chol`

---

### 🔹 4. Boxplots

* Clear outliers in:

  * `chol` (cholesterol)
  * `oldpeak` (ST depression)
  * `thalch` (heart rate)

---

### 🔹 5. Pairplot Analysis

* Patients with heart disease tend to:

  * Have **higher oldpeak**
  * Have **lower thalch**
  * Show unique patterns in `cp` (chest pain type)

---

### 🔹 6. Chest Pain Type vs Heart Disease

* **Asymptomatic pain** is strongly associated with heart disease.
* **Typical angina** more common among healthy patients.
* `cp` is a strong visual and statistical predictor.

---

## 🤖 Model Training & Evaluation

### 📍 Models Used:

* **Logistic Regression**
* **Decision Tree Classifier**

### 📉 Evaluation Metrics:

* **Accuracy**: 100% for both models
* **ROC-AUC**: 1.0
* **Confusion Matrix**: No false positives or negatives

⚠️ *Note:* These perfect scores suggest **possible overfitting** or **data leakage** due to the small dataset or lack of cross-validation.

---

## 💡 Feature Importance

### Logistic Regression:

* `cp_asymptomatic`
* `oldpeak`
* `thalch`
* `exang`
* `slope_flat`

### Decision Tree:

* `cp_asymptomatic`
* `oldpeak`
* `thalch`
* `ca`
* `slope_flat`, `slope_downsloping`

🧠 **Conclusion**: The most critical predictors are:

* **Chest pain type (cp)**
* **ST depression (oldpeak)**
* **Exercise-induced angina (exang)**
* **Maximum heart rate achieved (thalch)**

