# World_Weather_Analysis

# Summary

## Purpose
This project involves processing weather data from an API to generate random Geographic Coordinates and a list of cities. It then uses this city data to filter cities based on specific criteria, performing linear regression analysis on different datasets, and preparing a DataFrame for storing hotel information. The aim is to refine the dataset, visualize relationships, and prepare for integration with external APIs to find hotels.

## Steps

### 1. Data Preparation and Processing
- **Initial Preparation**: Use OpenWeatherMap API to retrieve weather data from the cities list. Generate the Cities List by Using the `citipy` Library.
  - **Analysis**:Create Plots to Showcase the Relationship Between Weather Variables and Latitude

### 2. Linear Regression Analysis
- **Northern Hemisphere**:
  - **Filter and Prepare Data**: Filter and prepare data for Northern Hemisphere cities.
  - **Perform Linear Regression**: Analyze the relationship between latitude and Temperature, Humidity, Cloudiness and wind speed.
  - **Visualization**: Plot the regression line and annotate the equation on the graph.
- **Southern Hemisphere**:
  - **Filter and Prepare Data**: Filter and prepare data for Southern Hemisphere cities.
  - **Perform Linear Regression**: Analyze the relationship between latitude and Temperature, Humidity, Cloudiness and wind speed.
  - **Visualization**: Plot the regression line and annotate the equation on the graph.

### 3. Data Fitering
- **Initial Filtering**: Cities are filtered based on:
  - **Humidity**: Less than 60
  - **Wind Speed**: Less than 4.5
  - **Max Temperature**: Less than 27
  - **Cloudiness**: Set to zero for all filtered cities.
- **Handling Null Values**: Rows with null values are removed to ensure clean data.

### 4. Creating and Modifying DataFrame
- **Create DataFrame for Hotels**: A new DataFrame, `hotel_df`, is created to include:
  - City
  - Country
  - Longitude (`Lng`)
  - Latitude (`Lat`)
  - Humidity
- **Add "Hotel Name" Column**: An empty column is added to store hotel names retrieved via external APIs.
- **Plotting**: Plot graph to show location of cities with criteria selected. Use the Geoapify API to find the first hotel located within 10,000 metres of coordinates.

### Dependencies and Setup
- **Install libraries**: 
  - **import matplotlib.pyplot as plt**
  - **import pandas as pd**
  - **import numpy as np**
  - **import requests**
  - **import time**
- - **import hvplot.pandas**
  - **from scipy.stats import linregress**
  - **from citipy import citipy**

### References
https://pandas.pydata.org/pandas-docs/stable/reference/index.html