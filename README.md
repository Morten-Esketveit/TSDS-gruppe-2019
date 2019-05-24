# TSDS-gruppe-2019
Exam project in Topics in Social Data Science course joint with [Thor D. Noe](https://github.com/thornoe) and [Christian L. Sørensen](https://github.com/ChristianLS).

See [abjer/tsds](https://github.com/abjer/tsds) for the public course material.

## *Prices in Air Transport*
### *Can Airport Network Characteristics Aid in Prediction?*

From the abstract in our [project paper](https://github.com/Morten-Esketveit/TSDS-gruppe-2019/blob/master/main.pdf):
> *In this paper, we investigate whether network-related features of airports can add predictive power to a model predicting flight prices. We analyze the domestic US air transport sector as a network with airports as nodes, and direct flights as links.*

#### Overview of notebooks
The following notebooks are used for the paper: 

1. Data_Compiling
2. Scraping
3. Descriptive_Statistics
4. Network_Types
5. Maps
6. AttacksAndErrorsAnalysis18
7. Prediction


#### 1. [Data_Compiling](https://github.com/Morten-Esketveit/TSDS-gruppe-2019/blob/master/Exam/Data_compiling_v3.ipynb)
In this notebook, we gather and clean the data used in the analysis.  
Airport data is taken from OpenFlights, while data on flights is from Bureau of Transportation Statistics.
The airport data is saved as Airports.pkl and flights data is saved as FlightsNx98.pkl, FlightsNx07.pkl, and FlightsNx18.pkl respectively.
Observations in the flights dataset consist of origin and destination airports with a number of related variables (e.g. distance).  

#### 2. [Scraping](https://github.com/Morten-Esketveit/TSDS-gruppe-2019/blob/master/Exam/Scraping/scraping_code.ipynb)
In this notebook we scrape data from Skyscanner.com.

#### 3. [Descriptive_Statistics](https://github.com/Morten-Esketveit/TSDS-gruppe-2019/blob/master/Exam/Descriptive_Statistics.ipynb)
This notebook produces a range of descriptive statistics on the basis of the datasets on flights produced in Data Compiling.  
A number of network-level characteristics are calculated (e.g. average shortest path length), and the degree distributions are produced.

#### 4. [Network_Types](https://github.com/Morten-Esketveit/TSDS-gruppe-2019/blob/master/Exam/Network_Types.ipynb)
In this notebook we produce the stylized networks to illustrate fully connected and hub-and-spoke networks. 

#### 5. [Maps](https://github.com/Morten-Esketveit/TSDS-gruppe-2019/blob/master/Exam/Maps.ipynb)
In this notebook we map the networks in each of the three years onto a map of the continental US, where nodes (airports) are at their actual geographical locations. This is done on the basis of the flights dataset, that are converted to NetworkX networks, and then longitude and latitude from Airports.pkl are added as position attributes for the nodes.

#### 6. [AttacksAndErrorsAnalysis18](https://github.com/Morten-Esketveit/TSDS-gruppe-2019/blob/master/Exam/AttacksAndErrorAnalysis18.ipynb)
In this notebook, we investigate how removal of either the most connected nodes ("attacks"), removal of the least connected nodes ("errors"), and removal of random nodes affect key network characteristics. This is done on the basis of the dataset FlightsNx18. 

#### 7. [Prediction](https://github.com/Morten-Esketveit/TSDS-gruppe-2019/blob/master/Exam/Prediction/Prediction2018.ipynb)
In this notebook, we clean the scraped data and merge in with data our network dataset. We then estimate two prediction models in order to assess whether network characteristics can improve a baseline model that includes time, distance, total flights to and from origin airport, flights to and from destination airport and airport fixed effects. 
