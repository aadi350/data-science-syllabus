# k-Nearest Neighbours  
*keeps all data points in memory, makes predictions for new unseen data points based on majority similarity of nearby points*  
Similarity can be measured using *Euclidean*, *Cosine*, *Hamming*, *Manhattan* or *Minkowski* distances  
No learning is required
*k* is inversely proportional to bias but directly proportional to variance  

<span style="color:green;">**Advantages**</span>  
- Does not assume much about data distribution   
- Simple to interpret  
- Applicable in multiple cases and ver high accuracy  

<span style="color:red">**Disadvantages**</span>  
- Very sensitive to outliers, data curation is necessary  
- Memory-intensive, data can be stored on disk and indexed using a **k-d** tree to improve performance  
- Computational complexity increases exponential to size of dataset, kNN can be made stochastic by taking a random sample from the dataset to make predictions  
- Struggles in high-dimensional space  
- Performs best in normalized data