# NYC Taxi Fare Prediction – Regression & Classification Approach

This project explores New York City Yellow Taxi trip data for **January 2025**, with the goal of predicting taxi fare amounts using both **regression** and **classification** models. It demonstrates an end-to-end data science workflow including data cleaning, feature engineering, modeling, and evaluation.

---

## Project Overview

We explore two predictive approaches:

- **Regression**: Predict the exact `total_amount` a taxi driver will earn for a given trip.
- **Classification**: Categorize fares into three buckets: `low` (< $20), `medium` ($20–$30), and `high` (> $30).

By comparing both methods, we gain insight into which modeling strategy is more practical and accurate depending on the use case.

---

## Features & Data Engineering

The notebook includes:

- Filtering and cleaning real NYC taxi trip data
- Parsing temporal features (hour, day, weekday, holiday)
- Weather enrichment from January 2025 NYC data
- Location grouping using borough information
- Feature scaling and one-hot encoding

---

## Models Used

- **DecisionTreeRegressor** – as a benchmark
- **RandomForestRegressor** – for advanced regression
- **XGBoostRegressor**
- **XGBoostClassifier** – to predict fare range classes

---

## Evaluation Metrics

For regression:
- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

For classification:
- Precision, Recall, F1-score
- Confusion Matrix

---

## Data Sources

This project uses public and derived datasets related to NYC taxi trips and weather:

- **NYC Yellow Taxi Trip Records (January 2025)**  
  Source: [New York City Taxi & Limousine Commission (TLC)](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)  
  Description: Includes detailed trip-level data for yellow taxi rides, such as timestamps, pickup/dropoff location IDs, distance, fare, and payment type.

- **NYC Taxi Zone Lookup Table**  
  Source: [TLC Zone Lookup CSV](https://d37ci6vzurychx.cloudfront.net/misc/taxi_zone_lookup.csv)  
  Description: Provides a mapping of `LocationID` values to `Borough` and `Zone` for use in spatial aggregation.

- **NYC Weather Data (January 2025)**  
  Source: [Visual Crossing Weather Data](https://www.visualcrossing.com/)
  Description: Daily weather observations.


  ---

  ## Conclusions

- Regression offers a precise estimate but is moderately limited by available features, particularly the absence of route-specific or traffic data.
- Classification offers a more interpretable, actionable alternative, especially when fare ranges are sufficient for business decisions.
- Feature engineering significantly improved model performance, especially weather and location-based aggregations.


