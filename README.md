# Dengue-case-prediction-using-weather-data

## Project Overview:
This project focuses on predicting dengue cases by leveraging historical weather data to assess environmental conditions that may contribute to the spread of the disease. Using a dataset with 26 attributes, I built a machine learning model that forecasts dengue case occurrences based on various weather parameters. The goal was to enable health authorities to proactively manage and allocate resources based on predicted dengue case volumes.

## Data Attributes and Analysis: The dataset includes critical weather-related features, such as:

Temperature Metrics: tempmax, tempmin, temp (average temperature), and feelslike metrics, which measure the maximum, minimum, and average daily temperatures.
Humidity & Dew Point: humidity and dew, which are vital for understanding moisture levels conducive to mosquito breeding.
Precipitation and Cloud Cover: precip (rainfall), cloudcover, and visibility provide insights into rainfall patterns and sunlight exposure, factors that influence mosquito activity.
Solar and UV Metrics: solarradiation, solarenergy, and uvindex help assess conditions that may impact mosquito population dynamics.
Additional Parameters: sealevelpressure, stations, and conditions reflect atmospheric and observational data relevant to disease transmission.
Model Development: Utilizing regression and classification algorithms, the model was trained on these attributes to predict the number of cases (cases) and classify risk levels (labels). By analyzing correlations among environmental factors and dengue case counts, the model offers a predictive tool that aids in understanding the influence of weather on dengue outbreaks.

## Tools & Technologies:

Python: For data preprocessing, model building, and evaluation.
Machine Learning Techniques: Regression analysis and classification algorithms to predict case counts and label risk levels.

This project provides actionable insights into the interplay between weather patterns and dengue prevalence, supporting timely interventions and resource planning in affected areas.
