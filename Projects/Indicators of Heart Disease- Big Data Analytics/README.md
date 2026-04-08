<div align="center">

# Heart Disease Risk Analysis & Prediction

### Big Data Analytics Project using CDC Health Indicators, Exploratory Analysis, and Machine Learning

<p>
  A data-driven study on heart attack risk factors using large-scale public health survey data, combining
  data cleaning, feature engineering, exploratory analysis, imbalance handling, and predictive modeling.
</p>

</div>

---

## Overview

This project analyzes large-scale U.S. health survey data to identify which factors are most associated with heart attack risk and to build a predictive machine learning model for classification.

The work was completed as part of the **CIS5450: Big Data Analytics** final project in the **University of Pennsylvania MCIT program**, and is connected to the companion Medium article:

**Heart Health Education — Is There Something We’re Missing?**

The notebook shows a full workflow from raw data ingestion and cleanup through exploratory analysis and classification modeling. :contentReference[oaicite:2]{index=2}

---

## Problem Statement

Heart disease remains one of the leading health concerns, but risk is influenced by more than a few obvious variables. This project explores:

- Which health and behavioral factors are most associated with heart attacks
- Whether overlooked indicators, such as dental health, may reveal useful signals
- How well machine learning models can predict heart attack outcomes from survey-based health data

---

## Dataset

This project uses the **2022 CDC Behavioral Risk Factor Surveillance System-style health indicators dataset**, imported from `heart_2022_with_nans.csv`. The raw dataset contains **445,132 rows and 40 columns** before cleaning. :contentReference[oaicite:3]{index=3}

### Example feature groups
- Demographics: `Sex`, `RaceEthnicityCategory`, `AgeCategory`, `State`
- General health: `GeneralHealth`, `PhysicalHealthDays`, `MentalHealthDays`
- Conditions: `HadAngina`, `HadStroke`, `HadDiabetes`, `HadCOPD`, `HadKidneyDisease`
- Behaviors: `PhysicalActivities`, `SmokerStatus`, `AlcoholDrinkers`
- Access and prevention: `LastCheckupTime`, `FluVaxLast12`, `PneumoVaxEver`
- Physical indicators: `BMI`, `SleepHours`, `RemovedTeeth`

The notebook also documents each variable and its meaning. :contentReference[oaicite:4]{index=4}

---

## Project Workflow

## 1. Data Cleaning

The notebook performs substantial preprocessing before modeling:

- Dropped rows with missing values
- Reduced the dataset from **445,132 rows** to **246,022 fully populated rows**
- Removed duplicate rows
- Dropped `HeightInMeters` and `WeightInKilograms` because BMI already captures that information
- Standardized state names to abbreviations for visualization
- Converted BMI into a new categorical feature:  
  `Underweight`, `Normal`, `Overweight`, `Obese`
- Converted Yes/No fields into binary numeric values
- Resolved mixed-category issues in `HadDiabetes` and `CovidPos`
- Simplified long categorical labels for readability in charts and analysis

These steps are explicitly shown in the notebook’s cleaning pipeline. :contentReference[oaicite:5]{index=5} :contentReference[oaicite:6]{index=6} :contentReference[oaicite:7]{index=7} :contentReference[oaicite:8]{index=8}

---

## 2. Exploratory Data Analysis

The project explores heart attack patterns across multiple dimensions:

### Geographic exploration
- Distribution of rows by state
- Heart attack percentages by state
- Later conclusion: `State` was dropped from the modeling dataset because it added noise and would excessively bloat one-hot encoded features. :contentReference[oaicite:9]{index=9}

### Demographic analysis
- Heart attack rate by gender
- Heart attack rate by age group
- Heart attack rate by race/ethnicity

### Health and behavior analysis
- Heart attack rate by BMI category
- Heart attack versus removed teeth
- Heart attack versus sleep hours
- Heart attack versus smoking status
- Heart attack versus alcohol consumption
- Heart attack versus chest scan history
- Heart attack versus last checkup timing

### Access and awareness analysis
The notebook also creates custom state-level analyses for:
- health awareness patterns
- medical care access patterns

These EDA sections appear throughout Part III of the notebook. :contentReference[oaicite:10]{index=10} :contentReference[oaicite:11]{index=11} :contentReference[oaicite:12]{index=12} :contentReference[oaicite:13]{index=13}

---

## Key Insights

### 1. Angina is the strongest observed correlate
The notebook’s correlation analysis shows that `HadAngina` has the strongest correlation with `HadHeartAttack` at about **0.446**, far above other non-target features. :contentReference[oaicite:14]{index=14}

### 2. BMI matters
The SQL summary for BMI category shows heart attack prevalence is highest among the **Obese** group, followed by **Overweight**, then **Underweight**, then **Normal**. :contentReference[oaicite:15]{index=15}

### 3. Age strongly increases risk
The age-group visualization in the notebook shows heart attack percentages rising steeply with older age groups, with the highest prevalence in the oldest populations. The chart on page 18 illustrates this clearly. :contentReference[oaicite:16]{index=16}

### 4. Gender differences appear meaningful
The gender breakdown shows that heart attacks in the analyzed population are disproportionately associated with males, with the chart showing roughly **65.1% male** and **34.9% female**. The pie chart appears on page 17. :contentReference[oaicite:17]{index=17}

### 5. Dental health is an important signal
The project devotes specific analysis to `RemovedTeeth`, especially for age 45+, where the visualization suggests higher heart attack rates among groups with more teeth removed. This supports the project’s broader thesis that oral health may be an overlooked indicator. The chart on page 23 shows the highest share in the “All” and “6 or more” removed-teeth groups. :contentReference[oaicite:18]{index=18}

### 6. Lifestyle-related factors matter
Smoking, lower physical activity, and other behavioral signals appear meaningfully associated with heart attack outcomes in both charts and correlations. In the correlation table, `PhysicalActivities` and `AlcoholDrinkers` are negatively associated with `HadHeartAttack`, while multiple chronic-condition indicators are positively associated. :contentReference[oaicite:19]{index=19}

---

## Feature Engineering

The notebook uses two encoding paths:

### One-hot encoding
Used for categorical expansion into model-ready features.

### Label encoding
A second encoded dataset was also created by label encoding fields such as:
- `Sex`
- `BMI_Category`
- `GeneralHealth`
- `LastCheckupTime`
- `RemovedTeeth`
- `SmokerStatus`
- `RaceEthnicityCategory`
- `AgeCategory`

The final label-encoded dataset contains **34 columns**. :contentReference[oaicite:20]{index=20}

Additional preprocessing steps:
- Min-max scaling for feature normalization
- Train/test split
- Feature reduction after dendrogram-based correlation inspection  
  The notebook drops `DifficultyDressingBathing`, `DifficultyWalking`, and `MentalHealthDays` due to strong inter-feature correlation. :contentReference[oaicite:21]{index=21} :contentReference[oaicite:22]{index=22}

---

## Modeling Approach

The project frames heart attack prediction as a binary classification problem with `HadHeartAttack` as the target variable.

### Models used
- Logistic Regression
- Logistic Regression with SMOTE oversampling
- Decision Tree with SMOTE oversampling

### Why SMOTE was used
The notebook explicitly notes that the dataset is imbalanced, which led to poor recall for the positive class in the initial logistic regression model. SMOTE was applied to synthetically balance the minority class before retraining. The oversampled training target becomes balanced at **186,020 / 186,020**. :contentReference[oaicite:23]{index=23} :contentReference[oaicite:24]{index=24} :contentReference[oaicite:25]{index=25}

---

## Model Results

### Logistic Regression
- Accuracy: **0.948**
- But positive-class recall was only **0.24**
- This means the model missed too many true heart attack cases despite high overall accuracy, a classic class-imbalance problem. :contentReference[oaicite:26]{index=26}

### Logistic Regression with SMOTE
- Accuracy: **0.800**
- Precision/Recall became much more balanced
- Positive-class recall improved substantially to **0.77**. :contentReference[oaicite:27]{index=27}

### Decision Tree with SMOTE
- Accuracy: **0.951**
- Precision and recall were both about **0.95**
- This was the strongest model shown in the notebook. :contentReference[oaicite:28]{index=28}

---

## Tech Stack

```text
Python
Pandas
NumPy
PandasQL
Matplotlib
Seaborn
Plotly
scikit-learn
imbalanced-learn (SMOTE)
SciPy
mlxtend
