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
## Deliverable 1
- from splinter import Browser
- from bs4 import BeautifulSoup
- url = https://static.bc-edx.com/data/web/mars_news/index.html

## Deliverable 2
- from splinter import Browser
- from bs4 import BeautifulSoup as soup
- import matplotlib.pyplot as plt
- import pandas as pd
- import datetime as date
- url = https://static.bc-edx.com/data/web/mars_facts/temperature.html

# Output/Analyses



# Author 
-Brittany Wright github:brittanynicole7
