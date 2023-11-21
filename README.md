# Python Rutgers Bootcamp Challenge - CryptoClustering

This activity is broken down into Python code which uncovers was of predicting group clusters using unsupervised machine learning. 

## Description

In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Instructions

The instructions for this Challenge are divided into the following subsections:

1. Split the Data into Training and Testing Sets

2. Create a Logistic Regression Model with the Original Data

3. Write a Credit Risk Analysis Report

## Prepare the Data

* Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

* Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

- The first five rows of the scaled DataFrame should appear as follows:

![Screenshot 2023-11-13 143742](https://github.com/Connextstrategy/CryptoClustering/assets/18508699/e2ee7df3-1d4a-4561-a19a-6dc1627fd9c5)

## Find the Best Value for k Using the Original Scaled DataFrame

* Use the elbow method to find the best value for k using the following steps:
  
  * Create a list with the number of k values from 1 to 11.
  * Create an empty list to store the inertia values.
  * Create a for loop to compute the inertia with each possible value of k.
  * Create a dictionary with the data to plot the elbow curve.
  * Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
  * Answer the following question in your notebook: What is the best value for k?
 
 ## Cluster Cryptocurrencies with K-means Using the Original Scaled Data


* Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:
  
  * Initialize the K-means model with the best value for k.
  * Fit the K-means model using the original scaled DataFrame.
  * Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
  * Create a copy of the original data and add a new column with the predicted clusters.
  * Create a scatter plot using hvPlot as follows:
    
    *  Set the x-axis as "PC1" and the y-axis as "PC2".
    *  Color the graph points with the labels found using K-means.
    *  Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
 
 ## Optimize Clusters with Principal Component Analysis
 
* Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
  
* Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:
  
  * What is the total explained variance of the three principal components?
    
* Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame:
  
  * The first five rows of the PCA DataFrame should appear as follows:

![Screenshot 2023-11-13 145133](https://github.com/Connextstrategy/CryptoClustering/assets/18508699/508359d4-23df-4b8b-b5c8-1fa88a48147c)

 ## Find the Best Value for k Using the PCA Data

 Use the elbow method on the PCA data to find the best value for k using the following steps:
 
   * Create a list with the number of k-values from 1 to 11.
   * Create an empty list to store the inertia values.
   * Create a for loop to compute the inertia with each possible value of k.
   * Create a dictionary with the data to plot the Elbow curve.
   * Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
     
   * Answer the following question in your notebook:
       * What is the best value for k when using the PCA data?
       * Does it differ from the best k value found using the original data?

## Cluster Cryptocurrencies with K-means Using the PCA Data

Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:

   * Initialize the K-means model with the best value for k.
   * Fit the K-means model using the PCA data.
   * Predict the clusters to group the cryptocurrencies using the PCA data.
   * Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
   * Create a scatter plot using hvPlot as follows:
     
       * Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
       * Color the graph points with the labels found using K-means.
       * Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
         
   * Answer the following question:
     
       * What is the impact of using fewer features to cluster the data using K-Means?

### Dependencies

* Using Visual Studio Code or Jupyter notebooks for coding and data visualization

### Installing

* No modifications needed to be made to files/folders

## Help

* Use console.log inside of your JavaScript code to see what your data looks like at each step.

* Refer to the Plotly.js documentationLinks to an external site. when building the plots.

## Authors

Christopher Manfredi

## Version History
