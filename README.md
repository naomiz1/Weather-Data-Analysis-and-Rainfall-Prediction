# Weather Data Analysis and Rainfall Prediction

## Project Overview
This project focuses on predicting whether it will rain on the next day using historical weather data. The goal is to build a reliable classification model that can capture patterns in temperature, precipitation, and atmospheric conditions.

The dataset contains daily weather observations, and the project includes data cleaning, feature engineering, exploratory data analysis, and machine learning modeling.

---

## Dataset
- Source: Daily weather data (New York Central Park station)
- Features include:
  - Temperature (TMAX, TMIN, TAVG)
  - Precipitation (PRCP)
  - Wind (AWND, WSF2, WSF5)
  - Weather indicators (fog, snow, etc.)
- Target variable:
  - `RainTomorrow` (binary classification)

---

## Data Processing
- Converted date columns into datetime format
- Handled missing values:
  - Interpolation for temperature and wind
  - Zero-filling for precipitation and snow
- Removed irrelevant columns
- Created new features:
  - Lag variables (e.g., PRCP_lag1)
  - Rolling averages
  - Seasonal features (Month, DayOfYear)

---

## Exploratory Data Analysis
- Identified strong correlations among temperature variables
- Found class imbalance (about 70% no rain, 30% rain)
- Observed seasonal patterns in rainfall probability
- Confirmed that previous-day rainfall strongly affects future rainfall

---

## Models Used
- Logistic Regression (L1 & L2)
- Decision Tree
- Random Forest

---

## Model Performance
| Model            | Accuracy | Recall | AUC  |
|-----------------|---------|--------|------|
| Logistic Reg    | 0.65    | 0.25   | 0.60 |
| Decision Tree   | 0.60    | 0.23   | 0.53 |
| Random Forest   | 0.63    | 0.38   | 0.60 |

- Random Forest achieved the best balance between accuracy and recall
- Recall is emphasized due to importance of detecting rainfall events

---

## Key Insights
- Lag features (e.g., yesterday's rain) are highly predictive
- Temperature and seasonal patterns significantly influence rainfall
- Ensemble models outperform linear models in this problem

---

## Future Improvements
- Use advanced models (e.g., LSTM for time series)
- Add external features (humidity, pressure, satellite data)
- Address class imbalance with resampling techniques

---

## Tech Stack
- Python (Pandas, NumPy)
- Scikit-learn
- Matplotlib / Seaborn

---

## Author
Xumeng Zhang (Naomi)  
Columbia University | MS Business Analytics
