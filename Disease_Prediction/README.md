# Heart Disease Prediction using Machine Learning
## Overview

This project predicts the likelihood of heart disease using medical diagnostic data.
By comparing multiple machine learning models, we determine which algorithm performs best in classifying patients as healthy (0) or heart disease (1).

## Objective

To develop and evaluate machine learning models for early heart disease detection, helping doctors and patients make proactive health decisions.

## Dataset

**Source:** UCI Heart Disease Dataset

**Records:** 297

**Features:** 13 medical attributes (e.g., age, cholesterol, thalach, etc.)

**Target:** condition (0 = healthy, 1 = heart disease)

## Steps & Workflow

- Data Preprocessing

- Handled missing values

- Standardized numerical features

- Encoded categorical variables

- Modeling

Algorithms used:
- Logistic Regression

- Support Vector Machine

- Random Forest
  
- XGBoost

Evaluation Metrics:

- Accuracy, Precision, Recall, F1-Score, ROC-AUC

Result

- Best Model: Random Forest

- Accuracy: 73.3%

- ROC-AUC: 0.85

Key Insights

The most important features were:

- thalach — Maximum heart rate achieved

- thal — Thalassemia type

- ca — Number of major vessels colored by fluoroscopy

**These variables strongly correlate with the presence of heart disease.**

## Tech Stack

- Python

- pandas, numpy, seaborn, matplotlib

- scikit-learn, xgboost

## Results Visualization

**Feature Importance (Random Forest)**
Shows which medical indicators impact the prediction most.

**ROC Curve**
Illustrates model’s ability to distinguish between classes.

## Conclusion

The Random Forest model outperformed all others, achieving a 0.85 ROC-AUC, proving to be highly effective for identifying patients at risk.
This model could assist in early detection and prevention strategies for heart disease.


| *“The goal is not just to predict disease — it’s to save lives through data.” ❤️*
