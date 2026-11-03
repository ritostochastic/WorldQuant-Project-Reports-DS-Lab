# Project 01 — Mexican Real Estate Data Analysis

## Overview

This project explores the Mexican real estate market through exploratory data analysis, data cleaning, statistical inspection, and regional property valuation.

The primary objective is to investigate how property prices vary across different geographical regions of Mexico, with particular emphasis on price per square meter (USD/m²). The analysis also establishes a structured data-cleaning workflow to address inconsistencies, missing observations, and statistical outliers before drawing meaningful conclusions.

This report documents my understanding and independent application of the data analysis techniques explored during the WorldQuant University Data Science Lab.

## Objectives

- Inspect and understand the structure and quality of the real estate dataset.
- Identify missing values, inconsistent data types, and improperly formatted numerical attributes.
- Develop a systematic data-cleaning and preprocessing workflow using Python.
- Apply statistical techniques to identify and handle extreme observations.
- Examine regional differences in property valuations using price per square meter.
- Interpret the findings and identify potential directions for further analysis.

## Methodology

The project follows a structured analytical workflow:

1. **Data Inspection:** Examine dataset dimensions, column information, data types, sample observations, and missing-value distributions using Pandas.

2. **Data Cleaning and Preprocessing:** Parse string-encoded numerical attributes, standardise data types, and handle missing or invalid observations.

3. **Statistical Outlier Detection:** Apply Z-score thresholds and the Interquartile Range (IQR) method to identify potentially erroneous extreme values.

4. **Exploratory Data Analysis:** Investigate distributions and descriptive statistics to understand property prices and area measurements.

5. **Regional Valuation Analysis:** Calculate and compare average property prices per square meter across selected Mexican states.

6. **Interpretation:** Evaluate geographical price discrepancies and consider their implications for subsequent predictive modelling.

## Key Findings

- Data quality issues, including missing property-area measurements and inconsistently formatted price values, required attention before meaningful analysis.
- Approximately 18.4% of property listings lacked valid area dimensions.
- Statistical outlier handling helped address extreme observations that could distort valuation metrics.
- Distrito Federal (CDMX) exhibited the highest mean property valuation per square meter among the selected regions, at approximately USD 2,130.43/m².
- Yucatán recorded the lowest mean valuation among the selected regions, at approximately USD 864.86/m².
- The findings indicate substantial geographical variation in property valuations, highlighting the importance of location as an analytical factor.

## Tools and Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Statistical analysis and exploratory data analysis techniques

## Learning Outcomes

Through this project, I strengthened my understanding of:

- Structured data inspection and quality assessment.
- Handling missing values and inconsistent numerical representations.
- Statistical outlier detection using Z-scores and IQR.
- Vectorised data manipulation and preprocessing with Pandas.
- Exploratory analysis and descriptive statistics.
- Translating analytical findings into meaningful interpretations.

## Scope for Further Exploration

Potential extensions of this analysis include:

- Incorporating geographical coordinates and neighbourhood-level information.
- Investigating the relationship between property area, location, and valuation.
- Exploring predictive modelling approaches for property price estimation.
- Examining whether regional valuation patterns remain consistent across different property categories.

## Report

The accompanying PDF contains the detailed methodology, statistical formulations, visualisations, analysis, and conclusions developed for this project.

**Author:** Ritobroto Chandra  
**Programme:** WorldQuant University — Data Science Lab  
**Project:** 01 of 08

---

*This documentation represents my own understanding, interpretation, and application of the analytical concepts explored during the programme. It is not an official WQU publication and does not reproduce coursework answers, assessment solutions, or restricted course materials.*
