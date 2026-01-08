# Telco Customer Churn Prediction

Customer churn is a critical problem in the telecom industry, as retaining existing customers is significantly cheaper than acquiring new ones.

This project builds an end-to-end machine learning pipeline to identify customers who are likely to churn, enabling proactive and data driven retention strategies.

---

## Problem Statement

The objective of this project is to predict whether a telecom customer will churn based on historical usage, billing, and service related data.

This is framed as a  binary classification problem , where:
- `1` → Customer churns
- `0` → Customer stays

---

## Dataset

- Source: IBM Telco Customer Churn dataset
- Observations: ~7,000 customers
- Target variable: `Churn`
- Key features:
  - Customer tenure
  - Contract type
  - Monthly and total charges
  - Internet and phone services
  - Billing and payment methods

> Note: The `TotalCharges` feature required preprocessing due to mixed data types and missing values.

---
