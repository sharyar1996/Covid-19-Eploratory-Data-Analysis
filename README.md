# 🦠 COVID-19 Global Time-Series Analysis

This project analyzes the global spread of COVID-19 using time-series case data. It includes exploratory data analysis, time-based aggregations, data cleaning, and visualizations to better understand infection patterns across countries.

## 📊 Features

- 🧹 **Data Cleaning**  
  - Handling missing latitude/longitude values
  - Merging provincial data into unified country-level data

- 📈 **Time-Series Analysis**
  - Cumulative and daily new confirmed cases
  - Recovery ratios and comparison between confirmed vs recovered cases
  - Peak day identification for individual countries

- 📉 **Visualizations**
  - Multi-country line plots of confirmed cases over time
  - Bar charts comparing recovery performance
  - Annotated peaks and labels for maximum case days

## 🔧 Technologies Used

- **Python 3**
- **Pandas** – Data manipulation
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization

## 📁 Dataset

Used publicly available COVID-19 time-series datasets from [Johns Hopkins University](https://github.com/CSSEGISandData/COVID-19) containing daily case reports from January 2020 to May 2021.

- Columns: Province/State, Country/Region, Lat, Long, daily dates
- 10,000+ rows × 200+ date columns

## 📌 Key Insights

- Top 10 countries by confirmed cases and recovery rate
- Daily case spikes visualized per country
- Differences in reporting granularity (country vs province) handled with aggregation logic

## 🧪 Example Functions

```python
def get_daily_new_cases_for_each_country(country, dataframe):
    # Computes daily case deltas from cumulative case time series
