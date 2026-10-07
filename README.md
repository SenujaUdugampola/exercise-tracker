# 🏋️‍♂️ Fitness Tracker: Barbell Exercise Classification

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)

## 📌 Overview
This repository contains an end-to-end Machine Learning project that processes sensor data (accelerometer and gyroscope) to automatically classify different barbell exercises and count repetitions. 

This project was built following the [Full Machine Learning Project series by Dave Ebbelaar](https://youtube.com/playlist?list=PL-Y17yukoyy0sT2hoSQxn1TdV0J7-MX4K) and is structured using the [Datalumina Data Science Template](https://github.com/daveebbelaar/data-science-template).

## 🚀 The Machine Learning Pipeline

The project is broken down into several core stages of a professional data science workflow:

1. **Data Processing:** Ingesting raw MetaMotion sensor data, handling timestamps, and merging accelerometer and gyroscope datasets.
2. **Data Visualization:** Using Matplotlib to visually explore exercise patterns and sensor axes.
3. **Outlier Detection:** Identifying and handling anomalies and noise in the raw sensor data using statistical methods.
4. **Feature Engineering:** 
   - *Temporal Abstraction:* Using rolling windows to compute statistical properties over time.
   - *Frequency Abstraction:* Applying Fast Fourier Transformations (FFT) to extract frequency domain features.
   - *Clustering:* Using K-Means to group similar data points.
5. **Predictive Modeling:** Splitting data, applying forward feature selection, and using Grid Search to tune hyperparameters for classification models (Decision Trees, Random Forests) to accurately identify the specific exercise being performed.
6. **Repetition Counting:** Implementing peak detection algorithms to count the number of reps per set.

## 📂 Project Structure

This project follows a logical, standardized structure for data science work:

```text
├── data            <- Raw, intermediate, and processed data (ignored by git)
├── models          <- Trained and serialized models
├── notebooks       <- Jupyter notebooks for step-by-step exploration
├── references      <- Data dictionaries and explanatory materials
├── reports         <- Generated analysis
│   └── figures     <- Generated graphics and Matplotlib figures
├── src             <- Source code for this project
│   ├── __init__.py <- Makes src a Python module
│   ├── config.py   <- Store useful variables and configuration
│   ├── dataset.py  <- Scripts to download or generate data
│   ├── features.py <- Code to build temporal and frequency features
│   └── models.py   <- Code to train models and make predictions
├── .env.example    <- Example of environment variables
├── .gitignore      <- Excludes data and trained models from source control
├── pyproject.toml  <- Project configuration and dependencies
└── README.md       <- The top-level README for developers using this project.
