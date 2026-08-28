# HR Job Change Classification

## Overview

This project applies machine learning classification techniques to predict whether a candidate is likely to be looking for a job change.

The project focuses on building and comparing multiple classification models while addressing challenges such as categorical data, feature preprocessing, dimensionality reduction, and class imbalance.

## Project Workflow

The analysis includes:

- Exploratory data analysis
- Missing-value analysis
- Categorical feature encoding
- Feature scaling using MinMaxScaler
- Stratified train/test splitting
- Class balancing using SMOTE
- Dimensionality reduction using PCA
- Hyperparameter tuning with GridSearchCV
- Model training and comparison
- Evaluation using multiple classification metrics

## Machine Learning Models

The following models were evaluated:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Gaussian Naive Bayes
- Support Vector Machine (SVM)
- Decision Tree
- Random Forest
- AdaBoost
- Gradient Boosting

## Model Evaluation

Because the target variable is imbalanced, model performance was evaluated using more than accuracy alone.

Metrics included:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion matrices

Gradient Boosting achieved the highest overall accuracy at approximately **86%**. AdaBoost provided a strong balance between precision and recall for the positive class, while Gaussian Naive Bayes achieved the highest positive-class recall but produced substantially more false positives.

These results demonstrate the importance of considering multiple evaluation metrics when working with imbalanced classification problems.

## Key Techniques

### Class Imbalance

SMOTE (Synthetic Minority Over-sampling Technique) was used on the training data to increase representation of the minority class and improve the models' ability to identify candidates looking for a job change.

### Dimensionality Reduction

Principal Component Analysis (PCA) was evaluated to determine whether reducing the dimensionality of the feature space could improve model performance.

### Hyperparameter Tuning

GridSearchCV was used to evaluate different hyperparameter configurations for selected models.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- Jupyter Notebook

## Project File

[`Classification.ipynb`](./Classification.ipynb)
