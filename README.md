# Customer Churn Prediction Using PySpark

This repository contains an end-to-end solution for predicting customer churn in the telecom sector using **PySpark** and **Apache Spark's MLlib**. The goal is to help businesses proactively identify customers likely to churn and implement data-driven retention strategies.

---

## Overview

Customer churn prediction is critical for telecom companies aiming to reduce customer attrition and improve profitability. This project builds and evaluates predictive models on large-scale telecom datasets using PySpark to handle scalable distributed processing.

Key highlights:
- End-to-end data pipeline from preprocessing to evaluation
- Implementation of ML algorithms like Naive Bayes, Random Forest, and Gradient Boosted Trees
- Evaluation using metrics such as Accuracy, AUC, Precision, Recall, and F1-Score

---

## Tech Stack

- **PySpark (Apache Spark)**
- **Spark MLlib**
- **Python**
- **Pandas / Seaborn / Matplotlib** (for EDA and correlation visualization)

---

## Dataset

We used publicly available telecom churn datasets from [Kaggle](https://www.kaggle.com/datasets/muhammedsar/churn-datacsv) where each row represents a customer and columns represent attributes such as:

- Call usage (day/evening/night/international)
- Charges
- Voicemail & international plans
- Customer service calls
- Churn status (target variable)

---

## Pipeline Structure

1. **Data Preprocessing**
   - Transforming categorical variables into numeric (e.g., Yes/No → 1/0)
   - Handling nulls and scaling features

2. **Exploratory Data Analysis**
   - Summary statistics
   - Correlation analysis using sampled data
   - Feature importance

3. **Modeling**
   - Models: Naive Bayes, Random Forest, Gradient Boosted Trees
   - Pipeline using `StringIndexer`, `VectorAssembler`, `CrossValidator`
   - 5-fold cross-validation for robust evaluation

4. **Evaluation**
   - Confusion Matrix, AUC, Accuracy, Precision, Recall, F1-score
   - Binary and Multiclass Evaluators
   - Addressed class imbalance using stratified sampling

---

## Model Performance

| Model                 | Accuracy | AUC  |
|----------------------|----------|------|
| Naive Bayes          | 53.67%   | 0.61 |
| Random Forest        | 88.91%   | 0.88 |
| Gradient Boosted Tree| **92.05%** | **0.86** |

Gradient Boosted Trees performed best overall and were recommended for deployment.

---

## Future Enhancements

- Implement real-time ETL pipelines using Apache Spark and PostgreSQL
- Integrate external customer data sources (CRM, behavior logs)
- Expand model selection with SVM, XGBoost, and ensemble stacking
- Deploy the model as an API using Flask or FastAPI
- Enable live monitoring of churn predictions on streaming data

---

## Resources

- Dataset:  
  [Telecom Churn Data](https://www.kaggle.com/datasets/muhammedsar/churn-datacsv?select=churn_data.csv)

- Tools Used:
  - Apache Spark
  - PySpark MLlib
  - Jupyter Notebook / Google Colab (for prototyping)
  - Pandas / Seaborn / Matplotlib

---

## Contributions

Developed and maintained by:
- Namratha Nagathihalli Anantha – Modeling & Implementation  
- Gahana Nagaraja – Data Collection & Processing  
- Niharika Mysore Prakasha – Evaluation & Reporting


