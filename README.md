# Decision Trees, LASSO, and Boosting for Regression

This repository contains solutions and implementations for interpretable decision trees and advanced regression techniques, including LASSO and boosting. The tasks use two datasets: **Acute Inflammations** and **Communities and Crime**.

---

## Table of Contents

- [Introduction](#introduction)
- [Data](#data)
- [Project Tasks](#project-tasks)
  - [Decision Trees as Interpretable Models](#decision-trees-as-interpretable-models)
  - [The LASSO and Boosting for Regression](#the-lasso-and-boosting-for-regression)
- [Results](#results)

---

## Introduction

This project covers:
1. Decision trees for interpretable classification using the **Acute Inflammations** dataset.
2. Advanced regression techniques like Ridge Regression, LASSO, Principal Component Regression (PCR), and Boosting for the **Communities and Crime** dataset.

This project was done as part of an assignment for my graduate Machine Learning course.

---

## Data

### Acute Inflammations Dataset
- **Description**: The dataset consists of attributes for diagnosing acute inflammations in humans.

### Communities and Crime Dataset
- **Description**: The dataset contains demographic and socio-economic factors to predict crime rates. Some features are non-predictive and need to be ignored.

---

## Project Tasks

### Decision Trees as Interpretable Models

1. **Build a Decision Tree**:
   - Train a decision tree on the entire dataset and plot the tree.

2. **Convert Decision Rules**:
   - Translate the decision tree into a set of IF-THEN rules for interpretability.

3. **Pruning for Interpretability**:
   - Use cost-complexity pruning to create a minimal decision tree.
   - Translate the pruned tree into decision rules.

---

### The LASSO and Boosting for Regression

1. **Data Preparation**:
   - Use the **Communities and Crime Dataset**.
   - Split the data: first 1495 rows for training and the rest for testing.
   - Handle missing values using an imputation technique.
   - Ignore non-predictive features as specified in the dataset documentation.

2. **Correlation Analysis**:
   - Compute and plot the correlation matrix for the features.

3. **Feature Selection with Coefficient of Variation (CV)**:
   - Calculate the CV for each feature using:
     \[
     CV = \frac{s}{m}
     \]
     where \( s \) is the standard deviation and \( m \) is the mean.
   - Select \( \lfloor \sqrt{128} \rfloor \) features with the highest CV.
   - Create scatter plots and box plots for the selected features.

4. **Linear Model**:
   - Fit a linear regression model using least squares on the training set.
   - Report the test error.

5. **Ridge Regression**:
   - Fit a ridge regression model with \( \lambda \) chosen by cross-validation.
   - Report the test error.

6. **LASSO Regression**:
   - Fit a LASSO model with \( \lambda \) chosen by cross-validation.
   - Report the test error and the variables selected.
   - Repeat the process with standardized features and compare the results.

7. **Principal Component Regression (PCR)**:
   - Fit a PCR model with the number of components \( M \) chosen by cross-validation.
   - Report the test error.

8. **Boosting**:
   - Fit a gradient boosting model using **XGBoost**.
   - Use L1-penalized regression at each node to handle the large number of variables.
   - Report the test error and compare with other models.

---

## Results

- **Decision Trees**:
  - Generated interpretable IF-THEN rules from decision trees.
  - Pruned decision trees improved interpretability with minimal performance loss.
- **Regression**:
  - Ridge Regression, LASSO, and PCR were compared on test error.
  - Boosting demonstrated improved predictive performance.

---
