# viabill


Utilizing your business knowledge and skills please accomplish the following tasks:  
1. Select transactions that you use as credit applications (write SQL query): 
a. select the last transaction (transactionID increases with time) for each customer in  Transaction table, 
b. join result from previous point with customer Income - if Income is Missing replace it  with -999 value,  
2. Create a new feature based on transaction data - using Python or/and SQL: a. create “trans_price_avg_lst3” – for credit applications (transactions selected in point 1 ) calculate a value that present an average price of 3 previous transactions,  
3. Check if there is a dependency between age and sex in the data – use statistical test if  applicable, 
4. We want to send adequate marketing communication to customer – propose customers  segments that we could use when we want to send emails with offers, 
5. Perform exploratory data analysis (EDA) and present interesting findings related to credit risk, 6. Build model/models that predict if customer will not pay back the loan.  


SOLUTION.

Task was done in 3 different ways:

1. Assigning standartization score for each value and using target category as paid/not-paid (where paid but late also included inside of paid category).
2. Assigning standartization score for each value and using target category as paid/paid but late /not-paid.
3. Using optimal binning each variable was binned with weight of evidence WOE metric and monotonic trend. target category was used as paid/not-paid

Pre processing steps include:

1. exploratory data analysis (EDA)
2. null values
3. outlier detection and treatment
4. feature creation
5. feature importance

Modeling stpes include:

1. ML models used - Logistic Regression, Random Forest, XGB and LightGBM
2. Optimization techniques - Grid search and cross validation
3. Performance measures  - confusion matrix, classification table ( recall, f1 score an etc.), Roc curve , Roc Auc score and Gini coefficient

Deployment:

1. Deployment was done on sample new 10 customers with 'price', 'sex', 'age', 'income','trans_price_avg_lst3' informations.
2. Probability of default was calculated by given ML model for new customers.

Customer segmentation:

1. Dendogram was used to clarify segment size.
2. Hierarchical Clustering was utilized to predict target.
3.  groupby method customer segmentation analysis was shown.
