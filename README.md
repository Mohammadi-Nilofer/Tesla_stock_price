📈 **Tesla Stock Price Forecasting (ARIMA & SARIMA)**

This project focuses on forecasting the price of Tesla (TSLA) stock using classical time series analysis techniques, specifically ARIMA and SARIMA models.
Historical stock price data was obtained using the yfinance library.

**Table of Contents**

Project Overview

Dataset

Methodology

Exploratory Data Analysis (EDA)

Seasonality Decomposition

Stationarity

ACF & PACF for Model Order Selection

Model Building (ARIMA & SARIMA)

Forecasting

Results

Future Work

Installation

Usage

Contributing

License

Contact

**Project Overview**

The goal of this project is to build time series models capable of predicting future Tesla stock prices.
Understanding TSLA price movements is valuable for traders, investors, analysts, and financial strategists.

This project demonstrates a complete time series workflow:

Data acquisition

Exploration and preprocessing

Stationarity testing

Seasonal decomposition

Model training & comparison

Forecast visualization

**Dataset**

Source: yfinance

Ticker: TSLA

Date Range: 2015-01-01 to 2025-07-15

Interval: Monthly

Feature Used: Closing Price

🛠 Methodology
Exploratory Data Analysis (EDA)

Included:

Line plot of historical TSLA prices

Summary statistics

Trend and volatility inspection

Seasonality Decomposition

Used STL decomposition to extract:

Trend

Seasonal component

Residuals

Stationarity

Since ARIMA/SARIMA require stationarity:

First-order differencing was applied

ADF Test performed

ADF p-value ≈ 0.80 → Non-stationary before differencing

ACF & PACF

Used to identify:

AR (p)

MA (q)

Seasonal parameters (P, Q, S)

**Model Building (ARIMA & SARIMA)**
ARIMA Model

Model: ARIMA(1,1,1)

Captured basic structure but failed to model strong trend & volatility

Higher AIC score → weaker performance

SARIMA Model

Model: SARIMA(1,1,1)(1,1,1,12)

Included yearly seasonality

More realistic forecasts

Lower AIC → Better fit

Model	AIC	Seasonal	Stationarity	Notes
ARIMA	1219.68	❌ No	Differenced	Limited performance
SARIMA	1141.39	✅ Yes	Differenced	Preferred model
🔮 Forecasting

Both models were used to generate 12-month forecasts, with SARIMA producing smoother, more credible future price trends.

📈 Results

Key insights:

Tesla prices show a strong long-term upward trend

Mild yearly seasonality detected

SARIMA outperformed ARIMA based on AIC

Forecast shows stable-to-slightly upward price movement

**Future Work**

Add external macroeconomic variables (SARIMAX)

Implement advanced models: Prophet, LSTM/GRU

Hyperparameter optimization (GridSearch, Auto-ARIMA)

 Repository Structure
 tesla-price-forecasting/
├── notebooks/

│   └── Tesla_TimeSeries_Forecasting.ipynb

├── images/

├── data/

├── requirements.txt

└── README.md

🧰 Technologies Used

Python

Pandas, NumPy

Matplotlib, Seaborn

Statsmodels

yfinance

Jupyter Notebook

⚙️ Installation
# Clone the repository
git clone https://github.com/your-username/Tesla-Price-Forecasting
cd Tesla-Price-Forecasting

# Install dependencies
pip install -r requirements.txt

requirements.txt (example)

pandas

numpy

matplotlib

seaborn

statsmodels

yfinance

jupyter

▶️ Usage

Open the notebook:

jupyter notebook notebooks/Tesla_TimeSeries_Forecasting.ipynb


Run all cells to:

Load data

Fit ARIMA/SARIMA

Visualize forecasts

🤝 Contributing

Contributions are welcome!
Feel free to open issues or submit pull requests.

📄 License

This project is open-source under the MIT License.

👤 Author

Mohammadi Nilofer
📧 niloferm7@yahoo.com

🌐 GitHub: https://github.com/Mohammadi-Nilofer
