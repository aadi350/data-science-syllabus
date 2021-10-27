# SVM
Support Vector Machines (SVMs) use a different loss function (Hinge) from LR.  
they are also interpreted differently (maximum-margin).  
SVM with a linear kernel is similar to a Logistic Regression in practice 
if the problem is not linearly separable, use an SVM with a non linear kernel (e.g. RBF). (Logistic Regression can also be used with a different kernel) 

<h2 style="color: #0AA">Advantages</h2>  

good in a high-dimensional space (e.g. text classification).  
high accuracy  
good theoretical guarantees regarding overfitting  
no distribution requirement  
compute hinge loss  
flexible selection of kernels for nonlinear correlation  
not suffer multicollinearity  

 
<h2 style="color: red">Disadvantages</h2>  
can be inefficient to train, memory-intensive and annoying to run and tune  
not for problems with many training examples.  
not for most "industry scale" applications (anything beyond a toy or lab problem)  
 