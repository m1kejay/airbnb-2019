# Analysing AirBNB data from 2019 for NYC

The analysis can be found in the jupyter notebook located here: **[airbnb_2019_ny.ipynb](airbnb_2019_ny.ipynb)**.

Data originally downloaded from here: https://www.kaggle.com/dgomonov/new-york-city-airbnb-open-data

This is a bit of a meandering 'stream of consciousness' analysis of AirBNB listings within NYC as of 2019. I'm relatively new to Python, having only ever used it to write small scripts, never for the purposes of data exploration or visualisation before (my bread and butter being R). In other words, there are likely errors in this analysis. Additionally, prior to this I had *never* done any sort of geospatial analysis so take what I've done with a huge pinch of salt! 

In the first section, I've imported and cleaned the data, identifying outliers, missing data and any interesting observations which may be worth chasing up.

In the second section (and partly during data cleaning) I've performed some preliminary exploratory data analysis.

In part three, I did some geospatial analysis, attempting to determine whether there was any relationship between the price per night and location of the listing relative to subway stations. 

Finally, I look at which neighbourhoods are over- or under-represented on AirBNB by combining population data with the AirBNB data.

## TODO
* Look at other buffers around stations.
    - Is there a better way? Instead of an arbitrary buffer can we find raw distances from station to house?
        - use that as a predictor for cost?
* Dig into the descriptions.
    - What are the popular descriptors used by hosts?
    - Can they be used to predict popularity (reviews as proxy)?
    - Predict how much they charge?
* Build some sort of recommendation system incorporating my subway station data which let's me find places close to public transport.
* Can we build a model to predict price?
    - From looking on kaggle people have tried but IMO their data cleaning is poor. For instance, there are many properties listed which are likely inactive which many have not removed.