# Bias-Variance Tradeoff  
The rror of a given model using squared-error loss cann be thought of as
$$
Err(x_0) = \text{Irreducible Error} + \text{Bias}^2 + \text{Variance}
$$  
**Irreducible Error** is the variance of the target about its true mean  
**Bias** is the amount by which the average of the estimate varies from the true mean  
**Variance**  is the expected squared deviation of our estimate about its mean  

**ROC Curve**  
Plot of *True-positive rate* against *False-positive rate*. Visually shows trade-off between sensitivity (recall) and specificity (or TPR for FPR)

**AUC**  
*Area-Under-Curve* for ROC, aiming for high AUC $X\%$ implies that model will be able to distinguish between output class $X\%$ of the time

**PRC**  
*Precision-Recall Curve* plots Precision against Recall. This is analagous to the *bias-variance* tradeoff.

**AIC**  
*Akeikie Information Criterion* estimates the amount of information lost by a model, promoting goodness of fit whilst penalizing complexity.  
Both AIC and *BIC* (or *Schwarz criterion*) are applicable where fitting is carried out by maximization of a log-likelihood. *BIC* is proportional to AIC, but penalizes complex models more heavily.

**MDL**  
*Minimum-Description-Length* derived as a result of Occam's Razor, which favours simpler models. The best hypothesis to describe data is the one that compresses it the most


# Overfitting and Underfitting
In overfitting, a statistical model describes random error or noise instead of the underlying relationship.
Overfitting occurs when a model is excessively complex, such as having too many parameters relative to
the number of observations. A model that has been overfitted, has poor predictive performance, as it
overreacts to minor fluctuations in the training data.

**Addressing Overfitting**  
1. Add noise
2. Feature selection  
3. Increase training set size  
4. Regularization 
5. Cross-validation  
6. Boosting and bagging  
7. Dropout  
8. Early stopping   


**Addressing Underfitting**  
1. Add features  
2. Increase training time  
3. Increase model complexity  

Underfitting occurs when a statistical model or machine learning algorithm cannot capture the underlying
trend of the data. Underfitting would occur, for example, when fitting a linear model to non-linear data.
Such a model too would have poor predictive performance.



# Sampling Methods
### Key Terms
**Imbalanced Data Set**  
Data with skewed class proportions.  
With imbalanced data, a model may too much (or too little) from positive/negative examples. 

## Techniques
### Downsampling
Training on a disproportionately low subset of majority class examples, by randomly sampling from the majority an number equalling the minority.
**Advantages**  
Model converges faster
Space is saved on disk  
Upweighting ensures outputs can still be interpretted as probabilities

**Disadvantages**  
Important information may be left out  
Less data may result in less generalizability of the model  


### Upweighting  
Adding example weight to downsamplied class equal to the factor by which downsampling was carried out

### Resampling
Resampling is a methodology of economically using a data sample to improve the accuracy and quantify the uncertainty of a population parameter. Given a single estimate of a population parameter, the variability is not known, this can be found by multiplie estimates of the parameter. 

This is done to estimate the accuracy of sample statistics, to sample labels on data points and validating models on random subsets

### Bootstrap
Samples are drawn from the dataset with replacement (allowing the same sample to appear more than once in the sample), where those instances not drawn into the data sample may be used for the test set.

### k-Fold Cross Validation  
A dataset is partitioned into k groups, where each group is given the opportunity of being used as a held out test set leaving the remaining groups as the training set. The k-fold cross-validation method specifically lends itself to use in the evaluation of predictive models that are repeatedly trained on one subset of the data and evaluated on a second held-out subset of the data.   

**Choosing K**  
With $K=N$, the estimator is unbiased but exhibits high variance and highlu computationally complex. Lower *K* values exhibit lower variance by higher bias.  
Cross-validation is carried out *after* feature-selection.
**Rule of thumb is to use 5- or 10-fold CV*
