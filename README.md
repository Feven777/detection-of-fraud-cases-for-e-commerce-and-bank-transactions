# Fraud Detection in E-Commerce and Banking Transactions

## Overview
This project presents an end-to-end machine learning approach for detecting fraudulent transactions in e-commerce and banking systems. The work focuses on addressing severe class imbalance, comparing multiple machine learning models, and providing transparent and interpretable predictions using SHAP (SHapley Additive exPlanations).

---

## Datasets
The project uses two real-world financial transaction datasets:

- **fraud.csv**  
  An anonymized transaction dataset with PCA-transformed features (V1–V28). This dataset is widely used in fraud detection research and contains a highly imbalanced class distribution.

- **credit.csv**  
  Credit card transaction data used to evaluate model robustness and generalization across different financial contexts.

In both datasets, fraudulent transactions represent a very small fraction of the total observations.

---

## Project Workflow
1. Exploratory Data Analysis (EDA)
2. Data preprocessing and feature engineering
3. Handling class imbalance using SMOTE
4. Model training and evaluation
5. Performance comparison and model selection
6. Model explainability using SHAP

---

## Models Evaluated
- Logistic Regression  
- Random Forest  
- Gradient Boosting (**final selected model**)

Models were evaluated using recall, precision, F1-score, and ROC-AUC, with special emphasis on detecting fraudulent transactions and maintaining consistency across both datasets.

---

## Explainability
SHAP (SHapley Additive exPlanations) was used to:
- Identify globally important features
- Explain individual fraud predictions
- Validate that the model learned meaningful and consistent fraud-related patterns

---

## Key Findings
- Fraud detection depends on combinations of features rather than individual variables
- Gradient Boosting achieved the best balance between performance and interpretability
- SHAP analysis confirmed that model decisions are transparent and logically consistent

---

## Repository Structure
```text
data/
├── fraud.csv
├── credit.csv

notebooks/
├── modeling.ipynb
├── model-explainability.ipynb

requirements.txt
README.md
