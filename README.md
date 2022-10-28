# Module 18
# Cryptocurrencies

## Objective and the purpose of the analysis

In this module I am asked to perform the unsupervised machine learning to create a report on the cryptocurrencies that are on the trading market and to group them in order to classify them for an investment.
In this module I learned about unsupervised machine learning. I learned to process the data, clustering and reducing the dimensions and how to use Principal components analysis. 

## Deliverable 1: Preprocessing the Data for PCA

The data provided for this challenge was not fit for the machine learning models, hence required some processing. First, I kept only those cryptocurrencies which are being traded. Removed those rows which do not have any working algorithm. Then dropped the column “IsTrading” as this column was not giving any useful information. Dropped the rows containing the null values and only those rows are kept whose has the value for “TotalCoinsMined”. Dropped another column with “CoinName” and used the get dummies() method to create binary encoded data frame for the columns "Algorithm" and "ProofType". Then I standardized the data using “StandardDcaler() method.

![Picture_1](https://github.com/gothwalritu/Cryptocurrencies/blob/main/ScreenShots/D1.png)

## Deliverable 2: Reducing Data Dimensions Using PCA

In this section of the challenge, I reduced the Data Dimensions into three principal components using pcs.fit_transform() method. I created a data frame for the three principal components as shown in the table below.

![Picture_2](https://github.com/gothwalritu/Cryptocurrencies/blob/main/ScreenShots/D2.png)

## Deliverable 3: Clustering Cryptocurrencies Using K-means

In this section of challenge I am clustering the cryptocurrencies. The output of the analysis is not known and that is why I am using the unsupervised machine learning. Frist, I created and, then plotted the elbow curve. With the help of the elbow curve I was able to find out the suitable number of clusters for the cryptocurrencies. I created a new data frame with the columns: Algorithm, ProofType, TotalCoinSupply, PC1, PC2, PC3, CoinName and Class. This new data frame is shown below.

![Picture_3a](https://github.com/gothwalritu/Cryptocurrencies/blob/main/ScreenShots/D3a.png)


![Picture_3b](https://github.com/gothwalritu/Cryptocurrencies/blob/main/ScreenShots/D3b.png)

## Deliverable 4: Visualizing Cryptocurrencies Results

•	In this section I created the visualizations for the results using px.scatter_3d() method.

![Picture_4](https://github.com/gothwalritu/Cryptocurrencies/blob/main/ScreenShots/D4a.png)

•	Created a table with tradable cryptocurrenies as shown below.

![Picture_5](https://github.com/gothwalritu/Cryptocurrencies/blob/main/ScreenShots/D4b.png)

•	Scaled the “TotalCoinSupply” and “TotalCoinsMined” using MinMaxScaler().fit_transfrom() method. Created another scatter plot using hvplot.scatter() method, the figure the shown below. In this 2-d scatter plot, it is difficult to distinguish the different classes. Hence, performing the PCA method is giving better visualizations.

![Picture_6](https://github.com/gothwalritu/Cryptocurrencies/blob/main/ScreenShots/D4c.png)


## Summary

There are 532 cryptocurrencies which are tradable and are classified into 4 groups based on the similarities among their features. Finding the principal components and K value really helped in forming the clusters. However, more analysis would be needed to be able to determine which cryptocurrency would be most suitable for investment.
