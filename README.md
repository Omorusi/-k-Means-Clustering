 # K-Means Clustering on Online Purchase Data
This project demonstrates the application of K-Means clustering on an online purchase dataset to segment customers based on their age and salary. The goal is to use clustering to identify distinct customer groups for better targeting.

# Techologies

# Dataset
The dataset used for clustering contains the following columns:

Customer_ID: Unique ID for each customer
Gender: Gender of the customer (Male/Female)
Age: Age of the customer
Salary: Salary of the customer
Purchased: Whether the customer made a purchase (1 = Purchased, 0 = Not Purchased)
Dataset Preview
csv
Copy
Edit
Customer_ID,Gender,Age,Salary,Purchased
1,Male,35,500,0
2,Female,25,300000,1
3,Female,100,200000,0
...
Steps
# 1. Data Loading and Cleaning
The dataset is loaded using pandas and cleaned by removing any rows with missing values.
### Loaded the datset
![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20134850.png?raw=true)
### Cleaned by removing any rows with missing values.

![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20140722.png?raw=true)
python
Copy
Edit

## 2. Data Visualization
Before applying clustering, the relationship between Age and Salary is visualized using a scatter plot.
### Visualisation of the Graph before applying a filter
![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20141016.png?raw=true)

### Visualisation of the Graph after applying a filter
![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20135012.png?raw=true)
python
Copy
Edit

## 3. K-Means Clustering

### We apply the K-Means clustering algorithm to segment the customers into different clusters based on Age and Salary.
![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20135023.png?raw=true)

![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20135023.png?raw=true)
python
Copy
Edit

4. Visualizing Clusters
### The customers are segmented into clusters, and the results are visualized using different colors for each cluster.
![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20135042.png?raw=true)
python
Copy
Edit

5. Data Normalization
To scale the data between 0 and 1, we apply Min-Max scaling on the Age and Salary columns using sklearn.preprocessing.MinMaxScaler.
![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20135112.png?raw=true)
python
Copy
Edit


6. Re-run Clustering on Scaled Data
After scaling the data, we apply the K-Means clustering algorithm again to see how the clusters change after normalization.
![image alt](https://github.com/Omorusi/-k-Means-Clustering/blob/main/Screenshot%202025-03-03%20154936.png?raw=true)
python
Copy
Edit

Conclusion
This project demonstrates how to use K-Means clustering to segment customers based on their Age and Salary. The results of clustering can be used for targeted marketing or personalized recommendations.


