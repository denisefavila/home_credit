# Home Credit Default Risk
https://www.kaggle.com/c/home-credit-default-risk/data

Objective : predict clients' repayment abilities.

Version 1.0
Score: 0.783

Version 2.0
Score: 0.790

# Data description

## application_{train|test}.csv
This is the main table, broken into two files for Train (with TARGET) and Test (without TARGET).
Static data for all applications. One row represents one loan in our data sample.

Training: 307511 examples, 122 features

Test: 48744 examples, 121 features
## bureau.csv
All client's previous credits provided by other financial institutions that were reported to Credit Bureau (for clients who have a loan in our sample).
For every loan in our sample, there are as many rows as number of credits the client had in Credit Bureau before the application date.

1716428 examples, 17 features
## bureau_balance.csv
Monthly balances of previous credits in Credit Bureau.
This table has one row for each month of history of every previous credit reported to Credit Bureau – i.e the table has (#loans in sample * # of relative previous credits * # of months where we have some history observable for the previous credits) rows.

27299925 examples, 3 features
## POS_CASH_balance.csv
Monthly balance snapshots of previous POS (point of sales) and cash loans that the applicant had with Home Credit.
This table has one row for each month of history of every previous credit in Home Credit (consumer credit and cash loans) related to loans in our sample – i.e. the table has (#loans in sample * # of relative previous credits * # of months in which we have some history observable for the previous credits) rows.

10001358 examples, 8 features
## credit_card_balance.csv
Monthly balance snapshots of previous credit cards that the applicant has with Home Credit.
This table has one row for each month of history of every previous credit in Home Credit (consumer credit and cash loans) related to loans in our sample – i.e. the table has (#loans in sample * # of relative previous credit cards * # of months where we have some history observable for the previous credit card) rows.

3840312 examples, 23 features
## previous_application.csv
All previous applications for Home Credit loans of clients who have loans in our sample.
There is one row for each previous application related to loans in our data sample.

1670214 examples, 37 features
## installments_payments.csv
Repayment history for the previously disbursed credits in Home Credit related to the loans in our sample.
There is a) one row for every payment that was made plus b) one row each for missed payment.
One row is equivalent to one payment of one installment OR one installment corresponding to one payment of one previous Home Credit credit related to loans in our sample.

13605401 examples, 8 features


# Archives description
## home_credit.ipynb 
Main archive with the application_{train|test}.
## bureau_balance.ipynb 
bureau + bureau_balance
## previous_application_POS_CASH.ipynb
POS_CASH_balance + credid_card_balance + previous_application
## installments_payment.ipynb 
installments_payments
## home_credit_models.ipynb 
Merge all datasets + machine learning models with features selection an hyperparameters tunning.


# Feature pre-processing
MinMaxScale

Imput missing values

Feature creation and selection

Encode categorical variables

# Algorithm
## Supervised learning
Light Gradient Boosting

Features importance

Hyperparameter tuning - Random Search

Cross-validation

# Perfomance metric
Accuracy

ROC
