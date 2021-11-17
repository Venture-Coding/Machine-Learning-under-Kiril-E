## Upper Confidence Bound Algo ##


The Multi-Armed Bandit problem is the often considered the motivation for the UCB algo. The algorithm is based on the principle of "optimism in the face of uncertainty", which is to choose your actions as if the environment is as nice as is plausibly possible. By this we mean that the unknown "mean" payoffs of each arm (of the Multi-Armed Bandit) is as large as plausibly possible based on the data that has been observed. 

  
  Given below are the intuitive steps behind UCB for maximizing the rewards in a MABP:  
  
Step 1: Each machine is assumed to have a uniform Confidence Interval and a success distribution. This Confidence Interval is a margin of success rate distributions which is the most certain to consist of the actual success rate distribution of each machine which we are unaware of in the beginning.  
  
Step 2: A machine is randomly chosen to play, as initially, they have all the same confidence Intervals.  
  
Step 3: Based on whether the machine gave a reward or not, the Confidence Interval shifts either towards or away from the actual success distribution and the also converges or shrinks as it has been explored thus resulting in the Upper bound value of the confidence Interval to also be reduced.  
  
Step 4: Based on the current Upper Confidence bounds of each of the machines, the one with the highest is chosen to explore in the next round.  
  
Step 5: Steps 3 and 4 are continued until there are sufficient observations to determine the upper confidence bound of each machine.   The one with the highest upper confidence bound is the machine with the highest success rate.  
  
    
<img width="926" alt="Screenshot 2021-11-17 at 12 47 24 PM" src="https://user-images.githubusercontent.com/61674750/142153749-cb4c572f-6e97-49d1-8662-8be3be7e97d5.png">  
  


A quick graphical explanation from geeksforgeeks.com (notations or ri replaced with Q).  

  Since, the Upper Confidence Bound follows the principle of optimism in the face of uncertainty, it implies that if we are uncertain about an action, we should optimistically assume that it is the correct action.  

For example, let’s say we have these four actions with associated uncertainties in the picture below, our agent has no idea which is the best action. So according to the UCB algorithm, it will optimistically pick the action that has the highest upper bound i.e. A. By doing this either it will have the highest value and get the highest reward, or by taking that we will get to learn about an action we know least about.  
<img width="582" alt="Screenshot 2021-11-17 at 1 32 15 PM" src="https://user-images.githubusercontent.com/61674750/142159703-65d8ac07-3bfe-48c3-ac8a-10858d3f63da.png">

Let’s assume that after selecting the action A we end up in a state depicted in the picture below. This time UCB will select the action B since Q(B) has the highest upper-confidence bound because it’s action-value estimate is the highest, even though the confidence interval is small.  
<img width="565" alt="Screenshot 2021-11-17 at 1 33 36 PM" src="https://user-images.githubusercontent.com/61674750/142159849-ce186784-bf73-4e37-91f7-3109b71e3700.png">


Initially, UCB explores more to systematically reduce uncertainty but its exploration reduces over time. Thus we can say that UCB obtains greater reward on average than other algorithms such as Epsilon-greedy, Optimistic Initial Values, etc.


Assumption :  
- Each ad has a fixed conversion rate in our model sample.  
- Convergence needed in minimum rounds to optimize cost.  

Reference readings for depth:  
i)   Tzu L. Lai and Herbert Robbins. Asymptotically efficient adaptive allocation rules, 1985  
ii)  Rajeev Agrawal. Sample mean based index policies with regret for the multi-armed bandit problem, 1995  
iii) Michael N Katehakis and Herbert Robbins. Sequential choice from several populations, 1995  
iv)  Peter Auer, Nicolo Cesa-Bianchi, and Paul Fischer. Finite-time analysis of the multiarmed bandit problem, 2002
