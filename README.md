# 🌍 Global Weather Trend Forecasting

A machine learning project for forecasting global weather trends using historical weather observations, environmental indicators, geographical information, and time-based feature engineering.

## 📌 Project Overview

This project analyzes a global weather dataset and builds multiple machine learning models to predict weather conditions, with a primary focus on temperature forecasting.

The workflow includes:

* Data cleaning and preprocessing
* Anomaly detection
* Exploratory Data Analysis (EDA)
* Feature engineering
* Spatial and climate analysis
* Machine learning model training
* Ensemble learning
* Model comparison and evaluation

The project demonstrates a complete end-to-end machine learning pipeline from raw weather data to production-style forecasting models.

---

## 🎯 Objectives

* Analyze global weather patterns.
* Clean and preprocess real-world environmental data.
* Engineer meaningful temporal and geographical features.
* Compare multiple machine learning algorithms.
* Build an ensemble model for improved forecasting accuracy.
* Identify the most influential weather predictors.

---

## 📊 Dataset

Dataset Source:

Global Weather Repository Dataset

The dataset contains weather observations from locations around the world, including:

### Weather Features

* Temperature
* Humidity
* Pressure
* Wind Speed
* Wind Direction
* Cloud Cover
* Visibility
* UV Index
* Precipitation

### Air Quality Features

* PM2.5
* PM10
* Carbon Monoxide (CO)
* Nitrogen Dioxide (NO₂)
* Sulfur Dioxide (SO₂)
* Ozone (O₃)

### Geographical Features

* Latitude
* Longitude
* Country
* Location Name

### Time Features

* Last Updated Timestamp
* Date and Time Components

---

## 🛠 Data Cleaning & Preprocessing

Several preprocessing techniques were applied:

### Missing Values

* Dataset checked for null values.
* Dataset checked for duplicated records.

### Invalid Sensor Readings

Physically impossible values such as:

* Negative Carbon Monoxide
* Negative Sulfur Dioxide

were treated as sensor errors and corrected through interpolation techniques.

### Multicollinearity Removal

Highly correlated and redundant variables were removed to:

* Reduce noise
* Improve model stability
* Prevent information leakage

### Anomaly Detection

Both univariate and multivariate anomaly detection techniques were applied to identify unusual weather observations.

---

## ⚙️ Feature Engineering

Feature engineering significantly improved model performance.

### Time-Based Features

Extracted from timestamps:

* Hour
* Day of Week
* Month

### Cyclical Encoding

To preserve cyclical relationships:

* Hour Sin
* Hour Cos
* Month Sin
* Month Cos

This helps models understand that:

23:00 is close to 00:00

instead of treating them as distant values.

### Lag Features

Temperature memory was introduced using:

temp_lag_1

which represents the previous temperature reading for a given location.

---

## 🌎 Spatial & Climate Analysis

Several geographical analyses were performed:

### Country-Level Climate Comparison

* Average temperatures
* Humidity trends
* Air quality comparison

### Global Temperature Mapping

Interactive visualizations were used to observe:

* Hot regions
* Cold regions
* Geographical temperature distribution

### Environmental Impact Analysis

Relationships explored:

* PM2.5 vs Humidity
* PM2.5 vs Wind Speed

---

## 🤖 Machine Learning Models

The following models were trained and compared:

### 1. XGBoost

Advantages:

* Handles nonlinear relationships
* High predictive performance
* Feature importance analysis

---

### 2. Random Forest Regressor

Advantages:

* Strong baseline model
* Robust to noise
* Easy interpretation

---

### 3. LightGBM

Advantages:

* Fast training
* Efficient memory usage
* Excellent performance on tabular data

---

### 4. CatBoost

Advantages:

* Strong handling of categorical variables
* Reduced preprocessing requirements
* High accuracy

---

### 5. Ridge Regression

Used as a linear baseline model.

Provides insight into whether relationships are primarily linear or nonlinear.

---

### 6. Neural Network

A feed-forward neural network was trained to learn complex weather relationships.

Capabilities:

* Nonlinear pattern learning
* High-dimensional feature interactions
* Deep feature extraction

---

## 🔥 Ensemble Model

A weighted ensemble was created by combining predictions from multiple models.

Benefits:

* Reduced variance
* Better generalization
* Improved prediction accuracy

The ensemble achieved the best overall performance among all tested approaches.

---

## 📈 Evaluation Metrics

Models were evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score

These metrics provide insight into:

* Prediction accuracy
* Error magnitude
* Overall model quality

---

## 📌 Key Findings

### Data Quality

* Sensor-generated anomalies were successfully identified and corrected.
* Redundant variables were removed to improve model efficiency.

### Environmental Insights

* PM2.5 generally decreases as wind speed increases.
* Humidity exhibits complex interactions with air quality.

### Geographical Insights

* Latitude strongly influences temperature.
* Equatorial regions remain consistently warmer.
* Higher latitude regions exhibit lower average temperatures.

### Forecasting Insights

* Previous temperature observations are highly predictive.
* Geographic location remains one of the strongest predictors.
* Ensemble learning consistently outperformed individual models.

---

## 📂 Project Structure

```text
Global-Weather-Trend-Forecasting/
│
├── data/
│   └── GlobalWeatherRepository.csv
│
├── notebooks/
│   └── weather-trend-forecasting.ipynb
│
├── models/
│   └── saved_models/
│
├── visualizations/
│   └── plots/
│
├── README.md
│
└── requirements.txt
```

## 🚀 Technologies Used

### Programming Language

* Python

### Data Analysis

* Pandas
* NumPy

### Visualization

* Matplotlib
* Seaborn
* Plotly

### Machine Learning

* Scikit-Learn
* XGBoost
* LightGBM
* CatBoost

### Deep Learning

* TensorFlow / Keras

---

## Future Improvements

* Weather forecasting horizons (1-day, 3-day, 7-day ahead)
* Advanced neural architectures (LSTM, GRU, Transformer)
* Geospatial clustering
* Real-time weather API integration
* Model deployment using FastAPI
* Interactive dashboard using Streamlit

---

## Author

Lalit Mishra

Machine Learning & AI Enthusiast

Focused on:

* Machine Learning
* Deep Learning
* Search Systems
* Forecasting Models
* Artificial Intelligence Research
