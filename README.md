# python_api_challenge
What's the Weather Like?

## Data Collection
This activity is broken down into two parts, WeatherPy and VacationPy.
-   WeatherPy: A Python script is created to collect the weather details of over 500 cities of varying distances from the equator, using citipy python library and OpenWeatherMap API.
-   VacationPy: The final csv cities.csv created at the end of the WeatherPy analysis is used as an input here.

### Python Scripts and Results
#### WeatherPy
1)  A Cities list is generated using random sets of latitude and longitude combinations, using the python library citipy.
2)  A weather check is performed on each city in the list using a series of successive OpenWeatherMap API calls.
3)  In order to API call rate restrictions, the API calls are made in sets of 50 cities with a break of 5 seconds between each set. Also the API calls are stopped after the data for 500 cities are collected.
4)  The weather data collected for the 500 cities are then held in the dataframe weather_data.
5)  This data is also stored in the csv file python_api_challenge\output_data\WeatherPy\cities.csv
6)  The following graphs are created for Cities, Northern and Southern Hemispheres and stored as png images in the folder python_api_challenge\output_data\WeatherPy\
-   Latitude Vs. Max Temp
-   Latitude Vs. Humidity
-   Latitude Vs. Cloudiness
-   Latitude Vs. Wind Speed

#### VacationPy
1)  