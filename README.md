## Stock Price Time Series Analysis
The stock market is influenced by various factors such as politics, monetary and fiscal policy, industry conditions, the world economy, and financial crises. It has experienced significant fluctuations over the years, including the 2008 financial crisis, the rise of tech stocks due to innovations like Apple's smartphones, and the extreme volatility caused by the 2020 pandemic. Unlike the bond market, stocks carry higher uncertainty as future returns are not guaranteed. However, the higher risks are associated with the potential for higher returns. Therefore, understanding the risk-return tradeoff and analyzing company management strategies are crucial for investors in making investment decisions. In this project, we focused on analyzing stock price movements through a statistical modeling approach known as technical analysis.

+ Stock daily price from Yahoo’s finance website
+ Apple stock from Jan 2007 to May 2023
+ Chevron stock from Jan 1962 to May 2023
+ Conducting Time Series Analysis on stock price data


##### A forecasting algorithm is an information process that seeks to predict future values based on pase and present data.

#### Apple

![image](https://github.com/user-attachments/assets/12bbc872-3457-443a-873f-db08fe37c2f2)

![image](https://github.com/user-attachments/assets/4ef48840-668b-45af-bd1c-58e9d293e095)

![image](https://github.com/user-attachments/assets/9b53c688-77d7-44d1-a47c-40c5fb5525c8)

#### Chevron

![image](https://github.com/user-attachments/assets/879015d0-2407-4451-87f4-96bb01e2f16e)

The slow decay of the auto correlation on the ACF, the auto correlation of one at lag 1 on the PACF and the first row filled with xs on the EACF, as well as the ADF test failing to reject the null hypothesis of unit root and the KPSS test rejecting the null hypothesis of stationarity all indicate the series is a random walk



![image](https://github.com/user-attachments/assets/27264009-28e1-4698-a58e-abad786e67f3)

The model built has very significant coefficients, with very low RMSFE and MAPE, at .22 and 3.5%, respectively, as well as incredibly low AIC and BIC values. The performance of the model can be visually analyzed on the chart on the left, where the blue line represents the predictions produced and the red line represents the true values for the period.



![image](https://github.com/user-attachments/assets/1a4290ad-e85a-46d4-82ef-3039596dad54)
