# Insurance Cost Prediction with Gradient Descent Variants

This project implements various gradient descent methods to predict insurance costs based on age, BMI, and the number of children using a linear regression model. The model is trained and evaluated with Gradient Descent (GD), Stochastic Gradient Descent (SGD), and Mini-Batch Gradient Descent on both normalized and unnormalized data.

## Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [Data](#data)
- [Tasks](#tasks)
  - [1. Gradient Descent Methods Implementation](#1-gradient-descent-methods-implementation)
  - [2. Comparison of Zero vs. Random Weight Initialization](#2-comparison-of-zero-vs-random-weight-initialization)
  - [3. SGD with MAE Loss Function](#3-sgd-with-mae-loss-function)
  - [4. Convergence with Normalized vs. Unnormalized Data](#4-convergence-with-normalized-vs-unnormalized-data)
- [Results](#results)
- [Conclusion](#conclusion)

## Overview
In this project, a linear regression model is trained to predict **insurance costs** using features such as age, BMI, and the number of children. We explore and evaluate different gradient descent techniques and variations in data preprocessing to understand their influence on model performance.

## Project Structure
- `insurance.csv`: Dataset with columns for age, BMI, number of children, and insurance cost.
- `Insurance_Regression.ipynb`: Jupyter Notebook implementing and analyzing the different tasks in this project.
- `README.md`: Documentation for the project.

## Requirements
- Python 3.x
- `numpy`, `pandas`, `matplotlib`

Install the required libraries using:
```bash
pip install numpy pandas matplotlib
```

## Data
The dataset used here contains information on **insurance costs** based on:
1. **Age**
2. **Body Mass Index (BMI)**
3. **Number of Children**

The target variable is the **insurance cost**.

## Tasks

### 1. Gradient Descent Methods Implementation
We implemented three gradient descent methods:
- **Batch Gradient Descent (GD)**: Uses the entire dataset to update weights at each step.
- **Stochastic Gradient Descent (SGD)**: Uses one data point at a time for each weight update, leading to faster convergence but more variance in the updates.
- **Mini-Batch Gradient Descent**: Combines aspects of both GD and SGD by using small batches of data for weight updates.

The model minimizes the Mean Squared Error (MSE) loss, and we plotted the error over iterations for each method to visualize convergence.

### 2. Comparison of Zero vs. Random Weight Initialization
We trained the model using two different weight initialization methods:
- **Zero Initialization**: All weights are initialized to zero.
- **Random Initialization**: Weights are initialized randomly.

We then compared the convergence behavior of each initialization by plotting the error at each iteration. This task helps illustrate the importance of initial weights in the convergence rate of gradient descent.

### 3. SGD with MAE Loss Function
Using SGD, we implemented the model to minimize the Mean Absolute Error (MAE) instead of MSE and compared it with the MSE results. Since MAE is less sensitive to outliers, this comparison highlights the influence of different loss functions on convergence. We also checked if the model encountered any non-differentiable points due to the MAE loss.

### 4. Convergence with Normalized vs. Unnormalized Data
To understand the effect of feature scaling on model performance, we compared the convergence of SGD on:
- **Normalized Data**: Features were scaled to have a mean of 0 and standard deviation of 1.
- **Unnormalized Data**: Original feature values were used without any scaling.

We visualized the difference in convergence rates and stability, highlighting the importance of normalization in gradient-based optimization.

## Results
1. **Gradient Descent Methods**: Each method demonstrated distinct convergence behaviors, with Batch GD providing stable updates but slower convergence, and SGD showing faster but noisier updates.
2. **Weight Initialization**: Random initialization showed a slightly faster convergence compared to zero initialization.
3. **Loss Function Comparison**: MAE provided a different convergence path than MSE, with fewer large updates due to reduced sensitivity to outliers.
4. **Normalization Effect**: Normalized data led to faster and more stable convergence, showing the critical role of feature scaling.

## Conclusion
This project demonstrates how variations in gradient descent methods, loss functions, and feature scaling affect the performance of linear regression for insurance cost prediction. By understanding these factors, one can build more robust and efficient models for similar regression tasks.
