# 🛡️ Financial Transaction Fraud Detection

A Machine Learning-powered fraud detection system designed to identify suspicious financial transactions in real time.

Built for **NovaPay**, a digital-first cross-border money transfer platform, this solution helps prevent **identity theft**, **account takeover**, **unauthorized payments**, and **transaction laundering** while minimizing false positives and maintaining regulatory compliance.

---

## 🚀 Project Overview

Traditional rules-based fraud systems struggle to keep pace with evolving fraud tactics and often generate excessive false positives that frustrate legitimate customers.

This project replaces static fraud rules with a scalable, explainable, and adaptive machine learning solution capable of detecting fraudulent transactions in real time.

### Business Goals

✅ Improve fraud detection recall by at least **15%** over the existing rules-based system

✅ Reduce false positives and improve customer experience

✅ Support regulatory transparency through explainable AI

✅ Enable real-time fraud scoring through API deployment

✅ Establish a scalable framework for continuous model monitoring and retraining

---

## 🌍 Business Context

NovaPay operates across:

- 🇨🇦 Canada
- 🇬🇧 United Kingdom
- 🇺🇸 United States

The platform processes millions of cross-border transactions monthly for:

- Individuals sending money internationally
- Freelancers receiving global payments
- Businesses managing international payroll

As transaction volume grows, fraud prevention becomes a strategic requirement for maintaining:

- Customer trust
- Financial integrity
- Regulatory compliance
- Operational efficiency

---

## 🎯 Problem Statement

Digital payment providers face several fraud-related challenges:

### Operational Challenges

- Real-time transaction processing
- Limited manual review capacity
- Rapidly evolving fraud techniques

### Financial Challenges

- Chargebacks and refund costs
- Customer attrition caused by false positives
- Revenue losses from missed fraud

### Regulatory Challenges

- AML and KYC compliance requirements
- Explainable and auditable decision-making
- Increased regulatory scrutiny

---

## 📊 Dataset Overview

The dataset combines transaction, customer, and fraud investigation data.

### Transaction Data

- Transaction amount
- Currency pair
- Timestamp
- Channel (Web, Mobile, ATM)
- Device fingerprint
- IP address
- Geographic information

### Customer Data

- Account age
- KYC verification tier
- Historical transaction behavior
- Internal risk score

### Fraud Labels

Binary classification target:

- `0` → Legitimate Transaction
- `1` → Fraudulent Transaction

> Fraudulent transactions represent less than 1% of all observations, creating a highly imbalanced classification problem.

---

## 🏗️ Solution Architecture

### 1️⃣ Data Profiling

- Missing value analysis
- Fraud prevalence assessment
- Distribution analysis

### 2️⃣ Feature Engineering

Features include:

- Transaction velocity metrics
- Device mismatch indicators
- Geographic anomalies
- Time-based patterns
- Customer behavioral deviations

### 3️⃣ Exploratory Data Analysis

- Fraud trends by geography
- Channel-level analysis
- Temporal fraud patterns
- Outlier investigation

### 4️⃣ Model Development

Baseline Models:

- Logistic Regression
- Random Forest

Advanced Models:

- XGBoost
- LightGBM

Techniques:

- Class weighting
- Hyperparameter optimization
- Imbalanced learning strategies

### 5️⃣ Explainability

Using **SHAP** to provide:

- Transaction-level explanations
- Feature importance analysis
- Regulatory transparency

### 6️⃣ Deployment

Real-time scoring via:

- FastAPI
- Docker
- REST API Endpoint (`/score`)

### 7️⃣ Monitoring

- Data drift detection using Evidently
- Performance monitoring
- Quarterly retraining workflow

---

## 🛠️ Technology Stack

### Data Science

- Python
- Pandas
- NumPy
- Scikit-Learn

### Machine Learning

- XGBoost
- LightGBM
- SHAP

### Visualization

- Matplotlib
- Seaborn
- Plotly

### Deployment

- FastAPI
- Docker

### Monitoring

- Evidently AI

---

## 📈 Evaluation Metrics

Because fraud detection is highly imbalanced, model performance is evaluated using:

- Recall
- Precision
- F1 Score
- ROC-AUC
- PR-AUC

Primary objective:

> Maximize fraud detection recall while maintaining acceptable precision to minimize customer disruption.

---

## 🔄 End-to-End Workflow

```text
Raw Data
    ↓
Data Profiling
    ↓
Feature Engineering
    ↓
EDA
    ↓
Model Training
    ↓
Hyperparameter Tuning
    ↓
Model Evaluation
    ↓
SHAP Explainability
    ↓
FastAPI Deployment
    ↓
Monitoring & Retraining
```

---

## 📦 Deployment Architecture

```text
Transaction Request
        ↓
    FastAPI
        ↓
 Feature Pipeline
        ↓
 Fraud Model
        ↓
 Fraud Score
        ↓
 Decision Engine
```

Transactions are scored in real time and returned to downstream systems for approval, review, or rejection.

---

## 🔮 Future Enhancements

- Graph-based fraud detection
- Real-time streaming features
- Ensemble model stacking
- Online learning for adaptive fraud detection
- Fraud investigation dashboard

---

## 📜 License

This project is licensed under t