# VacationPy: 

This project was to import a list of 500+ cities from across the globe create a map and display their humidity levels in a heat map layer on top of the map. Then filter the data set to pick 10 to 15 cities with ideal weather conditions  for taking a vacation there and conducting an API data call to gather hotel data for those cities. The final step is to generate a marker layer to display the hotel information for the selected cities and overlay it on the same map. Challenges in this project involved generating and maintining API keys, conducting efficient API calls and formatting and filtering data for refined searches and clean display. 


### Documents in this repository are:


* VacationPy.ipynb - My Jupyter Notebook file running a Python 3 kernel that contains all of the code for conducting the data analysis 

* output_data directory - contains a copy of the output weather data file created by WeatherPy.ipynb - cities.csv

* api_keys.py - python file for holding user api key for https://console.cloud.google.com/ 

* images directory - contains images of the output scatter plots

* Checkpoints directory - contains checkpoint .ipynb files

* _pycache_ directory - holds api_key encrytion



### Design concept:

1) The project begins with importing the DataFrame of weather for 500+ random worldwide cities cities.csv created by WeatherPy. This is accomplished by using a read_csv() command.

![alt tag](https://github.com/robertjbowen/python-api-challenge/blob/main/VacationPy/images/Picture1.png)

2) The program then configures gmaps to display a 600 pixel by 500 pixel hybrid google world map. It then used the latitude and longitude positional data to generate a heat map layer of the humidity values for each city and overlays it onto the map. The heat map display humidity values in a green (low value) to red (high value) color scale.  

3) A new DataFrame is created (vac_cities) and is filtered by max temperature, humidity and cloudiness to find a few cities (10-15) with the ideal weather conditions for vacationing there. 

4) The program then conducts an API call for each of the vacation cities to find a hotel within a radius of 5000 meters from the city latitude and longitude positional data. A column holding the names of the hotels is appended to the vac_cities DataFrame.

5) A information box is formatted to display the hotel information along with city and country names and then again uses the latitude and longitude positional data to generate a marker layer and overlays it on the map created earlier. The marker layer allows you to select the individual markers and displays the information box with that particular hotel's information.
