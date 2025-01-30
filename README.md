# Sleep Pattern Analysis: Predicting Sleep Score and Optimal Bedtime

## Overview
This project analyzes sleep patterns using machine learning techniques to predict sleep scores and determine an 
optimal bedtime range. The study is based on sleep data collected from the Sleep Cycle app and employs clustering and regression models to identify key sleep factors and trends.
## How to run the project
1. Unzip the package and upload the notebook and dataset.zip it to JupyterHub
2. Uncomment the code '!unzip datatset.zip'
3. Run the code in the next cell to see if the dataset is retrieved

## Objectives
- Predict a sleep score based on various features using machine learning.

- Identify the optimal bedtime for the subject.

- Explore the correlation between time in bed, external factors, and sleep quality.

- Investigate the impact of seasonal variations on sleep quality.

## Dataset
The dataset, sourced from Kaggle at https://www.kaggle.com/danagerous/sleep-data, consists of 887 sleep entries recorded between 2014-2018. Each entry includes the following features:
- Start: datetime - Timestamp when the subject went to bed.
- End: datetime - Timestamp when the subject woke up.
- Sleep quality: float - Percentage measure of sleep quality.
- Time in bed: float - Total duration spent in bed.
- Heart rate: float - Average heart rate during sleep.
- Caffeine Consumption: binary - Indicator of caffeine intake (1/0).
- Exercise: binary - Indicator of exercise on that day (1/0).
- Stressed: binary - Indicator of stress on that day (1/0).
- Season: string - Season during which the sleep data was recorded.

## Methodology 
1. Preprocessing:
  - Handled missing values for heart rate, wake-up state, and sleep notes.
  - Derived new features: Caffeine Consum****ption, Stressed, Exercise, and Season.
  - Removed irrelevant features (e.g., Wake up, Activity steps).

2. Data Analysis:
  - Used correlation matrices and regression plots to identify influential factors.
  - Performed one-way ANOVA tests to assess the effect of seasons on sleep quality.
3. Machine Learning Models:
  - KMeans Clustering: Used to group sleep patterns and identify optimal cluster count.
  - Random Forest Regressor: Used to determine feature importance for sleep quality prediction.
  - Weighted Score Computation: Generated sleep scores using feature weights.
4. Finding optimal bedtime:
  - Divided bedtime timestamps into bins (1-hour intervals).
  - Used median sleep quality to determine the best bedtime range.
