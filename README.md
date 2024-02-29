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
