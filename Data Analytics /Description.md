# 🫀 Heart Disease Risk Analytics: Insights & Prevention Guidelines

## 📌 Introduction

Cardiovascular diseases (CVDs) are currently the leading cause of death globally, accounting for approximately **19.41 million deaths annually**. Despite being a major global health crisis, many of these cases are preventable through early detection and lifestyle management.

This project, developed as part of the **DS512/513 Data Analytics** course, focuses on analyzing the **Framingham Heart Study dataset**. Instead of solely relying on prediction, our primary goal is to derive actionable intelligence by identifying concrete **"Risk Indicators"**.

### 🎯 Project Objectives

The analysis aims to answer critical questions regarding heart disease risk factors through statistical analysis and visualization:

* **Analyze Risk Factors:** Identify key drivers of Coronary Heart Disease (CHD) risk, including demographic (Age, Gender), behavioral (Smoking), and clinical factors (Glucose, BMI, Blood Pressure).
* **Visualize Insights:** Create interactive visualizations to clearly communicate risk patterns, such as the correlation between Glucose levels and Blood Pressure.
* **Develop Guidelines:** Use data-driven insights to propose preventive guidelines that promote healthier lifestyle behaviors.
* **Predictive Modeling (Secondary):** Develop a machine learning model to estimate 10-year CHD risk using techniques to handle class imbalance.

---

## 📂 Data Description

The dataset used in this analysis is the **Framingham Heart Study** dataset, obtained from Kaggle. It includes health records of residents from Framingham, Massachusetts, consisting of **4,238 records** and **15 attributes**.

* **Source:** [Kaggle - Heart Disease Prediction Using Logistic Regression](https://www.kaggle.com/datasets/dileep070/heart-disease-prediction-using-logistic-regression/data)
* **Target Variable:** `TenYearCHD` (10-year risk of coronary heart disease)
    * `0` = No Risk
    * `1` = Risk

### 📝 Data Dictionary

The variables are categorized into four main groups:

| Category | Variable Name | Description |
| :--- | :--- | :--- |
| **Target** | `TenYearCHD` | 10-year risk of coronary heart disease (Binary: 0/1) |
| **Demographic** | `male` | Gender (0 = Female, 1 = Male) |
| | `age` | Age of the patient |
| | `education` | Education level |
| **Behavioral** | `currentSmoker` | Whether the patient is a current smoker (0/1) |
| | `cigsPerDay` | Number of cigarettes smoked per day |
| **Medical History** | `BPMeds` | Whether the patient is on blood pressure medication |
| | `prevalentStroke` | History of stroke |
| | `prevalentHyp` | History of hypertension |
| | `diabetes` | History of diabetes |
| **Current Health** | `totChol` | Total cholesterol level |
| | `sysBP` | Systolic blood pressure |
| | `diaBP` | Diastolic blood pressure |
| | `BMI` | Body Mass Index |
| | `heartRate` | Heart rate |
| | `glucose` | Glucose level |

---

## 🧹 Data Cleaning & Preprocessing

To ensure the accuracy of our analysis and model, the following preprocessing steps were performed:

1.  **Data Integration & Mapping:**
    * Converted numerical codes into human-readable labels for analysis (e.g., mapping `Sex` to Male/Female, `TenYearCHD` to Risk/No Risk).
2.  **Handling Missing Values:**
    * Identified missing values (NaNs) in the dataset and removed the corresponding rows to maintain data integrity.

### 🚩 Problems Identified
Three critical data quality issues were identified during the exploration phase that required preprocessing:

1.  **Missing Values:** Several records contained null values that needed to be dropped or imputed.
2.  **Extreme Outliers:** Significant outliers were observed in medical variables, which could skew the analysis.
3.  **Imbalanced Target:** The dataset shows a class imbalance, with significantly fewer "Risk" cases compared to "No Risk" cases.

## ❓ Key Questions & Hypotheses

### 1. General Information
* **Age Impact:** Does age significantly impact the 10-year CHD risk?
* **Gender Differences:** Does the impact of age on CHD risk differ between genders?

### 2. Medical Data Factors
* **Dominant Factor:** Which is the dominant risk factor: Glucose or Cholesterol?
* **Glucose & BP:** Is elevated blood glucose associated with higher systolic blood pressure?
* **BMI Trend:** Does the BMI category (Underweight to Obese) show a clear trend in CHD risk?
* **Combined Risks:** Does having multiple risk factors increase the risk compared to just one?


## 💡 Findings and Insights

Based on our statistical analysis and data visualization, we identified several critical patterns regarding heart disease risk:

### 1. Demographic Factors: Age vs. Gender
* **Age is the Dominant Driver:** Age has a significant and consistent impact on CHD risk across all groups. The "Risk" group is consistently older than the "No Risk" group.
* **Gender Impact is Minimal:** Unlike age, gender shows minimal impact on heart disease risk. Age proves to be the primary determinant for both men and women.

### 2. Medical Risk Factors
* **Glucose vs. Cholesterol:** High glucose levels were identified as a dominant risk factor, significantly outweighing the impact of high cholesterol.
* **The Glucose-BP Connection:** Elevated blood glucose is strongly associated with higher systolic blood pressure (approx. 141 mmHg vs. 131 mmHg), confirming a link to increased cardiovascular stress.
* **BMI Trends:** There is a clear upward trend in risk associated with BMI. The 10-year CHD risk peaks at nearly **20% for the Obese group**, compared to approximately **12% for those with normal weight**.

### 3. Combined Risk Effect
* **The Multiplier Effect:** Having multiple risk factors simultaneously results in the highest probability of CHD, significantly exceeding the risk associated with any single factor alone.



