# Python_Heart_Failure_Prediction_Analysis

## Overview
This project involves analyzing the **Heart Failure Prediction Dataset** to explore the relationship between various clinical features and the likelihood of heart failure mortality.The goal is to identify key features that contribute to heart failure mortality and provide insights based on statistica analysis and visualizations.

## Objective
The main objective of this analysis is to explore various factors that contribute to heart failure and its mortality risk.
We perform:
- **Exploratory Data Analysis**
- **Statistical Test** (T-Test, Chi-square test, Pearson Correlation)
- **Data Visualizations** (Heatmaps, Boxplot, Scatter plot, Bar plot, Pair plot, Histogram)
- **Outlier Detection**
By the end of this project, we aim to gain a deeper understanding of the key factors inclucing heart failure and mortality rates and providing actionable insights and recommendations for improving patient care.

## Dataset Information
The dataset is sourced from the **Kaggle Heart Failure Prediction** challenge. This dataset contains clinical records of patients with heart failure. The columns include various clinical features such as age, ejection fraction, serum creatinine and lifestyle factors like smoking and diabetes with the variable being **DEATH_EVENT** (whether the patient died during the follow-up).

## Columns:
1. **age**: Age of the patient (years)
2. **anaemia**: Anaemia status (1=Yes, 0=No)
3. **creatinine_phosphokinase**: Level of creatinine phosphokinase (mcg/L)
4. **diabetes**: Diabetes status (1=Yes, 0=No)
5. **ejection_fraction**: Percentage of blood pumped out of the heart per beat.
6. **high_blood_pressure**: High blood pressure status (1=Yes, 0=No)
7. **platelets**: Platelet count 100000 per microliter
8. **serum_creatinine**: Serum creatinine level (mg/dL)
9. **serum_sodium**: Serum sodium level (mEq/L)
10. **sex**: Gender of the patient (1=Male, 0=Female)
11. **smoking**: Smoking status (1=Yes, 0=N0)
12. **time**: Duration the patient was monitored (days)
13. **DEATH_EVENT**: Indicating whether the patient died during the follow-up(1=Yes, 0=No)

## Methodology
1. **Data Cleaning and Preprocessing**:
   - Load the dataset and handle mising values.
2. **Exploratory Data Analysis (EDA)**:
   - Plot distributions for numerical features.
   - Visualize relationship between features and mortality (DEATH_EVENT).
3. **Statistical Analysis**:
   - **T-Test** to compare the means of two groups (survival vs mortality).
   - **Chi-Square test** to examin the relationship between categorical features.
   - **Pearson Correlation Analysis** to measure the strength and direction of the linear relationship between two numerical variables.
4. **Outlier Detection**:
   - Identify and analyze outliers using boxplots for key features.
5. **Visualization**:
   - **Heatmaps** for correlation analysis.
   - **Boxplot** to visualize distributions and outliers.
   - **Pairplot** to analyze relationships between multiple numerical features.
   - **Barplot** helps in comparing categories.
   - **Scatterplot** to understanding relationships bewteen two continuous variables.
   - **Histogram** gives a detailed view of the distribution of a variable.

## Key Findings
1. **Age** is a significant factor in heart failure mortality. Older patients have a higher risk of mortality and younger patients may also face mortality dure to other health conditions. 
3. **Ejection Fraction** is a critical measures of heart function and lower values are associated with higher mortality rates in heart failure patients.
4. **Serum Creatinine** levels are strongly associated with heart failure risk and mortality. Elevated creatinine levels indicates impaired kidney function which could heart failure and it is a significant marker for poor health outcomes.
5. **Hypertention** and **Diabetes** are commomn in patients who died from heart failure.
6. **Smoking** and **Gender** did not show a statistically significant direct impact on mortalty but still important factors to monitor in the context of overall heart health.
7. **Creatinine Phosphokinase** levels elevated especially in the non-survivor group, suggest a potential link to severe heart or muscle damage which may contribute to mortality.

## Recommendations
- Implement a more frequent monitoring protocal for patients over the **age** of 60 especially those with high **serum creatinine** levels. This can
help early detection of heart failure progression and reduce mortality.
- Develop targeted interventions focusing on managing **diabetes** and **hypertension** in heart patients. Thid could include medications adjstments,
lifestyle changes and patient education.
- Ensure regular **ejection fraction** and **creatinine hosphokinase** testing  and clinical guidelines for high risk patients to monitor their heart health closely and early intervention could improve patients outcomes.
- Strengthen public health campaings focusing on **smoking** cessation and heart health awareness particularly in high-risk groups.
- Conduct gender-specific studies to refine heart failure treatment protocals as biological differences may effect heart disease progression and 
treatment efficacy.

## Project Structure
- **Heart Failure Prediction Analysis.ipynb**: Jupyter Notebook containing code for data analysis and visualizations.
- **requirements.text**: List of libraries required to run the project.
- **heart_failure_clinical_records_dataset.csv**: The dataset used in the analysis.
- **README.md**: Project overview and instructions (this file).
