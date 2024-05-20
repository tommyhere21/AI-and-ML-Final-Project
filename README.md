# AI-and-ML-Final-Project
Maratkyzy Zhanel (286251)
Issayeva Tomiris (289721)
Aruzhan Kenessova (286071)

# Introduction

ShopEasy is a leading e-commerce platform that aims to enhance user experiences through personalized services and promotions. This project focuses on understanding customer behavior by segmenting them into distinct groups based on their purchasing patterns. By applying clustering techniques, we aim to uncover hidden patterns and provide actionable insights for improving customer satisfaction and driving sales growth.

 #2 Methods

# Data Overview

The dataset includes various features related to customer purchases on the ShopEasy platform:

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

# Preparation of Data

We loaded the data into a pandas dataframe and cleaned it by removing invalid values. This step was essential for ensuring the accuracy and reliability of our analysis.

# Exploratory Data Analysis and Data Visualization

To gain a deeper understanding of the dataset, we performed exploratory data analysis (EDA) using data visualization and statistical analysis techniques. The main Python packages used for this analysis were:

- Numpy
- Pandas
- Seaborn
- Matplotlib

### Missing Values Heatmap

Visualized missing values to understand the extent of missing data.

![Missing Values Heatmap](images/missing_values_heatmap.png)

### Correlation Heatmap

Visualized the correlation between different features in the dataset.

![Correlation Heatmap](images/correlation_heatmap.png)

### Account Total vs. Item Costs

Visualized the relationship between the total account value and item costs.

![Account Total vs. Item Costs](images/account_total_vs_item_costs.png)

### Location Frequency

Visualized the distribution of users across different locations.

![Location Frequency](images/location_frequency.png)

### Feature Distributions

Visualized the distributions of various features in the dataset.

![Feature Distributions](images/feature_distributions.png)

### Silhouette Scores for Different Numbers of Clusters

Visualized the silhouette scores for different numbers of clusters.

![Silhouette Scores](images/silhouette_scores.png)

### Cluster Visualization

Visualized the clusters based on account total and item costs.

![Cluster Visualization](images/cluster_visualization.png)

## Methods

### Data Preparation

We loaded the data into a pandas dataframe and cleaned it by removing invalid values. This step was essential for ensuring the accuracy and reliability of our analysis.

### Exploratory Data Analysis

We performed exploratory data analysis to gain insights into the dataset and understand the relationships between different features. The analysis included the creation of various plots and visualizations, such as heatmaps, scatter plots, and histograms.

### Clustering

We applied clustering techniques to segment the users into distinct groups based on their purchasing behavior. The K-Means algorithm was used to identify the optimal number of clusters. The silhouette score was used to evaluate the clustering performance.

## Results

The clustering analysis revealed several distinct segments of users with different purchasing behaviors. These insights can be used to tailor marketing strategies and improve customer satisfaction by offering personalized recommendations and promotions.

## Conclusion

This project demonstrates the power of data analysis and machine learning in uncovering hidden patterns and providing actionable insights. By understanding customer behavior, ShopEasy can enhance user experiences and drive sales growth.

## Future Work

Future work could involve exploring more advanced clustering techniques, incorporating additional data sources, and implementing real-time analytics to further improve personalization and customer satisfaction.
