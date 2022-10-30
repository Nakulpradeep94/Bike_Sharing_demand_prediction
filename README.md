# Bike_Sharing_demand_prediction
# Problem Description
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.
# Data Description
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
* Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours)

# Observations from EDA
* There's a high correlation between the dependent variables and temperature.
* Temperature, Wind Speed, Solar Radiation, Visibility are positively correlated with the target variable.
* In general people used rented bikes more during evening.
* Weekdays are the ones where the demand of the bikes is comparatively high as compared with the weekends.
* Summer season was the most preferred season throughout the year where the count was very high.
* People use bikes more when there is no rainfall or snowfall. People in general use bikes less when humidity is very high
# CONCLUSION
* CATBOOST algorithm delivers the best model that can be used for bike sharing demand prediction since it has an r2 score of 0.929 and adjusted r2 score of 0.926.

* It has lower mse and rmse value compared to other models.

* Most importance features of this CatBoost model are Temperature, Humidity and Functioning day.
