# 💳 Credit Card Fraud Detection

## 📊 Dataset Information

The dataset contains the following columns:

`sn`, `trans_date_trans_time`, `cc_num`, `merchant`, `category`, `amt`, `first`, `last`, `gender`, `street`, `city`, `state`, `zip`, `lat`, `long`, `city_pop`, `job`, `dob`, `trans_num`, `unix_time`, `merch_lat`, `merch_long`, `is_fraud`

- **Problem Type:** Classification
- **Target Variable:** `is_fraud`

---

## 🔍 Data Analysis & Preprocessing

Exploratory data analysis revealed that there are **no missing values** present.

To ensure that both training and testing datasets represent the population uniformly, **stratified shuffling** was applied based on the target value. Moreover, as the dataset is highly imbalanced, the **SMOTE technique** was applied on the training dataset to balance the classes and ensure the model does not overfit.

The dataset was cleaned and preprocessed, including:

- Handling categorical features using **encoding**
- **Train-test split** using stratified sampling

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

---

## 📌 Conclusion

Among all the models tested, **Random Forest Classifier** outperformed other classification algorithms across 3 out of 4 evaluation metrics (Avg Precision, Matthews Correlation Coefficient, and Cohen Kappa Score), making it the most suitable model for detecting credit card fraud in this dataset.
