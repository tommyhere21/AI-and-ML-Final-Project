# AI and ML Final Project
- Issayeva Tomiris (289721)
- Maratkyzy Zhanel (286251)
- Aruzhan Kenessova (286071)
- George Maurice (E00308)

# ShopEasy Customer Segmentation Analysis

## 1) Introduction

ShopEasy is a leading e-commerce platform that aims to enhance user experiences through personalized services and promotions. This project focuses on understanding customer behavior by segmenting them into distinct groups based on their purchasing patterns. By applying clustering techniques, we aim to uncover hidden patterns and provide actionable insights for improving customer satisfaction and driving sales growth.

## 2) Methods

### Data Overview
The dataset utilized in our analysis consists of a single comprehensive file:

- **shopEasy.csv**: This dataset provides a detailed look at customer interactions and transactions on the ShopEasy platform. It encompasses a variety of information on 8,950 entries, giving us a deep dive into the purchasing patterns and behaviors of the customers. Here are the key components of this dataset:

  1. **Customer Details**: Each record includes the customer's identifier and demographic information like location and account type, which helps in understanding customer diversity and preferences.
  
  2. **Account Metrics**: Data such as account totals, emergency funds, and the maximum spend limit are available. These metrics help in assessing the financial engagement and capacity of the customers.
  
  3. **Transaction Details**: Detailed records of each transaction include the cost of items purchased, whether the purchases were single or multiple items, and the frequency of these transactions. This provides insights into the purchasing habits and preferences of the customers.
  
  4. **Engagement Metrics**: Information on the frequency of account usage, types of items bought, and customer loyalty indicators like subscription to newsletters or participation in the store’s club. These metrics are crucial for understanding customer loyalty and engagement levels.

This dataset forms a robust foundation for our analysis, enabling us to explore detailed customer demographics, financial behavior, and transactional data, which are crucial for developing effective segmentation and personalized marketing strategies.

### Preparation of Data:
Data cleaning involved handling missing values and erroneous entries, particularly in the 'maxSpendLimit' and 'leastAmountPaid' fields. This was crucial as it ensured the integrity and reliability of our analysis.


 ### Exploratory Data Analysis and Data Visualization

Our EDA focused on uncovering underlying patterns and relationships within the data, employing statistical analysis and visualization tools. Key insights were drawn from the distribution of account totals, item costs, and customer engagement metrics using Python libraries such as Pandas, Matplotlib, and Seaborn.

#### Data Visualisation

This histogram shows that most customers have low account balances, with the frequency decreasing as account values increase, indicating a right-skewed distribution.

![account total](https://github.com/tommyhere21/AI-and-ML-Final-Project-289721/assets/50324471/ea54bc02-a913-47a9-b022-b7fdd545b2d6)


#### Account Total vs. Item Costs

Visualized the relationship between the total account value and item costs.

![image](https://github.com/tommyhere21/AI-and-ML-Final-Project-289721/assets/50324471/d0155184-d5e1-4666-bb06-0999299165da)

#### Location Frequency

Visualized the distribution of users across different locations.

![Location Frequency](images/location_frequency.png)

#### Feature Distributions

Visualized the distributions of various features in the dataset.

![image](https://github.com/tommyhere21/AI-and-ML-Final-Project-289721/assets/50324471/be7fc9d0-7e8f-4d64-85c8-900807caf6ca)

# This scatterplot with regression line shows the relationship between account total and item costs for ShopEasy customers, indicating a general trend where higher account totals do not necessarily correlate with higher item costs
![image](https://github.com/tommyhere21/AI-and-ML-Final-Project-289721/assets/50324471/63fb252b-b0e1-4fc5-8558-68bed71fea63)

#  scatterplot with a regression line illustrates the relationship between account totals and emergency funds among ShopEasy customers, showing a moderate positive correlation where customers with higher account balances tend to have more in emergency funds.
![image](https://github.com/tommyhere21/AI-and-ML-Final-Project-289721/assets/50324471/e4388904-7dad-44d9-9f13-ba756be1e458)

#  histogram displays the distribution of account totals for ShopEasy customers in Chicago (blue), Los Angeles (yellow), and New York (green), showing that lower account totals are more common across all locations, with a significant concentration in the lowest bin.
![image](https://github.com/tommyhere21/AI-and-ML-Final-Project-289721/assets/50324471/124d440a-6d58-4580-a46f-e1ba03b6dadc)

# correlation heatmap displays the relationships between various metrics within the ShopEasy dataset. Each cell color indicates the strength of correlation, with warmer colors (orange to yellow) showing higher positive correlations, and cooler colors (purple) indicating lower correlations. Notable strong correlations are seen between related purchasing behaviors such as item costs and single/multiple item buy frequencies.
![image](https://github.com/tommyhere21/AI-and-ML-Final-Project-289721/assets/50324471/c2183681-f72e-49cf-9db2-708d3879d29f)

### Implementing clustering
# K-Means clustering
# StandardScaler
We first used StandardScaler, not aware of its detriments. The resulting analysis was skewed by using StandardScaler, which wasn't suitable for our data. The data has a lot of outliers, and StandardScaler is not suitable for data with a lot of outliers and the results come out skewed. Therefore the first time the elbow method was indicative of using 4 clusters.

The results were not satisfactory, the silhouette score was only 0.1 which is very small. The cluster visualisation provided not clear picture of the clusters, overall bad quality of the clustering.The  plot utilizes the Elbow Method to optimize the number of clusters for K-means clustering. It graphs the cluster count against inertia (sum of squared distances of samples to their closest cluster center). The plot shows a discernible elbow at four clusters, suggesting that increasing the number of clusters beyond this point yields diminishing returns in terms of intra-cluster variance reduction. This method helps in selecting a cluster count that balances complexity and explanatory power of the clustering model.

![image](https://github.com/tommyhere21/AI-and-ML-Final-Project-289721/assets/50324471/9cb6c2ac-7318-4b5c-b8c0-5e7db11c3ef8)

# The  visualization employs Principal Component Analysis (PCA)
to reduce dimensionality for effective visualization of K-means clustering results. It plots the first two principal components, showing data points grouped into four distinct clusters, each color-coded. Cluster centers are marked with red 'X' symbols, illustrating the centroids of the respective clusters. This visualization aids in assessing the clustering algorithm's effectiveness by observing the spatial distribution and overlap between clusters.

![image](https://github.com/tommyhere21/AI-and-ML-Final-Project-289721/assets/50324471/d0d7579b-32bb-42e7-817a-db7fff4517be)

# Elbow method to find the right number of clusters.
Iterate through 1-9 number of clusters and calculate the inertia for each number of clusters and plot it. The elbow point is where the inertia starts to decrease at a slower rate. The elbow point is not fully clear, but 3 is most likely it.
![image](https://github.com/tommyhere21/AI-and-ML-Final-Project-289721/assets/50324471/728e32ed-ed3c-46aa-8fd5-e236f8cc4741)

### Section 3) Experimental Design

**Experiment 1: K-means StandardScaler vs RobustScaler**
- **The main purpose**: To assess the suitability of StandardScaler or RobustScaler for preprocessing data with outliers and its impact on clustering analysis.
- **Baselines**: Clustering segmentation analysis was used to compare. 
- **Evaluation metrics**: We used silhouette scores to compare the suitability of StandardScaler, and the resulting score was 0.1, which is very small and is unsatisfactory. We also visualised the resulting clusters and the clusters were not easily defined, showing poor clustering quality.
- In the result, we came to the conclusion to move to different feature scaling technique - RobustScaler. StandardScaler is poor at addresing outliers of the data, which our dataset had in abundance, which skewed the results and clustering.

**Experiment 2: Number of clusters**
- **The main purpose**: To determine the right number of clusters for clustering algorithms. 
- **Baselines**: We used elbow method, silhouette scores for k-means and dendrograms for hierarchical clustering. 
- **Evaluation metrics**: We used silhouette scores to determine the suitable number of clusters. In both cases, 2 was the most optimal number of clusters. However, 2 segments in the segment analysis would provide limited insight into the segments, therefore we chose 3 clusters as it had acceptably high silhouette scores and overall suitable for our analysis. 

**Experiment 3: K-means vs Hierarchical clustering**
- **The main purpose**: To assess whether to better use K-means or Hierarchical clustering for our model.
- **Baselines**: We implemented both K-means and Hierarchical clustering to compare their results. 
- **Evaluation metrics**: We used silhouette scores to compare the suitability of each clustering method. K-means had value of 0.537 vs Hierchical 0.448. The cluster visualisation also showed clearly that the K-means clusters had better separation than the Hierarchical clusters. 

 
## 4) Results

### Cluster Descriptions

Clusters were described based on the mean values of features within each cluster. This provided insights into the characteristics of customers in each segment.

- **Cluster 0**: Customers with high account total and emergency funds, moderate item costs.
- **Cluster 1**: Customers with moderate account total and item costs, frequent single item purchases.
- **Cluster 2**: Customers with low account total, high frequency of emergency fund usage.

### Visualization of Clusters

Scatter plots were used to visualize the clusters, showing the distribution of customers across different spending patterns.

### Summary of Findings

The clustering analysis revealed distinct customer segments with unique purchasing behaviors:
- **Cluster 0**: High spenders with significant emergency funds.
- **Cluster 1**: Moderate spenders with frequent single purchases.
- **Cluster 2**: Low spenders with high reliance on emergency funds.

## 5) Recommendations

- **Cluster 0**: Target these customers with premium services and high-value promotions.
- **Cluster 1**: Encourage bulk purchases with bundle offers.
- **Cluster 2**: Provide financial incentives and loyalty programs to increase spending.

## 6) Conclusion

The clustering analysis provided valuable insights into customer segments, enabling ShopEasy to tailor marketing strategies and enhance user experiences. By leveraging these insights, ShopEasy can improve customer satisfaction and drive sales growth.
