# Technical Report: Forecasting Public Transport Passenger Journeys

## Objective
To build accurate forecasting models for daily public transport passenger journeys across various service types using the Prophet time series forecasting framework.

## Data Preparation
- Data sourced from the ACT Government open dataset.
- Date column converted to datetime and sorted chronologically.
- Missing values in the 'Other' service type were filled with zero.

## Exploratory Data Analysis (EDA)
- Visualized passenger counts over time, confirming trends, seasonality, and anomalies.
- Descriptive statistics and missing value checks performed.
- Identified weekly seasonality and impact of holidays and COVID-19 lockdowns.

## Algorithms used for the Task
- Prophet is ideal for your use case because of its built-in handling of seasonality, holidays, and changepoints.
- ARIMA is a solid classical approach for comparison or where data fits its assumptions.
- LSTM offers advanced modeling for more complex patterns but needs more data and training time.

## Forecasting Methodology
- Used Facebook Prophet, a decomposable time series model.
- Data transformed into Prophet’s required format (`ds` for date, `y` for value).
- Separate models built for each service type: Local Route, Light Rail, Peak Service, Rapid Route, School, Other.
- Model parameters tuned with weekly and yearly seasonality, holiday effects, and changepoint adjustments.

## Model Evaluation
- Conducted backtesting by splitting data into training and testing sets.
- Evaluated using MAE and RMSE metrics.
- Visualized forecast vs actual passenger counts for validation.

## Results
- Models capture seasonality and trends effectively.
- Forecast accuracy deemed sufficient for operational use.
- Forecast components plots help interpret underlying patterns.

## Future Work
- Incorporate additional regressors (e.g., weather, events).
- Automate forecasting pipeline and reporting.
- Explore advanced models like LSTM for comparison.

---
