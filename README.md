# AI-and-ML-Final-Project
Maratkyzy Zhanel (286251)
Issayeva Tomiris (289721)
Aruzhan Kenessova (286071)

# Introduction

ShopEasy is a leading e-commerce platform that aims to enhance user experiences through personalized services and promotions. This project focuses on understanding customer behavior by segmenting them into distinct groups based on their purchasing patterns. By applying clustering techniques, we aim to uncover hidden patterns and provide actionable insights for improving customer satisfaction and driving sales growth.

 2) Methods

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

#Missing Values Heatmap

Visualized missing values to understand the extent of missing data.
#Visualization 1: Missing Values Heatmap

