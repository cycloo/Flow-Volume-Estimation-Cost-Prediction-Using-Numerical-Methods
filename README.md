# Flow Volume Estimation & Cost Prediction Using Numerical Methods

This project processes flowmeter log data to correct invalid readings, estimate daily fluid volume, calculate usage costs, and forecast future consumption using numerical analysis. It demonstrates practical applications of interpolation, integration, and linear regression on real sensor-based time-series data.

---

## Features

- Data Cleaning  
  Repairs negative or corrupted sensor values using a custom numerical interpolation method.

- Volume Calculation  
  Computes daily fluid volume based on flow-rate data and pipe cross-sectional area.

- Cost Estimation  
  Applies tier-based pricing to calculate daily and weekly usage cost.

- Forecasting  
  Predicts 21 future days of fluid consumption using linear regression.

- Date-Range Filtering  
  Extracts data within user-defined start and end dates.

---

## Methods Used

### 1. Numerical Interpolation
Fixes invalid flow-rate values by analyzing surrounding valid points and applying a Lagrange-based estimation method. Outlier suppression is used to maintain physically realistic results.

### 2. Numerical Integration
Converts flow-rate data into volume using the formula:  

### 3. Linear Regression
Fits a linear model based on the first 7 days of volume data to predict the next 21 days.

### 4. Daily Aggregation
Groups time-stamped flow data by calendar day for volume and cost calculations.

---

## Technologies

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Scikit-learn  
- Babel (currency formatting)

---

## How to Run

1. Place your dataset file in the working directory:  
   `log_level_out_mini.csv`

2. Run the script:  
   ```bash
   python main.py
