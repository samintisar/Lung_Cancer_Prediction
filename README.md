# Breast Cancer Diagnosis Using Machine Learning

This project uses the Breast Cancer Wisconsin (Diagnostic) dataset to predict whether a tumor is malignant or benign based on various features such as radius, texture, smoothness, and concavity.

## 🧠 Objectives
- Clean and explore the dataset
- Build and evaluate multiple classification models
- Fine-tune hyperparameters using GridSearchCV
- Compare models based on evaluation metrics

## 🔍 Dataset Information
- 30 features related to tumor characteristics (mean, worst, standard error)
- Target variable: Diagnosis (`M = Malignant`, `B = Benign`)
- Total samples: ~570

## 🔧 Tools Used
- Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- Jupyter Notebook
- VS Code

## 📈 Models Implemented
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Decision Tree Classifier
- Random Forest Classifier

## 📊 Evaluation Metrics
- Accuracy, Precision, Recall, F1-Score
- Confusion Matrix
- ROC Curve and AUC Score

## 🚀 Future Work
- Add ensemble methods (e.g., XGBoost)
- Deploy with a simple Streamlit web app
- Add SHAP for model explainability

## 📜 License
This project is for educational purposes only. Dataset is publicly available via UCI Machine Learning Repository.
