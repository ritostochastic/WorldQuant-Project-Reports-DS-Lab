# Project 8: Financial Volatility Modeling and End-to-End Deployment

An applied quantitative finance project combining financial time series analysis, conditional volatility modeling, database integration, and API development.

## Project Overview

Financial returns often exhibit volatility clustering and heavy-tailed distributions. These properties make volatility modeling an important part of financial risk analysis.

This project investigates financial return behavior, estimates conditional volatility using ARCH-family models, evaluates out-of-sample forecasts, and develops an API-based deployment prototype backed by an SQLite database.

## Workflow

### 1. Financial Data Preparation
- Prepared daily asset price histories.
- Calculated logarithmic returns:

  r_t = ln(P_t / P_(t-1))

- Examined the statistical properties of the resulting return series.

### 2. Stationarity and Distributional Analysis
- Tested price levels and log returns using the Augmented Dickey-Fuller (ADF) test.
- Investigated volatility clustering and distributional characteristics.

Reported results:

| Series | ADF Statistic | p-value |
|---|---:|---:|
| Price levels | -1.120 | 0.707 |
| Log returns | -14.82 | < 0.001 |

The return series had a reported mean of 0.00042, standard deviation of 0.01850, skewness of -0.245, and kurtosis of 5.840.

### 3. Conditional Volatility Modeling
- Compared ARCH(1), ARCH(5), and GARCH(1,1) specifications.
- Evaluated Gaussian and Student's t error distributions.
- Examined model persistence and residual diagnostics.

The GARCH(1,1) model with Student's t errors achieved the best reported information criteria:

- AIC: -6,674.30
- BIC: -6,646.30
- Volatility persistence (alpha + beta): 0.9742

The Ljung-Box test on squared standardized residuals returned a p-value of 0.428.

### 4. Out-of-Sample Forecast Evaluation
- Conducted rolling forecasts over a 252-trading-day out-of-sample period.
- Evaluated forecasts across multiple horizons using MAE, RMSE, and QLIKE.

| Forecast Horizon | MAE | RMSE | QLIKE |
|---|---:|---:|---:|
| 1 day | 0.00214 | 0.00342 | -4.892 |
| 5 days | 0.00385 | 0.00511 | -4.410 |
| 10 days | 0.00520 | 0.00719 | -3.985 |

### 5. Database and API Integration
- Used SQLite to persist asset price and volatility forecast data.
- Implemented database tables named `asset_prices` and `volatility_forecasts`.
- Developed a FastAPI service exposing the following endpoints:

  - `GET /health`
  - `GET /fit`
  - `POST /predict`
  - `GET /history`

## Key Takeaways

- Financial return series can exhibit heavy tails and volatility clustering.
- GARCH models provide a framework for estimating time-varying conditional volatility.
- Student's t innovations can better accommodate heavy-tailed return distributions than a Gaussian specification in the reported comparison.
- Combining statistical modeling, database persistence, and API development demonstrates an end-to-end quantitative modeling workflow.

## Technologies

- Python
- pandas
- NumPy
- arch
- SQLite
- FastAPI
- Uvicorn
