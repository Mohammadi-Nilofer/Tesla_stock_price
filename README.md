📈 **Tesla Stock Price Forecasting**

Time series forecasting of Tesla (TSLA) stock prices using ARIMA and SARIMA models.

🔍 **Overview**

This project forecasts monthly Tesla stock prices to support investment decisions, risk management, and financial planning.
The goal is to model historical price patterns and generate short-term forecasts that can help analysts and investors understand potential future movements in TSLA stock.
The workflow includes EDA, stationarity checks, seasonality analysis, model building, and a 12-month forecast.

📊 **Dataset**

* Source: Yahoo Finance (yfinance)

* Ticker: TSLA

* Period: 2015–2025

* Frequency: Monthly

* Feature: Closing Price

🛠 **Methodology**

* Data exploration and trend analysis

* STL seasonal decomposition

* Stationarity testing (ADF)

* First-order differencing

* ACF/PACF for parameter selection

* ARIMA and SARIMA model training

* Forecast generation

🤖 **Models**

* Model	Seasonal	AIC	Notes
  * ARIMA(1,1,1)	No	1219.68	Basic fit
    
  * SARIMA(1,1,1)(1,1,1,12)	Yes	1141.39	Best model

**SARIMA provided the most stable and realistic forecasts.**

🔮 **Results**

* Strong long-term upward trend in TSLA prices

* Mild yearly seasonality detected

* SARIMA outperformed ARIMA in model fit and forecast reliability

* Forecast useful for trend insight, not exact price prediction

**Technologies Used**

* Python

* Pandas, NumPy

* Matplotlib

* Statsmodels

* yfinance

* Jupyter Notebook

🚀 **Future Improvements**

* Add exogenous predictors (SARIMAX)

* Implement Prophet, LSTM, or GRU models

🗂 **Repository Structure**

notebooks/
data/
images/
requirements.txt
README.md

▶️ Usage
pip install -r requirements.txt
jupyter notebook notebooks/Tesla_TimeSeries_Forecasting.ipynb

👤 Author

Mohammadi Nilofer
📧 niloferm7@yahoo.com

GitHub: https://github.com/Mohammadi-Nilofer
