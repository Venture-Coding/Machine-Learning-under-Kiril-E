Random Forest Classifier is just a kind of agglomeration of the Decision Tree Classifier, where multiple decision trees classify, on their own, any inout that is given to the RFC. The RFC then takes the majority decision and gives it out as the final output prediction. 

Intuition:  
<img width="717" alt="Screenshot 2021-11-03 at 4 30 30 PM" src="https://user-images.githubusercontent.com/61674750/140048950-5b0baac3-0e77-4a0e-b9b6-28bf6a3169c5.png">

A type of Ensemble Learning : learning from an entire group rather than an individual. No correlation between member model's predictions. The probability of ensemble being wrong is less than the lowest probability of any member being wrong. Generally, all members never overfit. Hence, safe!

Also, there must be Diversity, each individual can't be very similar to another. 
There also must be atleast acceptably efficient. Not a single one of them can be highly inefficient. Each member must be special at atleast something.

Acceptability ? --> Significantly better than random guessing. Probability of each member model's correct prediction must be higher than the general class probability of that output to be predicted.

Example : proves why probability of ensemble being wrong is significantly lesser.

<img width="594" alt="Screenshot 2021-11-04 at 12 27 51 AM" src="https://user-images.githubusercontent.com/61674750/140175080-b23d552a-f6f0-426a-8e4a-7f8426e93648.png">


Note : 
  Bagging aka Bootstrapping & Aggregating, is just a sampling technique, not specific to RF. Here it refers to bootstrapping samples from given data and feednig it to individual trees and then aggregating the output of all the indiv. models.
