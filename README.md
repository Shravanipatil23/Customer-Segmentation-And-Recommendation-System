# Customer-Segmentation-And-Recommendation-System-With-EDA
This repository contains a project that demonstrates Customer Segmentation and build a Product Recommendation System using Python. The project also includes Exploratory Data Analysis (EDA) to gain insights into customer behavior and product trends.

Problem Statement:

This project focuses on building a Customer Segmentation and Product Recommendation System using Python. The system leverages machine learning technique named K-Means clustering for customer segmentation and cosine similarity for content-based product recommendations. In today's competitive market, understanding customer behavior is crucial for personalized marketing and improving customer satisfaction. This project aims to solve two key problems:

1. Customer Segmentation:

Grouping customers based on their purchasing behavior and preferences to allow for targeted marketing strategies. Use clustering techniques to identify distinct customer segments from transactional and demographic data.

2. Product Recommendation:

Develop a recommendation engine that suggests products to customers based on similarities between product features (e.g., price, brand, customer reviews). Implement a content-based filtering system using cosine similarity to recommend products similar to the ones a customer has viewed or purchased.

Steps followed:
Step 1 : Imported pandas, matplotlib and seaborn. Used pandas to load the dataset into a DataFrame. Data was a csv file. Copied the original data to avoid altering of values of the original dataset. Inspected the data using functions head(), info(), and describe() to understand its structure and get an overview of the features available for analysis.

Step 2 : Checked for missing values by using function isnull().sum(). There were no missing values, the sum returned was 0 for all the columns of the table.

Step 3 : Categorized the columns of the table into categorical features and numerical features, each list named as catg_features and num_features respectively.

Step 4 : Performed Exploratory Data Analysis with descriptive statistics and used visualizations to explore relationships between variables. Used matplotlib to create histograms, bar plots, and pie plots to uncover insights into customer behavior and product patterns. For the column "Brand of the Product", since the number of distint values it contained were 48, therefore only top 10 brands were considered for better visualization and understanding.

Step 5 : Started for the segmentation of the customers. Encoded categorical features using LabelEncoder.

Step 6 : Scaled all features using StandardScaler to ensure that all features contributed equally to clustering and recommendation.

Step 7 : Appended list of inertia using KMeans to plot the graph.

Step 8 : Determined the optimal number of clusters using the Elbow Method by plotting inertia for different values of k. Used Matplotlib for plotting line graph with markers to obtain value of k.

Step 9 : Added column named "Clusters" to the original data, used KMeans.fit_predict() to predict the values of "Cluster" column.

Step 10 : Plotted 2D Scatter plot using Seaborn, the columns considered for the plotting the gragh were "Number of clicks on similar products" and "Price of the product" for better insights of the segmented customers. Used 'hue' as "Clusters" columns to help us differentiate different clusters.

Step 11 : Started with Recommendation System code which is based on content-based recommendation system. Imported cosine_similarity library to get products with high similarity scores which can be recomended together.

Step 12 : Copied the original data to avoid direct data manipulation of the original data.

Step 13 : Chose relevant product features that will be used for making recommendations, stored the names of the these columns\features in the "recommendation_cols" in the form of list.

Step 14 :Encoded categorical column "Brand of the product" using LabelEncoder.

Step 15 : Used cosine similarity to compute the similarity between products based on their feature vectors. The similarity matrix will contain values that represent how similar each product are to another.

Step 16 :Created a function that takes a product (by its index) and returns the most similar products based on the cosine similarity scores. Sorted the products by similarity scores and returned the top 5 recommendations, excluding the product itself.
