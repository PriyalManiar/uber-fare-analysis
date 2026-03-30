# Uber Fare Prediction

An data science project focused on predicting Uber fare amounts by analyzing geospatial, temporal, and passenger data. This project covers the full pipeline from raw data cleaning to feature engineering and predictive modeling.

## Project Structure

```text
uber-fare-analysis/
├── data/
│   └── uber.csv
├── scripts/
│   └── fare_analysis.ipynb
├── README.md
├── requirements.txt
```

## Overview

The objective of this project is to predict the `fare_amount` for a ride. The notebook explores the relationship between trip distance, time of day, and pricing, utilizing the Haversine formula to handle spherical geometry for distance calculations.

### Key Highlights
* **Geospatial Engineering:** Implemented the Haversine formula to calculate the actual distance between pickup and drop-off coordinates.
* **Temporal Analysis:** Extracted granular time features (Hour, Day, Month, Year) to account for peak-hour pricing and seasonal trends.
* **Data Quality:** Performed rigorous outlier detection to remove invalid coordinates and unrealistic fare amounts (e.g., negative fares).

## Dataset Features

* **Target Variable:** `fare_amount`
* **Temporal:** `pickup_datetime`
* **Geospatial:** `pickup_longitude`, `pickup_latitude`, `dropoff_longitude`, `dropoff_latitude`
* **Demographic:** `passenger_count`

## Tech Stack

* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib
* **Environment:** Jupyter Notebook

## Methodology

1.  **Exploratory Data Analysis (EDA):** Visualized distributions and correlations using Seaborn heatmaps and boxplots.
2.  **Preprocessing:** * Handled missing values and dropped unnecessary index columns.
    * Filtered data to include only realistic passenger counts (1–5) and fares.
3.  **Feature Scaling & Engineering:** * Converted timestamps into cyclic temporal features.
    * Calculated `distance_km` using the `sklearn.neighbors.DistanceMetric`.
4.  **Modeling:** Splitting data into training/testing sets to evaluate model performance on unseen ride data.

##  How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/uber-fare-analysis.git](https://github.com/your-username/uber-fare-analysis.git)
   cd uber-fare-analysis
2. Install dependencies:
   ```bash
   pip install requirements.txt
   ```
3. Open `notebooks/fare_analysis.ipynb` in Jupyter or Colab and run all cells.

---
*Built as part of Data Mining and Analysis undergrad coursework.*
