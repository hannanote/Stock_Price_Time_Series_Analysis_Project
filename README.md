## Stock Price Time Series Analysis

### Project Overview

The stock market is a complex system influenced by various factors such as politics, monetary policy, fiscal policy, industry conditions, the global economy, and financial crises, which greatly impact the economic decisions made by investors. However, predicting its volatility is quite difficult, and uncertainty always exists. To address this challenge and help investors make better decisions, I wanted to research stock price prediction. Analyzing stock market data and developing predictive models can provide significant value by helping to create better investment strategies and understand market trends.

In this project, I focused on time series analysis of stock prices and developing forecasting models, applying various techniques to improve prediction accuracy. Specifically, I chose **Apple** and **Chevron** for this analysis because these two companies represent key players in different industries. Apple plays a leading role in the technology sector, continually releasing innovative products such as smartphones and wearable devices. Apple's stock is greatly influenced by various factors related to technological innovation, and predicting and analyzing these changes is crucial in the stock market.

On the other hand, Chevron is a major player in the energy sector, operating in the oil and gas industry, and is closely tied to international political and economic factors. Chevron's stock is significantly affected by commodity prices, environmental regulations, and global demand, making the analysis and prediction of these energy sector fluctuations highly valuable for investors.

By analyzing both Apple and Chevron, I aimed to compare and examine the different factors affecting stock prices in diverse industries. These two companies have a significant impact on the market, making them excellent case studies for gaining deeper insights into stock market analysis.

주식 시장은 정치, 통화 정책, 재정 정책, 산업 상태, 세계 경제 및 금융 위기 등 다양한 요인에 의해 영향을 받는 복잡한 시스템으로, 투자자들에게 중요한 경제적 결정을 내리는 데 큰 영향을 미칩니다. 그러나 그 변동성을 예측하는 것은 매우 어렵고, 불확실성은 항상 존재합니다. 이러한 문제를 해결하고, 투자자들이 더 나은 결정을 내릴 수 있도록 돕기 위해 주식 가격 예측을 연구하고자 했습니다. 주식 시장의 데이터를 분석하여 예측 모델을 개발하는 것은 더 나은 투자 전략을 수립하고, 주식 시장의 동향을 이해하는 데 중요한 가치를 제공할 수 있기 때문입니다.

이 프로젝트에서는 주식 가격 시계열 분석과 예측 모델 개발에 주력하고, 예측 정확도를 높이기 위한 다양한 기법을 적용하고자 했습니다. 특히, 애플(Apple)과 셰브론(Chevron) 두 기업을 선택한 이유는 이들이 각각 다른 산업을 대표하는 중요한 기업들이기 때문입니다. 애플은 기술 산업에서 선두적인 역할을 하며, 스마트폰과 웨어러블 디바이스 등 혁신적인 제품을 지속적으로 출시하고 있습니다. 애플의 주가는 기술 혁신과 관련된 여러 요인에 큰 영향을 받기 때문에, 이러한 변화를 예측하고 분석하는 것은 주식 시장에서 매우 중요한 의미를 지닙니다.

반면, 셰브론은 에너지 산업의 주요 기업으로, 원유와 가스 관련 사업을 운영하며 국제적인 정치 및 경제적 요소와 밀접하게 연결되어 있습니다. 셰브론은 원자재 가격, 환경 규제, 글로벌 수요 등에 따라 큰 영향을 받으며, 이러한 에너지 산업의 변동성을 분석하고 예측하는 작업은 투자자들에게 중요한 가치를 제공합니다.

따라서, 애플과 셰브론을 분석함으로써 서로 다른 산업에서 주식 가격에 영향을 미치는 다양한 요인들을 비교하고 분석하고자 했습니다. 이 두 기업은 각각 매우 큰 시장 영향력을 가지고 있어, 주식 시장 분석에 대한 깊은 통찰을 얻을 수 있는 좋은 사례가 됩니다.

+ Stock daily price from Yahoo’s finance website
+ Apple stock from Jan 2007 to May 2023
+ Chevron stock from Jan 1962 to May 2023
+ Conducting Time Series Analysis on stock price data


##### A forecasting algorithm is an information process that seeks to predict future values based on pase and present data.


-----------
### Apple
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



-----------
### Chevron
![image](https://github.com/user-attachments/assets/879015d0-2407-4451-87f4-96bb01e2f16e)

The slow decay of the auto correlation on the ACF, the auto correlation of one at lag 1 on the PACF and the first row filled with xs on the EACF, as well as the ADF test failing to reject the null hypothesis of unit root and the KPSS test rejecting the null hypothesis of stationarity all indicate the series is a random walk



![image](https://github.com/user-attachments/assets/27264009-28e1-4698-a58e-abad786e67f3)

The model built has very significant coefficients, with very low RMSFE and MAPE, at .22 and 3.5%, respectively, as well as incredibly low AIC and BIC values. The performance of the model can be visually analyzed on the chart on the left, where the blue line represents the predictions produced and the red line represents the true values for the period.



![image](https://github.com/user-attachments/assets/1a4290ad-e85a-46d4-82ef-3039596dad54)

The forecast from the integrated model performed pretty well, with an MSE of .0003 and a MAE of .012.


