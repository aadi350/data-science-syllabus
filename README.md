# Data Science Syllabus
This is a collection of topics, resources and otherwise useful resources I found (am finding) during pursuit of my graduate degree in Data Science. This list may not be completely exhaustive, and I am going to miss some niche things, however this is what I'd consider a ground zero for covering important topics in data science.

# Sections to Add
*topic filepath*
## Data Engineering
- [ ] Binary Trees Regression to data-engineering/data-structures
- [x] B-Trees data-engineering/data-structures
- [ ] SSTables/LSMTrees data-engineering/data-structures
- [ ] Linked List data-engineering/data-structures
- [x] Hash tables data-engineering/data-structures

## Machine Learning
- [ ] ANNs machine-learning/algorithms/ann
- [ ] Gradient-boosted trees 
- [x] kNN
- [x] Linear Regression 
- [ ] Explaiability machine-learning/coding
- [ ] In-detail feature selection machine-learning/feature-selection
- [ ] Squared, Absolute, Huber, Cosine losses machine-learning/loss-functions
- [x]  time-series basic concepts machine-learning/time-series
- [x] Refactor algorithms in time-series to /algorithms folder  

## Probability  
- [ ] Binomial probability/distributions
- [ ] Normal probability/distributions
- [ ] Poisson probability/distributions
- [ ] Power Law probability/distributions

# SQL-Patterns 
- [ ] Common SQL Patterns sql-patterns/*

# Sections to Update
- [ ] Anomaly detection should be organised into general background and common algorithms machine-learning/anomaly-detection
- [x] Assumptions, intuition for logistic regression machine-learning/algorithms/logistic-regression  
- [ ] Assumptions, intution for SVM machine-learning/algorithms/svm
- [ ] Complete storage and replication from DA in data-engineering/

# Data Science Syllabus  
## Statistics  
### Experimental Tests 
--Practical Statistics for Data Scientists Ch3, Sulliivan Ch1
[A/B Testting](.)  
[Hypothesis Testing](statistics/hypothesis-testing.md)  
[Resampling](.)  
[Significance](.)  
[t-Tests](.)  
[Degrees of Freedom](.)
[ANOVA](.)  
[Chi-Squared Test](.)  
[Power and Sample Size](.)
### Data Sampling
[Sample Bias](.)
[Selection Bias](.)
[Bootstrap](.)
[Normal Distribution](.)
[t-Distribution](.)  
[Binomial Distribution](.)  
[F-Distribution](.)  
[$\chi^2$ Distribution](.)  
[Common Distributions](statistics/distributions.md)  


[Correlation](.)  
[Probability](.)  --Sullivan Ch 5   
[Summarising Data](.)  --Sullivan Ch3  
[Parameter Estimation](.)  --Sullivan Ch 9

## Data Engineering  
[Data Structures](data-engineering/data-structures.md)  
[Document Model](data-engineering/document-model.md)  
[Partitioning](data-engineering/partitioning.md)  
[Replication](data-engineering/replication.md)  
[Storage](data-engineering/storage.md)  

### Cloud  
[Kubernetes](data-engineering/containers/kubernetes.md)  

## Machine Learning  
[Metrics](machine-learning/metrics.md)  
[Data Cleaning](machine-learning/data-cleaning.md)  
[Dimensionality Reduction](machine-learning/dim-reduction.md)  
[Feature Engineering](machine-learning/feature-engineering.md)  
[Feature Selection](machine-learning/feature-selection.md)
[Sampling Methods](machine-learning/sampling-methods.md)  
[Loss Functions](machine-learning/loss-functions.md)  
[Model Selection](machine-learning/model-selection.md)  
[Linear Algebra](machine-learning/linear-algebra.md)  

### Specific Areas  
[Recommender Systems](machine-learning/recommender.md)  
[Time-Series](machine-learning/time-series.md)  
[Anomaly Detection](machine-learning/anomaly-detection.md)  

### Optimization Methods  
[Differential vs Non-Differential](.)  
[Gradient Descent](.)   
[Simulated Annealing](.)  


### Algorithms  
[Artificial Neural Networks](machine-learning/algorithms/ann.md)  
[Gradient-Boosted Trees](machine-learning/algorithms/gradient-boosted-tree.md)  
[k-Nearest Neighbours](machine-learning/algorithms/kNN.md)  
[Linear Regression](machine-learning/algorithms/linear-regression.md)
[Logistic Regression](machine-learning/algorithms/logistic-regression.md)
[Support Vector Machine](machine-learning/algorithms/svm.md)  
[Time-Series](machine-learning/time-series.md)  
[Model Explainability with Shapely Values](machine-learning/algorithms/shapely-values-for-explainability.md)  

## SQL Patterns  
[Constraints](sql-patterns/constraints.md)  
[Common-Table Expressions](sql-patterns/ctes.md)  
[Cursors](sql-patterns/cursors.md)  
[Group-by-Aggregate](sql-patterns/group-by-agg.md)  
[Having-vs-Where](sql-patterns/having-vs-where.md)  
[Joins](sql-patterns/joins.md)  
[Triggers](sql-patterns/triggers.md)  
[Cumulative Sum](sql-patterns/cumsum.md)  
[Having vs Where](sql-patterns/having-vs-where.md)  
[Partitioning](sql-patterns/partitioning.md)  

## Code Snippets
[Numpy](code-snippets/numpy.md)  
[cuDF](.)  
[TensorFlow](.)  
[Python](.)
