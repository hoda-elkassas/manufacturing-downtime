# manufacturing-downtime

A Machine Learning project for predicting factory downtime and providing actionable insights for production, maintenance, and planning teams.

---

## 🚀 Project Overview

Unplanned downtime is one of the biggest operational challenges in manufacturing. It leads to:

* Delayed orders
* Inefficient labor allocation
* Higher operational costs
* Reduced overall equipment effectiveness (OEE)

This project builds a **data-driven, predictive system** that estimates downtime per batch and identifies high-risk operators, machines, and conditions.
It also includes a dashboard for monitoring KPIs and operational patterns.

---

## 🎯 Project Objectives

* Predict total downtime per batch
* Provide factor-level contributions (why the downtime happened)
* Forecast next-day downtime for planning teams
* Identify risky operators/equipment to support maintenance
* Provide an operational dashboard for data exploration and monitoring

---

## 📊 Dataset Description

The dataset includes:

* Batch information (BatchID, ProductionLine, ProductType)
* Operator & shift details
* Machine parameters
* Historical downtime records (in minutes)
* Environmental factors
* Maintenance logs

Files expected:

```
data/
├── raw.csv
├── cleaned.csv
└── features.csv
```

---

## 🧹 Data Preprocessing

Main cleaning steps:

* Handle missing values
* Merge raw tables into a unified dataset
* Compute `TotalDowntime_minutes`
* Remove outliers
* Encode categorical features
* Normalize numerical fields

See notebook:
`Data_Preprocessing.ipynb`

---

## 🔍 Exploratory Data Analysis (EDA)

Key insights:

* Operators show different performance patterns
* Certain machines consistently cause high downtime
* Night shifts have different behavior vs day shifts
* Strong correlation between downtime and setup time

See notebook:
`EDA_and_Modeling.ipynb`

---

## 🤖 Machine Learning Model

We trained and evaluated multiple regression models:

* Linear Regression
* Random Forest
* XGBoost

Best model (example):
**XGBoost Regressor**

Performance Metrics (example):

* MAE = *X.xx*
* R² = *0.xx*

Saved model artifacts will be stored in:

```
models/
model.pkl
scaler.pkl
encoder.pkl
```

---

## 🖥 Deployment (App / Dashboard)

A lightweight dashboard + prediction interface.

App notebook:
`app_py.ipynb`

Planned deployment features:

* Batch prediction
* Daily forecast
* Operator/machine risk ranking
* Interactive KPIs and charts

A Streamlit or FastAPI version may be added later.

---

## 🏗 Project Structure

```
project/
│── README.md
│── Data_Preprocessing.ipynb
│── EDA_and_Modeling.ipynb
│── app_py.ipynb
│
├── data/
│   ├── raw.csv
│   ├── cleaned.csv
│   └── features.csv
│
├── models/
│   ├── model.pkl
│   ├── scaler.pkl
│   └── encoder.pkl
│
├── src/
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   ├── train_model.py
│   └── predict.py
│
└── docs/
    ├── ERD.png
    ├── DFD.png
    ├── Use_Case.png
    └── Architecture.png
```

---

## 🧪 Future Improvements

* Add SHAP interpretability
* Full FastAPI backend
* Deploy dashboard to cloud (Render / Railway)
* Add automated retraining pipeline
* Add real-time operator alerts

---
