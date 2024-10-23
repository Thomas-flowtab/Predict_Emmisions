## Project Overview

This project evaluates machine learning models to predict emissions. It focuses on three machine learning techniques: Random Forest Regression (RFR), XGBoost, and Support Vector Machines (SVM). The goal is to assess which model performs best in forecasting CO2 emissions based on historical data. The project uses various performance metrics, including R-squared (R²) and Mean Squared Error (MSE), to evaluate and compare model efficiency, accuracy, and error magnitude.

## Table of Contents

1. [Introduction](#introduction)
2. [Available Machine Learning Algorithms/Techniques](#available-machine-learning-algorithms-techniques)
   - 2.1. [Random Forest Regression](#random-forest-regression)
   - 2.2. [XGBoost](#xgboost)
   - 2.3. [Support Vector Machines (SVM)](#support-vector-machines-svm)
3. [Expected Insights](#expected-insights)
4. [Performance of Each Model](#performance-of-each-model)
   - 4.1. [Performance Metrics](#performance-metrics)
     - 4.1.1. [R-squared (R²)](#r-squared-r²)
     - 4.1.2. [Mean Squared Error (MSE)](#mean-squared-error-mse)
   - 4.2. [Comparison of Model Performance](#comparison-of-model-performance)
     - 4.2.1. [Random Forest Regression](#random-forest-regression-1)
     - 4.2.2. [XGBoost](#xgboost-1)
     - 4.2.3. [Support Vector Machines (SVM)](#support-vector-machines-svm-1)
   - 4.3. [Performance Comparison Summary](#performance-comparison-summary)
5. [Conclusions](#conclusions)

## Introduction

The estimation of emissions is essential for environmental management and policy-making. Machine Learning (ML) methods have demonstrated significant promise in emission modeling. In this project, three specific ML algorithms are chosen for analysis and comparison: Random Forest Regression (RFR), XGBoost, and Support Vector Machines (SVM). The primary goal is to predict CO2 emissions based on a dataset containing emissions data from different sources.

## Available Machine Learning Algorithms/Techniques

### 2.1. Random Forest Regression
Random Forest Regression (RFR) uses decision trees to manage data and predict outcomes, reducing overfitting by averaging multiple trees. It is particularly useful in capturing relationships between data points and is effective in understanding emission factors.

### 2.2. XGBoost
XGBoost (Extreme Gradient Boosting) is a highly efficient and scalable algorithm for handling data. It uses regularization techniques like L1 and L2 to prevent overfitting and is well-suited for emission data due to its ability to handle missing values and imbalanced datasets.

### 2.3. Support Vector Machines (SVM)
SVM is a powerful tool for classification and regression tasks. It is highly effective at managing noisy data and outliers, making it an ideal option for emissions forecasting. The kernel trick and sparsity features enable SVM to handle complex decision boundaries and efficiently use memory.

## Expected Insights

The dataset contains CO2 emissions data for multiple years, focusing on values from 2008 to 2013. After preprocessing, including label encoding and outlier identification, the data was prepared for model training. Key observations include:
![image](https://github.com/user-attachments/assets/469fd114-354d-417b-9a66-15dc19d17915)

- **Wide Range of Values**: The dataset has a wide range of total emissions values, from near zero to over two million.
  ![image](https://github.com/user-attachments/assets/1adf59df-770c-4b4a-bdff-f8eef2288df4)

- **High Variability**: The data has a high standard deviation, making prediction challenging and potentially increasing the Mean Squared Error (MSE).
  ![image](https://github.com/user-attachments/assets/443c08b8-1dd2-4bb0-b860-95dfab844693)

- **Presence of Outliers**: Outliers are present, which may significantly affect the MSE due to their large deviation from the mean.
  ![image](https://github.com/user-attachments/assets/cee3dfe2-53fb-4aab-86d0-7a42632f62b6)


## Performance of Each Model

### 4.1. Performance Metrics

#### 4.1.1. R-squared (R²)
R² measures how much variance in emission levels can be explained by the model. A higher R² value indicates better model performance.
![image](https://github.com/user-attachments/assets/2c8aed56-5e29-428f-a8ea-bb58094a6e94)
![image](https://github.com/user-attachments/assets/cc71f706-d7c3-48d9-8c84-16bdf9c3e9b3)

#### 4.1.2. Mean Squared Error (MSE)
MSE measures the squared differences between predicted and actual values. Lower MSE values suggest more accurate predictions.
![image](https://github.com/user-attachments/assets/e96fb665-c176-4890-b113-d548531b4189)
![image](https://github.com/user-attachments/assets/bf5173e2-875b-43c8-8b63-d34e98b8d541)

### 4.2. Comparison of Model Performance

#### 4.2.1. Random Forest Regression
RFR is a reliable model for managing non-linear relationships, but it may struggle with more complex data patterns. Its MSE is slightly higher compared to XGBoost.

#### 4.2.2. XGBoost
XGBoost excels in handling data complexity and preventing overfitting. It outperforms RFR and SVM in terms of accuracy, with higher R² and lower MSE values.

#### 4.2.3. Support Vector Machines (SVM)
SVM performs well with high-dimensional data and complex relationships. However, it is computationally intensive and requires careful parameter tuning to achieve optimal results.

### 4.3. Performance Comparison Summary
- **Random Forest Regression**: Performed well but had slightly higher MSE compared to XGBoost.
- **XGBoost**: The best performer, with higher R² and lower MSE across the models.
- **SVM**: Effective but more computationally expensive and with marginally lower accuracy than XGBoost.

## Conclusions

In evaluating the three machine learning models, XGBoost proved to be the most accurate and effective in predicting CO2 emissions. It consistently outperformed Random Forest Regression and Support Vector Machines in terms of R² and MSE. This makes XGBoost the recommended model for forecasting emissions in real-world applications, offering better performance with less computational demand compared to SVM.

For future improvements, the project could explore more advanced optimization techniques for SVM and consider the application of other ensemble methods for emissions forecasting.
