# CryptoClustering
## Module 19 Challenge Datavis Bootcamp
Using unservised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes

## **Overview of the Analysis**
This analysis aims to use unsupervised learning to evaluate scaled data clusters in comparison to scaled data clusters in combination with Principal Component Analysis. 

<details><summary>Our Task</Summary>

**Prepare the Data**
* Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.<br/>
* Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.<br/>

**Find the Best Value for k Using the Original Scaled DataFrame**
Use the elbow method to find the best value for k using the following steps: <br/>
* Create a list with the number of k values from 1 to 11.<br/>
* Create an empty list to store the inertia values.<br/>
* Create a for loop to compute the inertia with each possible value of k.<br/>
* Create a dictionary with the data to plot the elbow curve.<br/>
* Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.<br/>
* Answer the following question in your notebook: What is the best value for k?<br/>

**Cluster Cryptocurrencies with K-means Using the Original Scaled Data**
Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data: <br/>
* Initialize the K-means model with the best value for k.<br/>
* Fit the K-means model using the original scaled DataFrame. <br/>
* Predict the clusters to group the cryptocurrencies using the original scaled DataFrame. <br/>
* Create a copy of the original data and add a new column with the predicted clusters.<br/>
* Create a scatter plot using hvPlot as follows:<br/>
    * Set the x-axis as "PC1" and the y-axis as "PC2".<br/>
    * Color the graph points with the labels found using K-means.<br/>
    * Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.<br/>

**Optimize Clusters with Principal Component Analysis**
* Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.<br/>
* Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:<br/> 
    * What is the total explained variance of the three principal components? <br/>
* Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame. <br/>

**Find the Best Value for k Using the PCA Data**
Use the elbow method on the PCA data to find the best value for k using the following steps: <br/>
* Create a list with the number of k-values from 1 to 11. <br/>
* Create an empty list to store the inertia values. <br/>
* Create a for loop to compute the inertia with each possible value of k. <br/>
* Create a dictionary with the data to plot the Elbow curve. <br/>
* Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k. <br/>
* Answer the following question in your notebook: <br/>
    * What is the best value for k when using the PCA data? <br/>
    * Does it differ from the best k value found using the original data? <br/>

**Cluster Cryptocurrencies with K-means Using the PCA Data**
Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data: <br/>
* Initialize the K-means model with the best value for k. <br/>
* Fit the K-means model using the PCA data. <br/>
* Predict the clusters to group the cryptocurrencies using the PCA data. <br/> 
* Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters. <br/>
* Create a scatter plot using hvPlot as follows: <br/>
    * Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d". <br/>
    * Color the graph points with the labels found using K-means. <br/>
    * Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point. <br/>
* Answer the following question: <br/>
    * What is the impact of using fewer features to cluster the data using K-Means? <br/>

</details>

## **The Results**
After analyzing the cluster results, it can be determined that using fewer clusters reduces the amount of noise in the clusters and grouping has increased clarity with its better clusters. It has also allowed for its user to easily identify the outliers.

## **Data**
For my assignment, I have used data extracted from the following files available in the Resources folder. <br/>
   * crypto_market_data.csv<br/>

In this assignment, I receieved assistance through looking at previous activities, stackoverflow, and received some support through my partner who works in the data analyst field<br/>


