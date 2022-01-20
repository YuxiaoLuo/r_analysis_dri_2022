---
title: "Regression Warm-up"
author: "Yuxiao Luo"
output: 
  html_document:
    keep_md: yes
---



This section is part of the R Data Analysis Workshop and aims to introduce some basic concepts for regression analysis in R. If you want to learn more in details, I would recommend you read the [Introduction to Econometrics with R](https://www.econometrics-with-r.org/index.html), a free e-book. 

## Data Types 

- discrete 

- continuous

- binary

- categorical 

## Why Regression Model?

## Key Terms in Regression Model

- coefficient 
- correlation
- significance level
- t-statistic
- p-value
- independent/explanatory variable (predictor)

- dependent/response variable 

## Assumptions of Multiple Linear Regression 
Multiple linear regression analysis makes several key assumptions: 

- There must be a linear relationship between the outcome variable and the independent variables. Scatterplots can show whether there is a linear or curvilinear relationship.

- Multivariate Normality: Multiple regression assumes that the residuals are normally distributed.

- No Multicollinearity: Multiple regression assumes that the independent variables are not highly correlated with each other. This assumption can be tested with Variance Inflation Factor (VIF) values. 

- Homoscedasticity: This assumption states that the variance of error terms are similar across the values of the independent variables. A plot of standardized residuals versus predicted values can show whether points are equally distributed across all values of the independent variables.

Moreover, multiple linear regression requires at least two explanatory variables, which can be nominal, ordinal, or interval/ratio level variables. A rule of thumb for the sample size is at least 20 cases per independent variable in the analysis.

## Regression Tests

- VIF: Variation inflation factor (VIF) quantifies how much the variance is inflated. The variances of the estimated coefficients are inflated when multicollinearity exists and a variance inflation factor exists for each of the predictors in the model. How do we interpret the variance inflation factors for a regression model? A VIF of 1 means that there is no correlation among the jth predictor and the remaining predictor variables, and hence the variance of bj is not inflated at all. The rule of thumb is that VIFs exceeding 4 warrant further investigation, while VIFs exceeding 10 are signs of serious multicollinearity.

- Cook's Distance: Cook's distance measures how much all of the fitted values in the model change when the ith data point is deleted and is useful for identifying influential data points and outliers in the X values. A general rule of thumb is that any point with a Cook's distance over 4/n (where n is the number of observations) is considered to be an outlier. Please note that just because a data point is influential doesn't mean it should necessarily be deleted. More details [here](https://www.statology.org/how-to-identify-influential-data-points-using-cooks-distance/).

- Leverage: Leverage is a measure of how far away the independent variable values of an observation are from those of the other observations. High-leverage points, if any, are outliers with respect to the independent variables. hat is, high-leverage points have no neighboring points in  $R^p$ space, where $p$ is the number of independent variables in a regression model. This makes the fitted model likely to pass close to a high leverage observation. Hence high-leverage points have the potential to cause large changes in the parameter estimates when they are deleted i.e., to be influential points. Although an influential point will typically have high leverage, a high leverage point is not necessarily an influential point.

## Regression Performance

- r-squared

- AIC (Akaike Information Criterion)

- BIC (Baysian Information Criterion)

## Hypothesis Testing