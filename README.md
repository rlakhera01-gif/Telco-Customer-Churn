# Telco Customer Churn Prediction

Customer churn is a critical problem in the telecom industry, as retaining existing customers is significantly cheaper than acquiring new ones.

This project builds a **machine learning workflow** to predict whether a telecom customer will churn using historical customer, service, and billing data.

---

## Problem Statement

The objective of this project is to predict whether a customer will churn based on available customer attributes.

This is formulated as a **binary classification problem**:
- `1` → Customer churns  
- `0` → Customer stays  

---

## Dataset

- Source: IBM Telco Customer Churn dataset  
- Size: ~7,000 customer records  
- Target variable: `Churn`  

Key features include:
- Customer tenure  
- Monthly and total charges  
- Contract and payment information  
- Internet and phone services  

> The `TotalCharges` column required cleaning due to non-numeric values.

---

## Data Preparation

The following preprocessing steps were applied:

- Converted `TotalCharges` to numeric and handled missing values  
- Dropped the customer identifier column (`customerID`)  
- Identified numerical and categorical feature sets  
- Applied:
  - **StandardScaler** to numerical features  
  - **OneHotEncoder (handle_unknown='ignore')** to categorical features  

All preprocessing was implemented using **scikit-learn’s `ColumnTransformer` and `Pipeline`** to ensure consistent and reproducible transformations.

---

## Exploratory Analysis

Exploratory data analysis was conducted using visualizations to understand churn behavior and feature distributions.

Key observations:
- Higher churn rates among customers with **short tenure**
- Increased churn for **month-to-month contracts**
- Differences in churn behavior across internet service types  

EDA was used strictly for understanding data patterns.

---

## Modeling

The dataset was split into training and test sets using a **stratified train-test split**.

Model trained:
- **Logistic Regression** (`max_iter=1000`)

The model was trained as part of a complete preprocessing and modeling pipeline.

---

## Evaluation

Model performance was evaluated on the test set using:
- Precision  
- Recall  

Both predicted class labels and churn probabilities were generated from the trained model.

---

## Key Findings

- Customer tenure and contract type showed strong association with churn  
- Logistic Regression provided a simple and interpretable baseline model  
- Pipeline-based preprocessing ensured clean and reproducible modeling  

---

## Tools & Libraries

Python, Pandas, NumPy, scikit-learn, Matplotlib, Seaborn, Jupyter Notebook, Git

---

## Summary

- Built a complete preprocessing and modeling pipeline using scikit-learn  
- Properly handled categorical and numerical features  
- Developed a reproducible baseline churn prediction model  

This project demonstrates **core machine learning workflow skills** applied to a real-world telecom dataset.
