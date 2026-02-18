# Bitcoin (BTC-USD) Time Series Forecasting

A comprehensive time series analysis and forecasting project for Bitcoin price prediction using various machine learning and statistical models.

## 📊 Project Overview

This project explores time series forecasting techniques to predict Bitcoin prices using 5 years of historical BTC-USD data from Yahoo Finance. The analysis includes data preprocessing, seasonal decomposition, and evaluation of multiple forecasting models with different prediction horizons.

## 🚀 Features

- **Data Collection**: Automated fetching of 5 years of Bitcoin price data using Yahoo Finance API
- **Time Series Decomposition**: STL (Seasonal and Trend decomposition using Loess) analysis
- **Data Preprocessing**: Price averaging, normalization, and frequency adjustment
- **Multiple Forecasting Models**:
  - Naive Forecasters (Last Value & Mean strategies)
  - AutoETS (Exponential Smoothing State Space Model)
  - AutoARIMA (Autoregressive Integrated Moving Average)
- **Comprehensive Evaluation**: Multiple metrics and statistical tests
- **Visualization**: Detailed plots for trends, seasonality, residuals, and predictions

## 📈 Methodology

### Data Processing
1. **Price Calculation**: Average of daily high and low prices
2. **Normalization**: Min-max scaling to [0,1] range
3. **Frequency Adjustment**: Business day frequency alignment
4. **Train-Test Split**: 80-20 split for model validation

### Time Series Analysis
- **Seasonal Period**: 30 days (monthly cycles)
- **STL Decomposition**: Separation of trend, seasonal, and residual components
- **Stationarity Testing**: Anderson-Darling and Ljung-Box tests

### Models Implemented

#### 1. Naive Forecasting
- **Last Value Strategy**: Uses the most recent value for prediction
- **Mean Strategy**: Uses the average of historical values

#### 2. AutoETS (Exponential Smoothing)
- **Configuration**: Additive trend and seasonal components with damping
- **Seasonal Period**: 30 days
- **Variance Prediction**: Confidence intervals for forecasts

#### 3. AutoARIMA
- **Auto-tuning**: Automatic parameter selection
- **Seasonal Component**: 30-day seasonality
- **Statistical Foundation**: Box-Jenkins methodology

### Evaluation Metrics
- **MAE** (Mean Absolute Error)
- **MAPE** (Mean Absolute Percentage Error) 
- **MASE** (Mean Absolute Scaled Error)
- **RMSE** (Root Mean Squared Error)

### Prediction Horizons
- Short-term: 1-3 days
- Medium-term: 10 days
- Long-term: 30 days

## 🛠️ Technologies Used

- **Python 3.x**
- **Data Manipulation**: `pandas`, `numpy`
- **Financial Data**: `yfinance`, `pandas-datareader`
- **Machine Learning**: `scikit-learn`, `tensorflow`
- **Time Series**: `sktime`, `statsmodels`
- **Visualization**: `matplotlib`, `plotly`
- **Statistical Testing**: `scipy`

## 📋 Prerequisites

```bash
pip install pandas numpy matplotlib tensorflow scikit-learn
pip install yfinance pandas-datareader sktime statsmodels scipy
pip install plotly
```

## 🔍 Key Findings

The notebook demonstrates a systematic approach to time series forecasting with:
- Detailed seasonal decomposition revealing Bitcoin's cyclical patterns
- Comparative analysis of statistical vs. machine learning approaches
- Residual analysis for model validation
- Multiple forecasting horizons for different use cases

## 📁 Project Structure

```
BTC-USD-prediction/
├── main.ipynb          # Main analysis notebook
├── README.md           # Project documentation
```

## 🚀 Getting Started

1. Clone the repository
2. Install the required dependencies
3. Open `main.ipynb` in Jupyter Notebook or VS Code
4. Run the cells sequentially to reproduce the analysis

## 📊 Results Visualization

The project includes comprehensive visualizations:
- Time series decomposition plots
- Model prediction comparisons
- Residual analysis histograms
- Forecast vs. actual value comparisons

## 🎯 Future Enhancements

- Integration of additional technical indicators
- Ensemble methods combining multiple models
- Real-time prediction pipeline
- External factors incorporation (news sentiment, market indicators)
- Deep learning models (LSTM, GRU)

## ⚠️ Disclaimer

This project is for educational and research purposes only. Cryptocurrency investments carry high risk and predictions should not be used for actual trading decisions.

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

*First attempt to dive deeper into understanding time-series in ML.*
