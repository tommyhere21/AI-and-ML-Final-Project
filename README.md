# AI-and-ML-Final-Project
Maratkyzy Zhanel (286251)
Issayeva Tomiris (289721)
Aruzhan Kenessova (286071)
George Maurice (E00308)



# ShopEasy Customer Segmentation Analysis

## 1) Introduction

ShopEasy is a leading e-commerce platform that aims to enhance user experiences through personalized services and promotions. This project focuses on understanding customer behavior by segmenting them into distinct groups based on their purchasing patterns. By applying clustering techniques, we aim to uncover hidden patterns and provide actionable insights for improving customer satisfaction and driving sales growth.

## 2) Methods

### Data Overview

The dataset used for this analysis is `shopEasy.csv`, which contains information about 50,000 different customers. For each customer, we have data about their total spending, frequency of purchases, and several other attributes related to their buying behavior. The main features included in the dataset are:

- **personId**: Unique identifier for each user
- **accountTotal**: Total amount spent by the user
- **frequencyIndex**: Frequency of purchases
- **itemCosts**: Total cost of purchased items
- **singleItemCosts**: Costs of single purchase items
- **multipleItemCosts**: Costs of installment purchase items
- **emergencyFunds**: Amount kept for emergency purchases
- **itemBuyFrequency**: Frequency of purchases
- **singleItemBuyFrequency**: Frequency of single purchases
- **multipleItemBuyFrequency**: Frequency of installment purchases
- **emergencyUseFrequency**: Frequency of emergency fund usage
- **emergencyCount**: Number of times emergency funds were used
- **itemCount**: Total number of items purchased
- **maxSpendLimit**: Maximum spend limit set by ShopEasy
- **monthlyPaid**: Total amount paid monthly
- **leastAmountPaid**: Least amount paid in a single transaction
- **paymentCompletionRate**: Percentage of completed payments
- **accountLifespan**: Duration of account existence
- **location**: User's city or region
- **accountType**: Type of account (Regular, Premium, Student)
- **webUsage**: Frequency of web usage for shopping

### Preparation of Data

We loaded the data into a pandas dataframe and cleaned it by removing invalid values. This step was essential for ensuring the accuracy and reliability of our analysis.

### Exploratory Data Analysis and Data Visualization

To gain a deeper understanding of the dataset, we performed exploratory data analysis (EDA) using data visualization and statistical analysis techniques. The main Python packages used for this analysis were:

- Numpy
- Pandas
- Seaborn
- Matplotlib






#### Correlation Heatmap

Visualized the correlation between different features in the dataset.

![Correlation Heatmap](images/correlation_heatmap.png)

#### Account Total vs. Item Costs

Visualized the relationship between the total account value and item costs.

![Account Total vs. Item Costs](images/account_total_vs_item_costs.png)

#### Location Frequency

Visualized the distribution of users across different locations.

![Location Frequency](images/location_frequency.png)

#### Feature Distributions

Visualized the distributions of various features in the dataset.

![Feature Distributions](images/feature_distributions.png)

#### Silhouette Scores for Different Numbers of Clusters

Visualized the silhouette scores for different numbers of clusters.

![Silhouette Scores](images/silhouette_scores.png)

#### Cluster Visualization

Visualized the clusters based on account total and item costs.

![Cluster Visualization](images/cluster_visualization.png)

### KMeans Clustering

KMeans clustering was performed with the optimal number of clusters. Each customer was assigned to a cluster, and the characteristics of each cluster were analyzed.

### Cluster Descriptions

Clusters were described based on the mean values of features within each cluster. This provided insights into the characteristics of customers in each segment.

- **Cluster 0**: Customers with high account total and emergency funds, moderate item costs.
- **Cluster 1**: Customers with moderate account total and item costs, frequent single item purchases.
- **Cluster 2**: Customers with low account total, high frequency of emergency fund usage.

### Visualization of Clusters

Scatter plots were used to visualize the clusters, showing the distribution of customers across different spending patterns.
![Cluster Visualization](path/to/cluster_visualization.png)

## 4) Results

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
