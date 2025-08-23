# 🌦️ ForecastFlow-ML-Weather-Pipeline

**ForecastFlow is an end-to-end time-series forecasting and analytics pipeline, combines Machine Learning, rolling 7-day predictions on refresh, performance evaluation system, delivered through interactive, insightful Power BI dashboards**.

This project focuses on **Bengaluru (2022–2025)** and uses historical weather data, custom scoring logic, and automated scripts to produce high-accuracy daily forecasts. It's designed to showcase how predictive analytics and BI reporting can work together to deliver real-world insights.

---

## 🚀 Project Highlights
- 🔮**Predicts Bengaluru Weather Metrics**: (Rainfall, Wind, Temp, UV) (2022-25) using **ML Models** (e.g., XGBoost, Random Forest) with historical data.
- 📊 **Interactive Power BI Dashboards**: Visualize **actual vs predicted comparison**, **performance**, **scores**, **deduction logic**, documentation
- 📈 **Model Accuracy Evaluation:** Metrics include **MAE, MAPE, RMSE, NRMSE, Within% (±2,5,10,15)**, and weather condition match rate
- 🧮 **Custom Scoring Engine:** Dynamic performance scoring system from 0 to 30 based on accuracy thresholds
- ⚙️ **Automated Daily Update Script:** Python script generates dynamic 7-day forecasts for Power BI refresh
- 🧩 **Fact-Dimension Data Modeling:** Clean BI architecture using normalized structure

---

## 🧠 Key Features
- **Data Handling** - Trained on 10 years historical data (2010-2021), forecasting ahead (2022-2025).
- **Machine Learning** - machine learning models (XGBoost, Random Forest) for multi-parameter forecasting
- **Forecast vs. actual** - accuracy comparitive evaluation with - Error metrics (MAE, RMSE, MAPE, etc.), Weather match rates (e.g., “Cloudy match rate”).
- **Power BI visual storytelling** -  interactive report, predictions, deviations, insights, dynamic visuals, documentation.
- **Models** - Applies machine learning models (XGBoost, Random Forest) for multi-parameter forecasting
- **Rolling forecast** - Generates rolling 7-day daily forecasts with daily refresh ( currently manual due to free account limitations but possible with scheduled refersh)

---

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
│   ├── report_images/                              # Images of Report Pages
│   │   ├── Report_Data_Model                            
│   │   ├── Page_1_Home
│   │   ├── Page_2_Performance
│   │   ├── Page_2.1_Performance_Deductions
│   │   ├── Page_3_Forecast
│   │   ├── Page_4_Documentation
├── README.md
├── LICENSE
└── .gitignore
```

---
## 🛠️ Tools & Technologies

| Tool/Tech                  | Purpose                                 |
| -------------------------- | --------------------------------------- |
| **Python**                 | Data fetching, cleaning, forecasting    |
| **XGBoost, Random Forest** | ML models for prediction                |
| **Pandas, NumPy**          | Data processing and manipulation        |
| **Power BI**               | Interactive dashboards and scoring      |
| **OpenMeteo API**          | Historical weather data source          |
| **Google Colab**           | Model experimentation and visualization |
| **GitHub**                 | Project hosting & version control       |

---

## 📈 Evaluation Metrics

* **MAE**: Mean Absolute Error
* **MAPE**: Mean Absolute Percentage Error
* **RMSE/NRMSE**: Root Mean Square Error (Normalized)
* **Within % Accuracy**: Predictions within ±2%, 5%, 10%, 15% of actuals
* **Weather Match Rate**: Accuracy for categorical weather types (Clear, Rain, etc.)
* **Scoring System**: Parameters scored 0–30 based on thresholds

---

## 💡 Applications & Use Cases

* Urban planning & smart city dashboards
* Renewable energy & weather-dependent industries
* Model reliability diagnostics, demand prediction, weather risk modeling
* Educational or internal data science case studies
* Extension-ready for real-time, multi-location weather analytics

---

## 📌 Future Enhancements (Optional Ideas)

* Integration with Azure / AWS pipelines
* Expand to multi-city forecasting or hourly data
* Add model explainability (e.g., SHAP, feature importance)
* Incorporate satellite or external weather signals (e.g., El Niño index)

---

## 📖 Data Sources and References
- Open Meteo → Historical data for training and comparison against predicted.
- Weather pdf

---

## 📊 Report Video 

### 🎥 Project Demo Video
[![Watch the demo](https://img.youtube.com/vi/ShHrgLjokH0/0.jpg)](https://youtu.be/ShHrgLjokH0)

### 📊 Visual Reporting (Power BI)

Includes 5 interactive report pages:

1. **Home** – Key summary metrics and high-level visuals  
2. **Performance** – Forecast accuracy and evaluation  
3. **Performance Deductions** – Root cause & drill-downs  
4. **7-Day Forecast** – Auto-updating predictions  
5. **Documentation** – Metric definitions & project logic  


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

## 🤝 Contributing
Contributions and feature requests are welcome! Feel free to open issues or submit pull requests.
