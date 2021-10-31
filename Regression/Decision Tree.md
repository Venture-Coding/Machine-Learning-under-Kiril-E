Decision trees can handle any kind of data whether numeric or categorical. Especially helpful in handling categorical data.
Normalisation isn't required as it compares selectively, similar data.

It also plays an important role in telling us the imp data points, imp features.
Those are usually the ones at which the trees split.

Cons: 
    Makes it complex, and thus overfits the entire training data. Basically as many leaves as data points.  
    Variance become very high if bias tried to reduce too much. Model becomes complex and sensitive, unstable.  
    
So the tree needs to be kept in check, to prevent overfitting.  
    Truncation : Top down method, we consciously decide to stop at a particular depth. Not splitting further.  
    Pruning    : Bottom Up method, we let the tree grow and then cut its branches, etc to shape it up.  
