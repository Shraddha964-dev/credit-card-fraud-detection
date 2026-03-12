# 💳 Credit Card Fraud Detection

End-to-end machine learning pipeline to detect fraudulent credit card transactions 
on a highly imbalanced real-world dataset (284,807 transactions, only 0.17% fraud).

---

## 📌 Key Results

| Model | Recall | Precision | F1 Score | ROC-AUC |
|---|---|---|---|---|
| Logistic Regression | ~0.78 | ~0.87 | ~0.82 | ~0.97 |
| Random Forest | ~0.85 | ~0.95 | ~0.90 | ~0.98 |
| **XGBoost** ✅ | **~0.92** | **~0.93** | **~0.92** | **~0.98** |

> **XGBoost selected as final model** — highest recall means fewest missed fraudulent transactions.

---

## 🧩 Business Context

Credit card fraud costs the global financial industry **$32 billion+ annually**.  
Built with 3.5 years of financial services domain experience (Temenos Kony Infinity 
banking platform), this project mirrors real-world fraud detection pipelines used 
in digital banking systems.

**Core challenge:** A model predicting everything as legitimate would be 99.83% accurate — 
but completely useless. Recall is what matters: every missed fraud is a real financial loss.

---

## 🔍 Analysis Steps

1. **EDA** — class imbalance analysis, transaction patterns by time, amount distributions
2. **Feature Analysis** — top PCA features correlated with fraud, time-of-day patterns
3. **Preprocessing** — StandardScaler for Amount/Time, stratified train/test split
4. **SMOTE** — synthetic oversampling on training data only to handle class imbalance
5. **Model Training** — Logistic Regression, Random Forest, XGBoost
6. **Evaluation** — Confusion matrix, ROC curve, Precision-Recall curve, Feature importance
7. **Business Impact** — Financial cost analysis of false positives vs false negatives

---

## 💡 Key Insights

- **Time matters:** Fraud spikes during low-volume hours (late night) — a strong signal
- **SMOTE works:** Recall improved significantly after handling class imbalance
- **ROC-AUC is misleading** on imbalanced data — Precision-Recall AUC is more informative
- **Business cost:** Missing 1 fraud transaction (~£120 avg) costs 24x more than 1 false alarm (~£5)
- **XGBoost** captures complex non-linear fraud patterns that linear models miss

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python (Pandas, NumPy) | Data manipulation |
| Scikit-learn | Preprocessing, Logistic Regression, Random Forest, metrics |
| XGBoost | Gradient boosting classifier |
| imbalanced-learn (SMOTE) | Class imbalance handling |
| Matplotlib, Seaborn | Visualizations |
| Jupyter Notebook | Analysis environment |

---

## 📁 Project Structure

```
credit-card-fraud-detection/
├── notebook.ipynb          # Complete analysis notebook
├── requirements.txt        # Dependencies
├── data/
│   └── creditcard.csv      # Dataset (download from Kaggle)
├── images/                 # Generated visualizations
└── README.md
```

---

## ▶️ How to Run

```bash
# 1. Clone repo
git clone https://github.com/Shraddha964-dev/credit-card-fraud-detection.git
cd credit-card-fraud-detection

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download dataset
# Go to: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
# Place creditcard.csv in the data/ folder

# 4. Run notebook
jupyter notebook notebook.ipynb
```

---

## 📊 Dataset

**Source:** [Kaggle — ULB Machine Learning Group](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)  
**Size:** 284,807 transactions · 492 fraud cases (0.17%)  
**Features:** V1–V28 (PCA-transformed), Time, Amount, Class  
**Period:** September 2013 · European cardholders

---

## 🔗 Related Projects

- [E-Commerce Customer Segmentation](https://github.com/Shraddha964-dev/ecommerce-customer-analysis) — RFM + K-Means clustering with live Streamlit dashboard
- [Banking Transaction SQL Analysis](https://github.com/Shraddha964-dev/banking-transaction-sql-analysis) — 11 SQL queries covering fraud detection, RFM, cohort retention

---

## 👩‍💻 About

Built by **Shraddha Sajane** — Data Analyst with 3.5 years of experience  
in financial services (Temenos Kony Infinity banking platform).

[LinkedIn](https://www.linkedin.com/in/shraddha-sajane) | [GitHub](https://github.com/Shraddha964-dev)
# credit-card-fraud-detection
# credit-card-fraud-detection
# creditCard-fraud-detection
