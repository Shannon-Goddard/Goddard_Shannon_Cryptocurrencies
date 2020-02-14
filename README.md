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
### **Describe the differences between supervised and unsupervised learning**  
In **supervised learning**, the input data already has a paired outcome, which is plugged in to train the model to predict outcomes in new datasets. For example, we want to build a model that, when given unfamiliar data, can accurately predict the outcomes.  

In **unsupervised learning**, there are two key differences from the above approach:
- There are no paired inputs and outcomes.
- The model uses a whole dataset as input.  

Unsupervised learning is used in one of the following two ways:
- Transform the data to create an intuitive representation for analysis or to use in another machine learning model; or
- Cluster or determine patterns in a grouping of data, rather than to predict a classification.  

**Real-world examples of each:**  
For example, imagine a store owner is planning to stock up on back-to-school supplies. The owner’s challenges are selecting from a wide range of school supplies, devoting considerable space to the inventory, and maintaining a fast inventory turnover rate, from stocking to selling.  

**Supervised learning**  
The owner wants to predict the best time to start selling school supplies so staff can make room for the next big items to sell. The owner decides to focus on the previous year’s data, which includes the number of items sold, when they were sold, and the area schools’ start dates for 10, 20, and 30 days prior to the items’ sell dates. Since the owner knows what they are looking for, the best time to start selling school supplies, the best approach would be linear regression, a supervised learning model. The data from the previous year will have inputs (amount sold, date sold, schools’ start dates) that coincide during the time they stocked supplies. The owner will be able to see how sales in school supplies increased as the schools’ start dates approached.  

**Unsupervised learning**  
Now, imagine the owner notices that when customers come in to buy school supplies, they also purchase non-school items, giving other categories a bump in sales. There are a wide variety of products to offer different consumers, so the owner wants to know which consumers might buy more products and what items they might want to buy. We don’t really know how to group the data, but we know that grouping the data will be instructive. You’ll need to factor in many data points, such as age, race, gender, location, and much more. Since the owner doesn't know exactly how many groups or what kinds of customers those groups contain, the best method for finding out would be unsupervised learning. With unsupervised learning, the owner can plug the full dataset in and cluster groups of customers together.

### **Preprocess data for unsupervised learning.**  
Before moving data to our unsupervised algorithms, we complete the following steps for preparing data:
- Data selection
- Data processing
- Data transformation  

**Data Selection** entails making good choices about which data will be used. Consider what data is available, what data is missing, and what data can be removed.  

**Data processing** involves organizing the data by formatting, cleaning, and sampling it.  

**Data transformation** entails transforming our data into a simpler format for storage and future use, such as a CSV, spreadsheet, or database file.  

Once our data is cleaned and processed, we would export the final version of the data as a CSV file for future analysis.

### **Cluster data using the K-means algorithm.**  
Clustering is a type of unsupervised learning that groups data points together. This group of data points is called a **cluster**.  

**K-means** is an unsupervised learning algorithm used to identify and solve clustering issues.  
- K represents how many clusters there will be. These clusters are then determined by the **means** of all the points that will belong to the cluster.  
- The K-means algorithm groups the data into K clusters, where belonging to a cluster is based on some similarity or distance measure to a centroid.  

A **centroid** is a data point that is the arithmetic mean position of all the points on a cluster.  
- The centroid is found by taking the mean of all the x values in a cluster, and the mean of all the y values in a cluster.

### **Determine the best amount of centroids for K-means using the elbow curve.**  
One method for determining the best number for K is the elbow curve. Elbow curves get their names from their shape: they turn on a specific value, which looks like an elbow.  

To create an elbow curve:  
- Plot the clusters on the x-axis  
- Plot the values of a selected objective function on the y-axis.  

**Inertia** is one of the most common objective functions to use when creating an elbow curve. The inertia objective function measures the amount of variation in the dataset.  

To create an elbow curve:
- Plot the number of clusters (also known as the values of K) on the x-axis  
- Plot the inertia values on the y-axis.

### **Use PCA to limit features and speed up the model.**  
**PCA(Principal Component Analysis)** is a statistical technique to speed up machine learning algorithms when the number of input features (or dimensions) is too high. PCA reduces the number of dimensions by transforming a large set of variables into a smaller one that contains most of the information in the original large set.  

Stats concepts in a feature extraction:  
- **Mean** is the sum of a group of numbers divided by the total amount of numbers.  
- **Variance** is the square distance from each point from the center, added together, and divided by the total number of points. The variance measures the spread of a set of numbers.  

The center of the line is set to the mean.  

Covariance comes into play when the variances are exactly the same; however, it is very obvious that the two graphs are totally different. For example, when each has the same center, with different points on the left and the right, one sloping negatively and the other sloping positively. 
- **Covariance** is a metric that allows us to tell these two different sets of points apart.  

Covariance is the sum of the product of coordinates divided by the number of points. The Line can have:
- a negative covariance  
- a positive covariance  
- covariance of zero.  

Eigenvectors and eigenvalues show us the spread of the dataset and by how much.
- **eigenvectors** are the points that stretch out in our graph in different directions.  
- **eigenvalue** are the magnitude that each of these stretches.  

The higher eigenvalue is the axis that carries the most amount of information. The Final data points will give us a table of two columns. Ultimately, just reducing dimensions yet still keeping the values.

## Challenge Overview  
In this challenge, we use unsupervised learning to analyze data on the cryptocurrencies traded on the market. We present a report of what cryptocurrencies are on the trading market and how cryptocurrencies could be grouped toward creating a classification for developing a new investment product. The data we work with is not ideal, so we process it to fit the machine learning models. Since there is no known output for what we are looking for, we decided to use unsupervised learning. To group the cryptocurrencies, we decided on a clustering algorithm to help determine about investing in this product. We used data visualizations to share our findings.


## Objectives
- Prepare the data for dimensions reduction with PCA and clustering using K-means.
- Reduce data dimensions using PCA algorithms from sklearn.
- Predict clusters using cryptocurrencies data using the K-means algorithm form sklearn.
- Create some plots and data tables to present your results.

## Challenge Summary
### **Data Preprocessing**  
In this section, we had to load the information about cryptocurrencies from the provided CSV file and perform some data preprocessing tasks. The data was retrieved from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist)  

We started by loading the data in a Pandas DataFrame named “crypto_df” and continued with the following data preprocessing tasks:
- Remove all cryptocurrencies that aren’t trading.
- Remove all cryptocurrencies that don’t have an algorithm defined.
- Remove the IsTrading column.
- Remove all cryptocurrencies with at least one null value.
- Remove all cryptocurrencies without coins mined.
- Store the names of all cryptocurrencies on a DataFramed named coins_name, and use the crypto_df.index as the index for this new DataFrame.
- Remove the CoinName column.
- Create dummies variables for all of the text features, and store the resulting data on a DataFrame named X.
- Use the [StandardScaler from sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html) to standardize all of the data from the X DataFrame. 

### **Reducing Data Dimensions Using PCA**  
We used the [PCA algorithm from sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html) to reduce the dimensions of the X DataFrame down to three principal components.  

Once we had reduced the data dimensions, we created a DataFrame named “pcs_df” that includes the following columns: PC 1, PC 2, and PC 3. We used the crypto_df.index as the index for this new DataFrame.  

### **Clustering Cryptocurrencies Using K-means**  
We used the [KMeans algorithm from sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html) to cluster the cryptocurrencies using the PCA data.  

We completed the following tasks:

- Create an elbow curve to find the best value for K, and use the pcs_df DataFrame.
- Once you define the best value for K, run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data. Use the pcs_df to run the K-means algorithm.
- Create a new DataFrame named “clustered_df,” that includes the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class. You should maintain the index of the crypto_df DataFrames as is shown below: 


### **Visualizing Results**  
We created data visualizations to present the final results.  

By completing the following tasks:

- Create a 3D scatter plot using Plotly Express to plot the clusters using the clustered_df DataFrame. You should include the following parameters on the plot: **hover_name="CoinName"** and **hover_data=["Algorithm"]** to show this additional info on each data point.
- Use **hvplot.table** to create a data table with all the current tradable cryptocurrencies. The table should have the following columns: CoinName, Algorithm, ProofType, TotalCoinSupply, TotalCoinsMined, and Class.
- Create a scatter plot using **hvplot.scatter** to present the clustered data about cryptocurrencies having x="TotalCoinsMined" and y="TotalCoinSupply" to contrast the number of available coins versus the total number of mined coins. Use the hover_cols=["CoinName"] parameter to include the cryptocurrency name on each data point.
