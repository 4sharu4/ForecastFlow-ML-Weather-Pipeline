# 🌦️ Bangalore Weather Forecast (2022–2025)

This project is an **end-to-end weather forecasting analysis** for Bangalore.  
It uses **machine learning**, **Python scripting**,**Google collab**, and **Power BI** dashboards to predict weather and evaluate model performance, while supporting dynamic 7-day automated forecasts.

## 🚀 Project Highlights
- Collected and processed historical weather data (2010-21), actual weather data (2022-25) via **Open-Meteo** API using **Python**.
- Forecasted Bengaluru Weather (2022-25) using **ML Models** (e.g., XGBoost, Random Forest)
- Built interactive **Power BI dashboards** for both long-term performance & dynamic short-term (7-day) forecasts to visualize trends, accuracy & insights.
- Evaluated model performance using metrices like  **RMSE, MAE, MAPE, Weather Match Rate, and Within% bands**.
- Implemented Fact-Dimension **data modelling** for clean BI architecture.
- Developed a python script & Forecasted 7-day daily updating dynamic week data.

## 📂 Repository Structure
```text
bangalore-weather-forecast/
├── data/
│   ├── Dimension_CSV/
│   │   ├── Weather_Description.csv                 # Weather codes → readable types
│   ├── Fact_CSV/
│   │   ├── Actual_Weather_22-25.csv                # Actuals for 2022–2025
│   │   ├── Predicted_Weather_22-25.csv             # ML Predictions for 2022–2025
|   ├── PowerBI_Python_Script_CSV/
│   │   ├── bangalore_weather_2015_2025-07-31.csv   # Python, ML - fetching and predicting data
|   ├── PowerBI_Python_Script/
│   │   ├── Week_Predicted_Data.py                  # 7day updating weather data PowerBI python script
│   Google_Collab_Python/
│   ├── Weather_Analysis_Project.ipynb              # Python, ML - fetching and predicting data
├── docs/
│   ├── documentation.md                            # Metric definitions & model logic
├── report/
│   ├── Weather_Forecasting_Report.pbix             # Power BI report
│   ├── Report_Content/                             # Video & PDF of the report, interactivity
├── README.md
├── LICENSE
└── .gitignore
```

## 🛠️ Tools & Technologies
- **Power BI** → Data visualization & dashboards
- **GitHub** → Project hosting & version control
- **Python / ML** (optional extension) → Forecasting models
- **Google Collab** → To test, train and predict data, to download historical data.

## 📊 Use Cases & Applications

* Showcases end-to-end integration of **ML forecasting** with **BI reporting**.
* Adaptable for domains like **logistics**, **urban planning**, or **climate analytics**.
* Scalable to **multi-region forecasts** and **real-time data pipelines**.
* Forms a foundation for solutions in **demand prediction**, **weather risk modeling**, and more.

## 📖 Data Sources  
- Open Meteo → Historical data for training and comparison against predicted.
- Weather descriptions mapping (dimension table) → clear, rainy, codes, image, etc.
- Weather Variable Parameter → temp, wind, solar, precip, etc.

## 📐 Evaluation Metrices
- **MAE** (Mean Absolute Error)
- **MAPE** (Mean Absolute Percetnage Error)
- **NRMSE** (Normalized Root Mean Square Error)
- **Within % ±2%, 5%**, etc. ( Data within % of error)
- **Weather Match Rate** (e.g. - Cloudy Match rate etc.)
- **Scorecard** (Scored weather parameters on custom thresholds)

## 📊 Report ScreenShots / Video / PPT


➡️ Full metric logic is documented in docs/documentation.md


## 🖥️ Set up instructions & Pre-requisites
### ✅ Pre-requisites: 
Make sure the following are installed on your local machine:
- **Python** (with required modules: `pandas`, `requests`, etc.)
- **Power BI Desktop**
### ⚙️ Set up steps:
- **Download** the `.pbix` file from the repository -  * `reports/Weather_Forecast_Dashboard.pbix`
- **Open** the file using **Power BI Desktop** and **Refresh**

## 📜 License  
This project is licensed under the [MIT License](LICENSE).

## 📝 How to Use
1. Clone this repo:
   ```bash
   git clone https://github.com/your-username/bangalore-weather-forecast.git
