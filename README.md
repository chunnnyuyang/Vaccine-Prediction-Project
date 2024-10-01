# Vaccine-Prediction-Project

## By Chun-Yu (Peggy) Yang
This project aims to predict the likelihood of UWM Corp employees receiving H1N1 and seasonal flu vaccines. The purpose is to assist the company in designing targeted vaccination campaigns to protect its workforce from future flu outbreaks, using machine learning models.

## Problem Statement
UWM Corp is a large corporation with thousands of employees spread globally. The company is concerned about the potential impact of seasonal flu and H1N1 outbreaks on employee health and business operations. By predicting the likelihood of employees receiving the vaccines, UWM Corp can tailor its communication and vaccination efforts to specific demographic segments, leading to cost savings, increased employee satisfaction, and an improved corporate image.

The goal of this project is to create predictive models that can accurately assess the likelihood of each employee receiving the H1N1 and seasonal flu vaccines.

## Data
The dataset contains three files:
- training_set_features.csv: Contains features related to employees’ demographics, health behaviors, and opinions.
- training_set_labels.csv: Contains the labels for whether employees received the H1N1 or seasonal flu vaccine.
- test_set_features.csv: Contains features for testing predictions.

## Features:
- Demographic data: Age, income, education level, etc.
- Health behaviors: Wearing masks, washing hands, taking antiviral medications, etc.
- Opinions: Opinions about vaccine effectiveness, risks, and side effects.
- Medical history: Chronic conditions, presence of children, etc.
The goal is to predict two binary labels: h1n1_vaccine and seasonal_vaccine.

## Approach
1. Data Preprocessing:
- Handled missing values for numeric and categorical columns using median imputation and most frequent imputation, respectively.
- Applied one-hot encoding to categorical variables to prepare them for machine learning models.
2. Models Used:
Logistic Regression: For baseline classification of H1N1 and seasonal flu vaccines.
AdaBoost Classifier: Used for boosting performance and to handle class imbalances.
3. Hyperparameter Tuning:
Performed hyperparameter tuning using GridSearchCV to optimize n_estimators and learning_rate for the AdaBoost model.
4. Model Evaluation:
- Used Area Under the ROC Curve (AUC) to evaluate model performance for both Logistic Regression and AdaBoost.
- Displayed confusion matrices to analyze true positives, false positives, true negatives, and false negatives.
- Identified the most important features for both vaccines using AdaBoost feature importance.

## Results
Best Model: AdaBoost was the best performing model with AUC scores of:
- H1N1 Vaccine: 0.85 AUC
  - Seasonal Flu Vaccine: 0.83 AUC
Key Insights:
- The most important features for predicting H1N1 vaccination include the level of concern about H1N1 and opinions about the vaccine’s effectiveness.
- For seasonal flu, health worker status and opinions about seasonal flu vaccines were the most important predictors.
