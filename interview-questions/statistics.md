# Statistics
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
**What is the probability of getting a pair by drawing two cards separately in a 52-card deck?**  
This first card you draw can be whatever, so it does not impact the result other than that there is one card less left in the deck. Once the first card is drawn, there are three remaining cards in the deck that can be drawn to get a pair. So, the chance of matching your first card with a pair is 3 out of 51 (remaining cards). This means that the probability of this event occurring is 3/51 or 5.89%.

**In any 15-minute interval, there is a 20% probability that you will see at least one shooting star. What is the probability that you see at least one shooting star in the period of an hour?**  
1 - P(Not seeing any star) = $1 - (0.8)^2 = 0.5904$

**How can you generate a random number between 1 – 7 with only a die?**  
Any die has six sides from 1-6. There is no way to get seven equal outcomes from a single rolling of a die.
If we roll the die twice and consider the event of two rolls, we now have 36 different outcomes. To get
our 7 equal outcomes we have to reduce this 36 to a number divisible by 7. We can thus consider only 35
outcomes and exclude the other one. A simple scenario can be to exclude the combination (6,6), i.e., to
roll the die again if 6 appears twice. All the remaining combinations from (1,1) till (6,5) can be divided into 7 parts of 5 each. This way all the seven sets of outcomes are equally likely


# Graphs
**Differentiate between box plot and histogram**  
Box plots and histograms are both visualizations used for showing data distributions for efficient communication of information.
Histograms are the bar chart representation of information that represents the frequency of numerical variable values that are useful in estimating probability distribution, variations and outliers.
Boxplots are used for communicating different aspects of data distribution where the shape of the distribution is not seen but still the insights can be gathered. These are useful for comparing multiple charts at the same time as they take less space when compared to histograms.