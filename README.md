# Credit-Risk-Default-Prediction-Engine
Credit risk prediction project using the LendingClub dataset with data preprocessing, leakage detection, and machine learning modeling (work in progress).
# Credit Risk Default Prediction Engine

Machine learning project for predicting borrower loan default risk using the **LendingClub Loan Dataset (2007–2018)**.  
The goal of this project is to build a data-driven pipeline that estimates the probability of loan default based on borrower financial and credit-history features available at the time of loan application.

---

## Project Overview

Credit risk modeling is a critical component of lending decisions in financial institutions.  
This project explores how machine learning can be applied to borrower data to identify high-risk loans and support credit decision-making.

The workflow focuses on:

- Data auditing and cleaning
- Handling missing credit-history features
- Detecting and removing **data leakage variables**
- Feature engineering
- Exploratory data analysis
- Preparing the dataset for machine learning models

---

## Dataset

Dataset used:

**LendingClub Loan Data (2007–2018)**

The dataset contains borrower-level information including:

- Loan amount
- Interest rate
- Income
- Debt-to-income ratio
- Credit history variables
- Delinquency indicators
- Loan status

For modeling, loans were filtered to include only:

- **Fully Paid**
- **Charged Off**
- 
---

## Key Steps in the Pipeline

### 1. Data Filtering
Filtered loans to include only finalized outcomes (Fully Paid vs Charged Off).

### 2. Target Variable Creation
Generated a binary **default indicator** based on loan status.

### 3. Missing Value Analysis
Analyzed missing patterns across credit-history variables and applied appropriate handling strategies.

### 4. Data Leakage Detection
Removed variables that contain information unavailable at loan origination, including:

- Payment information
- Settlement data
- Post-loan recovery variables
- Hardship program attributes

Removing these variables ensures **realistic predictive modeling conditions**.

### 5. Feature Engineering
Created additional indicators for missing credit history values such as:

- `delinq_missing`

and applied imputations for sparse temporal variables.

### 6. Exploratory Analysis
Performed correlation analysis and feature inspection to understand relationships with loan default.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

---

## Project Structure
credit-risk-default-prediction/
│
├── credit_risk_default_prediction.ipynb # Main notebook
├── README.md # Project documentation
└── requirements.txt # Python dependencies

---

## Future Work

Planned extensions for the project include:

- Training multiple machine learning models
  - Logistic Regression
  - Random Forest
  - Gradient Boosting
- Model evaluation using:
  - ROC-AUC
  - Precision–Recall
  - Confusion Matrix
- Feature importance analysis
- Deployment as a lightweight **Flask web application** for real-time borrower risk prediction.

---

## Author

**Sashwath J**  
B.Tech CSE (AI & ML)  
VIT University

A binary target variable was created:
