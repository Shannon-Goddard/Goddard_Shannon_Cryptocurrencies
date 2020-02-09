![Header](/pics/header.png)

#### Table of Contents

[Project Overview](#project-overview)  
[Resources](#resources)  
[Objectives](#objectives)  
[Summary](#summary)   
[Challenge Overview](#challenge-overview)  
[Challenge Summary](#challenge-summary)  

## Project Overview  
Here, we dive deeper into machine learning using unsupervised algorithms, which help us explore data when we’re not sure what we’re looking for. Now we can analyze data without a clear output in mind.
We work primarily with the K-means algorithm, the main unsupervised algorithm that groups similar data into clusters. We build on this by speeding up the process using principal component analysis (PCA), which employs many different features.


## Resources


## Objectives 
- Describe the differences between supervised and unsupervised learning, including real-world examples of each.
- Preprocess data for unsupervised learning.
- Cluster data using the K-means algorithm.
- Determine the best amount of centroids for K-means using the elbow curve.
- Use PCA to limit features and speed up the model.

## Summary  
###Describe the differences between supervised and unsupervised learning, including real-world examples of each.
###Preprocess data for unsupervised learning.
###Cluster data using the K-means algorithm.
###Determine the best amount of centroids for K-means using the elbow curve.
###Use PCA to limit features and speed up the model.

## Challenge Overview  
In this challenge, we use unsupervised learning to analyze data on the cryptocurrencies traded on the market. We present a report of what cryptocurrencies are on the trading market and how cryptocurrencies could be grouped toward creating a classification for developing a new investment product. The data we work with is not ideal, so we process it to fit the machine learning models. Since there is no known output for what we are looking for, we decided to use unsupervised learning. To group the cryptocurrencies, we decided on a clustering algorithm to help determine about investing in this product. We used data visualizations to share our findings.


## Objectives
- Prepare the data for dimensions reduction with PCA and clustering using K-means.
- Reduce data dimensions using PCA algorithms from sklearn.
- Predict clusters using cryptocurrencies data using the K-means algorithm form sklearn.
- Create some plots and data tables to present your results.

## Challenge Summary
**Data Preprocessing**
In this section, you have to load the information about cryptocurrencies from the provided CSV file and perform some data preprocessing tasks. The data was retrieved from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist)  

Start by loading the data in a Pandas DataFrame named “crypto_df.” Continue with the following data preprocessing tasks:
- Remove all cryptocurrencies that aren’t trading.
- Remove all cryptocurrencies that don’t have an algorithm defined.
- Remove the IsTrading column.
- Remove all cryptocurrencies with at least one null value.
- Remove all cryptocurrencies without coins mined.
- Store the names of all cryptocurrencies on a DataFramed named coins_name, and use the crypto_df.index as the index for this new DataFrame.
- Remove the CoinName column.
- Create dummies variables for all of the text features, and store the resulting data on a DataFrame named X.
- Use the [StandardScaler from sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html) to standardize all of the data from the X DataFrame. Remember, this is important prior to using PCA and K-means algorithms.
<br/>
<img align="left" width="260" src="/pics/.png"><br/>  

**Reducing Data Dimensions Using PCA**
Use the [PCA algorithm from sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html) to reduce the dimensions of the X DataFrame down to three principal components.  

Once you have reduced the data dimensions, create a DataFrame named “pcs_df” that includes the following columns: PC 1, PC 2, and PC 3. Use the crypto_df.index as the index for this new DataFrame.  

You should have a DataFrame like the following:
<br/>
<img align="left" width="260" src="/pics/.png"><br/>

**Clustering Cryptocurrencies Using K-means**
You’ll use the [KMeans algorithm from sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html) to cluster the cryptocurrencies using the PCA data.  

Complete the following tasks:

- Create an elbow curve to find the best value for K, and use the pcs_df DataFrame.
- Once you define the best value for K, run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data. Use the pcs_df to run the K-means algorithm.
- Create a new DataFrame named “clustered_df,” that includes the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class. You should maintain the index of the crypto_df DataFrames as is shown below: 
<br/>
<img align="left" width="260" src="/pics/.png"><br/>

**Visualizing Results**
You’ll create data visualizations to present the final results.  

Complete the following tasks:

- Create a 3D scatter plot using Plotly Express to plot the clusters using the clustered_df DataFrame. You should include the following parameters on the plot: **hover_name="CoinName"** and **hover_data=["Algorithm"]** to show this additional info on each data point.
- Use **hvplot.table** to create a data table with all the current tradable cryptocurrencies. The table should have the following columns: CoinName, Algorithm, ProofType, TotalCoinSupply, TotalCoinsMined, and Class.
- Create a scatter plot using **hvplot.scatter** to present the clustered data about cryptocurrencies having x="TotalCoinsMined" and y="TotalCoinSupply" to contrast the number of available coins versus the total number of mined coins. Use the hover_cols=["CoinName"] parameter to include the cryptocurrency name on each data point.
<br/>
<img align="left" width="260" src="/pics/.png"><br/>

