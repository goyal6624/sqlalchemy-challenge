# sqlalchemy-challenge

In this module challenge, I was tasked with creating a Jupyter Notebook to access a database and perform data analysis on Hawaii climate using SQLAlchemy. I also created an app that uses the Flask API to serve data from the database and perform any calculations as needed. All of the data is sourced from the SQLite database located at `sqlite:///Resources/hawaii.sqlite`. The Jupyter Notebook `climate.ipynb` and app `app.py` are located in the `Climate Data` folder.

## Routes

### Static Routes

- `/`
    - Start at the homepage.
    - List all the available routes.

- `/api/v1.0/precipitation`
    - Returns the JSON representation of the last 12 months of precipitation data.
    - Data is converted to a dictionary using date as the key and prcp as the value.

- `/api/v1.0/stations`
    - Returns a JSON list of weather stations available in the dataset.

- `/api/v1.0/tobs`
    - Returns a JSON list of temperature observations for the previous year from the most-active weather station.

### Dynamic Routes

- `/api/v1.0/<start>`
    - Returns a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a specified start date.
    - Example Usage: `/api/v1.0/2017-01-01`

- `/api/v1.0/<start>/<end>`
    - Returns a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a specified date range.
    - Example Usage: `/api/v1.0/2017-01-01/2017-12-31`

## Data Source

The data used in this API is sourced from the SQLite database `hawaii.sqlite`. The database contains two tables: `measurement` and `station`. The `measurement` table holds weather data, including temperature and precipitation, while the `station` table contains information about the weather stations in Hawaii.

## Capabilities

With this API, you can retrieve various weather-related information from Hawaii, including:

- Precipitation data for the last 12 months.
- A list of weather stations available in the dataset.
- Temperature observations for the previous year from the most-active weather station.
- Minimum, average, and maximum temperatures for a specific start date or date range.

Please ensure that you have the required Python  packages installed before running the app with `python app.py`.