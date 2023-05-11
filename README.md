# CryptoClustering

# HTML Scraping Challenge

# Project Description 

## Prepare the Data
- Normalize the data from the CSV file using the StandardScaler() module from scikit-learn.
- Create a DataFrame with the scaled data and set the "coin_id" as the index.

## Find the Best Value for k Using the Original Scaled DataFrame
- Create a list with the number of k values from 1 to 11.
- Create an empty list to store the inertia values.
- Create a for loop to compute the inertia with each possible values of k.
- Create a dictionary with the data to plot the elbow curve.
- Plot the elbow curve. 
- Indicate the best value for k.

## Cluster Cryptocurrencies with K-means Using the Original Scaled Data
- Initialize the K-means model with the best value for k. 
- Fit the K-means model using the original scaled DataFrame.
- Predict the clusters to group the cryptocurrencies using the scaled DataFrame. 
- Create a copy of the data and add a column with the predicted clusters.
- Create a scatter plot with the x-axis displying the price change percentage in 24 hours and the y-axis displaying the price change percentage in 7 days. Color the points with the labels found using K-means and add the "coin_id" as a hover column.

## Optimize Clusters with Principal Component Analysis
- Perform a PCA to reduce the features to three components. 
- Calculate the explained variance of the three components. 
- Create a DataFrame with the PCA data and the "coin_id" as an index.

## Find the Best Value for k Using the PCA Data
- Create a list with the number of k-values from 1-11.
- Create an empty list for the inertia values.
- Create a for loop to compute the inertia with each possible value of k.
- Create a dictionary with the data to plot the Elbow curve. 
- Plot the PCA elbow curve. 
- Indicate what the best value is for k using the PCA data and if it differs from the best value for k in the original data. 

## Cluster Cryptocurrencies with K-means Using the PCA Data
- Initialize the K-means model with the best value for k.
- Fit the K-means model with the PCA data. 
- Predict the clusters using the PCA data. 
- Create a copy of the PCA DataFrame and add a column with the predicted clusters. 
- Create a scatterplot with x representing on PC value and y representing another. Color the graph points with the labels found using K-means and add the "coin_id" as a hover column. 
- Indicate the impact of using fewer features to cluster the data using K-means. 

# Software and Files
## Libraries and Dependencies
- import pandas as pd
- import hvplot.pandas
- from sklearn.cluster import KMeans
- from sklearn.decomposition import PCA
- from sklearn.preprocessing import StandardScaler
- CSV: crypto_market_data.csv

# Output/Analyses
- Imported the libraries and dependencies.
<img width="525" alt="Screenshot 2023-05-11 at 5 26 51 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/4785a5ae-002e-4a2e-9f50-7d7deb382c83">
- Loaded the data into a DataFrame.
<img width="558" alt="Screenshot 2023-05-11 at 5 27 19 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/f9b89335-3d66-4e74-872a-a8c62083541f">
- Generated summary statistics.
<img width="546" alt="Screenshot 2023-05-11 at 5 27 49 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/1f337add-76a1-4500-ac8f-458b87c15c7e">
- Plotted the data. 
<img width="565" alt="Screenshot 2023-05-11 at 5 28 11 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/1fce8658-83dc-46c3-92dc-5aba2621689f">
- Used the StandardScaler() module to normalize the csv data. 
<img width="1366" alt="Screenshot 2023-05-11 at 5 29 17 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/1b298379-0790-4d44-ba19-f1175fec9275">
- Created a DataFrame with the scaled data, copies the coin_id from the original data, and set coin_id as the index. 
<img width="1363" alt="Screenshot 2023-05-11 at 5 30 01 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/b6787798-3081-4d84-9bf2-78b9711b8df2">
- Created a list with the number of k-values from 1 to 11, created an empty list to store the inertia values, and created a for loop to compute the inertia with each possible value of k. 
<img width="1370" alt="Screenshot 2023-05-11 at 5 30 59 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/59ebc671-6a45-4569-9834-7a85d054ff14">
- Created a dictionary with the data to plot the Elbow curve, created a DataFrame with the data to plot the Elbow curve, plotted the elbow curve, determined that the best value for k is 4. 
<img width="1360" alt="Screenshot 2023-05-11 at 5 32 27 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/5677038b-9912-4609-9cba-38e7f30eb490">
- Initialized the K-means model using the best value for k, fit the model using the scaled data, predicted the clusters, and printed the array of cluster values. 
<img width="1364" alt="Screenshot 2023-05-11 at 5 41 29 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/effc6bb2-df30-43ba-a784-6e6c3c057735">
- Created a copy of the DataFrame and added a new column with the predicted clusters.
<img width="1372" alt="Screenshot 2023-05-11 at 5 45 48 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/fc8635e2-0f9e-4644-af63-2b8b78621104">
- Created a scatter plot using the 24 hour and 7 day price change by the predicted clusters. 
<img width="1267" alt="Screenshot 2023-05-11 at 5 46 43 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/a5332313-851a-49e7-ab4c-300e9bc355dd">
- Created a PCA model, reduced the components to three, and retrieved the explain variance of 89%.
<img width="1365" alt="Screenshot 2023-05-11 at 5 47 48 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/cd20551a-974b-4765-b0ba-2673afec4b6b">
- Created a new DataFrame with the PCA data and set the coin_id as the index.
<img width="1368" alt="Screenshot 2023-05-11 at 5 48 31 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/2b45f801-8595-4f84-a5d4-4539ec617e12">
- Created a list with the number of k-values from 1 to 11, created an empty list to store the inertia values, created a for loop to compute the inertia with each possible value of k. 
<img width="1349" alt="Screenshot 2023-05-11 at 5 49 25 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/df0fe9c4-10df-4ddd-ab84-45912fea9499">
- Created a dictionary to plot the Elbow curve and a DataFrame and plotted the PCA elbow curve. Indicated that the best value for k when using the PCA data is 4 and that it does not differ from the best value using the original data. 
<img width="1363" alt="Screenshot 2023-05-11 at 5 50 13 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/e8c88ec6-536d-41c3-a3a0-9f861b1a4f1e">
- Initialized the K-Means model, fit the model, predicted the clusters, and printed the array of cluster values. 
<img width="1363" alt="Screenshot 2023-05-11 at 5 51 28 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/dc223e13-a5e6-41c7-a47a-373fca2cbd24">
- Created a copy of the DataFrame and added a new column with the predicted clusters.
<img width="1367" alt="Screenshot 2023-05-11 at 5 52 07 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/4cb0d19e-ba52-4aef-ba32-8104929095a7">
- Created a scatter plot using the PCA data. 
<img width="1373" alt="Screenshot 2023-05-11 at 5 52 39 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/d351560a-ba6c-4144-a92a-0954c9635e2b">
- Created a composite plot to contrast the Elbow curves. 
<img width="1353" alt="Screenshot 2023-05-11 at 5 53 12 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/0d0a2171-95cd-4f57-9d55-9a6d795c162d">
- Created a composite plot to contrast the clusters. Indicated that using fewer features to cluster K-Means data resulted in more distinct clusters with less overlap. 
<img width="1366" alt="Screenshot 2023-05-11 at 5 53 43 PM" src="https://github.com/brittanynicole7/CryptoClustering/assets/119909433/ade9efda-f062-47da-8991-6fd5c94deaba">

# Author 
-Brittany Wright github:brittanynicole7
