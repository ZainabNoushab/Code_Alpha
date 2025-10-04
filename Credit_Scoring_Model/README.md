# 💳 Credit Scoring Model using Machine Learning

A data-driven Credit Scoring Model built to evaluate customer creditworthiness using machine learning algorithms.  
This project leverages **Logistic Regression**, **Decision Tree**, and **Random Forest** classifiers to predict a customer’s credit score category (Poor, Standard, Good) based on their financial behavior and demographic details.

---

## 📘 Project Overview

Financial institutions often face challenges in accurately assessing a customer's risk profile.  
This project provides an end-to-end **machine learning pipeline** that cleans, transforms, and models financial data to predict credit scores — helping automate credit decision processes.

---

## 🧩 Features

- End-to-end workflow: from data loading to model evaluation  
- Comprehensive data cleaning and preprocessing  
- Feature engineering for improved model accuracy  
- Comparison of three ML models  
- Hyperparameter tuning using `RandomizedSearchCV`  
- Visual insights via EDA and correlation analysis  

---

## ⚙️ Tech Stack

- **Language:** Python  
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn  
- **Environment:** Jupyter Notebook / Google Colab  

---

## 🧹 Data Preprocessing

- Removed irrelevant columns (`ID`, `Customer_ID`, etc.)  
- Cleaned and converted mixed-type numeric columns  
- Handled missing values using median and mode imputation  
- Encoded categorical features via one-hot encoding  
- Engineered new features:
  - `Total_Number_of_Accounts` = Num_Bank_Accounts + Num_Credit_Card  
  - `Payment_to_Income_Ratio` = Total_EMI_per_month / Monthly_Inhand_Salary  

---

## 🔍 Exploratory Data Analysis (EDA)

Key insights visualized using `matplotlib` and `seaborn`:
- Distribution of credit score categories  
- Relationship between annual income and credit score  
- Correlation heatmap of all numerical features  

---

## 🧠 Models Used

| Model | Accuracy | Notes |
|--------|-----------|-------|
| Logistic Regression | ~Baseline | Interpretable, sets initial benchmark |
| Decision Tree | Higher than Logistic | Captures non-linear relations |
| Random Forest | **Best Performing** | Achieved highest accuracy and balanced classification |
| Tuned Random Forest | **Optimized via RandomizedSearchCV** | Further improved results and reduced overfitting |

---

## 🧪 Evaluation Metrics

- Accuracy Score  
- Confusion Matrix  
- Classification Report (Precision, Recall, F1-Score)  
- ROC-AUC (optional extension)  

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/<ZainabNoushab>/Credit-Scoring-Model.git
   cd Credit-Scoring-Model
   ```
2. Run the notebook or script:
   ```bash
   python credit_scoring_model.py
   ```

---

## 📊 Results Summary

Random Forest Classifier outperformed other models in accuracy and stability.

Feature engineering and standardization significantly improved model robustness.

Hyperparameter tuning with RandomizedSearchCV led to optimal performance.

---

## 🎯 Future Enhancements

Implement deep learning alternatives (e.g., MLP Classifier)

Integrate SHAP or LIME for model explainability

Deploy via Streamlit or Flask for real-time credit scoring

---

## 🧑‍💻 Author

Zainab Noushab
Data Analyst | Machine Learning Enthusiast

---
| "Turning data into credit insights — one model at a time."
