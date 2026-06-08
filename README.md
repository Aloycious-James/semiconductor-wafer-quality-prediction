# Semiconductor Wafer Quality Prediction Using Machine Learning

## Project Overview

This project predicts semiconductor wafer pass/fail outcomes using machine learning techniques. The dataset contains manufacturing sensor measurements collected during semiconductor production.

The objective is to identify critical process indicators that influence wafer quality and assist engineers in improving manufacturing performance.

## Problem Statement

Semiconductor manufacturing involves hundreds of sensors monitoring production processes. Defective wafers increase production costs and reduce yield.

This project develops a machine learning model capable of predicting wafer quality based on sensor measurements.

## Dataset

* Total Records: 1567
* Features: 562 sensor measurements after preprocessing
* Target Variable:

  * 0 = Fail
  * 1 = Pass

## Data Preprocessing

* Removed columns with excessive missing values
* Filled missing values using median imputation
* Converted target labels to binary format
* Applied SelectKBest feature selection
* Reduced features from 562 to 50
* Addressed class imbalance using SMOTE

## Machine Learning Models

### Logistic Regression

Used as a baseline model.

### Random Forest Classifier

Used as the final predictive model.

Parameters:

* n_estimators = 300
* max_depth = 15
* class_weight = balanced

## Model Evaluation

Metrics Used:

* Precision
* Recall
* F1 Score
* ROC-AUC

### Results

* ROC-AUC Score: 0.798
* Feature Selection: Top 50 sensors
* Feature Importance Analysis: Top 10 influential sensors identified

## Key Findings

The feature importance analysis revealed the most influential sensors affecting wafer quality prediction.

These sensors can be prioritized for:

* Process monitoring
* Equipment maintenance
* Quality control
* Root cause analysis

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn
* Imbalanced-Learn

## Business Impact

This solution demonstrates how machine learning can support semiconductor manufacturers by identifying critical process indicators and improving production quality monitoring.
