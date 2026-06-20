# Loan Delinquency Prediction using CART Decision Tree

## 📌 Project Overview & Objective
In the banking and lending industry, identifying high-risk borrowers who might delay or fail to make payments is crucial for effective risk management. 

This project implements an end-to-end Machine Learning pipeline utilizing a **CART (Classification and Regression Trees) Decision Tree** model to predict whether a loan customer is likely to become **delinquent**. By identifying high-risk borrowers early, financial institutions can proactively mitigate credit risks, optimize monitoring strategies, and reduce potential credit defaults.

---

## 💼 Business Impact & Core Focus
* **Risk Mitigation:** Enables automated screening of loan portfolios to detect early-stage default markers.
* **Leakage Prevention:** Engineered features specifically to remove data leakage variables (such as redundant string targets and system IDs), ensuring high generalization on unseen datasets.
* **Model Interpretability:** Used a decision-tree structure so that credit risk managers can visually map out rules (e.g., FICO thresholds, loan terms) driving risk classifications.

---

## 📊 Dataset Profile
The dataset contains **11,548 entries** across the following structural dimensions:
* **Target Variable (`Sdelinquent`):** Binary classification indicator where `1` represents a delinquent account and `0` represents a non-delinquent/healthy account. 
* **Class Distribution:** The dataset contains an imbalanced ratio of **66.86% delinquent** to **33.14% non-delinquent** observations.
* **Predictor Features:**
  * `FICO`: Credit score ranges (Strongest predictor)
  * `term`: Duration of the loan (e.g., 36 months)
  * `age`: Age demographics of the borrower
  * `home_ownership`: Living status (Rent, Mortgage, Own)
  * `purpose`: Intended use of funds (House, Car, Debt consolidation, etc.)
  * `gender`: Demographic descriptor

---

## 🛠️ Technical Workflow & Architecture

### 1. Data Integrity & Preprocessing
* **Leakage Filtration:** Dropped `ID` and the text column `delinquent` to prevent target distribution bleeding.
* **Stratified Validation Split:** Split the dataset into a 70/30 train-test ratio using **stratified sampling** to preserve class balances across subsets.
* **Production-Grade Pipelines:** Implemented scikit-learn's `ColumnTransformer` combined with `OneHotEncoder(handle_unknown='ignore')` nested inside an atomic `Pipeline` structure to protect against training-to-testing data leakage during transformations.

### 2. Hyperparameter Tuning via Cross-Validation
GridSearchCV was used with **3-Fold Cross-Validation**, optimizing for **ROC-AUC** to maximize true-positive and false-positive resolution:
* **Hyperparameter Grid Tested:** Criterion (Gini/Entropy), Maximum Depth, Minimum Samples per Leaf, and Minimal Cost-Complexity Pruning Alpha (`ccp_alpha`).
* **Optimized Parameters Found:**
```python
  {
      'model__criterion': 'gini', 
      'model__max_depth': 5, 
      'model__min_samples_leaf': 25, 
      'model__ccp_alpha': 0.0
  }
