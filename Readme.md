# Credit Card Fraud Detection using Machine Learning

## Overview
This project implements an explainable machine learning pipeline to detect fraudulent credit card transactions using historical transaction data. The focus is on data analysis, handling class imbalance, and building a reliable and interpretable model suitable for real-world decision support systems.

---

## Dataset
- **Source:** Kaggle Credit Card Fraud Detection dataset  
- **Total Records:** 284,807 transactions  
- **Features:**  
  - V1–V28 (PCA-transformed features)  
  - Time, Amount  
- **Target Variable:** Class (0 = Legitimate, 1 = Fraud)  
- **Key Challenge:** Highly imbalanced dataset (~0.17% fraud cases)

---

## Exploratory Data Analysis (EDA)
- Verified absence of missing values  
- Analyzed class imbalance and transaction amount distribution  
- Observed that most transactions are of low value while fraud cases are rare  
- Visualized:
  - Class distribution
  - Transaction amount histogram and boxplot (log scale)

---

## Data Preprocessing
- Standardized `Time` and `Amount` features using `StandardScaler`  
- Constructed final feature set using:
  - V1–V28  
  - Scaled Time and Amount  
- Applied stratified train–test split to preserve class distribution

---

## Handling Class Imbalance
- Used `class_weight = 'balanced'` in Logistic Regression  
- Avoided resampling techniques to keep the pipeline simple, reproducible, and interpretable  

---

## Model
- **Algorithm:** Logistic Regression  
- **Solver:** saga  
- **Max Iterations:** 2000  
- **Rationale:**  
  Logistic Regression is fast, interpretable, and well-suited for imbalanced classification problems where explainability is important.

---

## Evaluation Metrics
Due to class imbalance, model evaluation focused on:
- ROC-AUC  
- Precision–Recall (PR-AUC)  
- Confusion Matrix  
- Precision, Recall, and F1-score  

Priority was given to **high recall** to reduce false negatives in fraud detection.

---

## System Perspective (AI Agent View)
- **Agent:** Logistic Regression classifier  
- **Environment:** Stream of incoming credit card transactions  
- **Perception:** Transaction feature vector  
- **Action:** Output fraud probability for each transaction  
- **Feedback:** Labeled outcomes used for offline retraining and performance monitoring  

---

## Results
- Achieved effective discrimination between fraudulent and legitimate transactions  
- Model performance evaluated on a stratified test set  
- Trained model saved as a reusable artifact:  
  - `logistic_model.joblib`

---

## Limitations & Future Improvements
- Anonymized PCA features limit interpretability  
- Potential improvements:
  - Advanced imbalance handling techniques  
  - Threshold tuning based on business cost  
  - Concept drift monitoring  
  - Model explainability (e.g., SHAP)  
  - Ensemble-based approaches  

---

## Tech Stack
- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib  
- **Tools:** Jupyter Notebook  

---

## Conclusion
This project demonstrates how structured data analysis and interpretable machine learning models can support fraud detection and risk reduction in financial systems. The emphasis on clarity, evaluation, and reproducibility makes the approach suitable for practical deployment scenarios.

---

## References
- Kaggle Credit Card Fraud Detection Dataset  
- Scikit-learn Documentation  
