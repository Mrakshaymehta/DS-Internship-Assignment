# Smart Factory Energy Prediction

This repository contains a machine learning project developed as part of a Data Science Internship Assignment for SmartManufacture Inc. The objective is to build a regression model to forecast equipment energy consumption in a manufacturing facility based on environmental sensor data.

---

## 📌 Problem Statement

The client is experiencing rising energy costs and wants to optimize consumption. Using a sensor network installed across multiple zones, the goal is to predict equipment energy consumption and provide actionable recommendations for operational efficiency.

---

## 📊 Dataset Overview

The dataset includes:

- Indoor temperature and humidity across 9 factory zones
- Outdoor environmental factors (temperature, dew point, humidity, pressure)
- Timestamp for time-based feature extraction
- Equipment and lighting energy consumption
- Two random variables included to test feature selection

---

## 🧠 Approach

### 1. Data Preprocessing
- Removed invalid entries (`'???'`, `'error'`)
- Imputed missing values using median
- Standardized numeric features using `StandardScaler`
- Extracted `hour`, `dayofweek`, and `month` from timestamp
- Dropped irrelevant/random variables after analysis

### 2. Model Development
- Problem type: **Regression**
- Model used: **Random Forest Regressor**
- Justification: Handles non-linear relationships, robust to overfitting, interpretable
- Applied 5-fold cross-validation

---

## 📈 Results

| Metric | Value    |
|--------|----------|
| MAE    | ~66.15   |
| RMSE   | ~158.09  |
| R²     | ~0.07    |

- **Predicted vs Actual** and **Residual plots** used for evaluation.
- Random Forest served as a reliable baseline.

---

## 💡 Recommendations

- Focus HVAC optimization on zones highly correlated with energy use
- Shift heavy-load operations to low-demand hours
- Remove or recalibrate noisy sensors
- Consider advanced models like **XGBoost**, **LightGBM**, or deep learning

---

