# Election Outcome Prediction using KNN

## Project Overview

This project applies the **K-Nearest Neighbors (KNN)** algorithm to analyze election-related data and predict election outcomes based on available political and demographic features.

The goal is to understand voting patterns and build a classification model that can support data-driven election analysis.

## Business Objective

The objective of this project is to:

* Predict election outcome categories
* Analyze key factors influencing election results
* Compare model performance for different K values
* Support political campaign planning and decision-making using analytics

## Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* K-Nearest Neighbors
* Jupyter Notebook

## Dataset

The dataset contains election-related attributes used to classify or predict election outcomes. It includes multiple input variables that help analyze voting behavior and political trends.

## Project Workflow

1. **Data Loading & Understanding**
   Loaded the election dataset and reviewed feature types, target variable, and data structure.

2. **Data Preprocessing**
   Checked missing values, encoded required variables, scaled numerical features, and split the dataset into training and testing sets.

3. **Exploratory Data Analysis**
   Analyzed feature distributions, target class balance, and relationships between variables.

4. **Model Building**
   Built a KNN classification model and tested different values of K to find a better-performing model.

5. **Model Evaluation**
   Evaluated the model using accuracy score, confusion matrix, classification report, and ROC-AUC score.

## Model Performance

| Model          | Test Accuracy |
| -------------- | ------------: |
| KNN Classifier |          ~84% |

## Key Observations

* Feature scaling was important because KNN is distance-based.
* Different K values produced different model performance.
* A properly selected K value helped improve prediction stability.
* The model achieved good classification accuracy on the test data.
* KNN is useful for pattern-based classification but can be sensitive to noisy data and feature scaling.

## Business Insights

* Election data can be analyzed to identify voting patterns and outcome trends.
* KNN can help classify election results based on similarity between records.
* The model can support campaign strategy, voter segmentation, and political data analysis.
* Proper preprocessing and scaling are important for reliable prediction.

## Conclusion

This project demonstrates how the KNN algorithm can be used for election outcome prediction. The model performed well after proper preprocessing and feature scaling, achieving around **84% test accuracy**.

From a business analytics perspective, this project shows how machine learning can support political decision-making, voter behavior analysis, and campaign strategy planning.
