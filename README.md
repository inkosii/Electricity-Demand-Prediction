# Electricity-Demand-Prediction

This repository contains a Jupyter notebook for predicting electricity demand using various machine learning models, including ARIMA and ARIMAX for time series forecasting. The goal of the project is to build an accurate model that can forecast electricity demand based on features such as temperature, time of day, and region.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Model Overview](#model-overview)
4. [Implementation](#implementation)
5. [Results](#results)
6. [Future Work](#future-work)


## Project Overview
In this project, I explore various machine learning techniques to forecast electricity demand over a given time period. The dataset includes variables such as temperature, hour of the day, and region, which are used to train an ARIMA model to predict future electricity demand.

### Key Features:
- Temperature: The temperature at the given time
- Hour: The time of day (from 0 to 23)
- Region: Geographical region (encoded as numerical labels)
- Demand_MW: The target variable, electricity demand in megawatts (MW)

### Goal:
- Build a time series forecasting model to predict electricity demand.
- Evaluate the model's performance and identify potential improvements.

## Dataset
The dataset used for this project contains historical data on electricity demand, temperature, and time-based features. 

### Columns:
- **Date**: Timestamp of the observation.
- **Region**: The geographical region where the observation was recorded.
- **Temperature_C**: Temperature in Celsius at the time of observation.
- **Hour**: Hour of the day (from 0 to 23).
- **IsHoliday**: Boolean flag indicating whether the day is a holiday.
- **Demand_MW**: The electricity demand in megawatts (target variable).

## Model Overview
The project applies time series forecasting models, specifically ARIMAX model, to predict future electricity demand. This model take into account the historical patterns of demand along with external variables like temperature and time of day.

- **ARIMAX (ARIMA with Exogenous Variables)**: This is an extension of ARIMA that includes additional external variables (like temperature and hour of the day) to improve the forecast.

### Steps followed:
1. **Data Preprocessing**: Cleaning, encoding categorical variables, handling missing data, etc.
2. **Exploratory Data Analysis (EDA)**: Visualizing trends, correlations, and identifying stationarity in the data.
3. **Model Training**: Using ARIMA and ARIMAX models for forecasting electricity demand.
4. **Model Evaluation**: Assessing the performance of the model using various error metrics.

## Implementation
The notebook file `Electricity_Demand.ipynb` contains detailed steps on how the model is built, trained, and evaluated.

### Key Sections:
1. **Data Preprocessing**: 
   - Cleaning the data
   - Encoding categorical variables (Region)
   - Handling missing values

2. **Exploratory Data Analysis (EDA)**:
   - Plotting time series data
   - Identifying correlations between temperature, hour, and electricity demand
   - Checking for stationarity

3. **ARIMA & ARIMAX Model Building**:
   - Hyperparameter tuning for ARIMA model (p, d, q)
   - Including external variables in ARIMAX for better performance

4. **Model Evaluation & Forecasting**:
   - Evaluating model accuracy using metrics like AIC, BIC, and RMSE
   - Forecasting future demand for the next 5 periods

## Results
The ARIMAX model demonstrated good forecasting capabilities, with the ARIMAX model outperforming the basic ARIMA model by including external variables like temperature and hour of the day. Future work involves further model tuning and testing with more external features like holiday data and regional weather patterns.

Example forecasted demand for the next 5 periods:
Date  Temperature_C  Hour  Predicted_Demand_MW
2184 2025-04-11             25    10           352.732515
2185 2025-04-12             26    11           368.865305
2186 2025-04-13             27    12           294.895880
2187 2025-04-14             28    13           362.206774
2188 2025-04-15             29    14           370.863799
