# Data Description

### New York Location Dataset
The data is taken from [NYU Spatial Data Repository](https://geo.nyu.edu/catalog/nyu_2451_34572). The original format of this dataset is a GeoJson file, which is then converted to a csv. The raw data can be found [here](https://github.com/KrishnaChaitanya1/Coursera_Capstone/blob/master/Final%20Capstone%20Project/Data%20Files/nyc_geojson.json).
The CSV File has the following features:
1. Borough
2. Neighborhood
3. Latitude
4. Longitude

There are a total of 307 records available in this dataset.
However cleaning needs to be done. The cleaned dataset is found [here](https://github.com/KrishnaChaitanya1/Coursera_Capstone/blob/master/Final%20Capstone%20Project/Data%20Files/New%20York%20City%20Boroughs.csv).  

### Toronto Location Dataset
The dataset is scraped from [this](https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M) link.
The dataset is then cleaned and saved as CSV file. The notebook for scraping is available [here](https://github.com/KrishnaChaitanya1/Coursera_Capstone/blob/master/Final%20Capstone%20Project/Scraping%20for%20Toronto%20Postal%20Codes.ipynb).  
This notebook will be updated with Markdown for easy understanding.
The [final CSV File](https://github.com/KrishnaChaitanya1/Coursera_Capstone/blob/master/Final%20Capstone%20Project/Data%20Files/Toronto%20Postal%20Codes.csv) will have the following features:
1. Postal Code
2. Borough
3. Neighborhood
4. Latitude
5. Longitude

The above mentioned datasets are used in conjunction with the [Foursquare API](https://foursquare.com/).
