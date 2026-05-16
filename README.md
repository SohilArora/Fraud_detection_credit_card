# 💳 Credit Card Fraud Detection

A machine learning project to detect **fraudulent credit card transactions**
using classification algorithms. Multiple models are trained and compared to
identify the best-performing approach.

---

## 📥 Dataset
The dataset is not included in this repository due to size constraints.

Download the dataset here: [Google Drive](https://drive.google.com/file/d/1XvkZeVyqoA6IGOYDaupyo0CljpRP90u7/view?usp=sharing)

> The notebook automatically downloads the dataset using `gdown`.
> No manual placement needed — just run the notebook!

---

## 📊 Dataset Information

The dataset contains the following columns:

| Feature | Description |
|---|---|
| `trans_date_trans_time` | Transaction date and time |
| `cc_num` | Credit card number |
| `merchant` | Merchant name |
| `category` | Merchant category |
| `amt` | Transaction amount |
| `first`, `last` | Cardholder name |
| `gender` | Cardholder gender |
| `street`, `city`, `state`, `zip` | Cardholder address |
| `lat`, `long` | Cardholder location coordinates |
| `city_pop` | City population |
| `job` | Cardholder occupation |
| `dob` | Date of birth |
| `trans_num` | Transaction ID |
| `unix_time` | Transaction Unix timestamp |
| `merch_lat`, `merch_long` | Merchant location coordinates |
| `is_fraud` | Fraud label (0 = Not fraud, 1 = fraud) |

- **Problem Type:** Classification
- **Target Variable:** `is_fraud`

---

## 🔍 Data Analysis & Preprocessing

- Exploratory Data Analysis (EDA) revealed **no missing values** in the dataset.
- **Stratified shuffling** based on the target variable was applied to ensure
  uniform representation in train/test splits.
- As the dataset is **highly imbalanced**, the **SMOTE technique** was applied
  on the training dataset to balance the classes and prevent overfitting.

### Preprocessing Steps:
- Encoding categorical features
- Train-test split using stratified sampling
- Balancing classes using SMOTE

---

## 🤖 Machine Learning Models Applied

The following classification models were trained and evaluated:

- Random Forest Classifier
- LightGBM Classifier
- XGBoost Classifier

---

## 📈 Model Evaluation

Models were evaluated using the following metrics:

| Metric | Random Forest | XGBoost | LightGBM |
|---|---|---|---|
| ROC-AUC Score | 0.8845 | 0.9550 | 0.9631 |
| Avg Precision Score | 0.7002 | 0.6495 | 0.4447 |
| Matthews Corr Coef | 0.8357 | 0.8049 | 0.6651 |
| Cohen Kappa Score | 0.8327 | 0.7987 | 0.6294 |

> ✅ **Best Model: Random Forest Classifier** — outperformed others across
> 3 out of 4 metrics (Avg Precision, Matthews Correlation Coefficient,
> and Cohen Kappa Score)

---

## 📌 Conclusion

Among all the models tested, **Random Forest Classifier** outperformed other
classification algorithms across 3 out of 4 evaluation metrics, making it
the most suitable model for detecting credit card fraud in this dataset.

---

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost, LightGBM
- Imbalanced-learn (SMOTE)
  

---



---

## 📁 Project Structure

```
Credit_card_fraud_detection/
├── Credit_card_fraud_ped.ipynb   # Main notebook
├── Original vs predicted.csv     # Model predictions
└── README.md                     # Project documentation
```
