# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
### 1.Load the customer dataset and select Annual Income and Spending Score features.
### 2.Apply the K-Means algorithm with 5 clusters to group customers.
### 3.Predict cluster labels and find the cluster centroids.
### 4.Visualize the customer clusters and centroids using a scatter plot.

## Program:

### Program to implement the K Means Clustering for Customer Segmentation.
### Developed by: Ezhilan H
### RegisterNumber:  212225240040
```
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

data = pd.read_csv("Mall_Customers.csv")

X = data.iloc[:, [3, 4]].values
kmeans = KMeans(n_clusters=5, random_state=0)
y_kmeans = kmeans.fit_predict(X)
plt.scatter(X[:, 0], X[:, 1], c=y_kmeans, s=50)

plt.scatter(kmeans.cluster_centers_[:, 0],
            kmeans.cluster_centers_[:, 1],
            s=200,
            marker='X')
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("Customer Segmentation using K-Means")

plt.show()
```


## Output:
<img width="737" height="433" alt="image" src="https://github.com/user-attachments/assets/a4454724-f717-4798-8828-5660f7e57cb1" />



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
