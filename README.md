# ### Financial Fraud Detection

This project aims to use machine learning techniques to detect fraudulent financial transactions. Using a synthetic dataset of bank transactions, the goal is to create a model to accurately recognize fraud and also be able to predict whether a transaction is fraudulent or not. 

##Project Overview
This project used the Logistic Regression and Naive Bayes classifiers to build a fraud detection model. The dataset was cleaned and preprocessed, SMOTE was applied for class balancing and the models were evaluated by Classification Report (accuracy, precision, recall), F1 Score and the Receiver Operating Characteristic (ROC) Curve. 

##Dataset
This dataset contained a mix of discrete and continuous variables:
* step: a unit of time that represents hours in the dataset (e.g. the timestamp of the transaction)
* type: the type of transaction
* amount: the amount of money transferred
* NameOrig: the origin account name
* OldBalanceOrg: the origin accounts balance before the transaction
* NewBalanceOrig: the origin accounts balance after the transaction
* NameDest: the destination account name
* OldbalanceDest: the destination accounts balance before the transaction
* NewbalanceDest: the destination accounts balance after the transaction
* isFlaggedFraud: a "naive" model that simply flags a transaction as fraudulent if it is greaer than 200,000 (this current is not USD)
* isFraud: was this simulated transaction actually fraudulent? In this case, we consider "fraud" to be a malicious transaction that aimed to transfer funds out of a victim's bank account before the account owner could secure their information.

## Key Insights from EDA
* Imbalanced Dataset: the dataset is imbalanced. Non-fraudulent transactions easily outnumbered fraudulent transactions.
* Transactions with highest fraud: Cash_Out and Transfer were the types with the most fraud. 
* Indicators of fraud: features like amount and balance changes were important indicators of fraud

## Exploratory Data Analyses: Univariate, Bivariate & Multivariate
## Univariate Analysis
In this dataset, the majority of transactions were not fraudulent. Approximately 0.1% of transactions were fraudulent. 
![alt text](image.png)

The transactions that were "isFlaggedFraud" were miniscule, and did not warrant a long look. 
![alt text](image-1.png)

Most fraudulent activity was seen in the Cash_Out and Transfer types.
![alt text](image-2.png)    ![alt text](image-3.png)


When analyzing distribution of transaction amounts, I found that it was highly skewed. There was a large number of small transactions and a few very large ones. I applied Log Transformation on "amount" to reduce the impact of extreme values. 
![alt text](image-5.png) ![alt text](image-4.png)




