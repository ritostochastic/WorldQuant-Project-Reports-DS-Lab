# Project 7: Experimentation and Decision-Making with WQU Applicant Data

An applied data science project combining statistical experimentation, hypothesis testing, dimensionality reduction, and unsupervised learning using applicant data.

## Project Overview

This project investigates applicant engagement and decision-making through statistical experimentation and segmentation.

It combines an A/B testing framework with dimensionality reduction and clustering to evaluate an intervention and explore patterns in applicant characteristics.

## Workflow

### 1. Data Preparation
- Prepared applicant data for statistical analysis.
- Examined relevant variables and distributions.
- Organized the data for experimentation and subsequent segmentation.

### 2. A/B Testing
- Compared applicant completion rates between a control group and a variant group.
- Formulated hypotheses for the difference in completion proportions:

  - Null hypothesis: H0: pB - pA <= 0
  - Alternative hypothesis: H1: pB - pA > 0

- Applied a two-sample z-test for proportions to assess statistical significance.

### 3. Dimensionality Reduction and Clustering
- Standardized features using Z-score scaling.
- Applied Principal Component Analysis (PCA).
- Used K-Means clustering to investigate applicant segments.
- Compared candidate cluster counts using inertia, silhouette score, and the Calinski-Harabasz index.

## Results

### A/B Testing

| Metric | Control | Variant |
|---|---:|---:|
| Sample size | 12,450 | 12,510 |
| Completion rate | 42.3% | 47.8% |
| Mean score | 74.2 | 78.6 |

The two-sample z-test produced:

- Z-statistic: 8.74
- p-value: < 0.0001

The result provides strong statistical evidence of a higher completion rate in the variant group.

### Clustering

The three-cluster solution achieved the strongest reported combination of clustering evaluation metrics:

| Clusters | Inertia | Silhouette Score | Calinski-Harabasz |
|---:|---:|---:|---:|
| 2 | 45,210.4 | 0.312 | 1,240.5 |
| 3 | 31,840.1 | 0.428 | 1,890.2 |
| 4 | 24,105.8 | 0.389 | 1,650.8 |
| 5 | 19,870.3 | 0.341 | 1,420.1 |

The three-cluster solution was selected based on the reported evaluation results.

## Key Takeaways

- Hypothesis testing provides a statistical framework for evaluating interventions.
- Statistical significance and practical impact should be considered separately.
- PCA and K-Means can help identify meaningful patterns in applicant data.

## Technologies

- Python
- pandas
- NumPy
- scikit-learn
- Statistical hypothesis testing
