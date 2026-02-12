# 💳 Credit Card Fraud Detection System

## 📌 Overview

This project implements a machine learning–based fraud detection system designed to identify potentially fraudulent credit card transactions using historical transaction data.

The primary objective is to detect anomalous transactions while minimizing false positives — a critical requirement in real-world financial systems.

In addition to model development, a simple frontend interface was created to demonstrate real-time fraud prediction using the trained model.

---

## 🎯 Objective

To design and implement a data-driven fraud detection pipeline that:

- Analyzes historical transaction patterns  
- Handles highly imbalanced datasets  
- Identifies potentially fraudulent transactions  
- Demonstrates practical ML model integration with a user interface  

---

## 🧠 Problem Statement

Credit card fraud results in substantial financial losses globally. Traditional rule-based detection systems struggle to identify evolving fraud patterns.

Machine learning provides a scalable and adaptive approach capable of detecting subtle and complex fraud behavior within high-volume transactional data.

---

## ⚙️ Methodology

The system follows a structured machine learning workflow:

1. Data preprocessing and cleaning  
2. Feature scaling and transformation  
3. Handling class imbalance  
4. Train-test split  
5. Supervised model training  
6. Performance evaluation  
7. Fraud prediction on unseen transactions  

The focus is on reproducibility, explainability, and practical implementation rather than black-box optimization.

---

## 📊 Dataset Information

Due to GitHub file size limitations, the complete dataset is not included in this repository.

A representative sample dataset is provided for demonstration and reproducibility.  
The sample maintains:

- Original feature structure  
- PCA-transformed features  
- Class imbalance characteristics  

Original dataset source:  
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

---

## 🤖 Models & Techniques Used

- Supervised Classification Algorithms  
- Feature Scaling (Standardization)  
- Handling Imbalanced Data  
- Performance Evaluation Metrics:
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix

Special emphasis is placed on **Recall**, as minimizing false negatives is critical in fraud detection systems.

---

## 🖥 Frontend Demonstration

A lightweight frontend interface was developed to simulate fraud prediction.

The interface allows:

- Input of transaction features  
- Real-time fraud prediction using the trained model  
- Display of prediction result (Fraud / Legitimate)  

This demonstrates practical integration of an ML model with a user-facing application.

---

## 🛠 Technologies Used

**Programming:** Python  
**Libraries:** NumPy, Pandas, Scikit-learn, Matplotlib  
**Interface:** HTML, CSS, JavaScript  
**Environment:** Jupyter Notebook  
**Version Control:** Git & GitHub  

---

## 📈 Key Results

- Effective identification of fraudulent transactions  
- Demonstration of anomaly detection in highly imbalanced datasets  
- Practical ML pipeline from preprocessing to prediction  
- Working frontend prototype for fraud classification  

---

## ▶️ How to Run the Project

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/credit-card-fraud-detection-system.git
cd credit-card-fraud-detection-system
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Run Notebook

```bash
jupyter notebook
```

Open the `.ipynb` file and execute cells sequentially.

---

## 🌐 Running the Frontend

If using static frontend:

Open:

```
frontend/index.html
```

in your browser.

If model is saved using `joblib`, ensure the prediction logic is correctly linked in the UI demonstration.

---

## 🔮 Future Improvements

- Deploy model as REST API (Flask/FastAPI)
- Add probability confidence score
- Implement real-time streaming fraud detection
- Deploy on cloud infrastructure (AWS / GCP)
- Improve imbalance handling using advanced techniques (SMOTE, XGBoost)

---

## 👤 Author

Adarsh Kumar  
AI & Full Stack Developer  

