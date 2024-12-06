# **Bank Marketing Campaign Prediction**

## **Overview**
This project predicts whether a customer will subscribe to a long-term deposit based on their demographic and campaign-related features. The project involves implementing two machine learning models:
1. **Support Vector Machine (SVM)**
2. **Logistic Regression using Gradient Descent**

Both models are evaluated and compared using various metrics to determine their effectiveness in solving this classification problem.

---

## **Dataset**
The dataset contains customer information from a bank's marketing campaign. Key features include:
- **Numerical Features**: `Age`, `Balance`, `Duration`, `Campaign`.
- **Categorical Features**: `Job`, `Marital`, `Education`, `Housing`, `Loan`, `Month`.
- **Target**: `Subscription` (1 if the customer subscribed to a long-term deposit, 0 otherwise).

The dataset is preprocessed by:
1. Encoding categorical features using one-hot encoding.
2. Handling missing values (`unknown`) via imputation.
3. Standardizing numerical features.

---

## **Methods**

### 1. **Support Vector Machine (SVM)**
- **Objective**: Use `scikit-learn`'s SVM implementation to classify customers.
- **Hyperparameter Tuning**: 
  - `C`: Regularization parameter.
  - `Gamma`: Kernel coefficient.
  - Performed using **GridSearchCV**.
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score, ROC-AUC.

### 2. **Logistic Regression**
- **Objective**: Implement logistic regression using custom **gradient descent**.
- **Loss Function**: Cross-Entropy Loss.
- **Optimization**: Gradient descent with a specified learning rate and number of iterations.

---

## **Results**
### Model Comparison:
![image](https://github.com/user-attachments/assets/6afc129e-890a-450f-9bbc-e328acbbce07)


- Both of these algorithms perfomed good with the accuracy of 90% but slightly better for logestic regression.


---

## **Visualizations**
### 1. Data Analysis:
- Distribution plots for numerical features.
- Count plots for categorical features grouped by the target variable.

### 2. Evaluation:
- Confusion matrices for SVM and Logistic Regression.
- ROC curves and AUC comparison between SVM and Logistic Regression.
  
![image](https://github.com/user-attachments/assets/5dfc36eb-5aaa-4699-92ed-6e7068239607)

---



## **Conclusion**
This project demonstrates the application of machine learning techniques to solve a real-world classification problem. The results highlight the strengths and weaknesses of each model, providing valuable insights for selecting the right approach.

---

## **Future Improvements**
1. Experiment with feature engineering, such as creating new features or selecting the most important ones.
2. Try advanced models like Random Forests or Gradient Boosting.
3. Implement regularization techniques in Logistic Regression.
