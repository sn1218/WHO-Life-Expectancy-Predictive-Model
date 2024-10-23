# WHO Life Expectancy Predictive Model
## Overview

This project aims to develop a predictive model for estimating life expectancy based on population statistics from 183 countries between 2000 and 2015. The dataset was provided by the World Health Organization (WHO) and includes both general population metrics and sensitive health-related data.

To address the need for privacy and ethical data use, the project produces two distinct models:

1. **Basic Model:** Uses only essential, non-sensitive features to predict life expectancy.
2. **Complex Model:** Incorporates sensitive data to improve prediction accuracy, but requires more extensive data sharing.

The focus of this project is not only on the accuracy of the predictions but also on upholding ethical data practices by carefully considering which features should be used in each model based on privacy concerns and data-sharing implications.

## Objectives

The key objectives of the project are:

* To predict life expectancy using population statistics.
* To build two models:
  * A basic model that uses only essential, non-sensitive features.
  * A complex model that can provide more accurate predictions if sensitive data is available.
* To maintain data integrity and ensure ethical use of sensitive information when determining which features to include in each model.

## Project Details
### Tools and Libraries
This project was implemented in Python and utilised several key libraries, including:

* **pandas and numpy:** For data manipulation
* **matplotlib and seaborn:** For visualising the data
* **sklearn and statsmodels:** For building and evaluatiing machine learning models (logistic regression and decision trees)
* **unittest:** For validating the performance and correctness of the interactive function

### Dataset
The dataset includes population statistics and health indicators from 183 countries over 15 years (2000-2015). Key features of the dataset include:

* **Country-level Information:** Country, year, region, and status.
* **Demographic Data:** Population, GDP, school enrollment rates, etc.
* **Health Metrics:** Life expectancy, adult mortality, infant deaths, immunisation rates, etc.
* **Sensitive Data:** Some health-related metrics (e.g., mortality rates, certain disease incidences) considered sensitive for data-sharing purposes.

The dataset is stored in the project directory and was preprocessed before being used in the models.

### Data Preprocessing and Exploratory Data Analysis (EDA)

The dataset was first divided into training and testing sets. Exploratory Data Analysis (EDA) was conducted on the training data to uncover key relationships and understand the factors impacting life expectancy. This is documented in 'EDA.ipynb'.

### Model Building

Two linear regression models were developed, both designed to predict life expectancy but differing in the features they use:

1. Basic Linear Regression Model:
 * Only utilises non-sensitive features, such as GDP, school enrollment rates, and general demographic information.
 * Aimed at providing predictions while adhering to strict data privacy standards.

2. Complex Linear Regression Model:
 * Incorporates additional sensitive features, such as health-related metrics (e.g. mortality data).
 * Achieves higher accuracy but requires the use of sensitive information, necessitating more stringent data-sharing policies.

The 'WHO_Lin_reg_function1.ipynb' notebook contains the details of both models, including the model-building process, feature selection, and evaluation of performance metrics (e.g., R-squared, Root Mean Squared Error (RMSE)).

### Interactive Predictive Function

An interactive function was created to allow users to input population statistics and receive life expectancy predictions. Depending on the data available, users can choose between the basic model and the complex model.

The function is implemented in 'Function_Lin_Reg.ipynb' and provides the following capabilities:

* **Model Selection:** Choose between the basic or complex model based on the available data and privacy requirements.
* **User Input:** Enter relevant population statistics such as GDP, years of schooling, etc..
* **Life Expectancy Prediction:** The function returns an estimated life expectancy based on the chosen model and inputted data.

This feature is particularly useful in real-world scenarios where data availability varies, and sensitive data may not always be accessible.

### Ethical Considerations

Given the sensitive nature of certain data (e.g., health-related metrics, mortality rates), the project carefully balances predictive power with ethical considerations. The basic model is designed to be used in cases where sensitive data cannot or should not be shared, allowing for accurate predictions without violating privacy.

The complex model, while more accurate, should only be applied when proper data-sharing agreements are in place, ensuring that sensitive information is handled responsibly.

## Repository Structure
* **Life Expenctancy Data.csv:** The primary dataset used for the project.
* **WHO Dataset - MetaData.ipynb:** Metadata for the dataset.
* **EDA.ipynb:** Notebook documenting the exploratory data analysis.
* **WHO_Lin_reg_function1.ipynb:** Notebook documenting the creation of the linear regression models and feature selection process.
* **Function_Lin_reg.ipynb:** Notebook implementing the interactive predictive function.

## How to Use the Project
1. Clone the repository and download the dataset and notebooks.
2. Open the EDA.ipynb notebook to explore the dataset and view key trends in life expectancy.
3. Use the Function_Lin_Reg.ipynb notebook to interactively predict life expectancy based on user input. Select the basic or complex model depending on the data you have available.
 * If sensitive data is available, use the complex model for better predictions.
 * If sensitive data is restricted, use the basic model for an ethical approach while maintaining reasonable accuracy.
