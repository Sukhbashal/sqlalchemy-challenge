**SQLAlchemy Challenge: Climate Analysis and Flask App**

*Overview*

In this challenge, you will work with a SQLite database containing weather data collected from various stations in Hawaii. You will use SQLAlchemy, an Object Relational Mapper (ORM), to connect to the database and perform two distinct analyses: Precipitation Analysis and Station Analysis. Additionally, you will design a Climate App using Flask, which will expose both static and dynamic API routes.

**Climate Analysis**

_Precipitation Analysis_

To analyze precipitation, follow these steps:

Find the most recent date in the dataset.
Get the previous 12 months of precipitation data by querying the dataset.
Select the "date" and "prcp" columns.
Load the query results into a Pandas DataFrame and explicitly set the column names.
Sort the data by date in ascending order.
Plot the precipitation data using the Pandas plot method.
Use Pandas to display summary statistics for the precipitation data.

_Station Analysis_

For station analysis, complete the following steps:

Calculate the total number of stations in the dataset.
Identify the most active station (the one with the most rows of data).
List the stations and their corresponding observation counts in descending order.
Identify the station with the greatest number of observations.
Find temperature statistics (min, max, and average) for the most active station identified in the previous step.
Retrieve the last 12 months of temperature observations (TOBS) for the most active station.
Plot the TOBS data for the most active station as a histogram with 12 bins.

**Climate App**

Using Flask, build an API to serve the results from your queries:

_Static Routes_

/: Display the homepage with an introduction to the app.
/api/v1.0/precipitation: Convert the precipitation analysis data into a dictionary (with date as the key and prcp as the value) and return it in JSON format.
/api/v1.0/stations: Return a JSON list of stations from the dataset.
/api/v1.0/tobs: Return a JSON list of temperature observations (TOBS) for the most active station for the past year.

_Dynamic Routes_

/api/v1.0/[start]: Accept a start date as a parameter and return a JSON response with the minimum, average, and maximum temperatures for all dates from the start date onward.
/api/v1.0/[start]/[end]: Accept both a start date and an end date as parameters. Return a JSON response with the minimum, average, and maximum temperatures for all dates between the start and end date, inclusive.
