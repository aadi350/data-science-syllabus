# Statistics
### In what situation would you consider mean over median?   
The median splits the data roughly into two halves. Advantages of median:  
- Robust to outliers, e.g. median of (121, 124, 132, 142, 171) with outlier and (142, 124, 121, 151, 132) without outlier is the same, whilst mean is not 
- Robust to skewed distributions, general approach is to calculate both, if the mean is vastly different it could indicate highly skewed or noisy data  
However, the mean can be used if the data distribution is symmetric and continuous
### How do you ineterpret the standard error of the median and mean? 
The standard error of the mean how far the sample mean is likely to be from the true population mean, whilst the standard error of the median is the same for median. It indicates roughly by how much the sample statistics will vary from the actual population statistics, and will generally approach the population statistics as the number of samples increase.
### For sample size n, the margin of error is 3. How many more samples do we need to make the margin of error 0.3? 
Formula for margin-of-error:
$$
E = z_{\alpha/2}\sqrt{\frac{\hat{p}(1-\hat{p})}{n}}
$$
To scale $E$ from 3 to 0.3 would require an increase in sample-size by $\sqrt{10}$ 

### What is the assumption of error in linear regression?**  
- There is not a relationship between the residuals and the  variable; in other words,  is independent of errors. Check this assumption by examining a scatterplot of “residuals versus fits”; the correlation should be approximately 0. In other words, there should not look like there is a relationship.  
- The residuals must be approximately normally distributed. Check this assumption by examining a normal probability plot; the observations should be near the line. You can also examine a histogram of the residuals; it should be approximately normally distributed.  
 
### Given data from two product campaigns, how could you do an A/B test if we see a 3% increase for one product?
Pick one variable to test, in this case it would be the $3\%$ increase *(clarify what type of increase, or increase in what specific metric)*.  Create a control and a challenger, which changes (two different product campaigns), and split the sample groups equally and randomly. Determine how significant these results have to be, for a smaller increase, we want higher confidence level, since at such a small level of increase, random variance may play a larger part in the test. Our null hypothesis is our intervention (the challenger) having a positive effect (or a negative effect no larger than a margin).  
Statistical significance is calculated by simulating assignments of both campaigns randomly to conversions for a large number of simulations, and comparing the distribution of these conversions to the actual conversions rate.

### I have a deck and take one card at random. What is the probability you guess it right?  
$$
\frac{1}{52}
$$

### Explain a probability distribution that is not normal and how to apply that.  
*See [Distributions](../statistics/distributions.md)

### Given uniform distributions X and Y and the mean 0 and standard deviation 1 for both, what’s the probability of 2X > Y?  
Informal method, $2X \in [-2a, 2a]$ and $Y\in[-a, a]$. Probability is $\frac{1}{}$

### There are four people in an elevator and four floors in a building. What’s the probability that each person gets off on a different floor?  
This is a basic permutation/counting question:
$$
\frac{\text{Number of ways for 4 people to get off on 4 floors}}{\text{Number of ways each passenger can get off the elevator}} = \frac{5C1\cdot 4C1\cdot 3C1\cdot 2C1 \cdot 1C1}{5\cdot 5\cdot5\cdot5\cdot5}
$$

#### Make an unfair coin fair 
Mathematician John von Neumann is credited with figuring out how to take a biased coin (whose probability of coming up heads is p, not necessarily equal to 0.5) and “simulate” a fair coin. Simply flip the coin twice. If it comes up heads both times or tails both times, then flip it twice again. Eventually, you’ll get two different flips — either a heads and then a tails, or a tails and then a heads, with each of these two cases equally likely. Once you get two different flips, you can call the second of those flips the outcome of your “simulation.”


**What is an example of a data type with non-Gaussian distribution**  
A Gaussian distribution is a distribution where a certain known percentage of the data can be found when examining standard deviations from the mean, otherwise known as a normal distribution. Some of the examples of the non-Gaussian distribution can be exponential distribution or binomial distribution.

**Eigenvectors vs Eigenvalues**  
Eigenvectors are column vectors or unit vectors whose length/magnitude is equal to 1. They are also called right vectors. Eigenvalues are coefficients that are applied on eigenvectors which give these vectors different values for length or magnitude.

**Are there any differences between the expected value and mean value?**  
There are not many differences between these two, but it is to be noted that these are used in different contexts. The mean value generally refers to the probability distribution whereas the expected value is referred to in the contexts involving random variables.

**What do you understand by Survivorship Bias?**   
This bias refers to the logical error while focusing on aspects that survived some process and overlooking those that did not work due to lack of prominence. This bias can lead to deriving wrong conclusions.


**What is bias-variance tradeoff?**  
Normally, as you increase the complexity of your model, you will see a reduction in error due to lower bias in the model. However, this only happens until a particular point. As you continue to make your model more complex, you end up over-fitting your model and hence your model will start suffering from high variance.

**List properties of the normal distribution**
Unimodal, symmetrical, bell-shaped (maximum height or mode at the mean), mean mode and median are at the center and asymptotic

**Why do we need selection bias?**
Where no randomized way of picking a sample.

**Difference between a point estimate and a confidence interval**  
Point estimation gives a particular value as an estimate of a population parameter, confidence interval gives us range of values which is likely to contain the population parameter.

**What is A/B testing?**  
Hypothesis test for a randomized experiment with two variables.

# Probability
**Given 3 i.i.d. variables from a uniform distribution of 0 to 4, what’s the chance the median is greater than 3?**   
The answer is 5/32. In order to make the median greater than 3 ,atleast 2 i.i.d should be greater than 3. Hence the probability of getting median greater than 3 is equal to the probability of getting 2 i.i.d greater than 3 + the probability of getting 3 i.i.d greater than 3. The probability of getting 2 i.i.d greater than 3 is equal to 9/64 and the probability of getting 3 i.i.d greater than 3 is 1/64 , which adds up to give 5/32  
P(exactly two variables > 3) * 3 + P(all three variables >3)  

**What is the probability of getting a pair by drawing two cards separately in a 52-card deck?**  
This first card you draw can be whatever, so it does not impact the result other than that there is one card less left in the deck. Once the first card is drawn, there are three remaining cards in the deck that can be drawn to get a pair. So, the chance of matching your first card with a pair is 3 out of 51 (remaining cards). This means that the probability of this event occurring is 3/51 or 5.89%.

**In any 15-minute interval, there is a 20% probability that you will see at least one shooting star. What is the probability that you see at least one shooting star in the period of an hour?**  
1 - P(Not seeing any star) = $1 - (0.8)^4 = 0.5904$

**How can you generate a random number between 1 – 7 with only a die?**  
Any die has six sides from 1-6. There is no way to get seven equal outcomes from a single rolling of a die.
If we roll the die twice and consider the event of two rolls, we now have 36 different outcomes. To get
our 7 equal outcomes we have to reduce this 36 to a number divisible by 7. We can thus consider only 35
outcomes and exclude the other one. A simple scenario can be to exclude the combination (6,6), i.e., to
roll the die again if 6 appears twice. All the remaining combinations from (1,1) till (6,5) can be divided into 7 parts of 5 each. This way all the seven sets of outcomes are equally likely

**How would you determine if two factors are dependent from a contingency table?**  
Step 1  
Compute the row and column totals.  
Step 2 Compute the relative marginal frequencies for the row variable and column   variable.
Step 3  
Use the Multiplication Rule for Independent Events to compute the expected proportion of observations within each cell, assuming independence.  
Step 4  
Multiply the proportions by 2985, the sample size, to obtain the expected counts within each cell  
Follow this by carrying out the $\chi^2$ test for parameter independence  

**Let A and B be events on the same sample space, with P (A) = 0.6 and P (B) = 0.7. Can these two events be disjoint?**  
These two events cannot be disjoint because P(A)+P(B) >1.
$$
P(AꓴB) = P(A)+P(B)-P(A\cap B).
$$
An event is disjoint if P(A\cap B) = 0. If A and B are disjoint $P(A\cup B) = 0.6+0.7 = 1.3$
And Since probability cannot be greater than 1, these two mentioned events cannot be disjoint.

**Alice has 2 kids and one of them is a girl. What is the probability that the other child is also a girl? You can assume that there are an equal number of males and females in the world**  
The outcomes for two kids can be {BB, BG, GB, GG}

Since it is mentioned that one of them is a girl, we can remove the BB option from the sample space. Therefore the sample space has 3 options while only one fits the second condition. Therefore the probability the second child will be a girl too is 1/3.

**Consider a tetrahedral die and roll it twice. What is the probability that the number on the first roll is strictly higher than the number on the second roll?**
There are 6 out of 16 possibilities where the first roll is strictly higher than the second roll.


# Graphs
**Differentiate between box plot and histogram**  
Box plots and histograms are both visualizations used for showing data distributions for efficient communication of information.
Histograms are the bar chart representation of information that represents the frequency of numerical variable values that are useful in estimating probability distribution, variations and outliers.
Boxplots are used for communicating different aspects of data distribution where the shape of the distribution is not seen but still the insights can be gathered. These are useful for comparing multiple charts at the same time as they take less space when compared to histograms.