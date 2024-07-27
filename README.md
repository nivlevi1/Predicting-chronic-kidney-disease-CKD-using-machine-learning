# Predicting chronic kidney disease (CKD) using Machine Learning
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/nivlevi1/Predicting-chronic-kidney-disease-CKD-using-machine-learning/HEAD)
Technical Report: Applications of Machine Learning in Medicine
Faculty of Engineering, Ariel University
Department of Industrial Engineering and Management
Date: 28.07.24

Abstract
This report investigates the effectiveness of supervised Machine Learning techniques for predicting Chronic Kidney Disease (CKD) using a dataset collected from patients hospitalized in 2008, with follow-up data available until 2017. Various Machine Learning models, including Logistic Regression, Decision Trees, Random Forests, and Support Vector Machines (SVM), were applied to the dataset. The models were evaluated based on their ability to accurately predict the onset of CKD events, with feature selection methods used to enhance model performance. The findings suggest that Random Forest models coupled with feature selection techniques provide a robust approach to predicting CKD.

Introduction and Purpose of the Work
Chronic Kidney Disease (CKD) is a significant public health issue characterized by a gradual loss of kidney function over time. Early prediction and diagnosis of CKD can lead to better patient outcomes and reduced healthcare costs. This work assesses the effectiveness of different supervised Machine Learning algorithms in predicting CKD events. By leveraging a comprehensive dataset with various clinical features, we aim to identify the most predictive factors and evaluate the performance of different models in forecasting CKD progression.

Methods
Data Collection
The dataset includes clinical data from 421 patients hospitalized in 2008, with follow-up data collected until 2017. Variables include age, BMI, history of various diseases, medication use, and baseline measurements of cholesterol, creatinine, blood pressure, and estimated glomerular filtration rate (eGFR).

Exploratory Data Analysis (EDA)
Summary Statistics: Overview of data distribution.
Distribution Plots: Histograms and density plots revealed variable skewness.
Box Plots: Identified and mitigated outliers.
Categorical Analysis: Pie charts visualized demographic and diagnostic variables.
Handling Outliers
Outliers were capped at the 2.5th and 97.5th percentiles to reduce their impact on model performance.

Preprocessing
Handling Missing Values: Imputed using statistical methods.
Encoding Categorical Variables: Applied one-hot and binary encoding.
Normalization: Standardized numerical features.
Features Selection
SelectKBest: Identified top features based on ANOVA F-value.
RFECV: Determined optimal feature set using cross-validation.
RFE Feature Importance: Visualized feature importance.
Handling Class Imbalance
Techniques Explored: Over-sampling, SMOTE, and Under-sampling.
Chosen Method: SMOTE for generating synthetic samples.
Model Training and Evaluation
Initial Training with SMOTE: Evaluated Logistic Regression, Decision Tree, Random Forest, and SVM.
Hyperparameter Tuning: Improved performance metrics for all models.
Comparison with Models without SMOTE: Notable differences in precision-recall trade-offs and F1 scores.
Explanatory AI: SHAP Model Analysis
Logistic Regression: Identified key features affecting class probability.
Decision Tree and Random Forest: Analyzed feature impacts.
SVM: Evaluated feature importance and impact on class probability.
Subgroup Analysis Using K-means Clustering
Optimal Number of Clusters: Identified five distinct patient subgroups.
Cluster Characteristics: Analyzed subgroup traits related to CKD risk.
Findings
Model Performance: SVM and Random Forest models excelled, with improved recall and F1 scores due to SMOTE and hyperparameter tuning.
Feature Importance: TimeToEventMonths was the most influential feature.
Patient Subgroups: Identified five clusters with distinct characteristics.
Conclusion
Machine learning techniques, particularly SVM and Random Forest, demonstrated effectiveness in predicting CKD progression. The use of SMOTE for class balancing and feature importance analysis provided robust results. The study highlights the importance of monitoring key biomarkers and suggests personalized treatment approaches based on patient subgroups.
