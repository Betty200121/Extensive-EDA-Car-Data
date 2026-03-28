# 🚗 Used Vehicle Market EDA: Uncovering Pricing Trends

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-yellow.svg)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Data%20Visualization-orange.svg)](https://matplotlib.org/)

## 📌 Project Overview
This repository features an in-depth **Exploratory Data Analysis (EDA)** on a dataset of over 426,000 used vehicles listed on Craigslist across the United States. 

In the lifecycle of any Machine Learning project, high-quality data is the most critical component. This notebook demonstrates a rigorous, end-to-end data preprocessing and exploration pipeline, transforming raw, messy web-scraped data into a clean, structured format ready for predictive modeling (e.g., price prediction regression algorithms).

## 💡 Key Data Science & Machine Learning Skills Demonstrated

This project highlights several core competencies essential for Data Science and ML engineering roles:

* **Advanced Data Wrangling:** Handled a massive dataset (426K+ rows, 26 features), systematically identifying and dropping 13 non-predictive or redundant columns (e.g., URLs, highly granular geolocation data) to reduce dimensionality and noise.
* **Intelligent Missing Value Imputation:** Addressed varying degrees of missing data across multiple features. Utilized domain-appropriate strategies, such as median imputation for numerical data to resist skewness, and 'unknown' categorization for high-volume missing text data, preserving dataset size while preventing model bias.
* **Feature Extraction (RegEx):** Parsed unstructured categorical text into continuous numerical formats (e.g., extracting integers from "6 cylinders" using Pandas `.str.extract()`), enabling statistical analysis and correlation tracking.
* **Outlier Detection & Filtration:** Applied statistical filtering and domain logic to remove extreme anomalies (e.g., $1 billion price tags, vehicles from the year 1900, or 10-million-mile odometers). Filtered the dataset to a realistic representation (Prices < $60k, Odometer < 200k, Year > 1995) to ensure robust model training.
* **Data Visualization:** Leveraged `matplotlib` and `pandas` plotting to generate comparative subplots and boxplots, visually validating the distribution, spread, and median tendencies of key numerical features.

## 📊 Core Business Questions Addressed

By analyzing the cleaned data, this project successfully answers key market questions:
1.  **Are cars with higher mileage cheaper?** Yes. Visual and statistical distributions confirm that higher mileage directly correlates with a lower price point.
2.  **Are older cars cheaper than newer ones?** Yes. Depreciation heavily affects older cars, with the exception of specific vintage/classic models (pre-1995).
3.  **Are age and mileage of the car related?** Yes. There is a logical positive correlation between the age of the vehicle and its accumulated mileage.

## ⚙️ Methodology & Pipeline

1.  **Data Ingestion:** Loading the raw Kaggle dataset (`vehicles.csv`).
2.  **Structural Analysis:** Utilizing `.info()`, `.shape`, and `.isna().any()` to map the landscape of missing and unformatted data.
3.  **Dimensionality Reduction:** Dropping variables with 100% null rates (e.g., `county`) and features irrelevant to pricing.
4.  **Cleaning & Formatting:** Type casting (e.g., floats to Int64) and standardizing condition/size/type inputs.
5.  **Statistical Pruning:** Using `.describe()` and `.value_counts()` to identify thresholds for outlier removal.
6.  **Exporting for ML:** Saving the finalized, high-integrity dataset as `cleaned_vehicles.csv` for seamless integration into future algorithms.

## 🛠️ Technologies Used
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib
* **Environment:** Jupyter Notebook
