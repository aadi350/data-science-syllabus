# Hypothesis Testing

> Proof-by-contradiction, temporarily assume some thing is false (null hypothesis), we look at our data to see how much it agrees with our thing (p-value), conclude whether or not the thing (hypothesis) is true or not

- [x]  *Introduction to Probability and Statistics -* Chapter 9, 10, 15
- [x]  *Mathematical Statistics with Applications -* Chapter 10
- [x]  *Think Stats -* Chapter 7

## Parametric Testing
**Critical Value Approach**  | ***p*-value Approach** 
------------ | -------------
Set up rejection region based on critical values of statistic's sampling distribution, if stat falls in RR, null is rejected   | Find *p*-value based on observed value of test statistic, if smaller than alpha, null is rejected


### Important Terms

**Statistical Significance** $\alpha$ is robability of falsely rejecting null hypothesis, known as maximum tolerable risk for incorrect rejection, or *the likeliness of data to happen by chance*


**Practical significance** refers to the idea that, while small differences between the
statistic and parameter stated in the null hypothesis are statistically significant, the
difference may not be large enough to cause concern or be considered important
$\beta$ is probability of falsely non-rejecting null hypothesis when alternative is true

**Power** measures probability of taking the action that we wish to occur $1-\beta$

**p-value** or observed significance level is smallest value of $\alpha$ for which $H_{0}$ can be rejected, measures strength of evidence against null, is **actual** risk of committing a Type I error

**Two-tailed** test is non-directional, typically used to check a difference  
**One-tailed** test checks where parameter exceeds some limit


Test defined by **null** and **alternative** hypotheses $H_{0}$ and $H_{1}$


## Large-Sample Tests
Normalize data using $z = \frac{\bar{x}-\mu_{0}}{\sigma/n}$

### Difference of Means
*Assume normally distributed samples*  

**Independent Samples**  
**Welch's t-test** 

$t = \frac{\bar{x}_{2}-\bar{x}_{1}}{\sqrt{\frac{\sigma_{1}^{2}}{n_{1}}-\frac{\sigma_{2}^{2}}{n_{2}}}}$ 

**Paired/Dependent Samples**  
Difference in means are taken followed by t-test    
$t = \frac{\bar{d}}{s_d/\sqrt{n}}$ 



**Difference in binomial populations**  
$z = \frac{\hat{p_{1}}-\hat{p_{2}}}{\sqrt{\frac{p_{1}q_{1}}{n_{1}}}-\frac{p_{2}q_{2}}{n_{2}}}$


**Kolmogorov-Smirnov Test**  
Measures similarity between two cdfs  
Takes maximum separation between cdfs, compares this distance to a particular target $c(\alpha)\sqrt{\frac{n_{1}+n_{2}}{n_{1}n_{2}}}$  
Fewer technical assumptions than t-testing  
Can be used to test normality

### Difference in Standard Deviation 
**Fisher's F**  
This is a right-skewed distribution, which depends on the degrees-of-freedom afforded to it  
$F = \frac{s^2_1}{s^2_2}$

Hypothesis testing measures statistical significance, importance measures by how much

### Quantifying Importance
$$\text{Cohen's } d= \frac{|\mu - \mu'|}{\sigma}$$

### Measures of Explained Variance
**Pearson's $\bold{r^2}$**  
Square of correlation measures proportion of explained variance  
Assumes linear correlation, will not measure strenght of nonlinear relationships 



## Small-Sample

*Central limit theorem* does not guarantee that $\frac{\bar{x}-\mu}{s/\sqrt{n}}$ is normal for small populations (< about 30)

*Student's t-distribution* approaches normal for large n, is typically heavier tailed (more variability)  
Sample must be random and normally distributed  
Robust to non-normality, results do not vary very much

### Difference in Means

$t = \frac{\bar{x}-\mu}{s/\sqrt{n}}$

Null is rejected when $t > t_{\alpha}$ (or $t < -t_{\alpha}$ when alternative hypothesis is $\mu < \mu_{0}$
For two-tailed $t > t_{\alpha/2}\text{ or } t > t_{\alpha/2}$  
Confidence Interval for $\mu$ is $\bar{x} \pm t_{\alpha/2}\frac{s}{\sqrt{n}}$

#### Difference of Means 
**Pooled Variance**

Assume common variance, normal, independent populations, randomly sampled  
*Pooled* variance (weighted by size of population) used to calculate standard error  
t-statistic using pooled variance and difference, dof is sum of number of samples minus 2


CI for difference is $\bar{x}_{1}-\bar{x}_{2}\pm \sqrt{s^{2}\left(\frac{1}{n_{2}}+\frac{1}{n_{2}}\right)}$

---

**Paired Difference**

Assume dependent samples, pairing/blocking done before expierment

$$t = \frac{\bar{d}}{s_{d}\sqrt{n}}$$

CI for paired difference is $\bar{d}\pm t_{\alpha/2}\left(\frac{s_{d}}{\sqrt{n}}\right)$

**Testing for Variance**

Assume sample randomly selected from normal

Null hypothesis is $\sigma^{2} = \sigma^{2}_{0}$

Reject null when statistic $\chi^{2} = \frac{(n-1)s^{2}}{\sigma_{0}^{2}}$ greater than $\chi^{2}_{\alpha}$ (or less than $\chi^{2}_{1-\alpha}$ ) for one-tailed, two tailed replaces $\alpha$ with $\alpha/2$

CI for variance is $\frac{(n-1)s^{2}}{\chi^{2}_{\alpha/2}} < \sigma^{2} < \frac{(n-1)s^{2}}{\chi^{2}_{1-\alpha/2}}$

**Testing for Difference in Variances**

Assume random independent samples, measurements share a common variance

Take statistic $\frac{s^{2}_{1}}{s^{2}_{1}}\thicksim F$

## Non-parametric Tests

For data are ranks or scales (e.g. a 1-5 rating) and do not satisfy the normality assumption

**Wilcoxon Rank-Sum Test**

Tests difference in populations

Order all results and assign a 'rank' depending on value (if readings are 2,4,6 the ranks for 2=1, 4=2, 6=3 and so on)

Find $T_{1} = \text{Sum of the ranks for the first sample}$ then

$T_{1}^{*}= n_{1}(n_{1}+n_{2}+1)-T_{1}$

$n_{1}$ always chosen smaller, if $T_{1}^{*}$ is less than critical value, reject null, two-tailed test statistic is $min(T_{1}^{*}, T_{1})$

**Sign Test**

Assume paired observations

Statistic is number of times that measurements for population A exceeds B, remove all equal measurements from data

Testing to see probability of rejection exceeding not equal to 0.5, since we expect on average, half of the A's measurements to exceed B