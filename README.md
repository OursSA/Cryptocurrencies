# Cryptocurrencies
## Module 18 Challenge: Cryptocurrency Analysis with Unsupervised Learning

The overall purpose of this analysis was to use unsupervised learning to categorize actively traded cryptocurrencies. First, a large set of data about different currencies was loaded into Pandas. The data was then transformed to enable principal component analysis, which was then fed into the k-means clustering algorithm to provide insights into the various currencies that are traded.

### Data Preparation

In order to prepare the original data for PCA, the original data was filtered to exclude currencies not currently traded, currencies for which some of the input data was not known, and currencies that did not have a positive number of coins mined. The coin names were then removed temporarily to enable further processing, and numerical values were assigned in place of the string values for Algorithm and Proof Type.

### PCA and K-Means

Once the relevant data had been cleaned and standardized, Principal Component Analysis was then used to determine the most important features of the data set. In this case, three components were generated. Those components were then used to generate an elbow curve, which indicated that it would be appropriate to sort the currencies into four clusters. Once K-Means had been used to identify a "class" for each currency, the descriptive data regarding coin names, algorithms, and proof types was returned to the data to allow the classifications to be read alongside the principal components and the text values.

### Visualizations
To add accessibility to the findings, a few graphs and tables were then generated:
- A 3D scatterplot, indicating how the three principal components aligned with the four clusters
- A sortable table of the currencies, allowing for faster lookup of currencies that are similar in terms of number of coins, algorithm, or class
- A scatter plot of coin supply and coins mined, which also shows how coins of different "classes" are similar in those two dimensions, as well as more clearly demonstrating that two of the coins have much greater current supplies than any of the others.