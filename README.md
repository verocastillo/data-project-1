## Spotify trends & COVID-19: Correlations between music listening trends and hardship levels from COVID

Spotify_COVID_analysis.png

OBJECTIVE
Explore how COVID-19 affected music streaming user preferences:
- Are they listening to happy music to cheer up?
- Are we listening to sad music to cope?
- Does this vary by the country?

DATA 

As we know 2019 was relatively normal year, so were music trends different in 2020?

BUSINESS IMPACT
Spotify can use this data to improve their algorithms and offer more personalized suggestions to users in different regions, that could potentially provide a better experience to the user

Therefore, the questions to answer are:

1. Did the pandemic affect how people globally and locally listen to music?
2. Is there a correlation betweeen COVID-19 severity and music preferences by country?


DATA CLEAN-UP & EXPLORATION
1. Convert input CSVs into DataFrame
    COVID data in csv files from https://ourworldindata.org [5] and Spotify Top Charts at 
    spotifycharts.com. They were read and transformed into DataFrames using Pandas. 

2. Obtain track features from API 
    Using the Spotify API and the track names from the Spotify DataFrame, we got track information 
    regarding Valence

3. Delete faulty/repeated data
    Some tracks were not found, and some information was not available in certain countries. 
    These values in the DataFrame were dropped.
    
4. Plot key indexes over time
    Using the dates in which the data was obtained, we merged the DataFrames and plotted valence.

5. Obtain correlations between variables
    Correlations between variables were obtained by using scatter plots and linear regression analysis.







