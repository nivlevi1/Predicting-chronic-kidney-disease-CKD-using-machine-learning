# Predicting chronic kidney disease (CKD) using Machine Learning
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/nivlevi1/Predicting-chronic-kidney-disease-CKD-using-machine-learning/HEAD)

## Technical Report: Applications of Machine Learning in Medicine
**By: Niv Levi - nivvlevi@gmail.com & Yogev Ladani - yogevld123@gmail.com**  
**Faculty of Engineering, Ariel University**  
**Department of Industrial Engineering and Management**

**Abstract**: This report investigates the effectiveness of supervised Machine Learning techniques for predicting Chronic Kidney Disease (CKD).  
**Lecturer**: Dr. Orit Refaeli  
**Date**: 28.07.24

---

## Table of Contents

1. [Abstract](#abstract)
2. [Introduction and Purpose of the Work](#introduction-and-purpose-of-the-work)
3. [Methods](#methods)
   - [Data Collection](#data-collection)
   - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
   - [Handling Outliers](#handling-outliers)
   - [Preprocessing](#preprocessing)
   - [Features Selection](#features-selection)
   - [Handling Class Imbalance](#handling-class-imbalance)
   - [Model Training and Evaluation](#model-training-and-evaluation)
4. [Explanatory AI: SHAP Model Analysis](#explanatory-ai-shap-model-analysis)
5. [Subgroup Analysis Using K-means Clustering](#subgroup-analysis-using-k-means-clustering)
6. [Findings](#findings)
7. [Conclusion](#conclusion)
8. [Bibliography](#bibliography)

---

## Abstract

This report investigates the effectiveness of supervised Machine Learning techniques for predicting Chronic Kidney Disease (CKD) using a dataset collected from patients hospitalized in 2008 with follow-up data available until 2017. Various Machine Learning models, including Logistic Regression, Decision Trees, Random Forests, and Support Vector Machines (SVM), were applied to the dataset. The models were evaluated based on their ability to accurately predict the onset of CKD events, with feature selection methods used to enhance model performance. The findings suggest that Random Forest models coupled with feature selection techniques provide a robust approach to predicting CKD.

## Introduction and Purpose of the Work

Chronic Kidney Disease (CKD) is a significant public health issue characterized by a gradual loss of kidney function over time. Early prediction and diagnosis of CKD can lead to better patient outcomes and reduced healthcare costs. Machine Learning offers a powerful toolset for predictive analytics in healthcare, potentially enabling earlier interventions and better resource allocation. The purpose of this work is to assess the effectiveness of different supervised Machine Learning algorithms in predicting CKD events. By leveraging a comprehensive dataset with various clinical features, we aim to identify the most predictive factors and evaluate the performance of different models in forecasting CKD progression. This study explores the predictive power of various models and provides insights into the clinical features most strongly associated with CKD development. 

## Methods

### Data Collection

The dataset includes clinical data from 421 patients hospitalized in 2008, with follow-up data collected until 2017. Variables include age, BMI, history of various diseases, medication use, and baseline measurements of cholesterol, creatinine, blood pressure, and estimated glomerular filtration rate (eGFR).

### Exploratory Data Analysis (EDA)

EDA was performed to understand data distribution, patterns, and outliers:
- **Summary Statistics**: Overview of numerical columns.
- **Distribution Plots**: Histograms and density plots.
- **Box Plots**: Identified outliers and applied capping at 2.5th and 97.5th percentiles.
- **Categorical Analysis**: Pie charts for demographic and diagnostic variables.

### Handling Outliers

Outliers were capped at the 2.5th and 97.5th percentiles to mitigate their impact on model performance.

### Preprocessing

- **Handling Missing Values**: Imputation based on average values by segmentation.
- **Encoding Categorical Variables**: One-hot and binary encoding.
- **Normalization of Numerical Features**: Standard scaling of features.

### Features Selection

A two-step approach was used:
1. **SelectKBest**: Identified top features.
2. **RFECV (RFE with Cross-Validation)**: Determined the optimal number of features.

### Handling Class Imbalance

Addressed using:
1. **Over-sampling**
2. **SMOTE**: Synthetic Minority Over-sampling Technique.
3. **Under-sampling**

**Chosen Method**: SMOTE

### Model Training and Evaluation

Models were trained using SMOTE-balanced data and evaluated on the original test set:
- **Logistic Regression**
- **Decision Tree**
- **Random Forest**
- **SVM**

Hyperparameter tuning was applied, and models were also evaluated without SMOTE.

## Explanatory AI: SHAP Model Analysis

SHAP analysis provided insights into feature importance:
- **Logistic Regression**
- **Decision Tree**
- **Random Forest**
- **SVM**

## Subgroup Analysis Using K-means Clustering

K-means clustering identified five distinct patient subgroups, visualized using PCA. Performance metrics for models incorporating clustering insights are provided.

## Findings

- **Model Performance**: SVM and Random Forest performed best, with improvements noted from SMOTE and hyperparameter tuning.
- **Feature Importance**: TimeToEventMonths was the most influential feature.
- **Patient Subgroups**: Five distinct clusters were identified, reflecting varying disease progression patterns.

## Conclusion

The study demonstrates the effectiveness of Machine Learning techniques in predicting CKD progression. SVM and Random Forest models, combined with SMOTE for class balancing, offer robust predictive performance. The findings emphasize the importance of regular monitoring and personalized treatment strategies based on patient subgroups.

---


