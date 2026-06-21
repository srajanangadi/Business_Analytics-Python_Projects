# Sales Classification using Random Forest

## Project Overview

This project applies the **Random Forest algorithm** to analyze company sales data and classify sales performance into different categories. The goal is to understand the key factors that influence sales and build a predictive model that can support business decision-making.

## Business Objective

The objective of this project is to:

* Classify sales performance based on business attributes
* Identify important factors affecting sales
* Support pricing, advertising, and market strategy decisions
* Use machine learning to generate actionable business insights

## Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Random Forest Classifier
* Jupyter Notebook

## Dataset

The dataset contains company sales-related information such as price, advertising, income, population, age, shelving location, and competitor price. These features were used to predict sales performance categories.

## Project Workflow

1. **Data Loading & Understanding**
   Loaded the dataset and reviewed feature types, data structure, and target variable.

2. **Data Preprocessing**
   Checked missing values, handled categorical variables, created sales categories, and prepared the dataset for modeling.

3. **Exploratory Data Analysis**
   Analyzed sales distribution and explored how factors such as price, advertising, income, and shelf location affect sales.

4. **Model Building**
   Built a Random Forest classification model to predict sales performance categories.

5. **Model Evaluation**
   Evaluated the model using accuracy, confusion matrix, classification report, and macro F1-score.

6. **Feature Importance Analysis**
   Identified the most important business drivers influencing sales classification.

## Model Performance

| Metric         | Score |
| -------------- | ----: |
| Accuracy       |  ~66% |
| Macro F1-score |  ~65% |

## Key Business Factors

The most important features influencing sales performance were:

* Price
* Age
* Shelf Location
* Competitor Price
* Income
* Advertising
* Population

## Key Observations

* Price and competitor price had a strong influence on sales performance.
* Shelf location played an important role in product visibility and sales category.
* Advertising and income also contributed to sales variation.
* Random Forest helped identify important business drivers beyond only prediction accuracy.
* The model provided useful insights for pricing and marketing strategy.

## Business Insights

* Products placed in better shelf locations may have stronger sales performance.
* Pricing decisions should consider both product price and competitor price.
* Advertising investment can support sales growth, but its impact should be analyzed with other factors.
* The model can help businesses segment products into sales performance categories and plan strategy accordingly.

## Conclusion

This project demonstrates how Random Forest can be used for sales classification and business insight generation. The model achieved around **66% accuracy** and helped identify key factors influencing company sales.

From a business analytics perspective, this project shows how machine learning can support pricing decisions, advertising planning, product placement strategy, and sales performance analysis.
