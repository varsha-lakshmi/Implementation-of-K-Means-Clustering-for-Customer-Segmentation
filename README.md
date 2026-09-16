# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Start and load the customer dataset containing features such as age, income, and spending score.
2.Preprocess the data and choose the number of clusters (K) for grouping customers. 
3.Apply the K-Means Clustering algorithm to divide the customers into K clusters based on their similarities.
4.Analyze and visualize the clusters to identify different customer segments. Stop.

## Program:

```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: VARSHA S
RegisterNumber:  212225040482

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

# Load customer dataset
df = pd.read_csv(r"C:\Users\acer\Downloads\Mall_Customers.csv")

# Select features
X = df[["Annual Income (k$)", "Spending Score (1-100)"]]

# Create K-Means model
kmeans = KMeans(n_clusters=5, random_state=42, n_init=10)

# Fit the model and assign clusters
df["Cluster"] = kmeans.fit_predict(X)

# Display customer clusters
print(df[["CustomerID", "Annual Income (k$)",
          "Spending Score (1-100)", "Cluster"]])

# Display cluster centers
print("\nCluster Centers:")
print(kmeans.cluster_centers_)

# Visualize clusters
plt.scatter(
    X["Annual Income (k$)"],
    X["Spending Score (1-100)"],
    c=df["Cluster"]
)

plt.scatter(
    kmeans.cluster_centers_[:, 0],
    kmeans.cluster_centers_[:, 1],
    marker="X",
    s=200
)

plt.xlabel("Annual Income (k$)")
plt.ylabel("Spending Score (1-100)")
plt.title("Customer Segmentation using K-Means")
plt.show()


*/

```

## Output:


<img width="446" height="410" alt="Screenshot 2026-08-28 120609" src="https://github.com/user-attachments/assets/3d0b4967-17f4-4b60-8b7a-9694755464a6" />



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
