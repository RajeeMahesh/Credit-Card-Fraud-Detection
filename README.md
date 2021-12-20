# Credit-Card-Fraud-Detection

The goal was to predict the probability that an online credit card transaction is fraudulent, as denoted by the target label isFraud. A crucial part of data science is finding the interesting properties in the data with domain knowledge. 

For online credit card transactions, there are features associated with the transaction or credit card holder and features that can be engineered from transaction histories. 
**
Features associated with the transaction:** 

Date and time
Transaction amount
Merchant
Product
Features associated with the credit card holder:

Card type
Credit card number 
Expiration date
Billing address (street address, state, zip code), 
Phone number 
Email address

Features generated from transaction history:

Number of transactions a credit card holder has made in the last 24 hours (holder features plus device ID and IP address) 
Same or different credit card numbers?
Same or different shipping addresses? 
The total amount a credit cardholder has spent in the last 24 hours
Average amount last 24 hours compared to the historical daily average amount
Number of transactions made from the same device or IP address in the last 24 hours
Multiple online charges in close temporal proximity?
Frequent fraud at a specific merchant?
Group of fraud charges in certain areas?
Multiple charges from a merchant within a short time span?

Encoding target, frequency, and aggregation
To detect credit card fraud, you are looking for unusual credit card behavior. Target, frequency, and aggregation encodings add features that measure the rarity of features or combinations of features. 

With target encoding, features are replaced or added with the probability of the categorical value corresponding to the target. For example, if 3% of fraudulent transactions are of card type “debit,” then the value “debit” is replaced with .03.  

With frequency encoding, features are replaced or added with the count of the categorical value.

Evaluating the model 
To evaluate the model’s accuracy, you must test the model’s predictions against the target labels. To do this, split the training file that has labeled data, train the model on part of the data, and test the predictions with the rest. There are various methods for splitting and training validation. When dealing with time series or time-related data, you should use time-based splitting rather than random splitting. Because this data set is time-related, make sure that you train on data that is earlier in time than the validation data.  
