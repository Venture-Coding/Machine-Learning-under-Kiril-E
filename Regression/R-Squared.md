R-Squared is just one of the many ways of evaluating the performance of Regression Models.

We use the Coefficient of Determination denoted as R-square.

<img width="631" alt="Screenshot 2021-11-03 at 5 09 10 PM" src="https://user-images.githubusercontent.com/61674750/140053701-6b44714e-013a-4b71-bb16-dc3242947d49.png">
<img width="533" alt="Screenshot 2021-11-03 at 5 10 17 PM" src="https://user-images.githubusercontent.com/61674750/140053808-9cd82e12-d390-4ff7-824b-22da5089f9f7.png">

In the first diagram, we've taken the difference of each value and the average of the total sample. Hence, it is the Sum of Squares of Difference of all values and their combined average.
The second diagra, shows a line fit to the data, still having certain loss, on account of points not lying on it directly. The Sum of Squares of these Residuals, is SSR, also called as Sum of Squared Errors (SSE).

So, the closer R-Squared is to 1, the better is our model. It's the goodness of fit.

Point to note: R-Square will never decrease with addition of more variables, it will only increase or stay the same (if the coeff. of new variable comes close to 0).


We also have a way to penalize unuseful variables, Adjusted R-Square is used. 
So, we penalise such that if the new variable is insignificantly increasing the R-Squared value, then the penalisation will instead drag the Adjusted R-Square down.
As shown below :
<img width="526" alt="Screenshot 2021-11-03 at 5 23 39 PM" src="https://user-images.githubusercontent.com/61674750/140055379-355a59d9-ed55-4ce2-93fa-3ac453020036.png">
