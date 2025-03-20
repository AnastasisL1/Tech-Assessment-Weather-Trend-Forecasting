# Tech Assessment: Weather Trend Forecasting

## Project Overview
This project analyzes the **Global Weather Repository** dataset to forecast future weather trends using **basic and advanced data science techniques**.  
The dataset consists of **daily weather information for cities worldwide** with **over 40 features**, including **temperature, humidity, wind speed, and air quality indices**.

The objectives of this project are:
- Perform **data cleaning** and **exploratory data analysis (EDA)**.
- Develop **time series forecasting models** for temperature trends.
- Implement **anomaly detection** to identify unusual weather patterns.
- Conduct **feature importance analysis** to assess key weather predictors.
- Perform **spatial analysis** to explore geographical weather trends.

Dataset Source:  
[Kaggle - Global Weather Repository](https://www.kaggle.com/datasets/nelgiriyewithana/global-weather-repository/code)

---

## Key Features and Deliverables

| Feature | Description |
|------------|----------------|
| **Basic Assessment** | Data Cleaning, EDA, Forecasting |
| **Advanced EDA** | Correlations, Outlier Detection, Anomaly Analysis |
| **Multi-Model Forecasting** | ARIMA, SARIMAX, Exponential Smoothing, Ensemble Forecast |
| **Environmental Impact** | Air Quality vs. Weather Analysis |
| **Feature Importance** | Random Forest Feature Ranking |
| **Geographical Analysis** | Spatial Temperature Distributions, Choropleth Maps |
| **PM Accelerator Mission** | Displayed in the report |

Final Report: [Weather_Trend_Forecasting.pdf](./Weather_Trend_Forecasting.pdf)

---

## Methodology

### Data Cleaning & Preprocessing
- **Handled missing values** (filled numerical data with median, categorical with mode).
- **Removed outliers** using **Interquartile Range (IQR)**.
- **Normalized features** using **MinMax Scaling**.

### Exploratory Data Analysis (EDA)
- **Correlation matrix** to identify relationships between variables.
- **Histograms and trend analysis** for temperature and precipitation.
- **Geographical temperature distributions** to visualize regional variations.

### Forecasting Models
Implemented multiple time series forecasting models:
- **ARIMA (1,1,1)**
- **SARIMAX (1,1,1,365)** (including humidity as an exogenous variable)
- **Exponential Smoothing**
- **Ensemble Model** (combined forecasts)

Results Summary:

| Model | MAE | RMSE | MAPE |
|-----------|---------|---------|---------|
| ARIMA | 0.0300 | 0.0388 | 7.01% |
| SARIMAX | 0.0250 | 0.0346 | 5.85% |
| Exponential Smoothing | 0.0291 | 0.0377 | 6.77% |
| **Ensemble** | **0.0291** | **0.0376** | **6.75%** |

The ensemble model provided the best accuracy by reducing variance.

### Anomaly Detection
- Used **Isolation Forest** with **5% contamination rate** to identify **temperature anomalies**.

### Feature Importance Analysis
- Trained a **Random Forest Regressor** to determine feature importance.
- **Humidity and pressure** were the most influential factors affecting temperature.

### Geographical Analysis
- **Choropleth maps** visualizing global temperature trends.
- **Scatter plots and bar charts** analyzing regional variations.

---
