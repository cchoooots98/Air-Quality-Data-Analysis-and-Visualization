# Air Quality Data Analysis and Visualization in MATLAB

This project analyzes and visualizes urban air pollution data using MATLAB, focusing on identifying trends, outliers, seasonal patterns, and relationships between pollutants and environmental variables. The dataset is sourced from the [UCI Machine Learning Repository - Air Quality Dataset](https://archive.ics.uci.edu/ml/datasets/Air+Quality).

---

## 📊 Objectives

- Import and clean air quality data in MATLAB.
- Perform exploratory data analysis (EDA) to detect trends, anomalies, and seasonality.
- Visualize pollutant levels and their relation to environmental variables (e.g., temperature, humidity).
- Build a linear regression model to predict pollutant levels based on sensor outputs and meteorological factors.

---

## 🗂 Dataset

- **Source**: [UCI Machine Learning Repository - Air Quality Data Set](https://archive.ics.uci.edu/ml/datasets/Air+Quality)
- **Time Range**: March 2004 – April 2005 (Italian city)
- **Format**: CSV with hourly averages of pollutant levels, sensor signals, temperature, and humidity.
- **Missing Values**: Represented as `-200`

---

## 🔁 Project Workflow

### 1. 📥 Data Acquisition & Cleaning
- Load CSV data using `readtable`.
- Merge `Date` and `Time` into a unified `Datetime` column.
- Replace missing values (`-200`) with `NaN`.
- Drop invalid rows and rename variables for clarity.

### 2. 📈 Exploratory Data Analysis (EDA)
- Plot time series of pollutants and monthly statistics.
- Detect patterns and seasonality using autocorrelation.
- Identify outliers using the IQR method.

### 3. 🧪 Outlier Detection
- Detect and visualize outliers for:
  - Periodic variables (e.g., `CO(GT)`, `NOx(GT)`, sensor responses)
  - Non-periodic variables (e.g., `NMHC(GT)`, `PT08.S5(O3)`)
- Mark outliers on time series plots.

### 4. 📌 Correlation & Heatmaps
- Generate scatter plot matrix between pollutants, sensors, and environmental data.
- Compute Pearson correlation matrix and display as heatmap.
- Create heatmaps of pollutant levels based on temperature and humidity bins.

### 5. 📉 Predictive Modeling
- Build a multiple linear regression model to predict `CO(GT)` using:
  - `PT08.S1(CO)` (sensor response)
  - Temperature (`T`)
  - Relative Humidity (`RH`)
- Evaluate performance using R-squared and RMSE.
- Plot predicted vs. actual values.

---

## 📂 File Structure
📁 air_quality/
├── AirQualityUCI.csv           # Raw dataset
├── airQualityAnalysis0808.mlx  # Main live script (EDA + modeling)
└── results/
    └── summary.pdf             # Brief findings report 

---

## 📌 Requirements

- MATLAB R2021a or newer (Live Script compatible)
- Toolboxes:
  - Statistics and Machine Learning Toolbox
  - Signal Processing Toolbox (for autocorrelation)

---

## ✅ Deliverables

- MATLAB code with comments and documentation  
- Visualization plots (in `.mlx` and images)  
- Short report summarizing insights  

---

## 📘 Notes

- Dataset contains both ground truth measurements and raw sensor outputs.
- Alternative datasets (e.g., [EPA Air Quality Data](https://aqs.epa.gov/aqsweb/airdata/download_files.html)) may be used with minor adjustments.
- Suitable for education, research, and environmental data analytics.

---

## 💡 Future Work

- Apply STL or Fourier methods for seasonal decomposition.
- Use advanced models (ARIMA, LSTM) for time series forecasting.
- Add PCA for dimensionality reduction before modeling.

---

## 📬 Contact

Feel free to submit an issue or reach out for collaboration or suggestions.



