# CryptoClustering
## Module 19 Challenge

This repo contains,
- The Crypto_Clustering.ipynb file that shows my plots & clustering.
- A Resources directory containing the crypto market data in a CSV format.
- An Images directory containing screenshots of elbow plots and clustering plots created in my analysis.

<img src = "https://github.com/nivethasund/CryptoClustering/blob/main/Images/Crypto_Data.png">

## Clustering Crypto Currency Data

In this challenge, I utilize my knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes. I primarily use the scikit-learn library to preprocess my data with Standard Scaler, and further cluster my data with K-Means and PCA.

With the original data, I utilize the scaled data and apply K-Means to identify the optimal value of clusters (k value), using an elbow plot. The subsequent scatter plot created to analyze our clusters, shows us some interesting trends. 

<img src = "https://github.com/nivethasund/CryptoClustering/blob/main/Images/Original_KMeans_Elbow_Plot.png">
<img src = "https://github.com/nivethasund/CryptoClustering/blob/main/Images/KMeans_Clustering.png">

We also use PCA to dimensionally reduce our data, and again identify an optimal value of k and subsequently plot our PCA clusters

<img src = "https://github.com/nivethasund/CryptoClustering/blob/main/Images/PCA_KMeans_Elbow_Plot.png">
<img src = "https://github.com/nivethasund/CryptoClustering/blob/main/Images/PCA_Clustering.png">

## Analysis

**Question 1:** What is the best value for `k` in our original scaled data?

**Answer:**  The best value for `k` is 4 as indicated in the above graph.

**Question 2:** What is the total explained variance of the three principal components in our PCA?

**Answer:** 88%. This indicates that by applying PCA, we're dimensionally reducing our data by approximately 10%. This doesn't seem to be a significant loss. Often, data with high variance can be a good sign for industries like banking or crypto. High variance would mean more risk, but would result in higher returns.

**Question 3:** What is the best value for `k` when using the PCA data?

**Answer:** 4

**Question 4:** Does it differ from the best k value found using the original data?

**Answer:** No. It is the same as what we derived from our original data. However, there is a difference in inertia value. For a k value of 4, the inertia for PCA is at 49.6, and for our original data it is at 79. A lower inertia could indicate our clusters are closely packed.

**Question 5:** After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means?

**Answer:** 

Compared to our original data, the clusters indicated with PCA are more defined and clearly distinguishable. There is a stark difference in the distance between coins, ethlend & celsius-degree-token when comparing both cluster data. When we apply PCA with fewer features, we see those coins have a significant separation between the bulk of our clusters.

In our original data, our clusters overlap and aren't separated. With PCA, and the added evidence of lower inertia our data is more clean and can be used to draw clear predictions. So in conclusion, having fewer features to cluster our data using K-Means seems to have a positive impact on our data.


