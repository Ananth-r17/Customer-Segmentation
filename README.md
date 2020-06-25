# Customer-Segmentation
### Customer segmentation using simple clustering algorithm called K-Means and use Elbow Method. We will also implement it with the popular Scikit-learn library.

1. Customer Segmentation is the subdivision of a market into discrete customer groups that share similar characteristics. 
2. Customer Segmentation can be a powerful means to identify unsatisfied customer needs. Using the above data companies can then outperform the competition by developing uniquely appealing products and services.
3. The most common ways in which businesses segment their customer base are mentioned in the abstract.

#### Advantages of Customer Segmentation
1. Determine appropriate product pricing.
2. Develop customized marketing campaigns.
3. Design an optimal distribution strategy.
4. Choose specific product features for deployment.
5. Prioritize new product development efforts.

### Unsupervised ML

No labels are given to the learning algorithm, leaving it on its own to find structure in its input. Unsupervised learning can be a goal in itself (discovering hidden patterns in data) or a means towards an end (feature learning). In some pattern recognition problems, the training data consists of a set of input vectors x without any corresponding target values.
The goal in such unsupervised learning problems may be to discover groups of similar examples within the data, where it is called clustering, or to determine how the data is distributed in the space, known as density estimation. To put forward in simpler terms, for a n-sampled space x1 to xn, true class labels are not provided for each sample, hence known as learning without teacher.

#### Issues with Unsupervised Learning:

1. Unsupervised Learning is harder as compared to Supervised Learning tasks.
2. How do we know if results are meaningful since no answer labels are available?
3. Let the expert look at the results (external evaluation)


#### Why Unsupervised Learning is needed despite of these issues?

1. Annotating large datasets is very costly and hence we can label only a few examples manually. Example: Speech Recognition.
2. There may be cases where we don’t know how many/what classes is the data divided into. Example: Data Mining.
3. We may want to use clustering to gain some insight into the structure of the data before designing a classifier.

### Clustring

Clustering can be considered the most important unsupervised learning problem; so, as every other problem of this kind, it deals with finding a structure in a collection of unlabeled data. A loose definition of clustering could be “the process of organizing objects into groups whose members are similar in some way”. A cluster is therefore a collection of objects which are “similar” between them and are “dissimilar” to the objects belonging to other clusters.

### K-Means Clustring

K-means is one of the simplest unsupervised learning algorithms that solves the well known clustering problem. The procedure follows a simple and easy way to classify a given data set through a certain number of clusters (assume k clusters) fixed a priori. The main idea is to define k centres, one for each cluster. These centroids should be placed in a smart way because of different location causes different result. So, the better choice is to place them as much as possible far away from each other. The next step is to take each point belonging to a given data set and associate it to the nearest centroid. When no point is pending, the first step is completed and an early groupage is done. At this point we need to re-calculate k new centroids as barycenters of the clusters resulting from the previous step. After we have these k new centroids, a new binding has to be done between the same data set points and the nearest new centroid. A loop has been generated. As a result of this loop we may notice that the k centroids change their location step by step until no more changes are done. In other words centroids do not move any more.

### Clustring Animation

![](https://github.com/Ananth-r17/Customer-Segmentation/blob/master/Assets/K-Map.gif)

### Choosing Clusters:

The number of clusters that we choose for a given dataset cannot be random. Each cluster is formed by calculating and comparing the distances of data points within a cluster to its centroid. An ideal way to figure out the right number of clusters would be to calculate the Within-Cluster-Sum-of-Squares (WCSS). WCSS is the sum of squares of the distances of each data point in all clusters to their respective centroids.

![](https://github.com/Ananth-r17/Customer-Segmentation/blob/master/Assets/WCSS.jpg)

### Elbow Method

We can find the optimum value for K using an Elbow point graph. We randomly initialise the K-Means algorithm for a range of K values and will plot it against the WCSS for each K value. The resulting graph would look something like what’s shown below:

![](https://github.com/Ananth-r17/Customer-Segmentation/blob/master/Assets/Elbow.png)

For the above-given graph, the optimum value for K would be 5. As we can see that with an increase in the number of clusters the WCSS value decreases. We select the value for K on the basis of the rate of decrease in WCSS. For example, from cluster 1 to 2 to 3 in the above graph we see a sudden and huge drop in WCSS. After 5 the drop is minimal and hence we chose 5 to be the optimal value for K.


### ALGORITHM

##### 1. Selecting an appropriate value for K which is the number of clusters or centroids.
##### 2. Selecting random centroids for each cluster.
##### 3. Assigning each data point to its closest centroid.
##### 4. Adjusting the centroid for the newly formed cluster in step 4.
##### 5. Repeating step 4 and 5 till all the data points are perfectly organised within a cluster space.

![](https://github.com/Ananth-r17/Customer-Segmentation/blob/master/Assets/Cluster.png)
