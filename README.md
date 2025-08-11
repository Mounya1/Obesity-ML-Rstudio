

# Obesity Level Predictive Modeling

##  Project Overview

This project focuses on predicting **Body Mass Index (BMI)** and **Obesity Levels** using demographic, lifestyle, and health-related factors from individuals in Mexico, Peru, and Colombia. The dataset includes both real and synthetically generated records, enabling comprehensive predictive modeling for preventive healthcare interventions.

We implemented **data preprocessing, exploratory data analysis (EDA), feature engineering, outlier detection**, and built multiple **machine learning models** to identify key predictors and achieve high classification accuracy.

---

##  Dataset

* **Source:** [UCI Machine Learning Repository – Estimation of Obesity Levels](https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition)
* **Records:** 2,111 (77% synthetic, 23% collected via web platform)
* **Attributes:** 17 features including:

  * Demographics: Gender, Age, Height, Weight
  * Lifestyle: Eating habits, physical activity, alcohol consumption, technology usage
  * Health: Family history of overweight, BMI (calculated)

---

##  Technologies Used

* **Language:** R
* **Libraries:**

  * Data manipulation: `dplyr`, `tidyverse`
  * Visualization: `ggplot2`, `plotly`, `ggcorrplot`
  * Modeling: `caret`, `e1071` (SVM), `randomForest`, `nnet` (Multinomial Logistic Regression)
  * Utility: `caTools`

---

##  Project Workflow

### 1. **Data Preprocessing**

* Loaded dataset from a public CSV link.
* Converted data types, renamed columns, and calculated **BMI**.
* Removed outliers using **IQR filtering**.
* Applied **label encoding** for categorical variables.
* Standardized numerical features.

### 2. **Exploratory Data Analysis**

* Histograms of BMI by gender.
* Relationship between Age, BMI, Alcohol Consumption, and Family History.
* Boxplots for Obesity Level vs Age.
* Correlation heatmap of numerical variables.

### 3. **Modeling**

#### **Regression (BMI Prediction)**

* **Model:** Linear Regression
* **Performance:** R² ≈ 0.99 (Key predictors: height, weight, family history, dietary habits)

#### **Classification (Obesity Level Prediction)**

| Model                           | Accuracy   |
| ------------------------------- | ---------- |
| Random Forest                   | **99.28%** |
| Support Vector Machine (SVM)    | 96.04%     |
| Multinomial Logistic Regression | 93.88%     |

---

## Key Insights

* **Height and Weight** are the strongest predictors of BMI.
* Lifestyle factors (diet, physical activity, alcohol consumption) significantly influence obesity levels.
* **Random Forest** outperformed other models in accuracy and interpretability.
* Outlier removal improved classification performance.

---

