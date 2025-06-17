# 🏙️ Airbnb NYC - Exploratory Data Analysis & Price Prediction

This project contains an exploratory data analysis (EDA) and a predictive pricing model for Airbnb properties in New York City. It was developed using historical Airbnb data along with a list of properties provided by an agency seeking to rent their apartments or rooms through the platform.

## 📊 Overview

The goal was to understand the key pricing patterns in NYC's Airbnb market and to generate price suggestions for the new listings sent by the agency, based on similar properties in the dataset.

## 🔍 Key Insights

- **Price Distribution**: Most properties are priced between $50 and $300. Outliers were removed to improve model quality.
- **Room Type Differences**: Entire homes/apartments are the most expensive, followed by private rooms and shared rooms.
- **Location Impact**: The neighborhood group significantly influences price, with Manhattan having the highest average prices.
- **Reviews vs. Price**: There’s no strong linear correlation between number of reviews and price, but listings with more reviews tend to fall within mid-price ranges.

## 🤖 Predictive Model

A linear regression model was built using both numeric and categorical features (via one-hot encoding). Prices were log-transformed to handle skewness and improve performance.

### Model Performance:

- **MAE (Mean Absolute Error)**: ~$40.41  
- **R² Score**: 0.457

This indicates a moderate fit, appropriate given the complexity of the market and data variability.

## 💡 Price Recommendations for the Agency

Using the trained model, suggested prices were generated for each property submitted by the agency:

| Neighbourhood Group | Neighbourhood | Room Type         | Suggested Price (USD) |
|---------------------|---------------|--------------------|------------------------|
| Manhattan           | Midtown       | Entire home/apt    | $152.07                |
| Manhattan           | Midtown       | Entire home/apt    | $153.30                |
| Manhattan           | Midtown       | Private room       | $75.61                 |
| Manhattan           | Midtown       | Entire home/apt    | $153.12                |
| Manhattan           | Midtown       | Private room       | $76.29                 |
| Manhattan           | Midtown       | Entire home/apt    | $152.58                |
| Manhattan           | Midtown       | Private room       | $76.18                 |
| Manhattan           | Midtown       | Private room       | $76.09                 |
| Manhattan           | Midtown       | Entire home/apt    | $153.04                |
| Manhattan           | Midtown       | Entire home/apt    | $153.48                |
| Manhattan           | Midtown       | Entire home/apt    | $152.60                |
| Manhattan           | Midtown       | Private room       | $75.85                 |
| Manhattan           | Midtown       | Private room       | $76.32                 |

> **Note**: These suggestions are based solely on quantitative data. Final pricing should also consider qualitative factors such as amenities, decor, property condition, and seasonality.
