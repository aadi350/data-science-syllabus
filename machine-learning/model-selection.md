#### Overfitting and Underfitting
In overfitting, a statistical model describes random error or noise instead of the underlying relationship.
Overfitting occurs when a model is excessively complex, such as having too many parameters relative to
the number of observations. A model that has been overfitted, has poor predictive performance, as it
overreacts to minor fluctuations in the training data.

**Addressing Overfitting**  
1. Add noise
2. Feature selection  
3. Increase training set size  
4. Regularization 
5.  Cross-validation  
6. Boosting and bagging  
7. Dropout  
8. Early stopping   


**Addressing underfitting**  
1. Add features  
2. Increase training time  
3. Increase model complexity  

Underfitting occurs when a statistical model or machine learning algorithm cannot capture the underlying
trend of the data. Underfitting would occur, for example, when fitting a linear model to non-linear data.
Such a model too would have poor predictive performance.



# Sampling Methods

#### Resampling
Resampling is a methodology of economically using a data sample to improve the accuracy and quantify the uncertainty of a population parameter. Given a single estimate of a population parameter, the variability is not known, this can be found by multiplie estimates of the parameter. 

This is done to estimate the accuracy of sample statistics, to sample labels on data points and validating models on random subsets

**Bootstrap**  
Samples are drawn from the dataset with replacement (allowing the same sample to appear more than once in the sample), where those instances not drawn into the data sample may be used for the test set.

**k-Fold Cross Validation**  
A dataset is partitioned into k groups, where each group is given the opportunity of being used as a held out test set leaving the remaining groups as the training set. The k-fold cross-validation method specifically lends itself to use in the evaluation of predictive models that are repeatedly trained on one subset of the data and evaluated on a second held-out
subset of the data.

