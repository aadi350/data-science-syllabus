# Data Cleaning  
Data cleaning is the process of fixing or removing incorrect, corrupted, incorrectly formatted, duplicate, or incomplete data within a dataset.  

#### Duplicate Removal  
Irrelavant or unwanted data points removed. This may occur after combining data sources. Irrelevant sources may skew predictions and slow down inference.  

#### Fixing Structural Errors  
Structural errors are when you measure or transfer data and notice strange naming conventions, typos, or incorrect capitalization. These inconsistencies can cause mislabeled categories or classes. For example, you may find “N/A” and “Not Applicable” both appear, but they should be analyzed as the same category.  

#### Filtering Outliers  
Owing to improper data-entry or spurious events, unwanted outliers may occur. Remove if irrelevant to analysis.  

#### Handling Missing Data  
1. Drop observations with missing values, however this drops and loses information  
2. Input missing values based on others (mean, median, etc)  or use a standard value  
3. Use a model with a 'default' option for missing data  
4. Use a simple model to impute values  

#### Handling Noisy Data  
*Noise* is random variance, and is visualized using box-plots and scatter plots  
1. Binning methods smooths sorted values by using near values  
2. Regression forces data to conform to a function  
3. Outlier analysis (clustering) can be used to detect outliers  

# Data Transforms  
#### Smoothing  
Eliminating noise in the data to see more data patterns.

#### Attribute/feature construction  
New attributes are constructed from the given set of attributes  

#### Aggregation  
Summary and aggregation operations are applied on the given set of attributes to come up with new attributes  

#### Normalization  
The data in each attribute is scaled between a smaller range, for example, 0 to 1 or -1 to 1  

#### Discretization  
Raw values of the numeric attributes are replaced by discrete or conceptual intervals, which can be further organized into higher-level intervals  

#### Concept hierarchy generation for nominal data  
Values for nominal data are generalized to higher-order concepts.


# Feature Engineering  
*Good features should not only represent salient aspects of the data, but also conform to the assumptions of the model*  
## Binarization  
Conversion of a value to two classes by setting an appropriate threshold  

## Quantization  
Quantization maps a continuous number to a discrete one. 
Raw counts across several orders of magnitude would decrease the effectiveness of OLS in regression and other distance measures, a large count in one element would severely outweight similariyt between other elements  

### Quantile Binning  
To deal with large gaps in counts of data (if some bins are very empty), bins can be adaptively positions based on the data distribution using *quantiles*  
*Quantiles are values dividing data into equal proportions*  

## Power Transforms  
These are *variance-stabilizing* transforms  

### Box-Cox Transform  
Generalization of the square-root and log transforms and works for only positive data.  
*Negative data can be handled by shifting the data by a fixed constant*   
$$
 \bar{x} =
    \begin{cases}
      \frac{x^\lambda - 1}{\lambda} & \lambda\neq 0\\
      \ln{x} & \lambda=0
    \end{cases}       
$$
### Log Transformation  
Compresses the range of large numbers and expands the range of small numbers  
Useful in dealing with positive numbers from a heavy-tailed distribution by compressing the long tails in the high end and expanding the tail in the low end.  
Has the effect of increasing bin spacing  
Does not change the shape of the distribution (as in log and other power transforms)

## Scaling and Normalization  
Certain models are affected by scales of data
#### Min-Max Scaling  
Squeezes data points fo be wtihin $[0,1]$ range  
#### Standardization  
*Variance scaling*  
Results in feature with mean $0$ and variance unity  
$$
\tilde{x} = \frac{x - mean(x)}{\sqrt{var(x)}}
$$
#### $l^2$ Normalization  
Divides feature by its Euclidean norma  

## Handling Interaction Features  
A simple pairwise interaction feature is the product of two features  
Extending a model to account for multiplication between features can capture logical/mathematical predictions based on combinations of features  
Expensive to use, as traning time increased.  

# Feature Selection  
**Filter Methods**  
Filtering techniques preprocess features to remove ones that are unlikely to be useful for the model. For example, one could compute the correlation or mutual information between each feature and the response variable, and filter out the features that fall below a threshold. Chapter 3 discusses examples of these techniques for text features. Filtering techniques are much cheaper than the wrapper techniques described next, but they do not take into account the model being employed. Hence, they may not be able to select the right features for the model.  

**Wrapper Methods**  
which means you won’t accidentally prune away features that are uninformative by themselves but useful when taken in combination. The wrapper method treats the model as a black box that provides a quality score of a proposed subset for features. There is a separate method that iteratively refines the subset   

**Embedded Methods**  
These methods perform feature selection as part of the model training process.
For example, a decision tree inherently performs feature selection because it
selects one feature on which to split the tree at each training step