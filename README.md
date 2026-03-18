# Weather Data Analysis (SoftGrowTech)

This repository contains a Jupyter notebook that performs exploratory data analysis (EDA) on a historical weather dataset to uncover patterns in temperature, humidity, and weather conditions.

---

## Repository Contents
- `Weather Data Analysis.ipynb` – Main analysis notebook. Loads the dataset, cleans/structures the data, computes trends, and generates visualizations.
- `Weather Dataset.csv` – Hourly historical weather observations (temperature, humidity, pressure, visibility, wind speed, and reported weather conditions).

---

##  Dataset Overview
The dataset includes hourly observations with the following key fields:
- `Date/Time`: Timestamp of the observation (hourly granularity).
- `Temp_C`: Temperature in degrees Celsius.
- `Dew Point Temp_C`: Dew point temperature in degrees Celsius.
- `Rel Hum_%`: Relative humidity percentage.
- `Wind Speed_km/h`: Wind speed in kilometers per hour.
- `Visibility_km`: Visibility distance in kilometers.
- `Press_kPa`: Atmospheric pressure in kilopascals.
- `Weather`: Description of observed weather conditions (e.g., Fog, Cloudy, Mainly Clear).

---

## Setup & Run
### 1) Create / activate a Python environment
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
```

### 2) Install dependencies
```bash
pip install pandas matplotlib seaborn
```

### 3) Open and run the notebook
- Open `Weather Data Analysis.ipynb` in VS Code, Jupyter Lab, or any compatible notebook environment.
- Run cells sequentially to load the data, generate plots, and inspect results.

---

## Notebook Structure
The notebook is organized into the following sections:
1. **Load the data** – read the CSV and inspect the first rows.
2. **Exploratory Data Analysis** – data shape, data types, summary statistics, and value counts.
3. **Visualizations**
   - Distribution plots for temperature and humidity.
   - Time series plots for temperature and humidity.
   - Monthly average trends to highlight seasonality.
   - Scatter plot to inspect temperature vs humidity relationship.
   - Bar plot showing top weather conditions.
4. **Insights** – summary of key patterns and takeaways.

---

## Key Insights (What the analysis reveals)
- **Seasonal Temperature Variation**: Temperatures are lowest in winter (typically Jan–Mar) and highest in summer (Jun–Aug).
- **Humidity Seasonality**: Humidity is generally higher in colder months and lower in warmer ones.
- **Temperature vs. Humidity**: The dataset shows an inverse relationship—warmer periods tend to have lower humidity.
- **Common Weather Conditions**: The most frequent conditions are *Mainly Clear*, *Cloudy*, and *Fog*.

---

## Next Steps / Extensions
- Compare year-over-year changes if multiple years are added.
- Add additional weather variables (e.g., wind speed, pressure) to explore correlations.
- Build forecasting models (ARIMA/Prophet) for temperature or humidity.
- Add interactive visualizations with `plotly` or `altair`.

---

## Notes
- The notebook converts `Date/Time` into a pandas `DatetimeIndex` to facilitate time series analysis.
- Monthly averages are computed using `.resample('ME').mean()`.
- If you add new data, ensure the timestamp format matches the existing dataset.
