# Description 
Jusan has many clients and it wants to draw more of them by means of ads. But, to retain its current clients, it needs to identify the group of people who are interested in its advertisements and in using its products and services so that Jusan will send its ads primarily to them. In the meantime, the less interested group should receive fewer ads because Jusan does not want to lose its clients by bothering them with excess ads. 

# Task 
Jusan has accumulated many data on its clients. We have training and testing sets consisting of 48 features/columns, 950k and 450k rows/samples respectively. Our goal is to clean the data, train the most appropriate model based on the training data, and test it on the testing data. 

# Solution
## Data cleaning
Almost 90% of the of the rows are junk because over 50% of their features is NULL. So, we dropped such rows and were left with 90k samples. Because it also contains string objects representing date, we have converted them to datetime. 

## Model selection
We have considered such models as PLA, Logistic regression, Random Forest, K Nearest Neighbours, and Neural Networks. To compare them, we used the average scores obtained by applying 10-fold cross validation on each model. 

## Conclusion
The cross val scores for PLA, Logistic regression, Random Forest, K Nearest Neighbours, and Neural Networks were found to be 0.9296, 0.9394, 0.9497, 0.9246, 0.9128. Thererefore, the best model was found to be the Random Forest. To confirm, we have tested it on the testing set. The result was found to be 0.9999. 

Remark: because the results are too high, we suspect that overfitting has occurred when training. 
