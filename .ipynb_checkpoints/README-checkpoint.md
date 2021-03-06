# Time Series Analysis on Japanese Yen

![Yen Photo](Images/unit-10-readme-photo.png)

## Introduction

I have tested many time-series tools that you have learned in order to predict future movements in the value of the Japanese yen versus the U.S. dollar.

## Time-Series Forecasting

I start by loading historical Dollar-Yen exchange rate futures data and apply time series analysis and modeling to determine whether there is any predictable behavior.

Steps:

1. Decomposition using a Hodrick-Prescott Filter (Decompose the Settle price into trend and noise).
2. Forecasting Returns using an ARMA Model.
3. Forecasting the Settle Price using an ARIMA Model.
4. Forecasting Volatility with GARCH.

Used the results of the time series analysis and modeling to answer the following questions:

1. Based on your time series analysis, would you buy the yen now?
2. Is the risk of the yen expected to increase or decrease?
3. Based on the model evaluation, would you feel confident in using these models for trading?

Answer: Both ARMA and ARIMA have coffecients that are statistically insignificant therefore, those models cannot be used to predict the forecast of yen. GARCH has coffecients that are significant except the alpha[2] coffecient. Since the volatility is almost constant and the forecast shows it constant increases over time, the risk is expected to increase constantly and I would buy the yen now. 


#### Linear Regression Forecasting

Built a Scikit-Learn linear regression model to predict Yen futures ("settle") returns with *lagged* Yen futures returns and categorical calendar seasonal effects (e.g., day-of-week or week-of-year seasonal effects).

Steps:

1. Data Preparation (Creating Returns and Lagged Returns and splitting the data into training and testing data)
2. Fitting a Linear Regression Model.
3. Making predictions using the testing data.
4. Out-of-sample performance.
5. In-sample performance.

Used the results of the linear regression analysis and modeling to answer the following question:

* Does this model perform better or worse on out-of-sample data compared to in-sample data?
Answer: The out-of-sample RMSE is lower than the in-sample RMSE. RMSE is typically lower for training data, but is higher in this case.