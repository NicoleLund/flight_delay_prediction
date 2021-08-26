# flight_delay_prediction
UofA Data Analytics Bootcamp Final Group Project

**Team**:  
* Nicole Lund: <a href="https://www.linkedin.com/in/nicolelund-1/" target="_blank">https://www.linkedin.com/in/nicolelund-1/</a>
* Amber Royster: <a href="https://www.linkedin.com/in/amber-royster/" target="_blank">https://www.linkedin.com/in/amber-royster/</a>
* Anne Niemiec: <a href="https://www.linkedin.com/in/anne-niemiec/" target="_blank">https://www.linkedin.com/in/anne-niemiec/</a>
* Tarak Patel: <a href="https://www.linkedin.com/in/tarakpatel-1/" target="_blank">https://www.linkedin.com/in/tarakpatel-1/</a>

## Problem
Employees with frequent business travel experience time lost with family and productive work time while in transit. In order to minimize lost time, past flight history was examined and modeled to predict which flight routes experienced the smallest delay times.

## Resource and Scope Management
In order to manage project scope and operate within the constraints of the available tools, 2017 data was used to train and test machine learning models and the 2018 data was used to evaluate model predictions.  The data was further restricted to only model and predict flight disruptions for flights departing from Tucson International Airport (TUS).

## Model Development
Several machine learning models were deployed and tuned with the same input/output data.  Each model was scored on accuracy and precision.  The best model generated using a random forest classification algorithm.  The model was trained with 70% of the 2017 data on the following features:

**Input values (known by customer)**
* OP_CARRIER: airline designation code
* OP_CARRIER_FL_NUM: flight number
* day_of_week: flight day of the week calculated from FL_DATE
* DEST: destination airport code
* CRS_DEP_TIME: scheduled departure time 
* CRS_ARR_TIME: scheduled arrival time
* DISTANCE: flight distance

**Output values (of interest to the customer)**
* CANCELLED: flight canceled [0 = No, 1 = Yes]
* DIVERTED: flight diverted [0 = No, 1 = Yes]
* DELAY: flight ARR_DELAY greater than 30 minutes [0 = No, 1 = Yes]


## Webpage
https://nicolelund.github.io/flight_delay_prediction/

## Source Data
The Kaggle dataset provides flight performance data for each year between 2009 and 2018. The full data set requires 7.1 Gb of storage space. <a href="https://www.kaggle.com/yuanyuwendymu/airline-delay-and-cancellation-data-2009-2018" target="_blank">https://www.kaggle.com/yuanyuwendymu/airline-delay-and-cancellation-data-2009-2018</a>

airport_codes.csv provides a lookup table of airport codes to city name. <a href="https://www.transportation.gov/policy/aviation-policy/airport-codes-txt" target="_blank">https://www.transportation.gov/policy/aviation-policy/airport-codes-txt</a>