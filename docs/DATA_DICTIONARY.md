# 📖 Project Documentation: Bengaluru Weather Forecast (2010–2025)

This project is an end-to-end weather forecasting and reporting system for **Bangalore, India**, combining Python-based data science workflows with Power BI visualization.

---

## 📌 Objective

To simulate a **real-world weather application** that:

* Forecasts Bengaluru weather with daily updates,
* Evaluates and compares predictions to actuals,
* Presents insights through an interactive Power BI dashboard,
* Demonstrates ML, data engineering, and BI integration skills.

---

## 🔁 End-to-End Workflow Overview

| Step                     | Description                                                                                                  |
| ------------------------ | ------------------------------------------------------------------------------------------------------------ |
| **1️⃣ Fetch Data**       | Download historical weather data (2010–2025) using Open-Meteo API via Python (Google Colab)                  |
| **2️⃣ Clean & Format**   | Preprocess data: parse dates, handle missing values, and create features like `dayofyear`, `year`            |
| **3️⃣ Train Models**     | Use **Random Forest** and **XGBoost** models to forecast temperature, wind, precipitation, and weather types |
| **4️⃣ Forecast**         | Predict weather for **2022–2025** and generate **daily-updated 7-day forecasts** (Today + 6 days)            |
| **5️⃣ Export Outputs**   | Save predictions as CSV files and **upload to GitHub** for online access                                     |
| **6️⃣ Connect Power BI** | Use **Power Query** in Power BI to connect to GitHub CSV URLs for dynamic data refresh                       |
| **7️⃣ Build Dashboard**  | Visualize forecast accuracy, weather trends, and live forecasts through interactive Power BI pages           |

---

## 🧱 Data Pipeline

### 📥 Data Collection

* Used **Open-Meteo API** via Python (in Google Colab) to collect:

  * Historical data: `2010–2021` → for training.
  * Actuals: `2022–Jan 2025` → for validation.
  * Ongoing dynamic data: `2015–2025-07-31` → for 7-day forecasts.

### 🧹 Preprocessing

* Parsed and cleaned datasets: removed nulls, formatted dates, created features:

  * `dayofyear`, `year`, etc.
* Generated **Fact** and **Dimension** tables for BI reporting:

  * Fact: actual vs. predicted data
  * Dim: weather descriptions, date attributes

---

## 🤖 Machine Learning Models

### Models Used

| Target                                         | Model                   |
| ---------------------------------------------- | ----------------------- |
| `temperature_2m_min/max/mean`                  | Random Forest Regressor |
| `windspeed_10m_max`, `precipitation_sum`, etc. | Random Forest Regressor |
| `Weather Type`                                 | XGBoost Classifier      |

### Forecasting Logic

* Models are trained on past 10 years' data up to today.
* Every day, new predictions are made for **today + next 6 days**.
* Results are saved into `Weekly_7Day_Forecast.csv`.

---

## 📊 Dashboard Overview – Power BI

This Power BI dashboard presents an interactive weather forecasting analysis for **Bangalore (2022–2025)** using historical and predicted data. The dashboard is structured across multiple pages to help users explore the forecast accuracy, weather trends, and prediction insights effectively.

---
## 📖 Power BI Model

### Facts_CSV
- **Actual_Weather_22-25.csv** → Historical observed weather data (2022–2025).
- **Predicted_Weather_22-25.csv** → Model-generated forecasts for same period.
- **Week_Predicted_Data** → Model-generated forecasts for 7 days everyday updated.

### Dimension_CSV
- **Weather_Description.csv** → Lookup table mapping weather codes to human-readable descriptions (e.g., 0 = Clear, 1 = Partly Cloudy).
- **Date Table** → A commom table for dates and all its formats
  
---

### 🗂️ Pages & Descriptions

| Page              | Description                                                                     |
| ----------------- | ------------------------------------------------------------------------------- |
| **Home**          | Project introduction, methodology, and navigation guide for the dashboard       |
| **Performance**   | Forecasting accuracy evaluation using metrics like RMSE, MAE, MAPE, and Within% |
| **Forecast**      | Dynamic 7-day live-style forecast for Bengaluru with daily updating insights    |
| **Documentation** | Definitions and explanations of model evaluation metrics and scoring systems    |

---

### 📈 Visualized Insights

The dashboard delivers rich visual insights through graphs, cards, KPIs, and slicers.

#### 🌡️ Temperature Trends

* Track maximum, minimum, and average temperatures across months and years.
* Identify heatwaves, cooling trends, and seasonal patterns.

#### 🌧️ Rainfall & Precipitation

* Analyze total and average precipitation across different periods.
* Compare predicted vs. actual rainfall to assess forecasting quality.

#### 💨 Wind Speed & Gusts

* View trends in wind speed and gust intensity over time.
* Monitor calm vs. windy days and identify outliers.

#### 🔄 Weather Type Predictions

* Daily-level predictions for weather types: Clear, Rain, Drizzle, Thunderstorm, etc.
* Uses classification-based forecasting mapped with actuals for accuracy comparison.

#### 📉 Forecast Accuracy Metrics

| Metric                 | Description                                              |
| ---------------------- | -------------------------------------------------------- |
| **MAE**                | Mean of absolute prediction errors                       |
| **MAPE**               | Percentage-based error metric                            |
| **RMSE / NRMSE**       | Measures spread and scale-normalized error               |
| **Within% Bands**      | Shows what % of predictions are within ±2%, 5%, etc.     |
| **Weather Match Rate** | How well forecasted weather types match actuals          |
| **Scoring System**     | Converts each metric to a 0–10 score for easy comparison |


---

📌 *Tip:* Use filters to explore weather patterns by **Year-Quarter**, **Weather Parameters** like temp, wind, etc.

---

## 📊 Dashboard Integration (Power BI)

* **Power BI** connects to GitHub-hosted CSVs via **Power Query**.
* Refreshing the report updates:

  * Actuals (2022–2025)
  * Forecasts (next 7 days)
  * Model evaluation metrics

---

## 🗃️ Github Folder & Script Structure

```bash
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
---

## ⚙️ Setup Instructions (Recap)

> See full setup guide in `README.md`

* Requires: `Python`, `Power BI Desktop`
* Download `.pbix` → Open in Power BI → Click **Refresh**
* Python scripts can be run in Colab or locally to update forecasts

---

## 💡 Key Project Features

* Full-cycle project: data → ML → dashboard
* Live-style **7-day forecast**
* Weather type **classification + evaluation**
* Real-world use of **Fact/Dimension modeling**
* Daily-refresh-ready (with automation potential)

---

## 📌 Use Cases & Applications

* Showcases end-to-end integration of **ML forecasting** with **BI reporting**.
* Adaptable for domains like **logistics**, **urban planning**, or **climate analytics**.
* Scalable to **multi-region forecasts** and **real-time data pipelines**.
* Forms a foundation for solutions in **demand prediction**, **weather risk modeling**, and more.



