## K-Means Clustering ##

Clustering is a common exploratory data analysis (EDA) technique, to get an insight about the structure of the input data.  
Unsupervised clustering is the task of identifying groups inside the data, such that those input datapoints in the same subgroup (cluster) are very similar to each other, while those in different clusters are very different. So, we try to identify homogeneous groups within the data such that each point in the cluster is as similar as possible based on some measure (could be Euclidean distance, or any other measure of similarity).  

K-Means is one of the methods of such unsupervised clustering, and is pretty common first - approach.  

According to towardsdatascience.com ,  
The way kmeans algorithm works is as follows:  

1. Specify number of clusters K.  
2. Initialize centroids by first shuffling the dataset and then randomly selecting K data points for the centroids without replacement.  
3. Keep iterating until there is no change to the centroids. i.e assignment of data points to clusters isn’t changing.  
4. Compute the sum of the squared distance between data points and all centroids.  
5. Assign each data point to the closest cluster (centroid).  
6. Compute the centroids for the clusters by taking the average of the all data points that belong to each cluster.  


The approach kmeans follows to solve the problem is called **Expectation-Maximization.**

Loss Function is given as :  
<img width="332" alt="Screenshot 2021-11-16 at 6 42 11 PM" src="https://user-images.githubusercontent.com/61674750/141991481-95f44b52-875e-43fe-a3b0-42c07112633b.png">


Ways to find the right number of clusters :  
i)  Elbow method (plotting the squared sum of errors, selecting n where curve turns sharply).  
ii) Silhoutte method (finding the silhoutte score, better when closer to 1)

<img width="700" alt="Screenshot 2021-11-16 at 6 55 57 PM" src="https://user-images.githubusercontent.com/61674750/141993620-e7773294-d98b-4b78-906d-20d80868e216.png">


Notes:  
- Better to have data that is standardized with mean=0 and standard dev = 1.  
- Random initialization might lead to local minima and hence multiple different initializations must be used to effectively try to reach closer to global minima with least loss.  

Limitations: 
Only good at clustering spherically similar datapoints.  
Poor job at clustering the data if the classes are supposedly distributed/clustered in any other type of geometric figures.  

Example : (towardsdatascience.com)
<img width="688" alt="Screenshot 2021-11-16 at 6 51 15 PM" src="https://user-images.githubusercontent.com/61674750/141992873-eff3cc37-b489-408f-bb65-45aee0715cd9.png">

