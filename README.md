# CryptoClustering
# NU Bootcamp Module 19

# Overview:
# In this challenge, you will apply your Python skills and knowledge of unsupervised learning techniques to explore how 24-hour and 7-day price changes influence cryptocurrency clustering.

# Instructions:

## 1. Load and Explore the Data:
# - Load `crypto_market_data.csv` into a DataFrame.
# - Generate summary statistics to understand the data.
# - Plot the data to visualize initial relationships between variables.

## 2. Data Preparation:
# - Normalize the data using the `StandardScaler()` from scikit-learn.
# - Create a new DataFrame with the scaled data.
# - Set "coin_id" as the index in the new DataFrame.

## 3. Determine the Optimal Value of k Using the Elbow Method:
# - Create a list of k values ranging from 1 to 11.
# - Initialize an empty list to store inertia values.
# - Use a for loop to compute the inertia for each k value.
# - Plot the elbow curve to visually identify the optimal k.
# - Determine and document the best value for k.

## 4. Clustering Cryptocurrencies Using K-Means on the Scaled Data:
# - Initialize the K-Means model using the optimal k value identified.
# - Fit the K-Means model to the scaled DataFrame.
# - Predict the clusters for cryptocurrencies.
# - Create a new column in the original DataFrame to store cluster labels.
# - Plot a scatter plot using hvPlot with:
#     - x-axis: `price_change_percentage_24h`
#     - y-axis: `price_change_percentage_7d`
#     - Color points by the cluster labels.
#     - Include "coin_id" in hover columns for identification.

## 5. Optimize Clustering with Principal Component Analysis (PCA):
# - Perform PCA to reduce the dataset to three principal components.
# - Calculate the explained variance and document the total variance explained by the components.
# - Create a new DataFrame with PCA-transformed data, using "coin_id" as the index.

## 6. Determine the Optimal Value of k Using the PCA Data:
# - Repeat the elbow method steps on the PCA data to identify the optimal k.
# - Compare the best k value from PCA data with the original data's k value.
# - Document whether the k values differ between the original and PCA data.

## 7. Clustering Cryptocurrencies Using K-Means on the PCA Data:
# - Initialize the K-Means model using the optimal k value from PCA data.
# - Fit the model to the PCA-transformed data.
# - Predict clusters and add them as a new column in the PCA DataFrame.
# - Plot a scatter plot using hvPlot with:
#     - x-axis: `PC1`
#     - y-axis: `PC2`
#     - Color points by the cluster labels.
#     - Include "coin_id" in hover columns for identification.
# - Consider and document the impact of using fewer features for clustering.

# Conclusion:
# The README guides you through loading and exploring data, normalizing it, determining the optimal number of clusters using the elbow method, and applying K-Means clustering with and without PCA. The goal is to understand how reducing the number of features impacts the clustering results.
