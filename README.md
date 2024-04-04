# Price Prediction using Prophet Time Series

A project done for the course Machine Learning under <a href="https://github.com/radhikachapaneri"><b>Dr. Radhika Chapaneri</b> 
<h3>Team members</h3>
<ul>
<li><b>MAHIKA SHAH I038</b> </li>
<li><b>NAMAN CHHAPARIA I040</b> Github: <a href="https://github.com/NamanChh">NamanChh</a></li>


</ul>

## ABSTRACT

Predictive maintenance is a technique used to predict when equipment or machinery is likely to fail so that maintenance can be performed just in time to prevent the failure from occurring. It utilizes machine learning and statistical modeling techniques to analyze data collected from sensors, equipment logs, historical maintenance records, and other sources to predict potential failures or breakdowns.

Model Used: <b>Random Forest Classifier</b>

## Dataset Overview
The dataset provided by the UCI repository is synthetic and mirrors real predictive maintenance scenarios encountered in industries. It comprises 10,000 data points stored as rows, each containing 14 features in columns.

## Features
1. **UID:** Unique identifier ranging from 1 to 10,000.
2. **Product ID:** Consists of a letter L, M, or H indicating low (60% of products), medium (30%), and high (10%) quality variants, along with a variant-specific serial number.
3. **Air Temperature [K]:** Generated using a random walk process and later normalized to a standard deviation of 2 K around 300 K.
4. **Process Temperature [K]:** Generated using a random walk process normalized to a standard deviation of 1 K, added to the air temperature plus 10 K.
5. **Rotational Speed [rpm]:** Calculated from a power of 2860 W, overlaid with normally distributed noise.
6. **Torque [Nm]:** Torque values are normally distributed around 40 Nm with a standard deviation of 10 Nm and no negative values.
7. **Tool Wear [min]:** Quality variants H/M/L add 5/3/2 minutes of tool wear to the used tool in the process.
8. **Machine Failure:** Label indicating whether the machine has failed in a particular data point for any of the following failure modes:
   - **Tool Wear Failure (TWF):** The tool will be replaced or fail at a randomly selected tool wear time between 200 - 240 mins.
   - **Heat Dissipation Failure (HDF):** A process failure occurs if the difference between air and process temperature is below 8.6 K and the tool's rotational speed is below 1380 rpm.
   - **Power Failure (PWF):** The product of torque and rotational speed (in rad/s) equals the power required for the process. If this power is below 3500 W or above 9000 W, the process fails.
   - **Overstrain Failure (OSF):** If the product of tool wear and torque exceeds 11,000 minNm for the L product variant (12,000 M, 13,000 H), the process fails due to overstrain.
   - **Random Failures (RNF):** Each process has a 0.1% chance to fail regardless of its parameters. If at least one of the above failure modes is true, the process fails, and the 'machine failure' label is set to 1.

## Accuracy
Here, we've used 3 training splits for our model. 0.2, 0.4 and 0.5 respectively. We noticed that we attained the maximum accuracy while using the <b>0.4 test train split</b>.

## Conclusion
In conclusion, predictive maintenance offers organizations a powerful tool for optimizing asset performance, minimizing downtime, and reducing maintenance costs. By harnessing the power of data analytics and machine learning, organizations can transition from reactive or scheduled maintenance practices to a proactive and data-driven approach, ultimately improving operational efficiency, asset reliability, and overall business performance.
