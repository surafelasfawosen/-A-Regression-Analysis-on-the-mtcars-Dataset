# Predicting Fuel Efficiency of Cars: Multiple Linear Regression on mtcars Dataset

![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![Regression](https://img.shields.io/badge/Linear_Regression-FF6F00?style=for-the-badge)

---

## 📋 Project Overview

This project performs a complete **Multiple Linear Regression** analysis on the famous **mtcars** dataset to predict **miles per gallon (mpg)** — a key measure of car fuel efficiency.

Using engine and physical characteristics such as horsepower (`hp`), weight (`wt`), quarter-mile time (`qsec`), number of cylinders (`cyl`), and engine displacement (`disp`), I built, diagnosed, and significantly improved a regression model.

The project demonstrates a full statistical modeling workflow: model fitting, assumption checking, problem identification, remedial actions, and final interpretation.

---

## 🎯 Aim of the Project

- To predict car fuel efficiency (`mpg`) using important vehicle characteristics.
- To understand the relationship between engine/power features and fuel consumption.
- To properly check and validate all linear regression assumptions.
- To improve model quality by fixing issues like multicollinearity and non-linearity.
- To provide clear and actionable insights about factors affecting fuel efficiency.

---

## ❗ Problem Statement

Building a reliable regression model is challenging because real data often violates key assumptions:
- High **multicollinearity** among predictors (e.g., `disp`, `cyl`, and `wt` are strongly correlated).
- Slight **non-linearity** in the relationship between predictors and `mpg`.
- Some variables were not statistically significant in the initial model.
- These issues can lead to unstable coefficients and unreliable predictions.

---

## ✅ How I Solved It

I followed a systematic step-by-step approach:

1. Loaded the `mtcars` dataset and fitted an initial multiple linear regression model.
2. Thoroughly checked all major regression assumptions (linearity, homoscedasticity, normality, and multicollinearity).
3. Identified problems: high multicollinearity (especially `disp`) and mild non-linearity.
4. Applied remedial measures:
   - Centered the variables (`hp` and `wt`) to reduce multicollinearity.
   - Removed highly correlated variables (`cyl` and `disp`).
   - Added an interaction term (`hp_centered:wt_centered`) to capture combined effects.
5. Refitted the improved model and re-validated all assumptions.
6. Interpreted the final model and drew conclusions.

---

## 🛠️ Techniques and Methods Used

- **Multiple Linear Regression** using `lm()` in R
- **Model Diagnostics**:
  - Residual vs Fitted plot (for linearity)
  - Goldfeld-Quandt Test (for homoscedasticity – suitable for small n=32)
  - Shapiro-Wilk Test (for normality of residuals)
  - Variance Inflation Factor (VIF) (for multicollinearity)
- **Remedial Techniques**:
  - Variable centering
  - Dropping redundant predictors
  - Adding interaction terms
- **Model Evaluation**: R-squared, Adjusted R-squared, Residual Standard Error, F-statistic

**Libraries Used**: `lmtest`, `car`, `nlme`

---

## 📊 Key Results

**Initial Model**:
- Multiple R-squared: 0.8502
- Only `weight (wt)` was statistically significant.

**Improved Final Model**:
- Multiple R-squared: **0.8925** (89.25% of variation explained)
- Adjusted R-squared: **0.8766**
- Residual Standard Error: 2.117 (improved)
- Significant interaction between horsepower and weight

**Main Insights**:
- Vehicle **weight** has the strongest negative impact on fuel efficiency.
- The effect of **horsepower** on mpg depends on the weight of the car (significant interaction).
- After improvements, all regression assumptions were well satisfied.
- The final model is more accurate, stable, and interpretable.

---

## 📌 Conclusion

This project shows the importance of proper model diagnostics and remedial actions in regression analysis. By addressing multicollinearity and non-linearity through centering, variable selection, and interaction terms, I successfully improved the model fit and reliability.

The analysis reveals that **weight** is the dominant factor affecting fuel efficiency, while horsepower plays a conditional role depending on the car's weight. This kind of analysis is useful in automotive engineering and fuel economy studies.

---

## 🛠️ Technologies Used

- **Language**: R
- **Packages**: `lmtest`, `car`, `nlme`
- **Techniques**: Multiple Linear Regression, Assumption Checking, Centering, Interaction Terms, VIF Analysis

---


Feel free to explore the R code and analysis. Contributions and feedback are welcome!
