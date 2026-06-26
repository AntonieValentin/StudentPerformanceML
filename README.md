# OUALD Student Performance ML

A Python machine learning project built around the Open University Learning Analytics Dataset. The goal is to explore student-related data, prepare it for training, and build models for two tasks: predicting the final course result and estimating the final coursework score.

The project follows a typical ML workflow: exploratory data analysis, preprocessing, feature encoding, model training, and evaluation.

## Overview

The dataset contains information about students enrolled in online university modules. Each row describes a student using attributes such as module code, presentation, gender, region, education level, age group, previous attempts, studied credits, and disability status.

Two targets are used:

* `final_result` - multiclass classification with labels such as `Withdrawn`, `Fail`, `Pass`, and `Distinction`;
* `final_coursework_score` - regression target representing the final coursework score.

## Exploratory Data Analysis

The first part of the project focuses on understanding the dataset before training any model. The analysis includes both numerical and categorical attributes, class balance, missing values, and correlations between features.

The EDA step is used to decide which preprocessing choices make sense, instead of applying transformations blindly.

Typical visualizations include:

* histograms for categorical attributes;
* boxplots for numerical features;
* class distribution plots;
* correlation plots for selected attributes.

## Preprocessing

The preprocessing pipeline prepares the data for classical machine learning models. It handles missing values, outliers, categorical attributes, and numerical scaling.

Main steps include:

* separating the classification and regression targets;
* imputing missing values;
* detecting and treating outliers in numerical columns;
* encoding categorical features;
* standardizing numerical features where needed;
* keeping the same transformations for training, validation, and test data.

## Models

The project trains and compares models for both classification and regression.

For classification, a decision tree is used as a baseline, followed by experiments with different hyperparameters and other suitable models. The evaluation focuses not only on accuracy, but also on precision, recall, F1-score, and confusion matrices.

For regression, linear regression is used as a baseline. Regularized models are also tested to observe how they affect the prediction error and generalization on validation data.

## Evaluation

The models are compared through structured experiments. Each relevant change is tracked, such as preprocessing choices, hyperparameters, and model type.

Classification results are evaluated using:

* accuracy;
* precision;
* recall;
* F1-score;
* confusion matrix.

Regression results are evaluated using:

* MAE;
* MSE;
* RMSE;
* R² score;
* train and validation error curves.

## Notes

The focus of this project is not just obtaining a good score, but understanding why a model behaves the way it does. The experiments are built gradually, starting from simple baselines and improving them through preprocessing and hyperparameter tuning.

The final result is a compact ML pipeline for analyzing student data and comparing classical models on both classification and regression tasks.
