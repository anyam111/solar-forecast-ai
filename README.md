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

# 🔋 Solar Energy Forecasting with Machine Learning

This project builds a predictive model using historical solar production data from two inverters (Inv 0 and Inv 1) to forecast future solar energy generation for the next 30 days. It was developed and tested in Google Colab using Python, scikit-learn, and visualized with Matplotlib.

---

## 🚀 Project Objectives

- Analyze inverter-wise energy production
- Train machine learning models to predict daily energy output
- Forecast next 30 days of solar production (Psum) for both inverters
- Visualize and export predictions for analysis and reporting

---

## 📚 Dataset

The dataset contains daily aggregated solar production from two inverters:


- `#Date`: Date of reading (dd/mm/yy)
- `Inv`: Inverter number (0 = total, 1 = sub-inverter)
- `Psum`: Total energy generated that day (Wh)
- `Pmax`: Maximum power recorded (unused in this version)

---

## ⚙️ Steps Performed

1. **Data Cleaning & Preparation**
   - Uploaded `.csv` and `.xls` files in Google Colab
   - Parsed dates and numeric columns
   - Split data by `Inv 0` and `Inv 1`

2. **Feature Engineering**
   - Created `Day`, `Month`, `Weekday`, `Prev_Psum`, and 3-day rolling average

3. **Model Building**
   - Trained `RandomForestRegressor` for each inverter
   - Validated performance with Mean Absolute Error (MAE)

4. **Forecasting**
   - Predicted solar energy for the next 30 days
   - Used previous predictions to simulate future rolling averages

5. **Visualization**
   - Plotted actual vs predicted and 30-day forecast

6. **Exporting & Sharing**
   - Exported `.ipynb` notebook
   - Uploaded to GitHub with README and data

---

## 🧪 Technologies Used

- Python 3
- Google Colab (for development)
- Pandas (data handling)
- scikit-learn (ML)
- Matplotlib (visualization)

---

## 📈 Example Forecast Output

| Date       | Inv 0 Forecast (Wh) | Inv 1 Forecast (Wh) |
|------------|---------------------|---------------------|
| 2025-07-01 | 7862.18              | 2307.16             |
| 2025-07-02 | 10094.11             | 2310.48             |
| ...        | ...                  | ...                 |

---

├── solar_forecast_30days.ipynb   # Main Colab notebook
├── data/
│   └── export_day.csv            # Daily solar data
├── README.md
## 💡 How to Run

### Option 1: Google Colab (Recommended)
1. Open `solar_forecast_30days.ipynb` in Colab
2. Upload `export_day.csv` (from your `data/` folder)
3. Run all cells

### Option 2: Local (Jupyter Notebook)
```bash
pip install pandas scikit-learn matplotlib
jupyter notebook
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
