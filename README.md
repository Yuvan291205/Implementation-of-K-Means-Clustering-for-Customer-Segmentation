# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages using import statement.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

3.Import KMeans and use for loop to cluster the data.

4.Predict the cluster and plot data graphs.

5.Print the outputs and end the program

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Yuvan M
RegisterNumber:  212223240188
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Dataset-20230524.zip")
data

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss = []

for i in range(1,11):
    kmeans = KMeans(n_clusters = i,init = "k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

km = KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])

y_pred = km.predict(data.iloc[:,3:])
y_pred

data["cluster"] = y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="yellow",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="pink",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="purple",label="cluster4")
plt.legend()
plt.title("Customer Segments")
*/
```

## Output:
### Data Head():
![image](https://github.com/Yuvan291205/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/138849170/838541df-fc13-4a3e-b370-4b44f8d5bec1)
### Data info():
![image](https://github.com/Yuvan291205/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/138849170/20f83b48-069a-454f-be54-167273eb9790)
### Null values:
![image](https://github.com/Yuvan291205/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/138849170/9939e562-2620-4cf0-8f8e-c2543f1e8fad)
### Elbow graph:
![image](https://github.com/Yuvan291205/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/138849170/a6ab9966-8713-4bf5-a673-3aa6ebccd538)
### cluster formation:
![image](https://github.com/Yuvan291205/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/138849170/4cd56fd0-b0cd-4367-853b-c8aff0c60975)
### Predicted value:
![image](https://github.com/Yuvan291205/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/138849170/49584c80-e83c-4ab7-bdee-30f308b611a5)
### final graph:
![image](https://github.com/Yuvan291205/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/138849170/bee3386e-5fab-406e-96a6-39cea36efe05)
## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
