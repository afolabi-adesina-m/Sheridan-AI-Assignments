# Sheridan-AI-Assignments
# 📊 Data Science Portfolio — Afolabi Adesina
**Course:** STAT53894 | **Institution:**  Sheridan College

A collection of end-to-end data science assignments covering exploratory data analysis, statistical hypothesis testing, and predictive modelling. Each project applies industry-standard Python libraries to real-world datasets.

---

## 🗂️ Projects Overview

| # | Project | Dataset | Key Techniques |
|---|---------|---------|----------------|
| 1 | [Exploratory Data Analysis —  Titanic](#1-exploratory-data-analysis--titanic) | Titanic (Seaborn) | EDA, Descriptive Stats, Visualizations |
| 2 | [Global Happiness Analysis](#2-global-happiness-analysis-2020-2024) | World Happiness Report 2025 | Data Cleaning, EDA, Multivariate Analysis |
| 3 | [Hypothesis Testing — The Waiter's Data Challenge](#3-hypothesis-testing--the-waiters-data-challenge) | Tips (Seaborn) | T-Test, Statistical Inference |
| 4 | [Predictive Modelling — Bank Marketing](#4-predictive-modelling--bank-marketing) | UCI Bank Marketing | Linear Regression, Classification, Precision-Recall |

---

## 1. Exploratory Data Analysis — Titanic
**File:** `STAT_53894_Assignment1_Afolabi_Adesina.ipynb`  
**Date:** January 28, 2026

### Overview
A full EDA of the classic Titanic passenger dataset, exploring the relationships between passenger demographics and survival outcomes.

### Key Tasks
- **Data Types:** Identified 10 categorical and 2 key numerical variables (`age`, `fare`)
- **Summary Statistics:** Computed mean, median, range, and IQR for numerical variables
- **Frequency Analysis:** Explored distributions of `sex` and passenger `class`
- **Visualizations:** Histograms and boxplots for numerical variables; bar charts with survival hue for categorical variables
- **Percentile Analysis:** Identified top 10% of fare spenders using percentile thresholds

### Key Findings
- Fare distribution is highly right-skewed — most passengers paid low fares with a few extreme outliers
- Passengers embarking from **Cherbourg** had a higher survival proportion compared to those from Southampton
- Age distribution is slightly right-skewed with a concentration of young adults

### Libraries Used
`pandas` · `numpy` · `seaborn` · `matplotlib`

---

## 2. Global Happiness Analysis (2020–2024)
**File:** `STAT_53894_Assignment2_Afolabi_Adesina.ipynb`  
**Date:** February 12, 2026

### Overview
An end-to-end analysis of global happiness trends using data from the World Happiness Report 2025, covering 2020–2024.

### Dataset
- **Source:** [World Happiness Report 2025](https://files.worldhappiness.report/WHR25_Data_Figure_2.1v3.xlsx)
- **Target Variable:** `Life Evaluation (3-year average)` — the Cantril Ladder happiness score

### Key Tasks
- **Data Cleaning:** Filtered records to 2020–2024; renamed columns for readability
- **Missing Value Imputation:** Applied country-specific mean imputation, followed by global median imputation for remaining gaps
- **Country Name Standardisation:** Resolved inconsistencies across 15+ country name variants (e.g., "Türkiye" → "Turkey", "Viet Nam" → "Vietnam")
- **EDA:** Explored distributions of happiness scores and contributing factors (GDP, social support, freedom, generosity, corruption)
- **Multivariate Analysis:** Visualized relationships between happiness and its explanatory components

### Key Features Analysed
`Log GDP per capita` · `Social Support` · `Healthy Life Expectancy` · `Freedom` · `Generosity` · `Perceptions of Corruption`

### Libraries Used
`pandas` · `numpy` · `seaborn` · `matplotlib`

---

## 3. Hypothesis Testing — The Waiter's Data Challenge
**File:** `STAT_53894_Assignment3_Afolabi_Adesina.ipynb`

### Overview
Statistical hypothesis testing on the Tips dataset to provide data-driven recommendations for a high-end restaurant's management. Each test follows a rigorous **6-Step Hypothesis Testing Process**.

### Dataset
- **Source:** Seaborn built-in `tips` dataset
- **Shape:** 244 records across 7 variables

### Key Tasks & Tests

#### Task 1 — T-Test: Do Male Customers Tip More?
- **H₀:** No significant difference in average tips between male and female customers
- **H₁ (one-tailed):** Male customers leave significantly higher tips
- **Method:** Welch's independent samples t-test (`equal_var=False`)
- **Finding:** Tested whether the ~$0.26 gap (Male: ~$3.09 vs Female: ~$2.83) is statistically significant at α = 0.05

### Methodology
Each task follows:
1. Define hypotheses → 2. Set significance level (α = 0.05) → 3. Analyse data → 4. Calculate test statistic → 5. Make a decision → 6. Interpret & provide business recommendation

### Libraries Used
`pandas` · `numpy` · `seaborn` · `scipy.stats` · `matplotlib`

---

## 4. Predictive Modelling — Bank Marketing
**File:** `Assignment4_Folayinka_Afolabi.ipynb`  
**Team:** Folayinka Olaofe & Afolabi Adesina

### Overview
A full predictive modelling pipeline on the UCI Bank Marketing dataset, combining regression and multi-model classification to predict client behaviour from telephone marketing campaigns.

### Dataset
- **Source:** [UCI Machine Learning Repository — Bank Marketing](https://archive.ics.uci.edu/dataset/222/bank+marketing)
- **Size:** 45,211 rows × 17 columns
- **Regression Target:** `duration` — length of last phone call in seconds (continuous)
- **Classification Target:** `y` — did the client subscribe to a term deposit? (binary: yes/no)

### Key Tasks

#### Task 1 — Dataset Selection & Problem Definition
- Validated data quality: no missing values
- Documented full data dictionary with variable types and roles
- Identified factor variables: `job`, `education`, `marital`

#### Task 2 — Linear Regression: Predicting Call Duration
- 80/20 train-test split
- OLS regression via `statsmodels`
- Evaluated with **R²** and **RMSE**
- Residual plot analysis for model diagnostics

#### Task 3 — Classification Model Comparison
- Stratified 5,000-row sample to handle class imbalance
- Trained and compared three models:
  - **Logistic Regression**
  - **Gaussian Naïve Bayes**
  - **Linear Discriminant Analysis (LDA)**
- Evaluated with confusion matrices and a model comparison table
- **Priority metric:** Recall (False Negatives are more costly in a marketing context)

#### Task 4 — Precision-Recall Evaluation
- Generated full Precision-Recall curves
- Built threshold comparison table to support business decision-making
- Analysed the trade-off between False Positives (wasted calls) and False Negatives (missed subscribers)

### Libraries Used
`pandas` · `numpy` · `matplotlib` · `seaborn` · `statsmodels` · `scikit-learn`

---

## 🛠️ Tech Stack

```
Language:    Python 3
Environment: Jupyter Notebook

Core Libraries:
  pandas       — Data manipulation & cleaning
  numpy        — Numerical computing
  matplotlib   — Plotting & visualisation
  seaborn      — Statistical visualisation
  scipy.stats  — Hypothesis testing
  statsmodels  — OLS regression & statistical modelling
  scikit-learn — Machine learning (classification, metrics, preprocessing)
```

---

## 📁 Repository Structure

```
├── STAT_53894_Assignment1_Afolabi_Adesina.ipynb   # EDA — Titanic
├── STAT_53894_Assignment2_Afolabi_Adesina.ipynb   # Global Happiness Analysis
├── STAT_53894_Assignment3_Afolabi_Adesina.ipynb   # Hypothesis Testing — Tips
├── Assignment4_Folayinka_Afolabi.ipynb            # Predictive Modelling — Bank Marketing
└── README.md
```

---

## 👤 Author
**Afolabi Adesina**  
Course: STAT53894
