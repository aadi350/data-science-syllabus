# Feature Selection  
**Filter Methods**  
Filtering techniques preprocess features to remove ones that are unlikely to be useful for the model. For example, one could compute the correlation or mutual information between each feature and the response variable, and filter out the features that fall below a threshold. Chapter 3 discusses examples of these techniques for text features. Filtering techniques are much cheaper than the wrapper techniques described next, but they do not take into account the model being employed. Hence, they may not be able to select the right features for the model.  

**Wrapper Methods**  
which means you won’t accidentally prune away features that are uninformative by themselves but useful when taken in combination. The wrapper method treats the model as a black box that provides a quality score of a proposed subset for features. There is a separate method that iteratively refines the subset   

**Embedded Methods**  
These methods perform feature selection as part of the model training process.
For example, a decision tree inherently performs feature selection because it
selects one feature on which to split the tree at each training step