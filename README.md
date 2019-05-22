# TSDS-gruppe-2019

## Exam
#### Overview of notebooks
The following notebooks are used for the paper: 

1. Data_Compiling 
2. Descriptive_Statistics
3. Network_Types
4. Maps
5. AttacksAndErrorsAnalysis18
6. Prediction


#### 1. Data_Compiling
In this notebook, we gather and clean the data used in the analysis.  
Airport data is taken from OpenFlights, while data on flights is from Bureau of Transportation Statistics.
The airport data is saved as Airports.pkl and flights data is saved as FlightsNx98.pkl, FlightsNx07.pkl, and FlightsNx18.pkl respectively.
Observations in the flights dataset consist of origin and destination airports with a number of related variables (e.g. distance).  

#### 2. Scraping
In this notebook we scrape data from Skyscanner.com.

#### 3. Descriptive_Statistics
This notebook produces a range of descriptive statistics on the basis of the datasets on flights produced in Data Compiling.  
A number of network-level characteristics are calculated (e.g. average shortest path length), and the degree distributions are produced.  

#### 4. Network_Types
In this notebook we produce the stylized networks to illustrate fully connected and hub-and-spoke networks. 

#### 5. Maps 
In this notebook we map the networks in each of the three years onto a map of the continental US, where nodes (airports) are at their actual geographical locations. This is done on the basis of the flights dataset, that are converted to NetworkX networks, and then longitude and latitude from Airports.pkl are added as position attributes for the nodes.

#### 6. AttacksAndErrorsAnalysis18
In this notebook, we investigate how removal of either the most connected nodes ("attacks"), removal of the least connected nodes ("errors"), and removal of random nodes affect key network characteristics. This is done on the basis of the dataset FlightsNx18. 

#### 7. Prediction 
In this notebook, we clean the scraped data and merge in with data our network dataset. We then estimate two prediction models in order to assess whether network characteristics can improve a baseline model that includes time, distance, total flights to and from origin airport, flights to and from destination airport and airport fixed effects. 
