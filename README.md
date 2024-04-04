# Price Prediction using Prophet Time Series

A project done for the course Machine Learning under <a href="https://github.com/radhikachapaneri"><b>Dr. Radhika Chapaneri</b> 
<h3>Team members</h3>
<ul>
<li><b>MAHIKA SHAH I038</b> </li>
<li><b>NAMAN CHHAPARIA I040</b> Github: <a href="https://github.com/NamanChh">NamanChh</a></li>


</ul>

## ABSTRACT

The Avocado price forecasting project aims to predict future prices of avocados, which can have
various applications in the agricultural industry, retail sector, and food supply chain management.
Predicting avocado prices can assist farmers in planning their harvest and sales strategies, help
retailers in managing their inventory and pricing strategies, and enable consumers to make
informed purchasing decisions.

Model Used: <b>PROPHET TIME SERIES</b>

## Dataset Overview

Dataset Link: <a href="https://www.kaggle.com/datasets/neuromusic/avocado-prices"> Avocado Dataset</a></li>

The Dataset represents weekly 2018 retail scan data for National retail volume (units) and price. Retail scan data comes directly from retailers’ cash registers based on actual retail sales of Hass avocados.

## Features
Some relevant columns in the dataset:

- Date - The date of the observation
- AveragePrice - the average price of a single avocado
- type - conventional or organic
- year - the year
- Region - the city or region of the observation
- Total Volume - Total number of avocados sold
- 4046 - Total number of avocados with PLU 4046 sold
- 4225 - Total number of avocados with PLU 4225 sold
- 4770 - Total number of avocados with PLU 4770 sold

## Prophet - A way into the future!

Prophet is an additive model consisting of four components:

<img src="https://images.squarespace-cdn.com/content/v1/5bce4071ab1a620db382773e/1625500457398-BF8AHHUZWGKTLMN1RXOH/prophet_formula.png?format=2500w" alt="Prophet Equation" />


Let us discuss the meaning of each component:

- g(t): It represents the trend and the objective is to capture the general trend of the series. For example, the number of advertisements views on Facebook is likely to increase over time as more people join the network.

- s(t): It is the Seasonality component. The number of advertisement views might also depend on the season. For example, in the Northern hemisphere during the summer months, people are likely to spend more time outdoors and less time in from of their computers. Such seasonal fluctuations can be very different for different business time series. The second component is thus a function that models seasonal trends. 

- h(t): The Holidays component. We use the information for holidays which have a clear impact on most business time series. Note that holidays vary between years, countries, etc. and therefore the information needs to be explicitly provided to the model.

- εt:    The error term εt stands for random fluctuations that cannot be explained by the model. As usual, it is assumed that εt follows a normal distribution N (0, σ2) with zero mean and unknown variance σ that has to be derived from the data.

Prophet fits the model to the historical data using a Markov chain Monte Carlo (MCMC) algorithm or a gradient-based optimization algorithm. It estimates the parameters of the trend, seasonality, and holiday effects components by minimizing the sum of squared errors between the observed and predicted values.

Once the model is fitted to the historical data, Prophet can be used to generate forecasts for future time periods. It provides point forecasts as well as uncertainty intervals (e.g., confidence intervals) around the forecasts to quantify prediction uncertainty.


## Performance Evaluation

We’ve evaluated the performance of our Prophet model on MAPE metric. Mean absolute percentage error expresses accuracy as a percentage of the error. Because this number is a percentage, it can be easier to understand than the other statistics. For example, if the MAPE is 5, on average, the forecast is off by 5%.

In our model, when taking horizon = 365 days and period = 180 days, we obtained a MAPE score ranging from 0.1 to 0.3.

<img src="" alt="Residual Plot" />![download](https://github.com/NamanChh/PriceForecasting_Prophet_TimeSeries/assets/142370244/3aff9f80-6544-448b-8bf1-16d6a29c3489)


This graph shows our predicted values (yhat) vs the residual values. We can see that the values are centered around 0. This shows that our model has low residuals and it is performing well.

## Conclusion
In conclusion, the forecasting of avocado prices using the Prophet model offers numerous practical applications and benefits across various sectors. Through this project, we gained insights into the applications of time series forecasting, the effectiveness of machine learning models, and the challenges associated with real-world data analysis. Moving forward, further research and development in this field will continue to drive innovation and advancements in agricultural market analysis and many other domains and decision-making processes.
