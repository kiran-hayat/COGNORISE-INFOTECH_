# Diabetes Prediction - Machine Learning Models

This repository contains a Jupyter Notebook for predicting **diabetes** based on various medical features. The dataset includes factors such as age, gender, hypertension, heart disease, smoking history, BMI, HbA1c level, and blood glucose level. The notebook explores several machine learning models and applies various ensemble techniques to improve prediction accuracy.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Ensemble Techniques](#ensemble-techniques)
- [Model Evaluation](#model-evaluation)
- [Conclusion](#conclusion)
- [Dependencies](#dependencies)

## Introduction

The goal of this notebook is to train machine learning models on a dataset containing medical information to predict whether an individual has diabetes. We use various classification algorithms and evaluate their performance using accuracy scores and cross-validation.

## Dataset

The dataset contains the following columns:
- **gender**: Gender of the patient (categorical)
- **age**: Age of the patient (numeric)
- **hypertension**: Whether the patient has hypertension (binary: 0 = No, 1 = Yes)
- **heart_disease**: Whether the patient has heart disease (binary: 0 = No, 1 = Yes)
- **smoking_history**: Smoking history of the patient (categorical)
- **bmi**: Body Mass Index (numeric)
- **HbA1c_level**: HbA1c level (numeric)
- **blood_glucose_level**: Blood glucose level (numeric)
- **diabetes**: Target variable indicating diabetes presence (binary: 0 = No, 1 = Yes)

## Data Preprocessing

The following preprocessing steps are applied to the dataset:
1. **Handling Missing Values**: The dataset is assumed to be complete, with no missing values.
2. **Encoding Categorical Features**: One-Hot Encoding is applied to the categorical columns: `gender` and `smoking_history`.
3. **Scaling Numeric Features**: Features such as `age`, `bmi`, `HbA1c_level`, and `blood_glucose_level` are scaled using **StandardScaler** to ensure all numeric features are on the same scale.

## Modeling

The following machine learning models are trained and evaluated:
- **Random Forest Classifier**
- **K-Nearest Neighbors (KNN)**
- **AdaBoost Classifier**
- **Logistic Regression**
- **Decision Tree Classifier**
- **Support Vector Classifier (SVC)**

Each model is trained and evaluated using **accuracy** as the evaluation metric.

## Ensemble Techniques

To improve the performance of individual models, the following ensemble techniques are applied:
1. **Voting Classifier**: A combination of models using majority voting (soft voting).
2. **Stacking Classifier**: Uses a meta-model to combine predictions of base models.
3. **Bagging Classifier**: Uses bootstrapped samples to train multiple models and aggregate their predictions.

## Model Evaluation

The accuracy of each individual model and ensemble technique is evaluated as follows:

| **Model**                        | **Accuracy**  |
|-----------------------------------|---------------|
| **Random Forest Classifier**      | 0.9695        |
| **K-Nearest Neighbors (KNN)**     | 0.9625        |
| **AdaBoost Classifier**           | 0.9719        |
| **Logistic Regression**           | 0.9586        |
| **Decision Tree Classifier**      | 0.9498        |
| **Support Vector Classifier (SVC)** | 0.9643        |
| **Voting Classifier**             | 0.9699        |
| **Stacking Classifier**           | 0.9711        |
| **Bagging Classifier**            | 0.9684        |

### **Best Model**:
- The **AdaBoost Classifier** achieved the highest accuracy of **0.9719**, making it the best model for this dataset.
- **Stacking Classifier** (0.9711) and **Voting Classifier** (0.9699) also performed well.

## Conclusion

After evaluating various machine learning models and ensemble techniques, the **AdaBoost Classifier** provides the best performance for diabetes prediction with an accuracy of **0.9719**. Ensemble methods like **Stacking** and **Voting** further improved the results.

## Dependencies

The following libraries are required to run the notebook:
- **pandas**: For data manipulation.
- **numpy**: For numerical operations.
- **matplotlib**: For visualizations.
- **seaborn**: For statistical plots.
- **scikit-learn**: For machine learning models and preprocessing.

To install the required libraries, use the following command:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Key Points:

- **Project Overview**: A brief summary of the project's goal.
- **Dataset Description**: Information about the dataset columns.
- **Preprocessing**: Describes how data is prepared for modeling.
- **Modeling**: Explanation of the models used.
- **Ensemble Techniques**: Describes how ensemble methods were applied.
- **Results**: Clear tabular representation of the model's accuracy.
- **Conclusion**: Best model recommendation based on accuracy.
