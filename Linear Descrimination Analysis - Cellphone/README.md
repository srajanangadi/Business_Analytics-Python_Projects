# Cellphone Customer Churn Prediction using Linear Discriminant Analysis (LDA)

## 📌 Project Overview & Objective
In the highly competitive telecommunications sector, retaining customers is critical. Acquiring new customers is often significantly more expensive than maintaining existing ones, making predictive churn modeling an invaluable business asset.

This project implements an end-to-end predictive modeling pipeline utilizing **Linear Discriminant Analysis (LDA)** to classify cellphone subscribers into *churn* or *non-churn* categories. By leveraging historical customer usage characteristics and service-related variables, the model provides actionable predictions that allow telecom companies to design targeted proactive retention campaigns.

---

## 💼 Business Impact & Strategy
* **Proactive Customer Retention:** Helps the marketing and customer success teams flag accounts exhibiting high-risk churn patterns before they cancel services.
* **Strategic Threshold Tuning:** Focuses on addressing class imbalance by tuning decision thresholds—prioritizing *Recall* for the churn class to maximize the detection of at-risk revenue.
* **Dimensionality Reduction & Interpretability:** Uses LDA to map multi-dimensional customer features into a single discriminant component, keeping the decision boundaries easily interpretable for executive decision-making.

---

## 📊 Dataset Profile & Features
The model evaluates cellphone customer profiles containing key behavioral attributes:
* **Target Variable (`Churn`):** Binary indicator (`1` for customers who left the service, `0` for retained customers).
* **Predictor Features:**
  * **Usage Behavior:** Day minutes, evening minutes, night minutes, international minutes, and total calls.
  * **Account Information:** Account length, number of voicemail messages.
  * **Customer Care Interation:** Number of customer service calls (a key behavioral indicator of dissatisfaction).

---

## 🛠️ Technical Workflow & Implementation

### 1. Exploratory Data Analysis & Preprocessing
* **Feature Examination:** Evaluated the continuous usage distributions and interaction metrics across churn vs. non-churn segments.
* **Data Scaling:** Applied standard preprocessing techniques to stabilize the covariance matrices required by discriminant algorithms.
* **Data Splitting:** Structured the dataset into dedicated training and testing sets to guarantee unbiased performance evaluation.

### 2. Model Development & Comparative Analysis
* **Primary Model:** Implemented `LinearDiscriminantAnalysis` from `scikit-learn` to establish an optimized linear decision boundary.
* **Baseline Comparison:** Validated performance alongside a **Logistic Regression** model trained on the single extracted LDA component, ensuring a robust, mathematically cross-verified classification framework.

---

## 📈 Performance & Evaluation Insights

### Key Metrics & Findings
* **High Overall Accuracy:** The model demonstrates strong predictive performance, particularly in accurately classifying non-churn customers.
* **Handling Class Imbalance:** Due to standard real-world class imbalances (fewer churned examples than active ones), the default threshold prioritizes overall accuracy.
* **Business-Centric Optimization:** The analysis explicitly details how adjusting the classification probability threshold optimizes **Churn Recall**. This increases the detection rate of potential churners, providing the business with a wider net for preventive retention campaigns.
