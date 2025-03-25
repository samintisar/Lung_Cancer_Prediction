# 🧠 Breast Cancer Diagnosis - Machine Learning Project

## 🔍 Overview

This project applies machine learning to predict whether a breast tumor is **malignant** or **benign** using features extracted from digitized images of fine needle aspirate (FNA) of breast masses. The primary objective is to build an accurate and interpretable model that can assist with early detection and reduce the likelihood of misdiagnosis.

---

## 📊 Dataset

- **Source:** [Breast Cancer Dataset on Kaggle](https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset/data)
- **Samples:** 569
- **Target Variable:** `diagnosis` (M = Malignant, B = Benign)
- **Features:** 30 numeric features derived from tumor size, shape, texture, and perimeter.
- **Type:** Supervised binary classification

---

## 🎯 Project Objectives

- Perform Exploratory Data Analysis (EDA) to understand key variables
- Train multiple classification models
- Evaluate performance using metrics beyond accuracy (e.g., F1, recall, specificity)
- Fine-tune the best-performing model using `GridSearchCV`
- Identify most influential features using feature importance from Random Forest

---

## 📚 Features Description

Each tumor is described by 30 numeric features derived from a digitized image of a fine needle aspirate (FNA) of a breast mass. Features are computed for the mean, standard error (SE), and "worst" (largest) value. Here are some key features:

- **radius_mean**: Average distance from the center to points on the perimeter.
- **texture_mean**: Standard deviation of gray-scale values (texture).
- **perimeter_mean**: Length around the tumor boundary.
- **area_mean**: Approximate area of the tumor.
- **smoothness_mean**: Local variation in radius lengths.
- **compactness_mean**: Ratio of perimeter² to area — reflects roundness.
- **concavity_mean**: Severity of concave portions of the contour.
- **concave points_mean**: Number of concave portions.
- **symmetry_mean**: How symmetrical the tumor is.
- **fractal_dimension_mean**: "Roughness" or complexity of the contour.

Each of the above also has a:
- `_se` version: Standard error (e.g., `radius_se`)
- `_worst` version: Largest value recorded (e.g., `radius_worst`)

> Total: 30 features + 1 target (`diagnosis`) + 1 ID column

---

## 🧪 Models Used

| Model                 | Scaled Data? | Used in Comparison |
|----------------------|--------------|--------------------|
| Logistic Regression  | ✅ Yes        | ✅ Yes             |
| Random Forest         | ❌ No         | ✅ Yes (Best)      |
| Support Vector Machine (SVM) | ✅ Yes  | ✅ Yes             |
| K-Nearest Neighbors  | ✅ Yes        | ✅ Yes             |
| Decision Tree        | ❌ No         | ✅ Yes             |

---

## ✅ Final Model Performance (on Test Set)

| Metric      | Score |
|-------------|-------|
| Accuracy    | 0.97  |
| Precision   | 1.00  |
| Recall      | 0.93  |
| Specificity | 1.00  |
| F1-score    | 0.96  |

> Evaluation was performed using unseen test data (20% split), with cross-validation during training to avoid overfitting.

---

## 📊 Top 5 Most Important Features (Random Forest)

1. `concave points_worst`
2. `perimeter_worst`
3. `radius_worst`
4. `concave points_mean`
5. `area_worst`

These features primarily capture shape and boundary irregularities — important indicators of malignancy.

---

## 🧰 Tools & Technologies

- Python (pandas, seaborn, matplotlib)
- scikit-learn  
- statsmodels  
- Jupyter Notebook
