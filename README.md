# Python_Heart_Failure_Prediction_Analysis

## Overview
This project involves analyzing the **Heart Failure Prediction Dataset** to explore the relationship between various clinical features and the likelihood of heart failure mortality.The analysis combines **Exploratory Data Analysis (EDA)**, **Statistical hypothesis testing**, **Data visualization**, and **Machine learning** to identify patterns associated with mortality and evaluate the performance of classification models.
The project also compares **Logistic Regression** and **Random Forest** models to examine their ability to predict the **DEATH_EVENT** outcome.

## Objective
The main objectives of this project are to:
- Perform **Exploratory Data Analysis** (EDA) to understand the dataset and identify important patterns.
- Conduct **Statistical hypothesis** testing using T-tests, Chi-square tests, and Pearson correlation analysis.
- Visualize distributions, relationships, and potential **outliers** in clinical features.
- Investigate clinical variables associated with mortality outcomes.
- Develop **Machine learning** classification models using Logistic Regression and Random Forest.
- Evaluate and compare model performance using multiple evaluation metrics.
- Explore **feature importance** to understand the contribution of clinical variables to model predictions.

## Dataset Information
The dataset is sourced from **Kaggle's Heart Failure Clinical Records Dataset**.

It contains clinical records of 299 patients with heart failure and 13 variables, including demographic information, medical conditions, laboratory measurements, and follow-up duration.The target variable is DEATH_EVENT, which indicates whether a patient died during the follow-up period.

**Total Records**: 299

**Total Columns**: 13

**Target Variable**: DEATH_EVENT

**Source**: Kaggle - Heart Failure Clinical Records Dataset

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

## Tools and Technologies
 **Programming Language**: Python
 
 **Data Manipulation**: Pandas, NumPy

 **Data Visualization**: Matplotlib, Seaborn

 **Statistical Analysis**: SciPy

 **Machine Learning**: Scikit-learn

 **Development Environment**: Jupyter Notebook

## Methodology
**1. Data Loading and Preprocessing**

Loaded the dataset using Pandas.
- Inspected dataset structure, data types, and summary statistics.
- Checked for missing values and duplicate records.
- Prepared the data for exploratory and statistical analysis.
  
**2. Exploratory Data Analysis (EDA)**
- Analyzed numerical and categorical variables.
- Examined distributions of clinical features.
- Explored relationships between clinical variables and DEATH_EVENT.
- Identified potential patterns and differences between survival and non-survival groups.
  
**3. Statistical Analysis**

Several statistical techniques were applied to investigate relationships between clinical variables and mortality outcomes.
- **Independent T-Test**: Compared the means of numerical variables between survival and non-survival groups.
- **Chi-Square Test**: Examined associations between categorical variables and mortality outcomes.
- **Pearson Correlation**: Measured the strength and direction of linear relationships between numerical variables.

**4. Outlier Detection**
- Used boxplots to identify potential outliers in numerical variables.
- Examined the distributions of key clinical measurements.
- Considered the potential influence of extreme values on statistical analysis.
  
**5. Data Visualization**

The following visualizations were created to communicate patterns and relationships in the dataset:
- Histograms for numerical feature distributions.
- Boxplots for comparing distributions and identifying outliers.
- Bar plots for comparing categorical variables.
- Scatter plots for examining relationships between numerical variables.
- Pair plots for exploring relationships among multiple features.
- Correlation heatmaps for examining relationships between numerical variables.
  
**6. Machine Learning**

Two classification algorithms were developed to predict the DEATH_EVENT outcome.

**Feature Selection and Target Definition**
- Defined DEATH_EVENT as the target variable.
- Excluded DEATH_EVENT and time from the input features.
- Excluded time because it represents follow-up duration and may introduce outcome-related information into a baseline         prediction model.
  
**Train-Test Split**
- Split the dataset into 80% training data and 20% testing data.
- Used stratified sampling to preserve the target class distribution.
- Set a random state for reproducibility.
  
**Data Preprocessing**
- Used median imputation to handle missing values.
- Applied StandardScaler for Logistic Regression.
- Implemented preprocessing through Scikit-learn pipelines to reduce data leakage.
- 
**Classification Models**
- **Logistic Regression**: Used as a baseline classification algorithm.
- **Random Forest**: Used to explore potential nonlinear relationships among clinical features.
  
**Model Evaluation**

The models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
- ROC Curve
  
**Cross-Validation**

Stratified 5-fold cross-validation was performed on the training data to assess model performance across multiple data splits.

**Feature Importance**

  Permutation importance was used to investigate how individual clinical features influenced Random Forest model performance.
  
## Key Findings
**Exploratory and Statistical Analysis**
- **Age**: Older patients showed a higher likelihood of death during the follow-up period. However, mortality was also observed among younger patients, indicating that age alone does not explain patient outcomes.
- **Ejection Fraction**: Lower ejection fraction values were associated with higher mortality, highlighting the importance of cardiac pumping function when examining heart failure outcomes.
- **Serum Creatinine**: Higher serum creatinine levels were associated with mortality, suggesting that impaired kidney function may be an important indicator of poorer health outcomes.
- **Hypertension and Diabetes**: Both conditions were present among patients who died during follow-up. Their relationships with mortality should be interpreted in the context of the statistical results.
- **Smoking and Sex**: Smoking status and sex did not show statistically significant associations with mortality in this dataset. However, this does not establish that they are unrelated to heart health.
- **Creatinine Phosphokinase (CPK)**: CPK levels showed differences between outcome groups. Further investigation would be needed to establish the clinical significance of this finding.
  
**Machine Learning Results**

| Evaluation Metric | Logistic Regression | Random Forest |
| ----------------- | ------------------: | ------------: |
| Accuracy          |                0.70 |          0.72 |
| Class 1 Precision |                0.53 |          0.56 |
| Class 1 Recall    |                0.53 |          0.53 |
| Class 1 F1-score  |                0.53 |          0.54 |

## Key Observations:
- Random Forest achieved slightly higher test accuracy (0.72) compared with Logistic Regression (0.70).
- Random Forest also achieved slightly higher precision and F1-score for the positive class.
- Both models achieved the same recall (0.53) for DEATH_EVENT = 1.
- The similar recall scores indicate that both models identified a comparable proportion of actual positive cases.
- Overall, the models demonstrated similar performance on the test dataset.

## Recommendations
- Consider age, ejection fraction, and serum creatinine together when exploring patient outcome patterns.
- Further investigate the relationships between diabetes, hypertension, kidney function, and heart failure outcomes using      larger datasets.
- Continue monitoring relevant cardiac and kidney function indicators according to established clinical guidelines.
- Encourage smoking cessation and heart health awareness as part of broader cardiovascular health initiatives.
- Conduct further research to investigate potential differences in heart failure outcomes across demographic groups.
- Evaluate additional classification algorithms and use larger, independent datasets to improve model reliability.
- Explore feature importance and model interpretability techniques to better understand the relationships captured by          machine learning models.
- Perform external validation before considering any predictive model for clinical applications.

## Limitations
- The dataset contains only 299 patient records, limiting the generalizability of the findings.
- The analysis is based on observational data; therefore, statistical associations cannot establish causation.
- A single train-test split may produce unstable performance estimates because of the small sample size.
- Machine learning models were evaluated using a limited number of observations and require validation on larger               independent datasets.
- The time feature was excluded from the baseline prediction models because it represents follow-up duration and may introduce outcome-related information.
- The models are educational and exploratory demonstrations, not clinically validated prediction tools.

## Project Structure
Python_Heart_Failure_Prediction_Analysis/

│

├── Heart Failure Prediction Analysis.ipynb


├── heart_failure_clinical_records_dataset.csv

├── requirements.txt

└── README.md

## Installation and Usage
**1. Clone the Repository**

 git clone https://github.com/jannatularshi/Python_Heart_Failure_Prediction_Analysis.git
    
**2. Navigate to the Project Directory**

cd Python_Heart_Failure_Prediction_Analysis
    
**3. Install Required Libraries**

pip install -r requirements.txt
    
**4. Run the Jupyter Notebook**

jupyter notebook

Open Heart Failure Prediction Analysis.ipynb and run the notebook cells sequentially.

## Conclusion
This project combines exploratory data analysis, statistical hypothesis testing, data visualization, and machine learning to investigate factors associated with heart failure mortality.
The statistical analysis highlighted several clinical variables associated with mortality, including age, ejection fraction, and serum creatinine. The machine learning analysis extended this investigation by comparing Logistic Regression and Random Forest classification models.
Although Random Forest achieved slightly higher test accuracy than Logistic Regression, both models demonstrated similar recall for the positive class. These findings emphasize the importance of evaluating multiple performance metrics when working with imbalanced healthcare datasets.

Overall, this project strengthened my understanding of statistical analysis, Python-based data analysis, machine learning workflows, model evaluation, and feature interpretation.
The findings should be considered exploratory and require further investigation using larger and more diverse datasets.

   
