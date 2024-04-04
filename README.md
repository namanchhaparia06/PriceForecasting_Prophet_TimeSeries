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

## Accuracy
Here, we've used 3 training splits for our model. 0.2, 0.4 and 0.5 respectively. We noticed that we attained the maximum accuracy while using the <b>0.4 test train split</b>.

## Conclusion
In conclusion, predictive maintenance offers organizations a powerful tool for optimizing asset performance, minimizing downtime, and reducing maintenance costs. By harnessing the power of data analytics and machine learning, organizations can transition from reactive or scheduled maintenance practices to a proactive and data-driven approach, ultimately improving operational efficiency, asset reliability, and overall business performance.
