# Customer Churn Prediction Using Naive Bayes

## 🎯 Modeling Objective
The objective of this project is to develop and evaluate a Naive Bayes model for predicting customer churn using banking data.
Churn refers to customers leaving the bank, and by identifying them early, targeted actions—such as offering promotions or incentives—can be taken to improve customer retention.

## 🎯 Target Variable
The target variable is Exited, where:

0 = Customer stayed

1 = Customer left (churned)

The model is designed to predict whether each customer falls into the 0 or 1 category.

## 🛠️ Model Design
This is a binary classification task.
I chose the GaussianNB implementation of Naive Bayes because it is suitable for continuous variables and assumes a normal distribution.
Although the dataset does not perfectly meet these assumptions, GaussianNB often provides reliable results even with real-world imperfections.

## 📊 Dataset Features
![Diagram](images/dataset_preview.png)
The dataset includes the following features:
* CreditScore
* Age
* Tenure
* Balance
* NumOfProducts
* HasCrCard
* IsActiveMember
* EstimatedSalary
* Exited
* Loyalty
* Geography

## 🧹 Data Preprocessing
The following preprocessing steps were applied:

* Dropped irrelevant columns: RowNumber, CustomerId, Surname, and Gender
* Encoded the Geography (categorical) column into numerical format
* Engineered a new feature called Loyalty, calculated as:
  Loyalty = Tenure / Age
* applied normalization

## ⚖️ Handling Imbalanced Data
The dataset is moderately imbalanced (~80% stayed vs. ~20% churned).
Since Naive Bayes predictions rely on class priors (P(c)), applying techniques like oversampling or undersampling would distort these natural priors.
For this reason, I retained the original class distribution and did not apply any balancing methods.
