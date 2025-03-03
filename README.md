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

python
Copy
Edit
data = pd.read_csv("Online Purchase.csv")
data_cleaned = data.dropna()
2. Data Visualization
Before applying clustering, the relationship between Age and Salary is visualized using a scatter plot.

python
Copy
Edit
plt.scatter(data_cleaned['Age'], data_cleaned['Salary'], alpha=0.5)
plt.xlabel('Age')
plt.ylabel('Salary')
plt.title('Scatter Plot of Age vs Salary')
plt.show()
3. K-Means Clustering
We apply the K-Means clustering algorithm to segment the customers into different clusters based on Age and Salary.

python
Copy
Edit
from sklearn.cluster import KMeans

km = KMeans(n_clusters=3)
y_predicted = km.fit_predict(data_cleaned[['Age', 'Salary']])
data_cleaned['cluster'] = y_predicted
4. Visualizing Clusters
The customers are segmented into clusters, and the results are visualized using different colors for each cluster.

python
Copy
Edit
data1 = data_cleaned[data_cleaned['cluster'] == 0]
data2 = data_cleaned[data_cleaned['cluster'] == 1]
data3 = data_cleaned[data_cleaned['cluster'] == 2]

plt.scatter(data1['Age'], data1['Salary'], color='green')
plt.scatter(data2['Age'], data2['Salary'], color='red')
plt.scatter(data3['Age'], data3['Salary'], color='blue')
plt.xlabel('Age')
plt.ylabel('Salary')
plt.show()
5. Data Normalization
To scale the data between 0 and 1, we apply Min-Max scaling on the Age and Salary columns using sklearn.preprocessing.MinMaxScaler.

python
Copy
Edit
from sklearn.preprocessing import MinMaxScaler

scaler = MinMaxScaler()
data_cleaned[['Age', 'Salary']] = scaler.fit_transform(data_cleaned[['Age', 'Salary']])
6. Re-run Clustering on Scaled Data
After scaling the data, we apply the K-Means clustering algorithm again to see how the clusters change after normalization.

python
Copy
Edit
y_predicted = km.fit_predict(data_cleaned[['Age', 'Salary']])
data_cleaned['cluster'] = y_predicted
Conclusion
This project demonstrates how to use K-Means clustering to segment customers based on their Age and Salary. The results of clustering can be used for targeted marketing or personalized recommendations.

Troubleshooting
If you encounter a KeyError or ValueError while running the code, ensure that you're using the correct syntax and check the column names of the dataset. The error mentioned can occur if you're trying to apply transformations on incorrectly specified column names or shapes.

