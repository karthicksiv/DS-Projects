# Understanding Taxi Utilization in New York City
## Overview
This project utilizes geospatial and temporal data to understand the taxi utilization in New York City. Specifically, I am interested in determining the fraction of time that a cab is on the road and is occupied by one or more passengers, which is known as taxi utilization.

## Technologies Used
The project is written in Python and utilizes PySpark, GeoPandas, and GeoJSON data.

## PySpark
PySpark is a Python API for Apache Spark, which is a popular big data processing framework. It provides a programming interface to perform distributed data processing across multiple nodes in a cluster.

## GeoPandas
GeoPandas is a Python package that extends the pandas library to allow spatial operations on geospatial data. It provides an easy-to-use interface to handle geospatial data and supports common GIS file formats such as shapefiles, GeoJSON, and more.

## GeoJSON
GeoJSON is a format for encoding geospatial data in JSON (JavaScript Object Notation). It is commonly used for representing geographical features and supports different types of geometry such as points, lines, and polygons.

## Dataset
The dataset used for this project is the NYC Taxi and Limousine Commission (TLC) trip record dataset, which contains detailed trip data from yellow and green taxis, for-hire vehicles, and high-volume for-hire services. Specifically, the data is from the green taxis from January 2013 to December 2013. The data can be imported by running the following command:

curl -O https://storage.googleapis.com/aas-data-sets/trip_data_1.csv.zip

# Approach
I have used PySpark to process the large dataset and GeoPandas to perform geospatial operations on the data. I have used GeoJSON data to plot the results on a map.

Firstly, I filtered the data to only include trips where the cab had passengers. I then grouped the data by pickup location and time, and calculated the total time that the cab was occupied. I then calculated the total time that the cab was on the road, which is the duration between the pickup time and dropoff time. I then divided the total occupied time by the total on-road time to calculate the taxi utilization.

Next, I used GeoPandas to perform spatial operations on the data. I aggregated the data by pickup location and calculated the mean utilization for each location. I then plotted the results on a map using GeoJSON data.

