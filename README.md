# DBSCAN-Clustering-Algorithm-
Density-based — defines clusters as dense regions of space separated by low-density regions. 
As mentioned above, density-based algorithms work by identifying dense regions in space (i.e., populated with many data points) separated by less dense regions. To enable the algorithm to find these dense regions, we first need to establish what we consider to be sufficiently dense. We do this by specifying two hyperparameters:

•	Epsilon (ϵ, sklearn: eps) — the radius of the area around the point defining the maximum distance between such point and any other points for one to be considered in the neighborhood of the other.
•	Min points (MinPts, sklearn: min_samples) — the minimum number of points present in the neighborhood required to form a cluster.

Pros and cons of DBSCAN compared to other clustering methods:
Pros: 
First, DBSCAN doesn’t require users to specify the number of clusters.
Second, DBSCAN is NOT sensitive to outliers.
Third, the clusters formed by DBSCAN can be any shape, which makes it robust to different types of data.
•	Cons: It does not work well when there is varying density across the data since Epsilon and MinPts are fixed.

DBSCAN creates a circle of epsilon radius around every data point and classifies them into Core point, Border point, and Noise. A data point is a Core point if the circle around it contains at least ‘minPoints’ number of points. If the number of points is less than minPoints, then it is classified as Border Point, and if there are no other data points around any data point within epsilon radius, then it treated as Noise.

K-Means and Hierarchical Clustering both fail in creating clusters of arbitrary shapes. They are not able to form clusters based on varying densities. That’s why we need DBSCAN clustering. 
It groups ‘densely grouped’ data points into a single cluster. It can identify clusters in large spatial datasets by looking at the local density of the data points. The most exciting feature of DBSCAN clustering is that it is robust to outliers. It also does not require the number of clusters to be told beforehand, unlike K-Means, where we have to specify the number of centroids.

It creates clusters into density areas of data and separates clusters between empty areas or low areas of density, outliers are here, but the MAIN disadvantage is that since Epsilon and Min number of points are fixed parameters it assumes that all clusters have the same density, same shape, and that could be a an issue when clusters have difference densities, shapes, and each cluster should have its own parameters and not the same for the whole dataset. 
