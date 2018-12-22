# Full Report on the Capstone

## Sections:
**1. Introduction**  
**2. Data Description**  
**3. Methodology**  
**4. Results**  
**5. Discussions**  
**6. Conclusion**


## Introduction
**Identifying the relation between food in Toronto, Canada and New York City, USA.**  
How does the types of cuisines in Toronto and New York City vary?
Is there any dominant cuisine in these regions?
These are a few of the questions to be answered in the notebook. We don't know what insights we may uncover.  
We will dive deep into the location data and data from [Foursquare](https://foursquare.com).

## Data Description
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

## Methodology
This notebook follows the following Methodology:
1. Collecting the data
2. Cleaning the data
3. Visualization
4. Machine Learning

### Step 1: Collecting Data
The datasets used in this notebook are collected from two main sources namely, Wikipedia and [NYU Spatial Data Repository](https://geo.nyu.edu/catalog/nyu_2451_34572).
Please refer to the Data Description section for more information about the data.  
The **Foursquare** data, will be added within the notebook and no external file will be created for it.
The API calls will be made within the code cell. Once the necessary data is collected, cleaning the data is done.  

### Step 2: Cleaning Data
This step consumes a lot of time. The cleaning of data in this notebook is done in two phases, one for the Toronto Data and
other for the New York City Data. The notebook for Toronto Data cleaning is available [here](https://github.com/KrishnaChaitanya1/Coursera_Capstone/blob/master/Final%20Capstone%20Project/Scraping%20for%20Toronto%20Postal%20Codes.ipynb). The final dataset generated is available [here](https://github.com/KrishnaChaitanya1/Coursera_Capstone/blob/master/Final%20Capstone%20Project/Data%20Files/Toronto%20Postal%20Codes.csv).  
The notebook for Cleaning New York City Data is available [here](https://github.com/KrishnaChaitanya1/Coursera_Capstone/blob/master/Final%20Capstone%20Project/Notebooks/Cleaning%20for%20New%20York%20Boroughs.ipynb). The final dataset is available [here](https://github.com/KrishnaChaitanya1/Coursera_Capstone/blob/master/Final%20Capstone%20Project/Data%20Files/New%20York%20City%20Boroughs.csv).

### Step 3: Visualization
A few simple visualizations are made in order to get a better understanding of the data. **Folium** is used for this purpose.
**Folium** generates interactive and beautiful maps, using the Latitude and Longitude we provide. The folium visualizations will be made available in the comments section.  
Further to enhance the understanding of the data, **count plots** are used to better understand the final result.

### Step 4: Machine Learning
KMeans clustering algorithm is used on the most common venues dataframe to identify the probable clusters for different types of restaurants. In both the datasets, we have initialized 5 clusters.

## Results
1. As expected, American Restaurant has highest count in Brooklyn as **1st Most Common Restaurant**. But American Restaurant has highest count in Downtown Toronto as **2nd Most Common Restaurant**. However we can conclude that American Restaurants dominate both Brooklyn and Downtown Toronto. But the graph for 1st Most Common Restaurant says that highest count in Downtown Toronto is 'Restaurant'. But what type of cuisine does it serve is not mentioned. To further understand how to solve this refer **Discussions** section.
2. In Brooklyn, 1st Most Common Restaurant have American Restaurant as top followed by Italian and Caribbean Restaurant. For 2nd Most Common Restaurant, we have rather a different picture. It is topped by Chinese followed by American, Falafel and Vietnamese Restaurants.
3. In Downtown Toronto, 1st Most Common Restaurant we have 'Restaurant' as top. But what kind of cuisine they serve is unknown, which is a discrepancy. It shares top with Vietnamese Restaurant. For 2nd Most Common Restaurant, American and Greek Restaurants take top spot.

## Discussions
There is a small discrepancy in the datasets. There are some entries in the dataset that just say 'Restaurant'. We can consider this type as a restaurant which serves different cuisines. We may be right or we may be wrong. There are a few methods by which we can solve this discrepancy. One such method is to consider this restaurant as a majority cuisine in that area. Example: If in an area, American Cuisine has highest count, we can consider this 'Restaurant' as an American Restaurant.  
The problem with this method is we might not always be correct. Another concrete way of solving this is rather tiresome approach, which is not feasible. We look for the corresponding coordinates and use google to find what type of restaurant is that.

## Conclusion
Hence, this notebook serves as a reference to identify the relations between food cuisines between Toronto and New York City.
This notebook can be extended to include not only the data related to restaurants but also other aspects.
