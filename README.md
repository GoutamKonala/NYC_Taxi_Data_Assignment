# NYC Yellow Taxi Data Analysis (2023)

This repository contains an exploratory data analysis (EDA) of the New York City Yellow Taxi trip records from 2023. The analysis aims to uncover insights into taxi operations to inform strategic decisions for improving service efficiency, maximizing revenue, and enhancing the passenger experience.

## Objective

As an analyst for a taxi company in NYC, the primary goal is to analyze the 2023 taxi trip data to identify patterns that can help optimize taxi operations.

## Dataset

The data is from the NYC Taxi and Limousine Commission (TLC) and includes information about pick-up and drop-off times, locations, trip distances, fares, payment types, and passenger counts. The data for each month of 2023 is in a separate Parquet file.

Due to the large size of the dataset, a sampling strategy was employed. A 5% random sample was taken from each hour of each day to create a representative subset of the data for analysis.

## Methodology

The analysis is performed in a Jupyter Notebook (`EDA_NYC_Taxi_Analysis_Lakshmi_Goutam_Reddy_Konala.ipynb`) and involves the following steps:

### 1. Data Loading and Preparation

- Importing necessary libraries (pandas, numpy, matplotlib, seaborn).
- Loading the 12 monthly Parquet files.
- Sampling the data to create a manageable and representative dataset.
- Combining the sampled data into a single DataFrame.

### 2. Data Cleaning

- Fixing column names and data types.
- Handling negative monetary values by converting them to their absolute values.
- Imputing missing values in columns like `passenger_count`, `RatecodeID`, and `congestion_surcharge` using appropriate strategies (e.g., mode imputation).
- Handling outliers in `trip_distance`, `fare_amount`, and `passenger_count`.

### 3. Exploratory Data Analysis (EDA)

- **Univariate Analysis:** Analyzing individual variables to understand their distributions (e.g., trip distance, fare amount).
- **Bivariate Analysis:** Exploring relationships between pairs of variables (e.g., trip distance vs. fare amount, payment type vs. tip amount).
- **Multivariate Analysis:** Investigating interactions between multiple variables.
- **Geospatial Analysis:** Using GeoPandas to visualize pick-up and drop-off locations and identify high-demand areas.

## Key Findings

The analysis reveals several key insights, including:

- Identification of the busiest times of the day and days of the week for taxi rides.
- Understanding the relationship between trip distance, fare amount, and tipping behavior.
- Geospatial analysis of pick-up and drop-off hotspots, which can be used to optimize fleet allocation.
- Insights into the impact of different rate codes on revenue.

## Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- PyArrow
- GeoPandas (for geospatial analysis)

## How to Run

1.  Clone this repository.
2.  Ensure you have the required libraries installed (`pip install -r requirements.txt` - Note: a `requirements.txt` file would need to be created).
3.  Download the NYC Yellow Taxi data for 2023 from the [TLC website](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page).
4.  Place the data in a directory named `All_Data` at the same level as the `Code` directory.
5.  Open and run the `EDA_NYC_Taxi_Analysis_Lakshmi_Goutam_Reddy_Konala.ipynb` notebook.