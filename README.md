# Forecasting Electricity Prices of New York Residential Sector

## Project Overview

This project focuses on analyzing and predicting electricity prices in New York for the residential sector over time, with particular attention to seasonal trends, anomalies, and influencing factors such as weather. The analysis uses time-series data from 2001 to 2024, incorporating sector-level and state-level details, and builds machine learning models to forecast electricity prices effectively.

## Goals
	1.	Explore seasonality and trends in electricity prices
	2.	Create predictive models for electricity prices.
	3.	Incorporate external factors such as weather data to improve model accuracy.
	4.	Visualize insights using interactive dashboards.

## Data
	•	Primary Dataset: Electricity price data from Kaggle (/kaggle/input/electricity-prices/clean_data.csv) with attributes:
	  •	Year, Month
	  •	State, Sector
	  •	Number of Customers, Price, Revenue, Sales
	•	Weather Data: Monthly weather statistics for NYC, including temperature, precipitation, wind speed, and atmospheric pressure from the Meteostat API.

## Key Components

### 1. Exploratory Data Analysis (EDA)
	•	Univariate and bivariate analysis for attributes such as price, revenue, and sales.
	•	Time-series decomposition to identify trends, seasonality, and residuals.
	•	Outlier detection using Z-scores.

### 2. Data Preprocessing
	•	Handling missing values (e.g., forward-filling weather data).
	•	Creating features like day_of_week, day_of_year, and quarter.
	•	Normalizing data using MinMaxScaler.

### 3. Feature Engineering
	•	Seasonal differencing and detrending to make the time series stationary.
	•	Adding weather data as covariates for enhanced prediction accuracy.

### 4. Modeling
	•	ARIMA Models: Automatically selecting optimal parameters using auto_arima.
	•	XGBoost Regressor: Leveraging gradient boosting for predictions.
	•	Conducting hyperparameter tuning using GridSearchCV.
	•	Performance evaluation using metrics such as MAE, MSE, and MAPE.

### 5. Visualization
	•	Visualizing price trends by sector and state using line plots.
	•	Box plots to analyze price distribution by sector.
	•	Combined prediction plots for training and validation data.

### Tools & Libraries
	•	Python Libraries: pandas, numpy, matplotlib, seaborn, statsmodels, scipy, pmdarima, xgboost, sklearn, meteostat.
	•	Weather Data Source: Meteostat API.
	•	Visualization Tools: Seaborn and Matplotlib.

### How to Use
	1.	Set Up Environment:
	•	Install required Python libraries:

pip install pandas numpy matplotlib seaborn statsmodels scipy pmdarima xgboost sklearn meteostat


	2.	Download Data or Pull from Kaggle:
	•	Place clean_data.csv in the working directory.
	•	Fetch weather data via Meteostat API.
	3.	Run the Notebook:
	•	Ensure the environment matches the notebook setup (e.g., Python 3.10+).
	•	Execute the cells sequentially for data preprocessing, EDA, and modeling.

## Future Enhancements
	•	Extend analysis to include real-time electricity price updates.
	•	Develop an interactive dashboard for stakeholders.
	•	Incorporate additional external factors such as economic indicators or grid demand.

Contributors

This project was developed as a personal effort to forecast electricity prices using advanced data science techniques. 
