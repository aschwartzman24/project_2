# [Project 2](https://github.com/BNY-Lemon/KU-Project-2)
## **World Happiness Index Analysis**

## Main Contents:

	app.py
	sql_load.ipy
	logis.js	
	styles.css


## Tools used:

    Jupyter Notebook
    Pandas
    Flask
    MongoDB
    HTML
    CSS
    Javascript
    Mapbox API

### Description:

This project leverages Javascript, Flask, Python’s Pandas, MongoDB to analyze and draw conclusions about the happiest countries and other variables that may contribute to overall happiness including GDP Per-Capita, Social Support, Life Expectancy, Freedom Score, Generosity, Corruption Score, Dystopia Score. This descriptive information helps to understand how the happiness report works.The data collected from the Happiness Index Report was imported to a CSV file that is visualized here [Happiness Index data](https://github.com/BNY-Lemon/KU-Project-2/blob/main/Cleaned%20Data/WHR20.csv)

### What is the Happiness Index?

The well-being (or perception of well-being) of a specific country is recognized as a measure of social progress and the success of public policies. Many (but not all) local and national governments use this data and research to pursue policies that help their citizens live better lives. The happiness report measures the well-being of the citizens of different countries according to a series of statistical variables and different perceptions. These variables include GDP Per-Capita, Social Support, Life Expectancy, Freedom Score, Generosity, Corruption Score, Dystopia Score.

In the first visualization, you will find data that helps to see what other factors may affect happiness in each country. The first data visualization page includes the scatter plot that represents each country with circle elements. The Y axis contains the ladder score (happiness score) and the X axis see the hours average work week, education score, population density and the English-speaking population.

### Components of [sql_load.ipynd](https://github.com/BNY-Lemon/KU-Project-2/blob/main/Data%20Collection%20Scripts/sql_load.ipynb) include:
Components of the data_cleaning.ipynb file include:

1. Importing 5 datasets including global_weather_csv., population_density_and_english_speaking.csv, PISA.csv, Happiness_index_lat_longs.csv, and Standard workweek.csv. 
2.  Merge 5 datasets to one master table
3.  Load all tables into Mongo database
4.  Create a join table w

### Components of [app.py](https://github.com/BNY-Lemon/KU-Project-2/blob/main/app.py) include:
1. Create an instance of the Flask app.
2. Pass connection to the pymongo indstance.
3. Connect to a database
4. Set route 'index.html
5. Set page routes '/heatMap.html', '/visualization.html'
6. Create API route for each table '/api/v1.0/master', '/api/v1.0/happiness', '/api/v1.0/pisa', '/api/v1.0/population_english', '/api/v1.0/weather', '/api/v1.0/work'.



### Components of [logis.js](https://github.com/BNY-Lemon/KU-Project-2/blob/main/static/logic.js) include:
1. Fetch the happiness API
2. Create a map object
3. Add a title to the map
4. Create a GEOJSON layer with the GeoJSON layer with the retrieved data 
5. Create one marker for each city, bind a popup containing its name and population 
6. Insert a marker the populates GDP Per-Capita, Social Support, Life Expectancy, Freedom Score, Generosity, Corruption Score, and Dystopia Score when hovering over each city.

