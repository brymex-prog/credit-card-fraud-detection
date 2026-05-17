# Credit Card Fraud Detection — Machine Learning Project

This repository contains an end‑to‑end machine learning workflow for detecting fraudulent credit card transactions using the Kaggle Credit Card Fraud dataset.

## 📌 Project Overview
Credit card fraud is extremely rare (0.17% of all transactions), making this a highly imbalanced classification problem. The goal is to build a model that can accurately identify fraudulent transactions while minimizing false positives.

## 📊 Dataset Summary
- **Total transactions:** 284,807  
- **Fraud cases:** 492  
- **Fraud rate:** 0.17%  
- **Features:** 30 (V1–V28 PCA components, Amount, Hour)

## 🛠️ Preprocessing
- Created **Hour** feature from timestamp  
- Standardized Amount and Hour  
- Applied **SMOTE** to balance training data  
- Stratified 80/20 train‑test split  

## 🤖 Models Used
- **Logistic Regression** (baseline, class_weight='balanced')
- **Random Forest** (200 trees)

## 🧪 Model Performance (Test Set)
| Model | Precision | Recall | F1 | PR‑AUC |
|-------|-----------|--------|-----|--------|
| Logistic Regression | 0.055 | 0.918 | 0.104 | 0.728 |
| Random Forest | 0.851 | 0.816 | 0.833 | 0.869 |

Random Forest significantly outperformed Logistic Regression in precision and F1‑score.

## 🔍 Feature Importance (Top 5)
1. **V14**  
2. **V10**  
3. **V4**  
4. **V17**  
5. **V12**

These features account for **61%** of total importance.

## 📈 Visualizations
The repository includes:
- Class distribution plots  
- Confusion matrices  
- ROC & Precision‑Recall curves  
- Feature importance bar charts  
- Distribution plots for top features  

## 🏁 Conclusion
A Random Forest classifier combined with SMOTE provides strong performance for fraud detection and is suitable as a real‑time screening tool.
