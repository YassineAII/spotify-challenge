# Spotify Popularity Prediction Challenge

## Overview

This project aims to predict the popularity of songs using audio features from the Spotify API. The dataset contains over 115,000 tracks and includes both metadata like artist and year, as well as audio characteristics such as energy, danceability, and loudness. The objective is to develop a machine learning model to estimate the popularity of a song based on these features.

## Dataset

We used two datasets from Kaggle:
- `SpotifyAudioFeaturesNov2018.csv` (November 2018)
- `SpotifyAudioFeaturesApril2019.csv` (April 2019)

Some songs appear in both datasets with different popularity values due to recalculations over time. A new feature `time` was created to differentiate between the two periods:
- `0`: November 2018
- `1`: April 2019

## Project Structure

1. **Data Preprocessing:**
   - Combined both datasets and handled missing values.
   - Added a new `time` feature to account for the time of popularity measurement.
   
2. **Exploratory Data Analysis (EDA):**
   - Visualized the distribution of audio features and their correlation with popularity.
   - Analyzed categorical features such as `time_signature`, `mode`, and `key`.

3. **Modeling:**
   - Built a baseline linear regression model for predicting popularity.
   - Implemented a RandomForestRegressor with hyperparameter tuning using RandomizedSearchCV to optimize performance.

4. **Evaluation:**
   - The RandomForest model achieved an RMSE of 17.74 on the test set.
   - Visualized feature importance to understand which audio features contributed most to the prediction.

5. **Future Improvements:**
   - Explore advanced models like Gradient Boosting and Neural Networks.
   - Consider a classification approach, predicting whether a song's popularity exceeds a certain threshold.
   - Apply techniques such as PCA or synthetic data generation to further enhance performance.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/YassineAII/spotify-challenge.git
   ```

2. Open the Jupyter notebook `spotify_popularity_prediction.ipynb`.
3. 
4. Run the notebook to preprocess the data, visualize trends, and train the models.
