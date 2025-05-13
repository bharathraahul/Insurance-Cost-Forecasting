# Insurance-Cost-Forecasting
This project analyzes and predicts medical insurance costs based on demographic and lifestyle factors using the Kaggle Medical Cost Personal Datasets. The dataset includes features such as age, sex, BMI, number of children, smoking status, and region.

# 🩺 Insurance Forecast for a Medical Cost Personal Datasets

This project performs detailed exploratory data analysis (EDA), statistical testing, and predictive modeling on a medical insurance dataset. The goal is to understand the influence of various features (e.g., smoking status, age, BMI) on insurance charges and to develop models that can accurately predict these charges.

## 📂 Dataset

- **Source**: [Kaggle - Medical Cost Personal Datasets](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- **Size**: 1,338 entries with 7 features including:
  - `age`
  - `sex`
  - `bmi`
  - `children`
  - `smoker`
  - `region`
  - `charges`

## 🔍 Project Objectives

- Perform EDA to visualize trends in the data
- Conduct hypothesis testing to evaluate the impact of smoking and BMI
- Fit linear, stepwise, random forest, and XGBoost regression models
- Evaluate model performance using MAE, MSE, and RMSE

## 📊 Exploratory Data Analysis (EDA)

- Distribution plots for `charges`, grouped by `smoker`, `sex`, `region`, and `bmi_category`
- Boxplots to compare insurance charges across different demographics
- Overlay histograms and scatter plots for deeper insight into correlations

## 🧪 Hypothesis Testing

- **Variance test**: To test if smoker and non-smoker charge variances differ
- **T-test**: One-sided test to confirm if smokers are charged more than non-smokers
- **ANOVA**: To compare charges across different BMI categories

## 📈 Modeling

### ✅ Linear Regression Models
- Single feature: `smoker`, `bmi`, `age_group`
- Multi-feature: `smoker + bmi_category`, etc.

### 🔁 Stepwise Regression
- **Forward Selection**: Using AIC to add variables
- **Backward Elimination**: Using AIC to remove non-significant variables

### 🌲 Random Forest Regression
- Trained using all available features
- Evaluated with RMSE and actual vs predicted plots

### 🚀 XGBoost Regression
- Data transformed to DMatrix format
- Parameters tuned: `eta`, `max_depth`, `subsample`, etc.
- Output evaluated using RMSE and scatter plot comparison

## 📦 Libraries Used

- `tidyverse`, `ggplot2`, `MASS`
- `MLmetrics`
- `randomForest`
- `xgboost`

## 🧠 Key Insights

- Smokers have significantly higher insurance charges (confirmed by statistical testing and boxplots).
- BMI and age also have a strong correlation with charges.
- Ensemble models like Random Forest and XGBoost outperform linear regression in predictive accuracy.


## 🚀 How to Run

1. Clone this repository
2. Open the `insurance_analysis.Rmd` file in RStudio
3. Install required libraries (listed in the R Markdown)
4. Knit to HTML or run line-by-line for stepwise execution

