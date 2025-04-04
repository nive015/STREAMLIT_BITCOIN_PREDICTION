# STREAMLIT_BITCOIN_PREDICTION


REFER THIS SITE TO DOWNLOAD THE DATASET:

https://www.kaggle.com/datasets/novandraanugrah/bitcoin-historical-datasets-2018-2024

**Project Overview**

This project analysis **Bitcoin dataset** using **Big Data tools**, specifically **PySpark**, to handle large-scale time-series financial data. The data spans from **2018 to 2025** in **15-minute intervals**, making it massive and ideal for big data analysis. You're also building a **machine learning model** to predict Bitcoin’s **opening, closing, high and low prices of the next day**.

**Step-by-Step Breakdown**

1. **Setting Up the Environment**
You begin by installing and configuring all necessary tools:
- PySpark (for distributed data processing)
- findspark (to help run Spark from a notebook)
- Matplotlib, Seaborn, Pandas (for traditional data analysis and plotting)

You then initialize a **Spark session**, which is the entry point for working with Spark.

2. **Loading and Understanding the Data**
You read in a CSV file containing historical Bitcoin prices:
- Unix timestamp
- Opening, highest, lowest, and closing prices
- Volume of transactions
- A readable date/time column (`Open time`)

You explore:
- The data schema (column names and types)
- Total number of rows
- Null/missing values
- First few rows of the dataset
- actions and transformations are performed

3. **Data Cleaning & Visualization**
You convert the timestamp into a human-readable format and begin **exploring trends**:
- Plotting the **closing price** over time to see long-term trends
- Calculating **percentage change** between time intervals (returns) to examine volatility
- Plotting returns to understand how much and how often the price changes

4. **Feature Engineering**
You enhance your dataset by breaking down the timestamp into:
- Day of the month
- Hour of the day
- Minute of the hour
- Month

These are used to capture **seasonal or temporal patterns** in price behavior (e.g., are there patterns based on time of day or specific days?).

5. **Correlation Analysis**
You create a **heatmap** showing how features like opening price, high, low, close, and volume correlate with each other. This helps identify which features are most likely to influence the target (closing price).

6. **Preparing for Machine Learning**
You select a subset of features like:
- Opening price
- High, low
- Volume
- Time-based features (day, hour, minute)
- These features are compiled into a single vector — a format Spark’s ML library can use.


7. **Training a Machine Learning Model**
You use **Lasso Regression** (a simple but interpretable model) to predict the closing price. Steps include:
- Splitting the data into training and test sets
- Training the model on historical data
- At the end, the collab notebook is connected with Streamlit using local tunnel.


