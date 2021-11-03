# Logistic Regression
## Intuition  



<h2 style="color:#00A">Assumptions</h2>  

<h2 style="color:#0A0">Advantages</h2>  

- easy to interpret. the output can be interpreted as a probability: you can use it for ranking instead of classification.  
- good for cases where features are expected to be roughly linear, and the problem to be linearly separable.  
- can easily "feature engineering" most non-linear features into linear ones.  
- robust to noise  
- can use l2 or l1 regularization to avoid overfitting(and for feature selection)  
- efficient, and can be distributed(ADMM)    
- no distribution requirement  
- easily update the model to take in new data (using an online gradient descent method)  

<h2 style="color:#A00">Disadvantages</h2>
if the variables are normally distributed and the categorical variables all have 5+ categories: use Linear discriminant analysis  
if the correlations are mostly nonlinear: use SVM  
if sparsity and multicollinearity are a concern: Adaptive Lasso with Ridge(weights) + Lasso 

**Lasso(L1)**  
no distribution requirement  
compute L1 loss  
variable selection  
suffer multicollinearity  

**Ridge(L2)** 
no distribution requirement   
compute L2 loss   
no variable selection  
not suffer multicollinearity  

 