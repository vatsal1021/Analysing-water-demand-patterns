# WaterConsumptionForecasting  
## IIT Kanpur Residential Water Usage Prediction

## 🚀 Project Overview

This project aims to forecast **8-hourly water consumption** across residential buildings at IIT Kanpur (e.g., Hall 12, Hall 10, Hall 6). The goal is to develop reliable regression models that predict usage trends based on **meteorological, calendar-based, and engineered time-series features**. These insights can help optimize water resource allocation and support campus-level sustainability planning.

---

## 📊 Data Description

- **Target Variable:**  
  - Water consumption (in liters) at 8-hour intervals for residential buildings.

- **Features Incorporated:**
  - **Weather-Based:**
    - Temperature  
    - Relative Humidity  
    - Precipitation  
  - **Calendar & Temporal Indicators:**
    - `isday`, `isnight`  
    - `isnormalweekday`, `isholiday`, `isfest`
  - **Engineered Time-Series Features:**
    - Lag values (e.g., previous 8h, 16h, 24h)
    - Rolling window statistics (mean, std, etc.)
  - **Building Identifiers:**
    - One-hot encoded hostel names

---

## 🔁 Workflow Summary

### 1. **Data Collection & Preprocessing**
- Imported raw water usage, calendar, and weather data.
- Merged sources and filled missing values.
- Converted categorical columns to numerical format.
- Engineered lag-based and rolling features for time-series analysis.

### 2. **Exploratory Data Analysis**
- Visualized consumption patterns by hostel and time window.
- Explored feature-target relationships using correlation plots.
- Handled anomalies and skewed distributions.

### 3. **Feature Engineering**
- Generated lagged variables (8h, 16h, 24h).
- Applied rolling window techniques for smoothing.
- Integrated external calendar and weather features.

### 4. **Model Development**
- Divided data into training and validation sets.
- Trained and compared multiple models:
  - Random Forest Regressor  
  - Polynomial Regression (degree 2)
- Applied grid search and cross-validation to tune hyperparameters.

### 5. **Model Evaluation**
- Used **MAPE** (Mean Absolute Percentage Error) as the main evaluation metric.
- **Top model**: Polynomial Regression (degree 2)
- **Achieved validation MAPE**: **6.43%**

### 6. **Visualization & Insights**
- Compared predicted vs. actual water usage.
- Analyzed feature importance and residual patterns.

## Getting Started

1. **Clone the repository:**
    ```
    git clone <[repository-url](https://github.com/vatsal1021/Analysing-water-demand-patterns)>
    ```

2. **Install dependencies:**
    ```
    pip install -r requirements.txt
    ```

---

## Repository Structure

- `data/` — Raw and processed datasets
- `notebooks/` — Jupyter notebooks for EDA and modeling
- `src/` — Python scripts for feature engineering and utilities (optional)
- `README.md` — Project documentation

---

## Results

- **Best Model:** Polynomial Regression (degree 2, "poly2lin")
- **Best MAPE:** 6.5% on validation data

---

## Contact

For questions or collaboration, please contact [Vatsal Mittal] at [vatsalmittal05@gmail.com].

---

## Acknowledgements
- Project inspired by sustainable water management initiatives.

