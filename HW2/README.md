# HW2: Exploratory Data Analysis on Music Dataset

This notebook was developed as part of the CS210: Introduction to Data Science course. The assignment involved working with a structured music dataset in CSV format and performing exploratory data analysis using pandas and visualization libraries.

## Objective
To analyze various musical attributes and trends, such as popularity, tempo, genre characteristics, and artist styles, by using data analysis and visualization techniques.

## Dataset
- Filename: `cs210_hw2_dataset.csv`
- Format: CSV
- Contains numerical and categorical attributes of songs, such as:
  - Popularity
  - Tempo (BPM)
  - Danceability, Energy, Loudness
  - Acousticness, Valence, Speechiness
  - Artist, Genre, Year, Month

## Tools and Libraries Used
- pandas
- matplotlib
- seaborn

## Methodology
- Loaded and preprocessed the CSV data using pandas
- Created various plots to explore relationships between variables, including:
  - Histograms and bar charts for BPM and popularity categories
  - Scatter plot for Energy vs Loudness
  - Line plots to visualize average popularity over years and months
  - Grouped bar charts for BPM levels by artist
  - Stacked bar charts for Energy and Acoustic values by genre
  - Correlation heatmap for numerical attributes

## Key Observations
- Energy and Loudness are strongly positively correlated
- Tempo values mostly fall within the medium BPM category
- Popularity does not show strong correlation with audio features
- Indie and rock-related genres dominate in energy levels
- Different artists (e.g., Lorde, Big Thief) show varied BPM preferences

## Files
- `Beyza-Balota-CS210-HW2.ipynb`: Full implementation notebook
- `cs210_hw2_dataset.csv`: Dataset used in the analysis
- `README.md`: This project overview file

## Notes
This assignment focused on data cleaning, visualization, and interpretation. It does not include predictive modeling or classification tasks.
