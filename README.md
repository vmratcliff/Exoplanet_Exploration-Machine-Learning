# Machine Learning - Exoplanet Exploration

![exoplanets.jpg](Images/exoplanets.jpg)

## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, created machine learning models capable of classifying candidate exoplanets from the raw dataset.

In this project, tasks included:

1. Preprocess the raw data
2. Tune the models
3. Compare two or more models

- - -

## Resources

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

- - -

## Analysis

In this assignment, I created 3 Machine Learning Models. 
    1. Linear Regression
    2. Logistic Regression
    3. Sequential Neural Network

### Model 1 - SVM, Linear Regression
First step after reading the data to a dataframe was to drop any null values. 

Next was to select the features. I removed the columns that had mostly 0s to increase the accuaracy of the model. I also excluded the koi_err columns.

Next step was to scale and normalize the data to create more accurate model that has less gap between data points so they all have acurate weights for the model. Initially, using MinMaxScaler to scale the data with SVM model, the Training score was 0.5056 and Testing score of 0.4879. Changing to StandardScaler to scale the data resulted better numbers for the scores, Training and Testing Scores of 0.58.

Using GridSearchCV to tune the model's parameters and changing the grid parameters C and gamma improved the scores for both. With StandardScaler Training Score increased to 0.6069 and Testing Score of 0.6075

### Model 2 - Logisitic Regression
For this model, data cleaning and preprocessing steps were the same. 

To scale and  normalize the data, MinMaxScaler was used. Training score of 0.3108 and Testing score of 0.3312. This model will need to be refined for better results. 

### Model 3 - Sequential Neural Network
For this model, data cleaning and preprocessing steps were the same. 

This model has the best accuracy predictor with a accuracy score of 0.7397.
