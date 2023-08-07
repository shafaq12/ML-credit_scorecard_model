# ML-credit_scorecard_model


This repository contains code to perform credit score modeling and generate a scorecard using the TOAD package. The goal is to build a predictive model to assess the creditworthiness of customers and create a scorecard that assigns a credit score to each individual.

## Table of Contents

1. Data Preprocessing
2. Feature Filtering
3. Feature Binning
4. Transform to WOE (Weight of Evidence)
5. Model Tuning
6. Model Production
7. Scorecard Generation
8. Distribution Analysis
9. Threshold Tuning
10. Loss and Coverage Analysis

## 1. Data Preprocessing

The `data_split` function is used to split the dataset into training and testing sets based on a given date column. The `target_info` function provides information about the target variable's distribution.

## 2. Feature Filtering

Features are filtered based on missing value rates, Information Value (IV), and correlation. The `toad.selection.select` function is used for feature selection, and an exclude list is provided to exclude certain columns.

## 3. Feature Binning

Continuous features are binned to transform them into categorical variables. Binning is done using the `toad.transform.Combiner` class, and chi-square binning is employed for stability.

## 4. Transform to WOE

Features are transformed into Weight of Evidence (WOE) using the `toad.transform.WOETransformer` class. This transformation enhances model interpretability and performance.

## 5. Model Tuning

The `GradientBoostingClassifier` is trained and evaluated using KS and AUC metrics. Feature importance is calculated to understand the impact of each feature on the model's performance.

## 6. Model Production

A logistic regression model is trained and evaluated. ROC and precision-recall curves are plotted for model evaluation.

## 7. Scorecard Generation

A scorecard is generated using the `toad.ScoreCard` class. The scorecard assigns a credit score to individuals based on their feature values.

## 8. Distribution Analysis

The distribution of credit scores is analyzed using histograms. Both test set and entire dataset distributions are visualized.

## 9. Threshold Tuning

Credit score thresholds are tuned to balance loss and coverage. Different threshold levels are analyzed to find a suitable trade-off.

## 10. Loss and Coverage Analysis

Loss and coverage analysis is performed for each credit score level. This analysis helps determine the effectiveness of the credit score thresholds.

Please refer to the code for detailed implementation and further information.

## Dependencies

The following Python libraries are used in this project:

- pandas
- sklearn
- numpy
- math
- seaborn
- matplotlib
- toad

## How to Use

1. Install the required dependencies using `pip install pandas sklearn numpy seaborn matplotlib toad`.

2. Run the code step by step in a Python environment to perform credit score modeling and scorecard generation.

3. Review the generated scorecard, distribution analysis, threshold tuning, and loss-coverage analysis to make informed decisions regarding credit risk assessment.

.
