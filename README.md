# WHO Life Expectancy Predictive Model
## Overview

This project aims to build a predictive model for estimating life expectancy based on population statistics. The data provided by the World Health Organization (WHO) contains records for 183 countries from 2000 to 2015.

Due to concerns over sharing sensitive data, two separate models were built:

* A basic model that uses the minimum amount of data necessary for prediction.
* A more complex model that utilises additional sensitive data, providing more accurate predictions but requiring greater data sharing.

This project not only focuses on model accuracy but also adheres to ethical data practices by considering which features should or shouldn't be used, based on the implications of sharing sensitive information.

## Objectives

The key objectives of this project are:

* To predict life expectancy using population statistics.
* To build two models:
  * A basic model that uses only essential, non-sensitive features.
  * A complex model that can provide more accurate predictions if sensitive data is available.
* To maintain data integrity and ensure ethical use of sensitive information when determining which features to include in each model.

## The Project

The tools used in this project include: Python and Python libraries (pandas, numpy, matplotlib, seaborn, sklearn, statsmodels, unittest).

### Data Preprocessing and Exploration

The dataset was first divided into training and testing sets. Exploratory Data Analysis (EDA) was conducted on the training data to uncover key relationships and understand the factors impacting life expectancy. This si documented in 'EDA.ipynb'.

### Model Building

Two linear regression models were constructed (documented in 'WHO_Lin_reg_function1.ipynb'):

* Basic Linear Regression Model: Uses a minimal set of features that avoids sensitive data.
* Complex Linear Regression Model: Incorporates additional features that might be sensitive to improve prediction accuracy.

Both models were trained and tested on the dataset, and the performance metrics (e.g., R-squared, RMSE) were evaluated.

### Interactive Predictive Function

A standalone interactive function was developed that takes in user-inputted population statistics and predicts life expectancy. Users can choose between the basic and complex models, depending on the available data. This function is designed for practical use in real-world scenarios where data availability may vary.

The interactive function is available in 'Function_Lin_Reg.ipynb' and allows users to:

* Input relevant population statistics (e.g., GDP, years of schooling, immunisation rates).
* Choose between the basic or complex model for prediction.
* Receive a predicted life expectancy based on the provided data.

### Ethical Considerations

Given the sensitivity of certain data (e.g., health-related metrics, mortality rates), we made deliberate decisions on which features to include in the basic model to respect privacy concerns. The more sensitive data is only used in the complex model, which should only be applied if proper permissions for sharing have been obtained.
