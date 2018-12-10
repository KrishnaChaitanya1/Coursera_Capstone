# Full Report on the Capstone

## Sections:
**1. Introduction**  
**2. Data Description**  
**3. Methodology: EDA, Inferential Statistics, Machine Learning to be added**  
**4. Results**  
**5. Discussions: Observations and Recommendations to be made**  
**6. Conclusion**


## Introduction
**Identifying the relation between food in Toronto, Canada and Paris, France.**  
How does the types of cuisines in Toronto and Paris vary?
Does French cuisine has more domination in Toronto? Or any other cuisines are popular in Toronto and Paris?
These are a few of the questions to be answered in the notebook.  
Normally we would think that Paris has a domination of French cuisine, however our assumptions may be true or they may be false.
So we will dive deep into the location data and data from [Foursquare](https://foursquare.com).

## Data Description
### France Location Dataset
The list of postal codes data for Paris, France is taken from the website [AggData](www.aggdata.com).
The CSV File has the following features:
1. Postal Code
2. Place Name
3. State
4. County
5. City
6. Latitude
7. Longitude

There are a total of 20413 records available in this dataset.
However cleaning needs to be done. The cleaned dataset is available [here]()

### Toronto Location Dataset
The dataset should be scraped from [this](https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M) link.
A cleaned dataset will be pushed when available.
The final CSV File will have the following features:
1. Postal Code
2. Borough
3. Neighborhood
4. Latitude
5. Longitude

The above mentioned datasets are used in conjunction with the [Foursquare API](https://foursquare.com/).
This markdown will be updated whenever the datasets are updated.

## Methodology
This notebook will follow the same Methodology that nay data science project would follow.
1. Collecting the data
2. Cleaning the data
3. Visualization
4. Machine Learning (if needed)  

In this notebook, the data has already been collected and cleaned. The only thing that needs to be added is
the **Foursquare** data, which will be done within the notebook and no external file will be created for it.
The API calls will be made within the code cell. Once the necessary data is collected, cleaning the data is done.  

A few simple visualizations are made in order to get a better understanding of the data. **Folium** is used for this purpose.
**Folium** generates interactive and beautiful maps, using the Latitude and Longitude we provide.  

Once that is done, a machine learning algorithm is used, preferably **K-means**, to cluster or bring relations.

## Results





## Discussions



## Conclusion
Therefore, this notebook serves as a reference to identify the relations between food cuisines between Toronto and Paris.
