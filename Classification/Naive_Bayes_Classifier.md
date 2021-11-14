### Bayes Theorem ###

In probability theory and statistics, Bayes' theorem (alternatively Bayes' law or Bayes' rule; recently Bayes–Price theorem, named after Thomas Bayes, describes the probability of an event, based on prior knowledge of conditions that might be related to the event.  
For example, if the risk of developing health problems is known to increase with age, Bayes' theorem allows the risk to an individual of a known age to be assessed more accurately (by conditioning it on their age) than simply assuming that the individual is typical of the population as a whole.  

Bayes' theorem is stated mathematically as the following equation:  

<img width="323" alt="Screenshot 2021-11-14 at 8 48 07 AM" src="https://user-images.githubusercontent.com/61674750/141666096-5f7cbf30-c9cd-4587-9576-406530657c88.png">


In situations where p(B) is not directly available, we use the Bayesian average by using summation of all products of likelihoods and priors.  
p(B) is also called Marginal Probability in certain cases for Bayes theorem.  
p(A) is also called as A Prior, which gives the original probability of certain event given no data.

Often time, p(B|A) is denoted as p(h|D), which implies the probability of a Hypothesis given certain Data = {D}.  
In this case, the "Likelihood" will be calculated as p(D|h), "prior" will be the unconditional probability of 'h'-> p(h),  
And, the marginal probability shall be p(D) and can be calculated as a summation of product of all Likelihoods and Priors availble for the given set of hypotheses.  

<img width="671" alt="Screenshot 2021-11-14 at 9 05 53 AM" src="https://user-images.githubusercontent.com/61674750/141666385-6f3cbc18-b001-4d3b-9e7f-83fc99d748c7.png">

### Naive Bayes Classifier ###

Assumption : All naive Bayes classifiers assume that the value of a particular feature is independent of the value of any other feature, given the class variable. For example, a fruit may be considered to be an apple if it is red, round, and about 10 cm in diameter. A naive Bayes classifier considers each of these features to contribute independently to the probability that this fruit is an apple, regardless of any possible correlations between the color, roundness, and diameter features. 

Types:  
    1. Gaussian Naive Bayes  
    2. Multinomial Naive Bayes  
    3. Bernoulli Naive Bayes
    
All these models, typically have the same assumptions but only differ in their parametric estimation based in the distribution chosen for the prior.  
There is also a concept of *Conjugate Prior* which assists in the selection of such a prior, that allows for an easy estimation of the distribution of the Posterior, leaving less room for doubt and confusion.
