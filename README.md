# Credit Risk Classification

## Overview of the Analysis

The purpose of the analysis in this challenge was to develop and evaluate machine learning models to assess the creditworthiness of borrowers. The primary goal was to build models that can predict whether a loan is healthy (low risk) or high-risk based on various features and historical lending data that was provided in the csv file.

The financial information the data was on:

1- Loan Size: The size or amount of the loan requested by the borrower.

2- Interest Rate: The interest rate associated with the loan, representing the cost of borrowing.

3- Borrower Income: The income of the borrower, which is an important factor in assessing their ability to repay the loan.

4- Debt-to-Income Ratio (DTI): The ratio of the borrower's total debt to their income, which helps evaluate their debt management capability.

5- Number of Accounts: The number of financial accounts or lines of credit the borrower has, which provides insights into their credit history and financial stability.

6- Derogatory Marks: The presence of derogatory marks on the borrower's credit report, which can negatively impact their creditworthiness.

7- Total Debt: The total amount of debt owed by the borrower.

8- Loan Status: The target variable, which indicates whether the loan is healthy (low risk) or high-risk. A value of 0 represents a healthy loan, while a value of 1 indicates a high-risk loan.

The primary task was to predict the "Loan Status" based on the borrower's financial information and other features. In essence, the analysis aimed to build a machine learning model that could automatically assess the credit risk associated with each loan application.

### Variables to Predict (Loan Status):

The variable being predicted in this analysis is "Loan Status," which represents whether a loan is healthy (Class 0) or high-risk (Class 1).

The distribution of values in the "Loan Status" variable after handling class imbalance using oversampling (RandomOverSampler) is as follows:
Class 0 (Healthy Loans): 56,271 samples
Class 1 (High-Risk Loans): 56,271 samples

### Machine Learning Process:

The analysis went through several stages in the machine learning process:

1- Data Loading and Exploration: The dataset was loaded and explored to understand its structure, features, and target variable.

2- Data separation: The dataset was split into features (X) and the target variable (y).

3- Handling Class Imbalance: Class imbalance was assessed, revealing a significant imbalance between healthy and high-risk loans.

4- Resampling: RandomOverSampler was applied to balance the class distribution by oversampling the high-risk loans.

5- Model Building and Training: A logistic regression model was selected for binary classification due to its interpretability and suitability for this task.
The logistic regression model was trained using the resampled training data.

6- Model Evaluation: Various performance metrics were computed, including balanced accuracy, precision, recall, F1-score, and classification reports.

7- Confusion Matrix: A confusion matrix was generated to understand true positives, true negatives, false positives, and false negatives.

8- Analysis and Conclusion: the performance of the logistic regression model was summarized, highlighting high precision, recall, and overall accuracy.

9- Interpretation: Insights were provided regarding the model's ability to distinguish between healthy and high-risk loans.

### Methods used:

A logistic regression model was chosen for binary classification due to its simplicity and interpretability.

RandomOverSampler was used to address class imbalance by oversampling the minority class.

Various metrics such as balanced accuracy, precision, recall, F1-score, and classification reports were used to assess model performance.

The confusion matrix was employed to analyze model predictions in more detail.

## Results
* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores:
    
    * Balanced Accuracy Score: Approximately 0.952
    * Precision for Class 0 (Healthy Loans): 1.00
    * Recall for Class 0 (Healthy Loans): 0.99
    * F1-Score for Class 0 (Healthy Loans): 1.00
    * Precision for Class 1 (High-Risk Loans): 0.85
    * Recall for Class 1 (High-Risk Loans): 0.91
    * F1-Score for Class 1 (High-Risk Loans): 0.88


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores:
    
      * Balanced Accuracy Score: Approximately 0.994
      * Precision for Class 0 (Healthy Loans): 1.00
      * Recall for Class 0 (Healthy Loans): 0.99
      * F1-Score for Class 0 (Healthy Loans): 1.00
      * Precision for Class 1 (High-Risk Loans): 0.84
      * Recall for Class 1 (High-Risk Loans): 0.99
      * F1-Score for Class 1 (High-Risk Loans): 0.91

## Summary

Recommendation:

Based on the analysis results, the logistic regression model trained on resampled data is the recommended model for assessing the creditworthiness of borrowers based on the below:

High Balanced Accuracy Score: The model achieved a balanced accuracy score of approximately 0.994, indicating its ability to make accurate predictions for both healthy (Class 0) and high-risk (Class 1) loans.

High Precision and Recall: The model exhibits high precision and recall for both classes. It correctly identifies the majority of actual high-risk loans (Class 1) while maintaining low false positives for healthy loans (Class 0).

Favorable F1-Score: The F1-Scores for both classes are relatively high, indicating a good balance between precision and recall. This is essential for minimizing the risk of false positives and false negatives.

Balanced Performance: The model performs well for both predicting healthy and high-risk loans, which is crucial for lenders. However, the interpretation of "best" may depend on the specific priorities of the lending institution.

However, the choice may depend on the specific objectives and risk tolerance of the lending institution. Further fine-tuning and model selection can be explored based on the institution's priorities.
