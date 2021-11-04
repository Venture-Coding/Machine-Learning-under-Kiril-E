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

  The splitting here that happens at each node, is not based on all features, but rather on a random subset of features(typically root of total no. of features). That's because if there are some prominent features in the feature set, all trees might end up being more similar. Hence, better to have random subset of features to be used during each split, so that all trees dont end up with the similar structure.


Advantages :
    Immune to curse of dimensionality. 
    Easily parallelised, saving time.
    More the trees, more its stable. (Contrasts with other models where instability increases if complexity increase.)
    No need to keep train, test data separate.  Each tree has not seen some datapoints at all. So those datapoints become the test data for those trees. The output of majority of such trees is used to calculate the final decision of the model for that datapoint during testing. So calculate Out Of Bag error. The total wrong predictions out of all predictions give us the Out Of Bag error, which is more like a cross-validation error.
    
   <img width="680" alt="Screenshot 2021-11-04 at 12 40 44 AM" src="https://user-images.githubusercontent.com/61674750/140176865-da0d2c8a-b871-42c0-805a-45889ab42d2c.png">

