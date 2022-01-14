# Predicting Credit Card Customer Churn
Abeer Alahmadi


## Abstract
The goal of this project is to use classification models to predict customer who might churn to help the credit card company to proactively select customers and provide them with special offers and better services.
I worked on the data provided by [Kaggle](https://www.kaggle.com/sakshigoyal7/credit-card-customers?select=BankChurners.csv) which contains credit card customers data, by leveraging users demografics and feature engineering to develop and compare 3 prediction models (Logistic Regression, Naive Bayes, K-Nearest Neighbors) to predict which customers are most likely to churn.
Some challenges I had to overcome developing models are the unbalanced ratio of customers who churned and customers who stayed, which I had to use an Over-Sampling mechanisms using [SMOTE](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTE.html) which created synthetic records of data to balance the number of churned data in the dataset. Another challage whas the number of features provided in the dataset was big, and selecting the feature was challenging, therefore I have used a feature selecting technique called [Recursive Feature Elimination](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.RFE.html) which is a feature selection method that fits a model and removes the weakest features by recursively considering smaller and smaller sets of features to give me the features with the greatest impact in the dataset.

## Design
The dataset provided by kaggle contains 10127 customer records and 23 features (6 categorical features, 17 numerical features). A few features were analyzed in the EDA phase like the distibution of Gender, Age, Income, Marital Status and Education Level.

## Algorithms
#### Feature Engineering
* Converting categorical features to binary dummy variables
* Over-Sampling using SMOTE 
* Feature selection using Recursive Feature Elimination 
#### Models
* Logistic regression
* Naive Bayes
* K-nearest Neighbors
#### Model Evaluation
* accuracy_score
* roc_auc_score 
* recall_score 
* confusion_matrix 

## Tools
* Numpy and Pandas for data manipulation
* Plotly for interactive visualization
* Scikit-learn for data processing and modeling