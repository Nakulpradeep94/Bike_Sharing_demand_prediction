# Bike_Sharing_demand_prediction

## Problem Description
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

## Data Description
The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information.
Attribute Information:
* Date : year-month-day
* Rented Bike count - Count of bikes rented at each hour
* Hour - Hour of he day
* Temperature-Temperature in Celsius
* Humidity - %
* Windspeed - m/s
* Visibility - 10m
* Dew point temperature - Celsius
* Solar radiation - MJ/m2
* Rainfall - mm
* Snowfall - cm
* Seasons - Winter, Spring, Summer, Autumn
* Holiday - Holiday/No holiday
* Functional Day - Non Functional Days and Functional Days

## EDA (Basic)

* 8760 rows and 14 columns
* No null values or duplicates
* Date, Hour , Seasons, Functioning Day and Holiday are the categorical
* The dataset has weather information for every hour from 1st December 2017 to 30th November 2018.
* Maximum number of Bikes were rented on the Date: 13th June 2018 and the total number of bikes rented on that day is 36149.
* There where 12 days where there was zero rented bikes and on data analysis we found that all these where non functioning days.
* Day, month , year and weekday extracted from date column and made new columns out of it.


## Observations from EDA (Insights)
* There's a high correlation between the dependent variables and temperature.
* Temperature, Wind Speed, Solar Radiation, Visibility are positively correlated with the target variable.
* Bike rental demand is less on holidays. This indicates that people prefer to use these bikes as mode of transportation to work.
* In general people used rented bikes more during evening.
* Weekdays are the ones where the demand of the bikes is comparatively high as compared with the weekends.
* Summer season was the most preferred season throughout the year where the count was very high.
* People use bikes more when there is no rainfall or snowfall. People in general use bikes less when humidity is very high.

## Preprocessing
* Dew point temperature is highly correlated with temperature and on checking VIF multicollinearity is confirmed and the feature is dropped.
* Categorical features are nominal so one hot encoding is done on them.
* Except tree algorithms ,other models are transformed to accommodate the assumptions and since independent variables are having outliers and are not normally    distributed , we use yeo- Johnson power transformation before fitting it to the said models.
* Square root transformation is done for the dependent variable for non tree based algorithm like Linear and polynomial regression to satisfy their assumption before training them.

## CONCLUSION
* CATBOOST algorithm delivers the best model that can be used for bike sharing demand prediction since it has an r2 score of 0.929 and adjusted r2 score of 0.926.
* It has lower mse and rmse value compared to other models.
* Most importance features of this CatBoost model are Temperature, Humidity and Functioning day.
