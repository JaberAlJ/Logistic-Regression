# Diabetes Logistic Regression

> Written by: [*JaberAlJ*](https://github.com/JaberAlJ)

---

## 1. Project Overview

This repository implements a Logistic Regression model to predict diabetes based on patient medical data. The goal is to analyze, preprocess, and model the data using scikit-learn, and evaluate the performance of the model.

## 2. 📦 Library Imports

The following libraries were used throughout the repository:

* `pandas` for data manipulation
* `numpy` for numerical operations
* `seaborn` and `matplotlib.pyplot` for visualization
* `sklearn.model_selection` for splitting the dataset
* `sklearn.preprocessing` for scaling features
* `sklearn.linear_model` for implementing logistic regression
* `sklearn.metrics` for evaluation metrics

## 3. 📊 Dataset Description

The dataset used includes several medical predictor variables and one target variable (Outcome). Predictor variables include:

* Pregnancies
* Glucose
* BloodPressure
* SkinThickness
* Insulin
* BMI
* DiabetesPedigreeFunction
* Age

Target variable:

* Outcome (0 or 1, indicating non-diabetic or diabetic)

## 4. 🔍 Initial Data Assessment

* Loaded dataset from `diabetes.csv`.
* Displayed the first few rows using `.head()`.
* Used `.info()` and `.describe()` to understand the structure and summary statistics of the data.

## 5. 🧹 Data Cleaning

* Identified zero values in some numeric columns that are not possible (e.g., BMI, Glucose).
* Replaced invalid zero values with NaN.
* Used `.isnull().sum()` to check for missing values.

## 6. 🔢 Data Encoding

* No categorical variables required encoding.
* Target variable `Outcome` was already in numeric binary format.

## 7. 🛠️ Data Preparation

* Replaced missing values using `median()` of each column.
* Scaled features using `StandardScaler` to normalize the data.
* Split the data into training and test sets using `train_test_split`.

## 8. 🤖 Model Selection & Evaluation

* Used `LogisticRegression` from scikit-learn.
* Fitted the model on training data.
* Made predictions on test data.
* Evaluated performance using:

  * Accuracy score
  * Confusion matrix
  * Classification report
