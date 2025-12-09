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

## 📊 Dataset Overview

The dataset used in this project is from the **Framingham Heart Study**, an ongoing cardiovascular study on residents of Framingham, Massachusetts. [cite_start]It is publicly available on Kaggle and contains over 4,000 patient records[cite: 83, 98, 100].

* [cite_start]**Source:** [Kaggle - Heart Disease Prediction](https://www.kaggle.com/datasets/dileep070/heart-disease-prediction-using-logistic-regression/data) [cite: 83]
* [cite_start]**Total Records:** 4,238 records (before cleaning) [cite: 123]
* [cite_start]**Attributes:** 15 clinical, demographic, and behavioral features [cite: 100]

### 📖 Data Dictionary

The classification goal is to predict the **10-year risk of future coronary heart disease (CHD)**.

| Category | Variable | Description |
| :--- | :--- | :--- |
| **Target** | `TenYearCHD` | [cite_start]10-year risk of coronary heart disease (1 = Risk, 0 = No Risk) [cite: 73] |
| **Demographic** | `age` | [cite_start]Age of the patient [cite: 75] |
| | `sex` | [cite_start]Gender (Male / Female) [cite: 75] |
| | `education` | [cite_start]Educational background [cite: 75] |
| **Behavioral** | `currentSmoker` | [cite_start]Whether the patient is a current smoker [cite: 77] |
| | `cigsPerDay` | [cite_start]Number of cigarettes smoked per day [cite: 77] |
| **Medical History** | `BPMeds` | [cite_start]Whether the patient is on blood pressure medication [cite: 79] |
| | `prevalentStroke` | [cite_start]History of stroke [cite: 79] |
| | `prevalentHyp` | [cite_start]History of hypertension [cite: 79] |
| | `diabetes` | [cite_start]History of diabetes [cite: 79] |
| **Current Health** | `totChol` | [cite_start]Total Cholesterol level [cite: 80] |
| | `sysBP` | [cite_start]Systolic Blood Pressure [cite: 80] |
| | `diaBP` | [cite_start]Diastolic Blood Pressure [cite: 80] |
| | `BMI` | [cite_start]Body Mass Index [cite: 80] |
| | `heartRate` | [cite_start]Heart rate [cite: 80] |
| | `glucose` | [cite_start]Glucose level [cite: 80] |

---

## ⚙️ Data Cleaning & Preprocessing

[cite_start]From our initial inspection, we identified three critical issues: **Missing Values**, **Extreme Outliers**, and an **Imbalanced Target**[cite: 124].

### Key Steps Taken:
1.  [cite_start]**Data Integration:** Merged lookup tables to translate numerical codes (e.g., 0, 1) into human-readable labels like "Male/Female" and "No Risk/Risk" for clearer analysis[cite: 117].
2.  [cite_start]**Handling Missing Values:** Rows containing missing values (NaNs) were dropped to ensure data quality[cite: 118].
3.  **Imbalance Handling:** The target variable `TenYearCHD` was imbalanced. [cite_start]We applied **SMOTE (Synthetic Minority Over-sampling Technique)** and **Oversampling** to balance the dataset before training the model[cite: 118].

---
