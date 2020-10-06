<!---Project Logo -->
<br />
<p align="center">
  <h3 align="center">Dream Vacation Location</h3>
  <p align="center">
    A Python API Project
    <br />
  </p>
</p>


<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
  * [Built With](#built-with)
* [Usage](#usage)
* [Getting Started](#getting-started)
* [Results](#results)
<!-- ABOUT THE PROJECT -->
## About The Project

## Background

This project tackles the problem of weather patterns as one moves closer to equator using Python APIs. In the 2nd part, I find my ideal vacation location using data I used to analyze weather patterns. 

![Equator](Images/equatorsign.png)

## Part I - WeatherPy

In this project, I created a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, I utilized a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little common sense to create a representative model of weather across world cities.

First, I created a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

Then, I ran linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude


In the end, I accomplished the following:

* Randomly select **at least** 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a PNG image for each scatter plot.

### Part II - VacationPy

In this part, I use the weather data to plan future vacations. I used jupyter-gmaps and the Google Places API for this part of the assignment.

I accomplished the following with the data.

* Create a heat map that displays the humidity for every city from the part I of the project.

  ![heatmap](Images/heatmap.png)

* Narrow down the DataFrame to find my ideal weather condition. For example:

  * A max temperature lower than 26 degrees but higher than 19.

  * Wind speed between 2-5 mph.

  * Cloudiness under 10 percent.

  * Drop any rows that don't contain all three conditions. 

  
* Using Google Places API to find the first hotel for each city located within 5000 meters of the coordinates.

* Plot the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

  ![hotel map](Images/hotel_map.png)


### Built With
* [Python](https://www.python.org/about/)
  * [Matplotlib](https://matplotlib.org/3.3.1/contents.html)
  * [Pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/index.html)
* [Openweather APIs](https://openweathermap.org/api)
* [Google APIs](https://developers.google.com/maps/documentation)


<!-- GETTING STARTED -->

## Getting Started
* **Note:** if you having trouble displaying the maps try running `jupyter nbextension enable --py gmaps` in your environment and retry.


## Results
Based on my data and criteria for ideal vacation weather, I found out that my ideal vacation location is Lanzhou, China.


**Additional reference materials:**


_Best-README-Template_ Retrieved from: [https://github.com/othneildrew/Best-README-Template](https://github.com/othneildrew/Best-README-Template)






