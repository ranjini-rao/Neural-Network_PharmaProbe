# Neural-Network_PharmaProbe

# Project Outline

<img width="657" alt="image" src="https://github.com/ranjini-rao/Neural-Network_PharmaProbe/assets/81578500/b763e3b1-c4ca-4f85-92d7-5f99ce9ce16e">


# Exploratory Data Analysis (EDA)

Exploratory Data Analysis (EDA) is an essential approach in data analysis that involves identifying general patterns, outliers, and unexpected features in the data. It serves as a crucial first step in understanding and processing the dataset.

## Overview

After loading the data, we conducted a series of steps to clean and explore the dataset:

## Data Cleaning

We began by checking for NaN values in the conditions and other columns and removed records containing NaNs. Subsequently, we standardized the language in the review text by converting it to numerical representations. Additionally, we removed punctuations and special characters and converted all review text to lowercase to facilitate further processing.

## Outlier Detection and Removal

To identify outliers, we created a new column to count the number of words in the reviews (review_length) and removed outliers in review length, useful_count, and ratings. This step ensured that our analysis focused on reliable data points.

## Analysis of Relationships

We examined the relationships between review length, useful count, and ratings by plotting graphs to visualize these relationships. Furthermore, we explored the seasonality of user ratings to gain insights into potential patterns or trends over time.

## Analysis of Categorical Columns

We analyzed categorical columns in the dataset, particularly focusing on sickness conditions. Initially, we identified a total of 691 conditions but narrowed down our analysis to the top 10 conditions for further exploration.

## Visualization

We utilized various visualization techniques to present our findings effectively. For instance, we plotted graphs to illustrate the relationships between variables, such as the correlation between useful count and review length. Additionally, we used a pie chart to visualize the occurrence of the top 10 sickness conditions in the dataset, highlighting the most prevalent conditions being treated by drugs.

## Conclusion

This comprehensive EDA approach provided valuable insights into the dataset, enabling us to identify patterns, outliers, and relationships between variables. The findings serve as a solid foundation for further data exploration, modeling, and decision-making processes.

## Neural Network Drug Name cluster model
**Problem**: To check if we can predict the drug cluster for a drug with high confidence using features such as 
1) embedded review,
2) ratings,
3) useful_count and
4)  drug name dummy variable.

### File location
[Neural_network_Drug_name_cluster_model/Neural_Network_with_DrugNameTarget.ipynb](https://github.com/ranjini-rao/Neural-Network_PharmaProbe/tree/main/Neural_network_Drug_name_cluster_model)

### Model training approaches
We used word2vec google library to embed the drug name.This library organizes words based on their meanings, grouping similar words together closely in a geometric space. Then we used K-Means to group these words into clusters.
By using all available features (including drug name) and a similar Neural Net structure, our team was able to classify the Drug Name cluster with 95.41% accuracy.

Such a high prediction accuracy asserts that clustering was done appropriately and if a prediction is made for a new Drug, it is highly likely for it to be placed in correct cluster.

<img width="942" alt="Screenshot 2024-02-29 at 4 00 15 PM" src="https://github.com/ranjini-rao/Neural-Network_PharmaProbe/assets/139268721/d429734d-f6c5-4606-a3aa-7e67a4006527">

We used different approaches for model training as shown above.
1. We used *embedded review, condition-dummy-variable and useful count* to predict the drug cluster. This approach gave accuracy of 41.7 %
2. We added *hyper-parameters* in the next try but that didn’t help a lot in accuracy. Accuracy was 40.7%
3. We then used another csv file and introduced *sentiment analysis* as feature. There was again not a lot of impact on accuracy
4. Lastly, we introduced *drug-name dummy variable* as a feature and this helped to propel the accuracy to 95.4%.

### Test data classification
<img width="830" alt="Screenshot 2024-02-29 at 4 01 19 PM" src="https://github.com/ranjini-rao/Neural-Network_PharmaProbe/assets/139268721/4e8c2ddd-941f-4afa-81ee-defdbd270230">

As we can see here that accuracy is pretty high (greater than 88%) for all the cluster. This shows that the clustering we did for drugs was appropriate.

### Usefulness of the model

Given we can now predict drug cluster with high accuracy, we will have high confidence to put a new drug into pre-existing clusters. 
1. This approach can particularly useful for pharma companies who would want to group similar drugs together for storage and/or disposal purposes.
2. This can also be useful for seller companies to advertise/promote/recommend similar drugs if a customer is interested in particular type of drug.
