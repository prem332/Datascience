# Loan Approval Prediction System

This project is a **Loan Approval Prediction System** that predicts whether a loan will be approved or rejected based on various features related to the applicant's financial and personal information. The system is built using **XGBoost** due to its highest accuracy compared to other models. The project includes a Flask web application for making predictions based on user input.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Models and Performance](#models-and-performance)
- [Challenges](#challenges)

## Overview

The Loan Approval Prediction System helps financial institutions assess whether a loan should be approved or not. Various classification models like Logistic Regression, Support Vector Machines, Decision Trees, Random Forests, K-Nearest Neighbors, and XGBoost were used, with **XGBoost** achieving the highest accuracy of 98.13%.

## Features

- Prediction of loan approval based on user input.
- Flask-based web interface.
- Uses **XGBoost** for final predictions after model comparison.
- Preprocessing using StandardScaler and OneHotEncoder.

## Dataset

The dataset used contains various features such as:
- No. of dependents
- Income per annum
- Loan amount
- Loan term
- CIBIL score
- Asset values (residential, commercial, luxury)
- Education status
- Self-employment status

The dataset is preprocessed, including handling outliers using the IQR method and standardizing numerical features.
  

## Usage

Once the Flask application is running, access the web interface by navigating to `http://127.0.0.1:5000/` in your browser.

Enter the required input values for the loan applicant, such as number of dependents, income, loan amount, etc., and the system will return whether the loan is approved or rejected along with the probability.

## Technologies Used

- **Python**: Programming language.
- **XGBoost**: Machine learning model for classification.
- **Flask**: Web framework used to build the web application.
- **scikit-learn**: For preprocessing and other machine learning tasks.
- **pandas**: For data manipulation and analysis.
- **seaborn** and **matplotlib**: For data visualization.

## Models and Performance

Various machine learning models were tested on the dataset, and the following results were obtained:

| Model                    | Accuracy  |
|---------------------------|-----------|
| Logistic Regression        | 91.10%    |
| Support Vector Machine     | 93.44%    |
| Decision Tree Classifier   | 97.66%    |
| Random Forest Classifier   | 97.54%    |
| K-Nearest Neighbors (KNN)  | 90.05%    |
| **XGBoost**                | **98.13%**|

## Challenges

- **Handling Imbalanced Data**: The dataset was slightly imbalanced with more approved loans than rejected ones, making it crucial to evaluate metrics beyond just accuracy, such as precision and recall.
- **Outlier Detection and Removal**: Outliers in asset values and income data skewed model performance initially. Using the IQR method helped to mitigate this.
- **Feature Engineering**: Determining which features (like financial assets or education) contributed most to loan approval decisions was a critical step to improving model performance.
