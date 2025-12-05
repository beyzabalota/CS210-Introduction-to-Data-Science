# HW1: Spotify Playlist Analysis

This notebook was completed as part of CS210: Introduction to Data Science. The assignment involved retrieving audio features from a Spotify playlist analyzer website and conducting exploratory data analysis on the playlist content.

## Objective
The goal was to scrape the playlist's audio feature table and analyze aspects such as popularity, tempo, energy, valence, and other musical attributes.

## Dataset Source
The data was obtained by scraping the following website:  
https://www.chosic.com/spotify-playlist-analyzer/?plid=4wyQnWDDys6T8A2ni96Vfg

A static HTML version of the playlist page was used to allow scraping via BeautifulSoup.

## Tools and Libraries Used
- requests – for sending HTTP GET requests  
- BeautifulSoup (bs4) – for parsing HTML  
- pandas – for data manipulation and analysis  
- matplotlib, seaborn – for data visualization  

## Method
- Extracted the playlist table using BeautifulSoup
- Converted the scraped data into a structured pandas DataFrame
- Cleaned and formatted column names and data types
- Generated visualizations to analyze:
  - Popularity distribution
  - Tempo, energy, valence, danceability
  - Correlation between features (e.g., popularity vs. loudness)

## Key Observations
- Songs with high energy often had higher loudness and tempo
- Popularity showed weak correlation with most audio features
- Tempo distribution was centered around 120 BPM
- Valence and danceability were positively correlated

## Files
- `CS210 Homework #1  Spotify Playlist Analysis.ipynb`: Jupyter Notebook implementation
- `README.md`: This file

## Notes
This assignment focused on data scraping and visualization. No machine learning models were applied.
