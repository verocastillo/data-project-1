## Spotify trends & COVID-19: Correlations between music listening trends and hardship levels from COVID

Spotify_COVID_analysis.png


* OBJECTIVE

Explore how COVID-19 affected music streaming user preferences:
- Are they listening to happy music to cheer up?
- Are we listening to sad music to cope?
- Does this vary by the country?

* BUSINESS IMPACT

Spotify can use this data to improve their algorithms and offer more personalized suggestions to users in different regions, that could potentially provide a better experience to the user.

* DATA 

Spotify API for the tracks and music metrics was use and for COVID-19 information the official datasets from Our World data.

The questions to answer with this Data Analysis are:
1. Did the pandemic affect how people globally and locally listen to music?
2. Is there a correlation betweeen COVID-19 severity and music preferences by country?

* DEPENDENCIES
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
import requests
import json
import re, glob
import os, sys
from scipy import stats
import seaborn as sn
import spotipy                          
       
                                                
* DATA EXPLORATION

1. Convert input CSVs into DataFrame
    COVID data in csv files from https://ourworldindata.org [5] and Spotify Top Charts at 
    spotifycharts.com. They were read and transformed into DataFrames using Pandas. 

2. Obtain track features from API 
    Using the Spotify API and the track names from the Spotify DataFrame, we got track information 
    regarding Valence. This is a metric used by Spotify which characterize whether a song is sad or happy.

3. Delete faulty/repeated data
    Some tracks were not found, and some information was not available in certain countries. 
    These values in the DataFrame were dropped.
    
4. Plot key indexes over time
    Using the dates in which the data was obtained, we merged the DataFrames and plotted valence.

5. Obtain correlations between variables
    Correlations between variables were obtained by using scatter plots and linear regression analysis.


* DATA TRANSFORMATION

From Spotify we obtained CSV files for the weekly top 200 charts for each country and the global one. From Our World in Data COVID statistics divided by date and country were used. Also, the Spotify API was used to obtain track information and audio features for each track. 

From this data, key metric to study was Valence, defined from sounded studies as a measure which indicates whether  people associate happy or sad sounds. This is important because it is how Spotify describes the musical positiveness conveyed by a track. The number of COVID cases and deaths were also analysed in order to compare  how valence behaved over time.

Import CSV files obtained from the data sources, and turned them into Pandas DataFrames. From the DataFrame with the Spotify data the Spotify API was used to obtain the track ID associated with each song, and then the audio features of the song, which included song valence. 

* CLEAN-UP DATA

Dropped songs that are not in certain countries, songs that are no longer in Spotify and songs with missing values. 

* PANDAS ANALYSIS

Relevant mean values and weighted averages to simplify the data to be grouped by month and year were retrieved. Matplotlib helped to plot valence through time, comparing the monthly change in 2019 and 2020 also scatter plots and linear regression analysis to obtain the correlation between variables was used.

* RESULTS

Valence preference varies between countries.
Hispanic and Latin countries have higher mean valence.
Mean valence between 2019 and 2020 was significantly different in some countries.
México decreased in 2020.
Spain increased in 2020.
Globally, there was no significant change in mean valence.

Valence vs. Cases per Million
Global tendency shows a strong positive correlation. 
Germany and the US match the trend.
México, Spain and India show from a moderate to a strong negative correlation.
Valence vs. Deaths per Million
Global tendency shows a strong positive correlation. 
Germany and the US match the trend.
México, Brazil, Italy and India show from a moderate to a strong negative correlation.

* CONCLUTIONS

Spotify can use the data obtained to offer more personalized suggestions to users depending on the country, and optimize exclusive contracts with certain artists that match the ‘mood’ of each country. 
The majority of the countries analyzed presented a correlation.


=======
# COVID and Spotify Trends: Data-Project-1
![gettyimages-1217390845](https://user-images.githubusercontent.com/77795761/117542257-817cb900-afdd-11eb-8e25-e5951a95e7f6.jpg)

Testing, testing...
>>>>>>> 0a7e4daf1ad559302fffbf105079c7827ddc445a
