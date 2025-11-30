# manufacturing-downtime

A full **End-to-End Manufacturing Analytics & Downtime Prediction System** combining:
**data engineering, data analysis, machine learning, system design, dashboards, and deployment.**

---

## 🚀 Project Overview

Unplanned downtime is one of the biggest operational challenges in manufacturing. It leads to:

* Delayed orders
* Inefficient labor allocation
* Increased operational cost
* Reduced overall equipment effectiveness (OEE)

This project delivers a **complete analytical & operational system**, not just an ML model.
It includes:

* A fully cleaned and engineered dataset
* Exploratory analysis revealing operational patterns
* A predictive model to estimate downtime
* A dashboard for real-time monitoring & insights
* System documentation (ERD, DFD, Use Case, Architecture)
* A deployment-ready dashboard interface

---

## 🎯 Project Objectives

* Predict total downtime per batch
* Provide insights on **why** downtime happens
* Detect high-risk operators & faulty machines
* Support next-day planning with downtime forecasts
* Deliver an interactive dashboard for production teams
* Provide full **System Analysis & Design** documentation
* Build a modular codebase for future scaling and deployment

---

## 📊 Dataset Description

The dataset includes:

* Batch details (BatchID, ProductLine, ProductType)
* Operator information & shift schedules
* Machine parameters
* Historical downtime logs
* Maintenance records
* Environmental & operational conditions

Expected directory structure:

```
data/
├── raw.csv
├── cleaned.csv
└── features.csv
```

---

## 🧹 Data Preprocessing

Steps completed:

* Handling missing values
* Merging multiple raw tables
* Computing `TotalDowntime_minutes`
* Removing outliers
* Fixing inconsistencies
* Encoding categorical variables
* Scaling numerical features
* Exporting processed datasets

Notebook:
`Data_Preprocessing.ipynb`

---

## 🔍 Exploratory Data Analysis (EDA)

Main findings:

* Some operators consistently produce higher downtime
* Specific machines cause repeated failure patterns
* Night shifts show different behavior vs day shift
* Strong correlation between downtime and setup time
* Weekly seasonal patterns in downtime

Notebook:
`EDA_and_Modeling.ipynb`

---

## 🤖 Predictive Modeling

Trained & compared multiple regression models:

* Linear Regression
* Random Forest
* XGBoost

Selected Model: **XGBoost Regressor**
Includes:

* Hyperparameter tuning
* Error analysis
* Feature importance
* Model saving (.pkl files)

Artifacts stored in:

```
models/
model.pkl
scaler.pkl
encoder.pkl
```

---

## 🛠 System Analysis & Design

Delivered professional documentation:

### ✔ Use Case Diagram

Actors: Operator – Planner – Maintenance – Dashboard System

### ✔ ER Diagram

Database tables for batches, operators, machines, downtime logs.

### ✔ Data Flow Diagrams (DFD – Level 0, 1, 2)

Shows data movement from input → processing → prediction → dashboard.

### ✔ Sequence Diagram

Batch prediction workflow.

### ✔ Activity Diagram

Operator + dashboard usage flow.

### ✔ State Diagram

Machine/downtime lifecycle.

### ✔ Architecture Diagram

System layers:
UI → Backend → ML Service → Database → Dashboard Layer

All diagrams stored in:
`docs/`

---

## 🖥 Deployment (App & Dashboard)

Prototype dashboard includes:

* Batch-level prediction
* Operator/machine risk ranking
* Interactive KPIs
* Visual analytics
* Upload CSV for prediction

Notebook:
`app_py.ipynb`

Planned upgrades:

* Streamlit / FastAPI full deployment
* CI/CD pipeline
* Cloud hosting (Render / Railway)

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

## 🚀 Future Improvements

* SHAP explainability
* Full backend with FastAPI
* Cloud deployment
* Real-time alerts
* Automated retraining pipeline

---

**Good Luck :)**

---
