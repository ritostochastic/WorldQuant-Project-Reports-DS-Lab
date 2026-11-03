# Project 5: Bankruptcy Prediction in Poland and Taiwan Using Random Forests and Gradient Boosting

A supervised machine learning project focused on predicting corporate bankruptcy using financial indicators from companies in Poland and Taiwan.

## Project Overview

Financial distress prediction is an important application of statistical learning in credit risk analysis and corporate finance.

This project investigates how financial indicators can be used to distinguish between financially healthy and distressed companies. It applies tree-based ensemble learning techniques, with particular attention to the challenges associated with imbalanced classification data.

## Workflow

### 1. Data Preparation
- Prepared corporate financial datasets.
- Examined missing values and class distributions.
- Processed financial indicators for model development.

### 2. Handling Class Imbalance
- Investigated the imbalance between bankrupt and non-bankrupt observations.
- Considered techniques for improving model performance on the minority class.

### 3. Ensemble Modeling
- Applied Random Forest classification.
- Explored Gradient Boosting methods.
- Compared the predictive behavior of tree-based ensemble approaches.

### 4. Model Evaluation
- Evaluated classification performance using suitable metrics.
- Examined the models' ability to identify financially distressed companies.
- Investigated the contribution of financial indicators to model predictions.

## Key Takeaways

- Bankruptcy prediction is a challenging classification problem, particularly when positive cases are relatively rare.
- Ensemble methods can capture nonlinear relationships between financial indicators and bankruptcy outcomes.
- Evaluation should account for the cost of failing to identify a financially distressed company.

## Technologies

- Python
- pandas
- NumPy
- scikit-learn
- Matplotlib
- Seaborn
