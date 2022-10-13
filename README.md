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

3)  In order to limit API call rate, the API calls are made in sets of 50 cities with a break of 5 seconds between each set. Also the API calls are stopped after the data for 500 cities are collected.

4)  The weather data collected for the 500 cities are then held in the dataframe weather_data.

5)  This data is also stored in the csv file python_api_challenge\output_data\WeatherPy\cities.csv

6)  The following graphs are created for Cities, Northern and Southern Hemispheres and stored as png images in the folder python_api_challenge\output_data\WeatherPy\
-   Latitude Vs. Max Temp
-   Latitude Vs. Humidity
-   Latitude Vs. Cloudiness
-   Latitude Vs. Wind Speed

7)  The analysis of the plots above can be found in the Jupyter notebook as required.

8)  The Jupyter notebook also contains the observable trends explained at the bottom.

#### VacationPy

1)  The csv file (cities.csv) from WeatherPy is the input for VacationPy.

2)  The dataframe cities_weather is created by reading the data from cities.csv file. This dataframe is then used for all analysis.

3)  Humidity Heatmap: The latitudes and longitudes of the 500+ cities in the cities_weather dataframe are used as locations and Humidity as the weight to plot this heatmap.

4)  The dataframe cities_weather is then narrowed down to find the ideal weather condition for a vacation. The conditions used are 
-   The max temperature lower than 80 but higher than 70F
-   Wind Speed less than 10mph
-   Zero cloudiness

5) The cities filtered above are stored in the dataframe hotel_df.

6) This dataframe is then updated to store the hotel names. The Google Places APIis used to find the first hotel located within 5,000 meters of the coordinates of each city.

7)  These hotels are then plotted on the Humidity Heatmap created earlier with clickable pins displaying City, Country and Hotel Name.

8) the images of the heatmaps can be found in python_api_challenge\output_data\VacationPy\Heatmap_humidity.png and python_api_challenge\output_data\VacationPy\Heatmap_humidity_hotels.png.

### Files Submitted

#### WeatherPy

1)  Jupyter Notebook - python_api_challenge\WeatherPy.ipynb

2)  Output csv file - python_api_challenge\output_data\WeatherPy\cities.csv

3)  12 png images of the scatter plots in python_api_challenge\output_data\WeatherPy\

#### VacationPy

1)  Jupyter Notebook - python_api_challenge\VacationPy.ipynb

2)  Humidity Heatmap - python_api_challenge\output_data\VacationPy\Heatmap_humidity.png

3)  Humidity Heatmap with hotel pins - python_api_challenge\output_data\VacationPy\Heatmap_humidity_hotels.png