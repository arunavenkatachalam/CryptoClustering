# CryptoClustering

## Overview

In this challenge, our aim is to predict if cryptocurrencies are affected by 24-hour or 7-day price changes using k-means algorithm in unsupervised learning and optimize the cluster with Principal Optimal Analysis(PCA).

## Instruction

1. use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.
2. Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.
3. Use the elbow method to find the best value for k.
4. Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
5. Initialize the K-means model with the best value for k.
6. Fit the K-means model using the original scaled DataFrame.
7. Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
8. Create a copy of the original data and add a new column with the predicted clusters.
9. Create a scatter plot using hvPlot as follows:
10. Set the x-axis as "PCA1" and the y-axis as "PCA2".
11. Color the graph points with the labels found using K-means.
12. Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

###   Optimize Clusters with Principal Component Analysis

1. Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
2. Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.
3. Create a list with the number of k-values from 1 to 11.
4. Create an empty list to store the inertia values.
5. Create a for loop to compute the inertia with each possible value of k.
6. Create a dictionary with the data to plot the Elbow curve.
7. Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
8. Initialize the K-means model with the best value for k.
9. Fit the K-means model using the PCA data.
10. Predict the clusters to group the cryptocurrencies using the PCA data.
11. Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
12. Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
13. Color the graph points with the labels found using K-means.
14. Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

## Analysis

1. After scaling the data by ploting the elbow curve the best value for K is 4.
2. plot the scatter plot with  x="price_change_percentage_24h", y="price_change_percentage_7d".
3. Approximately 89% of total variance can be achieved from three principal components.
4. The best value for K is 2 using PCA data whereas k is 4 for original data.
5. By composing the elbow plots and cluster using the original method and PCA, we can compare that with PCA with less number of components we can get a clear datapoints.




