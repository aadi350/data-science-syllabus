# Metrics

*True Positive*  
Algorithm correctly identifies a '1' or positive case

*True Negative*  
Algorithm correctly identifies a '0' or a negative case  

*False Positive*  
Algorithm incorrectly flags a negative case as positive  

*False Negative*  
Algorithm fails to flag a positive case

**Error rate**  
$\frac{FP + FN}{P + N}$  
Optimize for low error rate is the converse of optimizing for accuracy

**Accuracy**  
$\frac{TP + TN}{P + N}$  
Great when dataset is symmetric, and the cost of false negatives and false positives are the same

**Sensitivity**  
$\frac{TP}{TP + FN}$  
Optimize for sensitivity (recall) when false positives can be tolerated, but not false negatives

**Specificity**  
$\frac{TN}{TN + FP}$  
Optimize for specificity when we don't want any false alarms (false positives)

**Precision**  
$\frac{TP}{TP + FP}$  
Optimize for precision when we wish to be confident about of true positives


**Harmonic Mean**  
$\frac{2TP}{2TP + FP + FN}$  
Best when class distribution is uneven, or weighting of false negatives and false positives are different