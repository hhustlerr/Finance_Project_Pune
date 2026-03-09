# Fraud Risk Analytics Framework

Author: Prachi Mittal  
Track: Business Analytics  

---

## Project Overview

This project analyzes digital transaction data to identify fraud patterns and develop a **Fraud Risk Scoring Framework** for proactive fraud detection.

With the rapid growth in digital transactions, traditional manual monitoring methods are no longer scalable. This analysis leverages **exploratory data analysis (EDA) and risk modeling** to identify high-risk behavioral patterns across customers, channels, and time windows.

The goal is to help organizations detect fraud earlier while minimizing false positives that negatively impact customer experience.

---

## Problem Statement

Financial institutions face increasing fraud risks due to:

- Growth in digital payments
- Limited scalability of manual monitoring systems
- Fraud spikes during specific transaction hours
- Channel-specific vulnerabilities

Key questions addressed:

1. Which factors have the strongest relationship with fraud?
2. How do **time and channel interactions** influence fraud?
3. Do variables like **Credit Score, Region Risk Score, and Transaction Amount** affect fraud probability?
4. Which customers are most likely to commit fraud?

---

## Dataset Overview

- **Total Transactions:** 10,000
- **Features:** 19 variables
- **Fraud Rate:** 13.77% (Imbalanced dataset)

Key attributes include:

- Age
- Location
- Account Type
- Transaction Amount
- Transaction Channel
- Region Risk Score
- Credit Score
- Transaction Frequency Band

---

## Data Preprocessing

Steps performed:

- Converted negative transactions to absolute values
- One-hot encoding for categorical variables
- Separate analysis of numerical and categorical features
- Addressed dataset imbalance (recommended oversampling/undersampling)

---

## Key Findings

### 1. Numerical Variables

Variables such as:

- Credit Score
- Region Risk Score
- Average Transaction Amount

show **very weak correlation with fraud**.

---

### 2. Categorical Risk Indicators

Strong fraud signals were found in:

- **ATM transactions**
- **Savings accounts**
- **Urban / Semi-Urban locations**
- **Low transaction frequency users**

---

### 3. Temporal Fraud Patterns

Fraud activity spikes at specific time windows:

| Channel | High Risk Time |
|-------|---------------|
ATM | 5–8 AM |
ATM | 4 PM |
ATM | 10–11 PM |
Branch | 8 AM |

These time windows represent **fraud opportunity periods** that should be monitored in real time.

---

## Fraud Risk Scoring Framework

A rule-based risk scoring model was designed to identify high-risk customers.

### Risk Score Formula

Factors considered:

- Past fraud history
- Transaction timing
- Transaction channel
- Transaction amount vs average
- Credit profile
- Customer literacy

### Risk Levels

| Score | Risk Level |
|------|-----------|
0–4 | Low Risk |
5–8 | Medium Risk |
9+ | High Risk |

---

## Example Customer Risk Profiles

| Person | Risk Level | Score | Key Indicators |
|------|------------|------|---------------|
Person 1 | High | 11 | Night-time online transactions, past fraud |
Person 2 | Medium | 6 | ATM usage, higher than average transaction |
Person 3 | Low | 3 | Branch transactions, normal behavior |

---

## Industry Context

Fraud in digital payments is estimated to cause **over $40B in global losses annually**.

Major industry challenges include:

- AI-driven fraud tactics
- Synthetic identities
- Regulatory compliance (KYC, AML, RBI standards)
- Balancing fraud detection with customer experience

---

## Proposed Solution

1. Deploy **real-time fraud monitoring dashboards**
2. Track **channel-time risk combinations**
3. Implement **fraud risk scoring**
4. Automate alerts for high-risk transactions
5. Reduce false positives to improve customer trust

---

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Google Colab
- Exploratory Data Analysis

---

## Notebook

Code implementation available here:

https://colab.research.google.com/drive/1IptW8w5gev6bkI117MlmkaW0bFDsg2ex

---

## Future Improvements

- Machine Learning models (Random Forest, XGBoost)
- Real-time fraud detection pipelines
- Fraud probability prediction models
- Dashboard visualization using Power BI or Streamlit

---

## Author

Prachi Mittal  
