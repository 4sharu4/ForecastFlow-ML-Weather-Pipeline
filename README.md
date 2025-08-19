# 🌦️ Bangalore Weather Forecast (2022–2025)

This project is an **end-to-end weather forecasting analysis** for Bangalore.  
It combines **historical weather data**, **predicted weather data**, **dimension tables** and a 7-day automation update **forecast-data** to build insights and Power BI dashboards.

## 📂 Repository Structure
```text
bangalore-weather-forecast/
├─ data/
│  ├─ Facts_CSV/ 
│  │  ├─ Actual_Weather_22-25.csv        # Historical weather (2022–2025)
│  │  ├─ Predicted_Weather_22-25.csv     # Forecasted weather (2022–2025)
│  ├─ Dimension_CSV/
│  │  ├─ Weather_Description.csv         # Lookup table for weather codes
├─ docs/ # Documentation
├─ reports/ # Power BI dashboards
├─ notebooks/ # Python / Jupyter notebooks
├─ README.md # Project overview
├─ LICENSE # Open-source license
└─ .gitignore # Ignored files
```

## 🚀 Project Highlights
- Collected actual and predicted weather data for Bangalore through Python & ML.
- Organized data into **Fact** and **Dimension** tables (data warehouse style).
- Built **Power BI dashboards** to visualize:
  - Temperature trends
  - Rainfall & precipitation
  - Wind speed and gust patterns
  - Weather condition predictions
- Evaluated accuracy using **RMSE, MAE, MAPE, and Within% metrics**.
- Forecasted 7-day daily updating dynamic week data.

## 🛠️ Tools & Technologies
- **Power BI** → Data visualization & dashboards
- **GitHub** → Project hosting & version control
- **Python / ML** (optional extension) → Forecasting models
- **Google Collab** → To test, train and predict data, to download historical data.

## 📊 Example Use Cases
- Show weather prediction performance to demonstrate **forecasting skills**.
- Display **data modeling concepts** (Fact vs. Dimension).
- Report and Data can be relied on and developed into Actual Weather App.

## 📖 Data Sources  
- Open Meteo → Historical data for training and comparison against predicted.
- Weather descriptions mapping (dimension table) → clear, rainy, codes, image, etc.
- Weather Variable Parameter → temp, wind, solar, precip, etc.

## 📊 Report ScreenShots / Video / PPT

## 📜 License  
This project is licensed under the [MIT License](LICENSE).

## 🚀 How to Use
1. Clone this repo:
   ```bash
   git clone https://github.com/your-username/bangalore-weather-forecast.git
