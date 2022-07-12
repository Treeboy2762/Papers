문제 1.

백테스팅이 가능한가? 다 일일이 훈련시켜야 하는 것 아닌가?

# Title

Stock Portfolio Optimization Using a Deep Learning LSTM Model

Nine portfolios based on historical prices of 2016-2020

- pharmaceuticals
- infrastructure
- realty
- media
- public sector banks
- private sector banks
- large-cap
- mid-cap
- small-cap.

## Data Processing

Gathered with yfinance

- Return: daily and log-scaled
- Volatility: daily and yearly (daily * 250)
- Covariance and Correlation 

## Portfolio optimization

Minimum risk = minimum variance, where variance within a portfolio consists of 5 terms for weighted sum of std and 10 terms for covariances

