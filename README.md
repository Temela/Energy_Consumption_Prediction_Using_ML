# Energy Consumption Prediction Using Machine Learning

![Python](https://img.shields.io/badge/python-3.9-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Status](https://img.shields.io/badge/status-completed-lightgrey.svg)

> ⚡ Forecasting energy usage from historical data using supervised regression models like Random Forest and XGBoost. This project helps utility managers reduce inefficiencies and plan better.

---

## 🔍 Project Overview

- **Type**: Supervised Machine Learning – Regression
- **Goal**: Predict daily power consumption values and evaluate forecasting accuracy
- **Dataset**: Public power consumption data from [UCI Machine Learning Repository](https://archive.ics.uci.edu/)  
- **Models Used**: Random Forest, XGBoost
- **Evaluation Metric**: Root Mean Squared Error (RMSE)

---

## 🧠 Problem Statement

Utility companies must accurately anticipate daily energy demand to manage supply and avoid over- or under-generation. However, daily consumption is volatile, affected by seasonal and behavioral patterns. This project uses historical consumption data to build models that forecast daily usage with quantifiable accuracy and reliability.

---

## 🎯 Objectives

- Forecast daily power consumption using historical data
- Compare regression models for accuracy and trend reliability
- Achieve RMSE below 450 kW
- Analyze if predicted values follow real-world consumption trends

---

## 🧰 Skills & Technologies

- **Languages**: Python
- **Libraries**: Pandas, Scikit-learn, XGBoost, Matplotlib
- **Modeling**: Random Forest Regressor, XGBoost Regressor
- **Visualization**: Plotting actual vs. predicted values
- **Evaluation**: RMSE, correlation coefficients
- **Tools**: Jupyter Notebook, Git & GitHub

---

## 📁 Dataset Description

The dataset spans several years of daily energy usage with time-based features:

- `date`: Day of measurement  
- `power_consumption`: Daily usage in kW  
- `year`, `semester`, `quarter`, `month`  
- `week_in_year`, `day_in_year`, `day_in_week`

### Files

- [`df_train.csv`](https://github.com/Temela/Energy_Consumption_Prediction_Using_ML/blob/main/data/df_train.csv) – Training data (2006–2009)
- [`df_test.csv`](https://github.com/Temela/Energy_Consumption_Prediction_Using_ML/blob/main/data/df_test.csv) – Test data (2010)
- [`Power_Consumption_Prediction.ipynb`](https://github.com/Temela/Energy_Consumption_Prediction_Using_ML/blob/main/Power_Consumption_Prediction.ipynb) – Full implementation notebook

---

## ⚙️ Quick Start

```bash
# Clone the repo
git clone https://github.com/Temela/Energy_Consumption_Prediction_Using_ML.git
cd Energy_Consumption_Prediction_Using_ML

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook Power_Consumption_Prediction.ipynb
```

---

## 🧪 Methodology

### 1. Data Preprocessing
- Verified data structure and types
- Converted categorical features to numeric format
- Checked for and handled missing values
- Standardized numerical features

### 2. Model Training
- Trained both Random Forest and XGBoost on 4 years of data
- Performed hyperparameter tuning (manual and grid search)
- Used RMSE for performance comparison

### 3. Trend Analysis
- Compared actual and predicted values using line plots
- Calculated correlation between predictions and actuals

---

## 📊 Results

- **Best RMSE**: `435.02 kW` with Random Forest  
- **Prediction Error**: Acceptable, below target threshold  
- **Trend Correlation**: Weak pattern alignment (Pearson r < 0.9)

![Actual vs Predicted Consumption](https://github.com/Temela/Energy_Consumption_Prediction_Using_ML/blob/main/img/energy_result.png)

> Despite good RMSE, the models struggled to replicate the real trend behaviour—suggesting missing external signals like weather or behavioral events.


---

## ⚖️ Ethical Considerations

- **Data Privacy**: The dataset is anonymized and publicly available. No personal or sensitive data is used.
- **Transparency**: All code, results, and methodology are openly shared in this repository.
- **Limitations**: Forecasts should not be used as-is for critical infrastructure without expert review and contextual data.
- **Bias Risks**: Since socioeconomic or geographical factors aren't present, the model may overlook underserved communities or infrastructure gaps.

> Predictive modeling should be used to assist, not replace, informed human decisions—especially in critical systems like power distribution.

---

## 🔄 Recommendations

- **Enhance Dataset**: Add weather, calendar events (e.g., holidays), or industrial activity indicators
- **Try Advanced Models**: Test LSTM or Prophet for temporal pattern learning
- **Use Cyclical Encoding**: Represent months and weeks with sine/cosine transforms to capture seasonality

---

## 📂 Project Structure

```
📦 Energy_Consumption_Prediction_Using_ML/
│
├── data/
│   ├── df_train.csv
│   └── df_test.csv
│
├── Power_Consumption_Prediction.ipynb
├── README.md
└── requirements.txt
```

---

## 👤 Contributor

**Fr. Nduka Anthony **  
Graduate Assistant, Department of Computer Science  
[GitHub Profile](https://github.com/Temela)

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/Temela/Energy_Consumption_Prediction_Using_ML/blob/main/LICENSE) file for details.
