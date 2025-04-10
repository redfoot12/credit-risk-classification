# Module 20 Report

## Overview of the Analysis

* **Purpose of the analysis** - The goal of this analysis was to determine if the Logistic Regression machine learning model can more accurately predict healthy loans versus high-risk loans using an original dataset or a resampled dataset to increase the size of the minority class.
* **The Dataset** - The dataset used to perform the analysis consists of information on 77,536 loans. The data includes columns for loan_size, interest_rate, borrower_income, debt_to_income ratio, number_of_accounts, derogatory_marks, total_debt, and loan_status. **loan_status** is the category intended for prediction from this analysis. The remaining columns will be used as features to train the data and inform predictions.
* **loan_status** was highly imbalanced with 75,036 healthy loans (0) and only 2500 high-risk loans (1)
* **Machine Learning Process** involved: 
	* Cleaning and preparing the data
	* Splitting into training and testing sets
	* Creating a logistic regression model
	* Evaluating the model
	* Using **RandomOverSampler** to rebalance the training data
	* Re-training and evaluating the model on the balanced dataset
	

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Logistic Regression on Original Data
  -  **Balanced Accuracy Score:** 96.80%
	-   **Precision:**
	    -   Class `0` (Healthy): 1.00
	    -   Class `1` (High-Risk): 0.84
    -  	 **Recall:**
	    -   Class `0`: 0.99
	    -   Class `1`: 0.94
        
	-   **F1-Score (Class `1`):** 0.89

* Machine Learning Model 2: Logistic Regression on Oversampled Data
	- **Balanced Accuracy Score:** 99.36%
	-   **Precision:**
	    -   Class `0` : 1.00
	    -   Class `1` : 0.84
    -  	 **Recall:**
	    -   Class `0`: 0.99
	    -   Class `1`: 0.99
        
	-   **F1-Score (Class `1`):** 0.91

## Summary



Both logistic regression models performed well in predicting loan outcomes, but the oversampled version showed a clear edge.

The original model achieved strong results, but its recall for identifying high-risk loans (Class 1) was 0.94. After applying oversampling to balance the training data, recall improved to 0.99 — a key improvement when the goal is to better identify borrowers who may pose a greater credit risk.

Given the improved recall and balanced accuracy (99.36%), the oversampled model is the better option for credit risk classification. It provides more reliable detection of high-risk loans while maintaining strong overall performance.
