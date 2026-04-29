# Automatidata Project — Course 2: Get Started with Python

> **Google Advanced Data Analytics Certificate · Course 2 End-of-Course Project**  
> Client: New York City Taxi & Limousine Commission (NYC TLC)  
> Firm: Automatidata (fictional data consulting firm)

---

## Overview

This project notebook covers the initial data inspection and analysis phase of a multi-course capstone project. As a new data professional at Automatidata, the goal is to load, inspect, and understand the NYC TLC 2017 Yellow Taxi Trip dataset — preparing it for future exploratory data analysis (EDA), visualizations, and statistical modeling.

The work follows the **PACE framework**: Plan → Analyze → Construct → Execute.

---

## Project Goals

1. Build a pandas DataFrame from the raw NYC TLC dataset
2. Inspect the data for structure, null values, and data types
3. Identify key variable distributions and flag anomalies
4. Investigate relationships between trip distance, total amount, payment type, and tipping behavior
5. Summarize findings for the data team and stakeholders

---

## Dataset

**File:** `2017_Yellow_Taxi_Trip_Data.csv`  
**Source:** New York City Taxi & Limousine Commission (NYC TLC)  
**Description:** Trip-level records from NYC yellow taxis in 2017, including fare amounts, trip distances, payment types, vendor IDs, passenger counts, and tip amounts.

Key variables analyzed:

| Variable | Description |
|---|---|
| `trip_distance` | Distance of the trip in miles |
| `total_amount` | Total fare charged to the passenger |
| `payment_type` | Payment method (1=Credit Card, 2=Cash, 3=No Charge, 4=Dispute, etc.) |
| `tip_amount` | Tip amount in dollars |
| `VendorID` | Taxi technology vendor (1 or 2) |
| `passenger_count` | Number of passengers in the trip |

---

## Notebook Structure

### Part 1 — Plan: Understand the Situation
- Prepare strategy for organizing and understanding the taxi dataset

### Part 2 — Analyze: Understand the Data
- Load dataset into a pandas DataFrame
- Inspect with `df.head()`, `df.info()`, and `df.describe()`
- Investigate null values, data types, and distributions

### Part 3 — Analyze: Understand the Variables
- Sort by `trip_distance` and `total_amount` to spot outliers
- Analyze payment type distribution
- Compare average tips for credit card vs. cash payments
- Calculate mean total amount by vendor
- Break down average tip amounts by passenger count (credit card only)

### Execute — Summary for Stakeholders
- Key finding: `payment_type` and tip-related variables are the most predictive features for building an NYC TLC revenue/tip model

---

## Key Findings

- **Payment type:** The majority of trips were paid by credit card or cash; disputes and no-charge trips were minimal.
- **Tipping behavior:** Credit card payments had measurable tip amounts; cash tips were not systematically recorded, making credit card data more reliable for tip modeling.
- **Outliers:** Sorting `total_amount` revealed some unusually high and negative values worth further investigation.
- **Vendor differences:** Mean total amounts differed slightly between the two vendors.
- **Passenger count vs. tip:** Tip averages varied across passenger counts for credit card trips.

---

## Technologies Used

- Python 3
- [pandas](https://pandas.pydata.org/) — data loading and manipulation
- [numpy](https://numpy.org/) — numerical support
- Jupyter Notebook

---

## How to Run

```bash
# Clone the repo
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

# Install dependencies
pip install pandas numpy jupyter

# Launch the notebook
jupyter notebook Activity_Course_2_Automatidata_project_lab.ipynb
```

Make sure `2017_Yellow_Taxi_Trip_Data.csv` is in the same directory as the notebook before running.

---

## Course Context

This notebook is part of the **Google Advanced Data Analytics Professional Certificate** on Coursera. It is Course 2's end-of-course project and is not intended for production use — it is an educational exercise in Python-based data inspection.

---

## Author

Anish — Data Analytics student, UCHS San Diego  
Certificate: Google Advanced Data Analytics (Coursera)
