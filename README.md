# 🚕 Uber NYC Ride Data Analysis

This project presents a detailed exploratory data analysis (EDA) on Uber ride data collected in New York City during 2014 and 2015. The dataset includes millions of ride records with timestamps and locations, allowing for temporal, geographic, and behavioral insights into ride demand and dispatch patterns.

---

## 📂 Dataset

The data is sourced from Uber’s publicly released FOIL request and includes:

- **Sample file (100k rows)**: `uber-raw-data-janjune-15_sample.csv`
- **Full month-wise data (2014)**: April to September 2014
- **Other sources**: Additional files including FHV (For-Hire Vehicle) trip data, Lyft, Carmel, and more

Each file contains:
- `Date/Time` of pickup
- `Lat`, `Lon` for pickup location
- `Base` dispatch number or affiliated base number

---

## 📌 Project Objectives

- Analyze Uber trip distribution by **month**, **weekday**, and **hour**
- Identify **peak ride hours** in NYC
- Compare activity across dispatch bases
- Visualize **geographic pickup hotspots** using latitude and longitude
- Aggregate and clean data from multiple CSV sources

---

## ✅ Key Steps

### 1. Data Preparation
- Combined multiple raw `.csv` files from 2014
- Removed duplicates (over 82,000 removed from 4.5M rows)
- Converted pickup date strings to `datetime` objects

### 2. Time-Based Feature Engineering
- Extracted `month`, `weekday`, `hour`, and `minute` from timestamps
- Analyzed ride counts by these time dimensions

### 3. Visual Analysis
- 📊 **Bar plots**: Monthly ride volume
- 📊 **Cross-tabulation**: Weekday trends by month
- 📈 **Point plots**: Hourly demand on different weekdays
- 🗺️ **Geospatial density**: Ride hotspots by latitude/longitude using `folium`

---

## 📈 Sample Visualizations

- **Monthly Trip Volume (2015 Sample)**
  ![monthly-bar](assets/monthly-bar.png)

- **Hourly Demand by Weekday**
  ![hourly-rush](assets/hourly-rush.png)

- **NYC Ride Hotspots**
  ![heatmap](assets/uber-map.png)

*(Add these images to an `assets/` folder in your repo)*

---

## 📦 Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `plotly`
- `folium`

---

## ▶️ Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/uber-ride-eda.git
   cd uber-ride-eda
