# ☀️ Solar Production Forecasting using Machine Learning

This project uses historical solar inverter data to predict future power production for the next 30 days using machine learning (Random Forest). The data is separated for two inverters (`Inv 0` and `Inv 1`), and predictions are made individually.

---

## 📊 Key Features

- 🔄 Forecast solar production 30 days ahead
- 📅 Time-series based feature engineering
- 🧠 Random Forest Regressor model
- 📈 Matplotlib visualization of actual vs predicted values
- 🧪 Developed and tested in Google Colab

---

## 📁 Files

| File | Description |
|------|-------------|
| `solar_forecast_30days.ipynb` | Main notebook with data loading, model training, and 30-day forecasting |
| `export_day.csv` | Daily solar data used as input (sample format required) |

---

## 🧠 How It Works

1. Load historical solar data (`Psum`, `Pmax`, `Date`, `Inv`)
2. Engineer time-based features: day, month, weekday, previous production, rolling average
3. Train separate Random Forest models for each inverter
4. Predict next 30 days by simulating one day at a time
5. Visualize results with Matplotlib

---

## 📎 Example Forecast Output

| Date       | Inv 0 Forecast (Wh) | Inv 1 Forecast (Wh) |
|------------|---------------------|---------------------|
| 2025-07-01 | 7862.18              | 2307.16             |
| 2025-07-02 | 10094.11             | 2310.48             |
| ...        | ...                  | ...                 |

---

## 🚀 How to Run

### Option 1: Run in Google Colab
1. Open the notebook in [Colab](https://colab.research.google.com)
2. Upload `export_day.csv`
3. Run all cells

#Date;Inv;Psum;Pmax
1/7/25;0;36378;0
1/7/25;1;3799;0


### Option 2: Run Locally (Jupyter)
```bash
pip install pandas matplotlib scikit-learn
jupyter notebook
