## Abstract:

The project analyzes tweets to get a better understanding of the difference between the Covid and In-Covid social media activity of people.The COVID-19 Pandemic has shifted and changed our day to day lives in a very exponential manner. While it is difficult to measure this due to the lack of everyday data of people’s lives, social media can provide us little insight into people’s emotions, spending habits, and actions. Twitter was selected due to its popularity and a common platform for people to express their emotions, share actions, and activities. We have used various clustering techniques to analyze tweets including K-Means, DB Scan, Gaussian, BIRCH, etc. Clustering provided insights into trending topics and a clear demarcation between them during the pre-covid and in-covid time period.


### Experiments/Analysis

#### Preprocessing:

Since the dataset imported from the Twitter developers Website using tweepy is not clean, it is required to do some preliminary preprocessing in order to remove the data which doesn’t play any influence in the data mining which is going to be performed later. Some essential preprocessing steps which are involved in data cleaning are: removing HTML tags, URL’S, numbers, hashtags,, and any other special characters in the tweets and further cleaning is done through lemmatization.

#### Clustering:

#### K-means clustering: K-Means clustering is an unsupervised machine learning algorithm. In this K specifies the number of centroids that are present in the clustering. 

We have performed the TFIDF vectorization to get the relative weight for words used in the tweets. This technique will provide us the most important or most frequent words used in the tweets. This will give us an opportunity to inspect the difference in the word importance before and during the pandemic.

In order to get the value of K for K-Means, we have used the elbow plot technique which has given us the optimal value of k as 3. We have used Principal Component Analysis for dimensionality reduction and reduced our data dimension to 2.

Applied k-means clustering, and observed the results that in 3 clusters formed before the covid time the tweets related to a specific topic like some trending movie,  some trending news or festival celebration have been clustered together in one cluster. In the clusters, during the covid times, the tweets are mostly concentrated related to the pandemic topics like Covid, wildfires, black lives matter.


#### DBSCAN(Density-Based Spatial Clustering of Applications with Noise) Clustering: 

As the data we get is very unstructured, it is always advantageous to use clustering techniques which can cluster arbitrary shapes too. DBSCan is one of such algorithms which can be used when there is too much noise in the data set. So we have used this technique in order to perform the clustering.

Density-based clustering, using this method we are able to see that there are outliers in the dataset. In the graphs below there are outliers that vary more for PC1 than for PC2. From the below graphs we can see that the DBSCAN is not an appropriate algorithm for our dataset; the labels have not been applied properly and all the data is assigned to one cluster.




#### Gaussian Mixture Model: 

Gaussian Mixture model also does unsupervised clustering of unlabeled. One of the main advantages of this model is that it takes into consideration the variance present in the data which is not considered in the case of K-means clustering. 

Also, since the Gaussian Model uses Gaussian distribution to fit arbitrarily shaped data. So this model calculates the probability of the data point under which cluster it lies which is called as soft clustering unlike the hard clustering where only the data points are classified into clusters. The clusters are a bit improved but compared to k-means still we are not able to find the appropriate clusters for the dataset.




#### Birch Model (Balanced Iterative Reducing and Clustering using Hierarchies (BIRCH) ): 

The BIRCH model is one of the popular clustering algorithms due to the computational simplicity of the model. This will give us the clustering with minimal computational resources such as CPU cycles. BIRCH will first try to generate the summary of the data that retains the distribution information and does clustering on this summary rather than on the total dataset. The results for this model are quite similar to k-means clustering; we are able to see three clusters but still there are few outliers that don't fit into any cluster.


#### Affinity Propagation model: 

This model can be used when we are not sure beforehand how many clusters to expect.Each datapoint communicates with other data points to identify how similar they are and that is how they start to make the clusters. There are a lot of clusters formed here so there is no clear identification of same.


MeanShift Model : This model is a good fit for handling images and computer vision processing. This is a hierarchical clustering method. It iterates over all the data points and shifts them towards the mode. Since our dataset was not having any hierarchy we can see the data points have formed several clusters. 




#### Comparisons

k-means:

![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/ScatterPlot1.png)
![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/ScatterPlot2.png)
![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/PrecovidC1.png)
![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/Precovidc2.png)
![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/Precovidc3.png)
![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/Precovidc4.png)
![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/Precovidc5.png)
![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/Precovid5.png)

DBScan:

![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/DBScan.png)

Gaussian:

![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/G.png)

BIRCH:

![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/birch.png)

Affinity Propagation:

![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/affinity.png)

MeanShift:

![BarCharts_PreCovid](https://github.com/revanth802/CMPE-255-FA2020-Team6/blob/main/Images_Figures/MeanShift.png)


## References
- https://towardsdatascience.com/k-means-clustering-8e1e64c1561c 
- https://medium.com/swlh/tweets-classification-and-clustering-in-python-b107be1ba7c7
- https://www.freecodecamp.org/news/8-clustering-algorithms-in-machine-learning-that-all-data-scientists-should-know/
- https://towardsdatascience.com/visualization-of-information-from-raw-twitter-data-part-1-99181ad19c

