# Feature Selection  
Justification for feature selection:
1. Prediction accuracy: can be improved by shrinking or setting features to zero, reducing variance but increasing bias
2. Interpretation: more full appreciate big-picture effects of features 
   
# Filter Methods
Filtering techniques preprocess features to remove ones that are unlikely to be useful for the model. For example, one could compute the correlation or mutual information between each feature and the response variable, and filter out the features that fall below a threshold. These are typically faster, but more subjective than wrapper methods. 

## Numeric Outcomes
### Sample Correlation  
Quantifies linear (Pearson's) or curved (Spearman's) correlation coefficient  

### $t$ Statistic
Assumes normal distribution, p-value represennts significance  

## Categorical Data  
- Test if mean coefficients per class are different 
- One-vs-all ROC/AUC comparisons
- Maximal Information Coefficient gives strength of the linear and non-linear association between two variables X and Y.

# Wrapper Methods
Search algorithms that treat predictors as inputs and model performance as outputs 

- Does not use previous data, adding new predictors does not re-evaluate adding previous predictors
## Forward, Backward and Stepwise  
*Forward:* predictors added one-by-one and model evaluated 
*Backward:* Full model incrementally stripped of predictors

## Simulated Annealing
An initial subset of predictors is selected and is used to estimate performance of the model (denoted here as $E_1$, for the initial error rate). The current predictor subset is slightly changed, and another model is created with an estimated error rate of $E_2$. If the new model is an improvement over the previous one (i.e., E 2 < E 1), the new feature set is accepted. However, if it is worse, it may still be accepted based on some probability p i a , where i is the iteration of the process. This probability is configured to decrease over time so that, as i becomes large, it becomes very unlikely that a suboptimal configuration will be accepted. The process continues for some pre-specified number of iterations and the best variable subset across all the iterations, is used. The idea is to avoid a local optimum.


## Genetic Methods  
A chromosome is a binary vector with length equal to number of features. Each binary entry represents presence or absence of feature, the "fitness" of a method is determined by the metric using the predictors. To begin the search process, GAs are often initiated with a random selection of chromosomes from the population of all possible chromosomes. Each chromosome’s fitness is computed, which determines the likelihood of the chromosome’s selection for the process of reproduction. Two chromosomes from the current population are then selected based on the fitness criterion and are allowed to reproduce. In the reproduction phase, the two parent chromosomes are split at a random position (also called loci), and the head of one chromosome is combined with the tail of the other chromosome and vice versa. After crossover, the individual entries of the new chromosomes can be randomly selected for mutation in which the current binary value is changed to the other value.

**Embedded Methods**  
These methods perform feature selection as part of the model training process.
For example, a decision tree inherently performs feature selection because it
selects one feature on which to split the tree at each training step