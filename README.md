# Analyzing International Debt Data

## Project Overview

This project analyzes international debt data collected by The World Bank. The dataset contains information about the amount of debt (in USD) owed by developing countries across several debt categories. The goal is to use SQL queries to interact with the data stored in a database, extract insights into debt management across countries, and understand the distribution of debt indicators.

## Dataset

* **Source:** The World Bank
* **File:** `datasets/international_debt.csv`
* **Description:** Contains debt statistics for various countries and debt indicators.

## Database Setup

1.  **Create Table:** Use the `datasets/create_table.sql` script to create the `international_debt` table in your chosen database system (e.g., MySQL, PostgreSQL). The table schema is defined as:
    * `country_name` (VARCHAR)
    * `country_code` (CHAR)
    * `indicator_name` (VARCHAR)
    * `indicator_code` (VARCHAR)
    * `debt` (DECIMAL)
2.  **Import Data:** Import the data from `datasets/international_debt.csv` into the created `international_debt` table.

## Analysis (`Analyze_International_Debt.ipynb`)

The Jupyter Notebook `Analyze_International_Debt.ipynb` performs the following analyses using SQL queries:

1.  **Data Inspection:** Displays the first 10 rows of the data.
2.  **Distinct Countries:** Counts the total number of distinct countries in the dataset.
3.  **Distinct Debt Indicators:** Lists all unique debt indicators present.
4.  **Total Debt Calculation:** Calculates the sum of all debt records, presented in millions of USD.
5.  **Highest Total Debt:** Identifies the country with the highest aggregate debt.
6.  **Highest Average Debt Indicators:** Determines the top 10 debt indicators with the highest average debt value across all countries.
7.  **Highest Debt for Specific Indicator:** Finds the country with the maximum debt for a specific indicator (`DT.AMT.DLXF.CD`).
8.  **Most Frequent Debt Indicators:** Lists the top 20 most frequently occurring debt indicators in the dataset.
9.  **Highest Maximum Debt per Country:** Identifies the top 10 countries with the highest single maximum debt value recorded across any indicator.

## Files in Project

* `Analyze_International_Debt.ipynb`: Jupyter Notebook containing the data analysis code and explanations.
* `datasets/`: Directory containing the data and database schema.
    * `international_debt.csv`: The raw dataset.
    * `create_table.sql`: SQL script to create the database table.
* `README.md`: This file.

## How to Run

1.  Set up a database server (e.g., MySQL).
2.  Create a database (e.g., `World_Debt` as used in the notebook).
3.  Run the `datasets/create_table.sql` script against your database to create the table structure.
4.  Import the data from `datasets/international_debt.csv` into the `international_debt` table.
5.  Update the database connection details (host, user, password, database name) in the `Analyze_International_Debt.ipynb` notebook.
6.  Run the cells in the Jupyter Notebook to perform the analysis. Ensure you have the necessary Python libraries installed (e.g., `pymysql`, `pandas`).
