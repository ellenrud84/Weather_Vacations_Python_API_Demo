# What's the Weather Like? Python API Demo

## Background
Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. Part I of this demo combines Python requests, APIs, and JSON traversals to quantitatevly demonstrate how weather changes as we approach the equator. Part II of this demo uses the Google Maps API and the data from Part I to assess ideal vacation spots based on user preferences.

## Part I - WeatherPy:
This example, is a Python script to visualize the weather of hundreds of cities across the world of varying distance from the equator. A simple Python library, the OpenWeatherMap API, was used to create a representative model of weather across world cities.

## Results:
TODO Add charts, tables, explanations and conclusions.

### Methods:
Within the jupyther notebook hundreds unique (non-repeating), cities are randomly selected based on latitude and longitude.
A weather check on each of the cities is performed using a series of successive API calls.
A print log of each city is creted as it's being processed with the city number and city name.
A CSV file of all retrieved data and a PNG image for each scatter plot is saved as an output of the jupyter notebook.

The following charts are created:

1. A series of scatter plots was created to showcase the following relationships:
  * Temperature (F) vs. Latitude
  * Humidity (%) vs. Latitude
  * Cloudiness (%) vs. Latitude
  * Wind Speed (mph) vs. Latitude

Each plot contains and explanatory statement.

2. The dataset was grouped into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude) and Linear regression was determined for each relationship as follows:
  * Northern Hemisphere - Temperature (F) vs. Latitude
  * Southern Hemisphere - Temperature (F) vs. Latitude
  * Northern Hemisphere - Humidity (%) vs. Latitude
  * Southern Hemisphere - Humidity (%) vs. Latitude
  * Northern Hemisphere - Cloudiness (%) vs. Latitude
  * Southern Hemisphere - Cloudiness (%) vs. Latitude
  * Northern Hemisphere - Wind Speed (mph) vs. Latitude
  * Southern Hemisphere - Wind Speed (mph) vs. Latitude

Each pair of plots has a statement explaining what the linear regression is modeling, and noted relationships.

## Part II - VacationPy:
This demo uses my skills in working with weather data to plan future vacations. I used jupyter-gmaps and the Google Places API to create the demo.

## Results:
TODO Add charts, tables, explanations and conclusions.

## Methods:
The jupyter notebook script performs the following:
1. Creates a heat map that displays the humidity for every city from the part I of the homework.

2. Narrow down the DataFrame to find your ideal weather condition. 
  For example:
    A max temperature lower than 80 degrees but higher than 70.
    Wind speed less than 10 mph.
    Zero cloudiness.
    
3. All rows of data that do not contain all three requirements are dropped from the dataframe, so that only locations are left

4. The Google Places API is used to find the first hotel for each city located within 5000 meters of each of the coordinate pairs from step 3.

5. Hotels are plotted on top of the humidity heatmap, each with a pin containing the Hotel Name,


Copyright
Trilogy Education Services © 2019. All Rights Reserved.
