# Cyber-Ransomware-Prediction-using-Machine-Learning-Comparing-Between-KNN-and-Naive-Bayes-
Machine Learning project for predicting high ransomware activity using a global cyber-attack dataset (77,623 rows. 225 countries, 14 months). Includes EDA, preprocessing, SMOTE balancing, Naive Bayes models, and optimized KNN with StandarScaler. Best model achieves F1-score 0.873 and ROC AUC 0.942.

# Overview 
This project analyzes a global cyber-attack dataset containing 77,623 records from 225 countries collected over 14 months (Oct 2022 - Dec 2023). 
The main objective is to predict whether a country experienced high ransomware activity on a given date 

The project includes:
* Data exploration (EDA)
* Handling missing value 
* Addressing class imbalance using SMOTE 
* Modeling with Naive Bayes and KNN (Compare between NB and KNN)
* Model Comparison and evaluation 

# Dataset 
Original data source:
https://github.com/DrSufi/CyberData

The dataset contains 18 fields:

* Attack date
* Country
* 8 cyber-attack percentage metrics (Spam, Ransomware, Exploit, Local Infection, etc.)
* 8 ranking features

The target variable (High_Ransomware) was created based on the 75th percentile cutoff of the Ransomware percentage.

# Tech Stack
* Python 3.x
* pandas, numpy
* scikit-learn
* seaborn, matplotlib
* imbalanced-learn (SMOTE)

# Exploratory Data Analysis

Key EDA steps:

* Identifying missing values
* Feature distribution analysis
* Correlation analysis
* Detecting class imbalance
* Outlier inspection

Visualizations:

* Correlation heatmap
* Missing value barplot
* Class distribution chart

# Data Preprocessing 
## ✔ Median Imputation

To handle missing values in percentage-based features.

## ✔ SMOTE (Oversampling)

The dataset is highly imbalanced:

* Before: 84% (class 0) vs 16% (class 1)
* After SMOTE: 50% – 50%

## ✔ Feature Scaling

Scaling applied only for KNN using StandardScaler.
