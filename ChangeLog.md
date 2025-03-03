# Changelog - K-Means Clustering for Online Purchase Data
## - Initial Implementation
Searched for a dataset related to online purchases using income and age of individuals.
Plotted Age vs. Salary to visualize relationships between the features.
## - Data Cleaning & Filtering
Identified two outlier points that were significantly affecting the graph’s scale.
  ![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20224209.png?raw=true)
Added a filter to exclude these extreme values, improving visualization clarity.
  ![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20135012.png?raw=true)
## - Cluster Evaluation Metrics
### Added Inertia (WCSS) to measure the compactness of clusters.
  ![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20224549.png?raw=true)
  -5.74 suggests that the clusters are relatively compact, but we would need to compare with other k-values to determine if k = 3 is optimal.
### Implemented Silhouette Score to assess the quality and separation of clusters.
 ![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20224555.png?raw=true)
-0.361 suggests that the clusters are moderately well-separated but could be improved. It indicates some overlap between clusters, meaning k = 3 might not be the best choice.
