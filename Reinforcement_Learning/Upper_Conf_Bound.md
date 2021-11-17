## Upper Confidence Bound Algo ##


<img width="926" alt="Screenshot 2021-11-17 at 12 47 24 PM" src="https://user-images.githubusercontent.com/61674750/142153749-cb4c572f-6e97-49d1-8662-8be3be7e97d5.png">  
  


A quick graphical explanation from geeksforgeeks.com (notations or ri replaced with Q).  

  The Upper Confidence Bound follows the principle of optimism in the face of uncertainty which implies that if we are uncertain about an action, we should optimistically assume that it is the correct action.  

For example, let’s say we have these four actions with associated uncertainties in the picture below, our agent has no idea which is the best action. So according to the UCB algorithm, it will optimistically pick the action that has the highest upper bound i.e. A. By doing this either it will have the highest value and get the highest reward, or by taking that we will get to learn about an action we know least about.  
<img width="582" alt="Screenshot 2021-11-17 at 1 32 15 PM" src="https://user-images.githubusercontent.com/61674750/142159703-65d8ac07-3bfe-48c3-ac8a-10858d3f63da.png">

Let’s assume that after selecting the action A we end up in a state depicted in the picture below. This time UCB will select the action B since Q(B) has the highest upper-confidence bound because it’s action-value estimate is the highest, even though the confidence interval is small.  
<img width="565" alt="Screenshot 2021-11-17 at 1 33 36 PM" src="https://user-images.githubusercontent.com/61674750/142159849-ce186784-bf73-4e37-91f7-3109b71e3700.png">


Initially, UCB explores more to systematically reduce uncertainty but its exploration reduces over time. Thus we can say that UCB obtains greater reward on average than other algorithms such as Epsilon-greedy, Optimistic Initial Values, etc.


Assumption :  
- Each ad has a fixed conversion rate in our model sample.  
- Convergence needed in minimum rounds to optimize cost.
