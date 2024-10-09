## Stock Price Time Series Analysis
The stock market is influenced by various factors such as politics, monetary and fiscal policy, industry conditions, the world economy, and financial crises. It has experienced significant fluctuations over the years, including the 2008 financial crisis, the rise of tech stocks due to innovations like Apple's smartphones, and the extreme volatility caused by the 2020 pandemic. Unlike the bond market, stocks carry higher uncertainty as future returns are not guaranteed. However, the higher risks are associated with the potential for higher returns. Therefore, understanding the risk-return tradeoff and analyzing company management strategies are crucial for investors in making investment decisions. In this project, we focused on analyzing stock price movements through a statistical modeling approach known as technical analysis.

+ Stock daily price from Yahoo’s finance website
+ Apple stock from Jan 2007 to May 2023
+ Chevron stock from Jan 1962 to May 2023
+ Conducting Time Series Analysis on stock price data


##### A forecasting algorithm is an information process that seeks to predict future values based on pase and present data.

#### Apple

![image](https://github.com/user-attachments/assets/12bbc872-3457-443a-873f-db08fe37c2f2)

By differencing the series we can see that it becomes stationary, and the T test rejects the null
hypothesis of constant mean throughout the series, indicating a random walk with a drift.
After differencing it, ACF, PACF and EACF as well as ADF and KPSS tests all corroborated a
stationary behavior. ACF of the differenced series indicates an MA behavior and the significant
auto correlation at lag 2 indicates it might be of second order. The PACF shows more clearly
some significant auto correlation at lags 2 and 3, aside from other ones at much higher orders.
EACF indicates many possible models, and of the many tried, the one with the best performance
and most conforming residuals was an ARIMA(2, 1, 2) with drift.

![image](https://github.com/user-attachments/assets/4ef48840-668b-45af-bd1c-58e9d293e095)

The model chosen has very significant coefficients, with very low RMSFE and MAPE, at 0.22 and 3.5%, respectively, as
well as incredibly low AIC and BIC values, at -76244.66 and -76199.42. The performance of the model can be visually analyzed on the chart on the left, where the blue line represents the predictions produced and the red line represents the true values for the period.


![image](https://github.com/user-attachments/assets/9b53c688-77d7-44d1-a47c-40c5fb5525c8)

The forecasts from the ARMA(2, 2) GARCH(1, 1) model can be seen below, with really low
MSE and MAE. The integrated model has equal contributions from auto regressive and moving
average processes, seeing that AR 1 and 2, MA 1 and 2, Alpha 1 and Beta 1 are all very
significant.


#### Chevron

![image](https://github.com/user-attachments/assets/879015d0-2407-4451-87f4-96bb01e2f16e)

The slow decay of the auto correlation on the ACF, the auto correlation of one at lag 1 on the PACF and the first row filled with xs on the EACF, as well as the ADF test failing to reject the null hypothesis of unit root and the KPSS test rejecting the null hypothesis of stationarity all indicate the series is a random walk



![image](https://github.com/user-attachments/assets/27264009-28e1-4698-a58e-abad786e67f3)

The model built has very significant coefficients, with very low RMSFE and MAPE, at .22 and 3.5%, respectively, as well as incredibly low AIC and BIC values. The performance of the model can be visually analyzed on the chart on the left, where the blue line represents the predictions produced and the red line represents the true values for the period.



![image](https://github.com/user-attachments/assets/1a4290ad-e85a-46d4-82ef-3039596dad54)

The forecast from the integrated model performed pretty well, with an MSE of .0003 and a MAE of .012.


