
# Bike Rental Demand Prediction Assignment

## Problem Statement

This assignment involves building a multiple linear regression model to predict the demand for shared bikes. The model will help BoomBikes, a US-based bike-sharing service provider, understand the factors influencing bike demand and prepare for the post-pandemic market scenario.

### Context

Bike-sharing systems provide short-term bike rentals, often using computer-controlled docks for bike pickup and return. BoomBikes has experienced a significant decline in revenue due to the ongoing COVID-19 pandemic. To recover and thrive in the future, the company aims to understand the demand for shared bikes once the lockdown ends and normalcy resumes.

The consulting company hired by BoomBikes needs to analyze various factors influencing bike demand in the American market. The objectives are:
- Identify significant variables in predicting bike demand.
- Determine how well these variables explain the demand.

### Business Goal

The goal is to develop a model that predicts the demand for shared bikes based on available independent variables. This model will assist BoomBikes' management in understanding demand variations and tailoring their business strategy to meet customer needs and optimize profits.

## Dataset

The dataset consists of daily records of bike rentals with the following features:

- **instant**: Record index
- **dteday**: Date
- **season**: Season (1: Spring, 2: Summer, 3: Fall, 4: Winter)
- **yr**: Year (0: 2018, 1: 2019)
- **mnth**: Month (1 to 12)
- **holiday**: Whether the day is a holiday (1: Yes, 0: No)
- **weekday**: Day of the week
- **workingday**: Whether the day is a working day (1: Yes, 0: No)
- **weathersit**: Weather situation (1: Clear, 2: Mist, 3: Light Snow/Rain, 4: Heavy Rain/Snow)
- **temp**: Temperature in Celsius
- **atemp**: Feeling temperature in Celsius
- **hum**: Humidity
- **windspeed**: Wind speed
- **casual**: Number of casual users
- **registered**: Number of registered users
- **cnt**: Total number of bike rentals (target variable)

### Data Preparation

Certain features like `season` and `weathersit` have numeric values representing categories. It is recommended to convert these into categorical string values to avoid incorrect assumptions of an ordinal relationship.

The `yr` column, indicating the year (2018 or 2019), may seem insignificant due to its binary nature. However, considering the increasing popularity of bike-sharing systems, it could be a valuable predictor and should not be discarded without analysis.

### Model Building

The model will be built with `cnt` (total rentals) as the target variable. You will need to perform the following steps:
1. Data cleaning and preparation.
2. Convert appropriate numeric variables to categorical.
3. Build and train the multiple linear regression model.
4. Evaluate the model using appropriate metrics.

### Model Evaluation

After building the model, evaluate its performance using the R-squared score on the test dataset. This can be done with the following code:

```python
from sklearn.metrics import r2_score
r2_score(y_test, y_pred)
```

Where `y_test` is the actual demand on the test set, and `y_pred` is the predicted demand.

## Submission

Submit the completed Jupyter notebook containing your analysis, model, and results.
