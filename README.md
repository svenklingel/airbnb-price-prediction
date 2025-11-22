# Airbnb Price Prediction

Predict Airbnb listing prices using **CatBoost** and **XGBoost** regression models with hyperparameter tuning via **Optuna**.
Data Source: New York City Airbnb Open Data

**Data Source:** [New York City Airbnb Open Data](https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data/data) (Kaggle)  

## Overview

This study highlights the potential of gradient boosting algorithms, such as CatBoost and XGBoost, in predicting Airbnb listing prices based on multiple features, such as location, room type, host activity, availability, proximity to attractions, and review statistics. Among the models tested, CatBoost demonstrated strong performance, particularly in handling categorical features, achieving an RMSE slightly better than XGBoost (0.338 vs. 0.339). Overall, the accommodation type and location of a listing play the most critical roles in price 
prediction.

## Features Used

- `neighbourhood_group` – City district  
- `neighbourhood` – Specific neighborhood  
- `room_type` – Type of room (entire home, private room, etc.)  
- `calculated_host_listings_count` – Number of listings by the host  
- `minimum_nights` – Minimum stay required  
- `availability_365` – Days available in a year  
- `dist_attraction` – Distance to nearest attraction  
- `dist_coastline` – Distance to coastline  
- `dist_restaurant` – Distance to nearest restaurant  
- `reviews_per_month` – Average number of reviews per month  
- `number_of_reviews` – Total reviews  

The target variable is the log-transformed `price`.

## Models & Tuning

- **CatBoost** and **XGBoost** regression  
- Hyperparameters optimized using **Optuna**  

## Performance

| Model       | RMSE (log scale) | RMSE (dollar) |
|------------|-----------------|---------------|
| CatBoost   | 0.338           | $47.46        |
| XGBoost    | 0.339           | $47.63        |
