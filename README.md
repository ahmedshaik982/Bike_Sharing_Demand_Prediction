# Bike_Sharing_Demand_Prediction

Currently, Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.

The main objective behind this project is to explore and analyze the data to discover the key understandings. And to predict the count of bikes required at each hour by using regression models

## Dataset
Download the dataset for this project from following Link
https://github.com/ahmedshaik982/Bike_Sharing_Demand_Prediction/blob/main/SeoulBikeData.csv

## Data Analysis
The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information.
* Attribute Information:
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

## Work Flow
![image](https://user-images.githubusercontent.com/117965293/209428187-c3c4c916-63c6-4a44-9a99-d4f90e1a6464.png)

## Tools used
* Google colab notebook
* Pandas library
* Numpy
* Matplotlib and Seaborn for data visualization
* Scikit Learn for implementing Machine Learning Models.

## Some Visualizations
![image](https://user-images.githubusercontent.com/117965293/209428523-b1c8cec5-79e0-43eb-912e-a61ca0203a40.png)


## Conclusions
From Exploratory Data Analysis, we can conclude that,

* Most Number of bike rented count ranges from 0 to 500.

* Temperature mostly varies from 20 to 30.

* Humidity mostly varies from 20 to 100.

* Wind speed mostly varies from 2 to 4 m/s.

* Visibility of 2000 count is high.

* Solar Radiation is mostly 0. And a few are in range of 1 to 4.

* Mostly there is no rainfall and snowfall. And a very few have rainfall and snowfall.

* The distribution between numerical features and dependent feature (Rented Bike Count) has been spread out entire area which means there is no specific relation between them.

* Most number of bikes are rented in the hour of 18 followed by 19th hour. And the least is 4th hour

* In summer season, most number of bikes are rented and the least is winter season.

* In working days(No Holiday), most number of bikes are rented.

* Thursday has high count of rented bike.

* In a functioning day, most number of bikes are rented.

* Multicollinearity exits between two features namely Temperature and Dew Point Temperature. And we can remove Dew Point Temperature because,

* Temperature is 54% correlated with dependent feature, Dew Point Temperature is 38% correlated with dependent feature.

After fitting the data into various regression models, we can conclude that

* Tree based models performs well than linear models beacuse, the independent features are not linearly related to the dependent feature ('Rented Bike Count').


For Linear Models (Linear Regression, Lasso Regression, Ridge Regression), 'Temperature' has more importance and least is 'Hour 7'.

For Decision Tree Regressor, 'Functioning Day_Yes' has more importance and the least is 'Functioning Day_No'

For Random Forest Regressor, 'Functioning Day_Yes' has more importance and the least is 'Hour_14'

For Gradient Boosting Regressor, 'Functioning Day_Yes' and has more importance and the least is 'Hour_16'

For XGBoost Regressor, 'Functioning Day_No' has more importance and the least is 'Hour_16'

From the above all observations, we can see the optimal model is XGboost regressor and Gradient boosting regressor because those only have required score(no overfitting and no underfitting).
