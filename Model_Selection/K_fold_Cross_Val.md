K Fold - Cross Validation.

Cross-validation is primarily used in applied machine learning to estimate the skill of a machine learning model on unseen data. That is, to use a limited sample in order to estimate how the model is expected to perform in general when used to make predictions on data not used during the training of the model.

It results in a less biased, sometimes less optimistic estimate of the model's skill, than other methods using a simple train/test split.

The K-Fold approach involves randomly dividing the set of observations into k groups, or folds, of approximately equal size. The first fold is treated as a validation set, and the method is fit on the remaining k − 1 folds.

<img width="707" alt="Screenshot 2021-11-07 at 12 26 54 PM" src="https://user-images.githubusercontent.com/61674750/140635600-78353e24-2dbd-41d5-ac26-28d392328efb.png">


The result is measured as a mean of all individual accuracies. We also calculate the Variance to get an idea of the range of accuracies churned out by the model. Lower it is, the better!

NOTES:

The choice of k is usually 5 or 10, but there is no formal rule. As k gets larger, the difference in size between the training set and the resampling subsets gets smaller. As this difference decreases, the bias of the technique becomes smaller.

— Page 70, Applied Predictive Modeling, 2013

To summarize, there is a bias-variance trade-off associated with the choice of k in k-fold cross-validation. Typically, given these considerations, one performs k-fold cross-validation using k = 5 or k = 10, as these values have been shown empirically to yield test error rate estimates that suffer neither from excessively high bias nor from very high variance.

— Page 184, An Introduction to Statistical Learning, 2013

Hence, we have used k=10 in this example.
