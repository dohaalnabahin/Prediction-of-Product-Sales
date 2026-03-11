
# Prediction of Product Sales

## Project Overview
This project analyzes sales data for food items sold across different retail stores.  
The main goal is to explore the dataset and identify the key factors that influence product sales.

## Objectives
- Explore and understand the structure of the dataset
- Clean and prepare the data for analysis
- Handle missing values and inconsistent categories
- Create visualizations to understand patterns in the data
- Identify relationships between product and outlet characteristics and sales

## Tools and Libraries
This project uses the following tools:

- Python
- Pandas
- Matplotlib
- Seaborn
- Google Colab

## Data Analysis
The project includes several exploratory visualizations to better understand the data, such as:

- Histograms to analyze the distribution of numerical features
- Boxplots to examine statistical summaries and detect outliers
- Countplots to visualize the frequency of categorical variables
- Heatmaps to explore correlations between features

## Goal
The goal of this analysis is to help retailers understand which product and outlet characteristics play an important role in increasing sales

 ### Distribution of Numerical Features
<img width="1241" height="990" alt="Histograms to view the distributions of numerical features in your dataset" src="https://github.com/user-attachments/assets/9b07ee12-6881-42da-bd77-b29311ac9eec" />

The histograms above show the distribution of several numerical variables in the dataset, including **Weight, Visibility, Max Price, Store Age, and Sales**.

From the plots, we can observe that **sales values are right-skewed**, meaning that most products have lower sales while a smaller number of products achieve very high sales. Additionally, **visibility values are concentrated near zero**, indicating that many items have relatively low visibility in stores.
-----------------------------------------------------------------------------------------------------------------------------------------------------
 ### Correlation Heatmap
 
<img width="515" height="418" alt="Heatmap to view the correlation between features" src="https://github.com/user-attachments/assets/d9ad4110-b1ad-4b97-97a1-f66fc708fd7d" />


The heatmap above illustrates the correlations between numerical variables in the dataset, including **Weight, Visibility, Max Price, Store Age, and Sales**.

- **Strong Positive Correlation (0.57):**  
  There is a strong positive correlation between **Max_Price** and **Sales**, suggesting that higher-priced products tend to generate higher sales revenue.

- **Weak Correlations (Near Zero):**  
  Other variables such as **Weight** and **Visibility** show very weak correlations with **Sales**, indicating that they may not be strong predictors of sales in this analysis.

