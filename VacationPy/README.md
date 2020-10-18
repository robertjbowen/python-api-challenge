# VacationPy: 

#This requires a complete edit
***

This project was to create a random list of 500+ cities from across the globe and conduct an API data call to gather current weather data for those cities. Then clean and analyze the weather data to generate a series of scatter plots and regression models in order to make data based observations about global weather patterns.


### Documents in this repository are:


* VacationPy.ipynb - My Jupyter Notebook file running a Python 3 kernel that contains all of the code for conducting the data analysis 

* output_data directory - contains the output weather data file - cities.csv

* api_keys.py - python file for holding user api key for openweathermap.org - link for generating an api ***https://openweathermap.org/api

* images directory - contains images of the output scatter plots

* Checkpoints directory - contains checkpoint .ipynb files

* _pycache_ directory - holds api_key encrytion



### Design concept:

1) The project begins with generating 1500 random latitude and longitude values and using citypy to determine the nearest cities to those coordinates and appending them to a list (duplicate cities are skipped).

2) The program then creates a series of successive API calls to openweathermap.org to collect the weather data for each of the cities into a list (weather_data) - (if a city is not found or is missing key weather data values, it is skipped)

3) The list of weather data is read into a dataframe (city_data) and output to cities.csv in the output_data directory

4) Summary data is calculated for the DataFrame and any cities with a humidity above 100% are identified and deleted as a new DataFrame is created (clean_city_data).

5) The clean_city_data is plotted into a series of scatter plots of weather variables vs. latitude and analyzed 

***
### Scatter Plots:


![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/images/Picture1.png)

####This plot shows Max Temperature is lower at the planets poles and increases as you approach the equator.


![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/images/Picture2.png)

####Humidity can vary widely but is relatively high for most cities across the entire planet
 

![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/images/Picture3.png)

####Cloudiness can vary widely across the entire planet, but tends to the extremes of no clouds to heavy overcast with relatively few in the middle


![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/images/Picture4.png)

####Wind speed is relatively low across the planet but increases as you approach the higher lattitudes


6) The final step in the project is to conduct linear regression analysis of the same data as above but split to look at the Northern and Southern Hemispheres independently of each other

***
### Linear Regression:

![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/images/Picture5.png)

![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/images/Picture6.png)

####This plot shows Max Temperature is lower at the planets poles and increases as you approach the equator.


![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/images/Picture7.png)

![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/images/Picture8.png)

####Humidity can vary widely but is relatively high for most cities across the entire planet


![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/images/Picture9.png)

![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/images/Picture10.png)

####Cloudiness can vary widely across the entire planet, but tends to the extremes of no clouds to heavy overcast with relatively few in the middle



![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/images/Picture11.png)

![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/images/Picture12.png)

####Wind speed is relatively low across the planet but increases as you approach the higher lattitudes