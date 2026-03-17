# Maji-Ndogo-Agri-Data-Integrity
An end-to-end data engineering and analytics pipeline that validates regional farm survey data against raw IoT weather station streams. This project utilizes SQL, Regex-based data extraction, and multivariate statistical analysis to ensure data reliability before optimizing crop yields in the Maji Ndogo region.

- Overview
This project focuses on the exploratory data analysis (EDA) and validation of agricultural data. The core objective is to determine if farm-level survey data is accurate by cross-referencing it with independent, raw data captured by IoT weather stations across the province.

- Key Technical Steps
1. Data Integration
SQL Joins: Combined geographic, weather, soil, and farm management data from an SQLite database into a single unified DataFrame.

Data Cleaning: Standardized crop names (e.g., "teaa" to "tea"), handled absolute values for elevation, and resolved duplicate record issues.

2. Exploratory Data Analysis (EDA)
Univariate Analysis: Used KDE plots to identify distribution patterns and outliers in environmental variables like Rainfall and pH levels.

Multivariate Analysis: Employed Violin plots and Pairplots to visualize how different crops (Coffee, Rice, Tea) respond to varying rainfall and soil conditions.

Correlation Mapping: Generated a correlation matrix to identify the primary drivers of standardized crop yields.

3. Data Validation
Regex Extraction: Developed complex Regular Expression patterns to parse unstructured "SMS-style" messages from IoT sensors to extract Temperature, Rainfall, and Pollution indices.

Integrity Testing: Automated a comparison between extracted weather station averages and the main dataset. Identified where data was "Within Spec" or required further investigation.

- Tech Stack
Language: Python

Database: SQL (SQLite / SQLAlchemy)

Libraries: Pandas, NumPy, Seaborn, Matplotlib, Re (Regex)

Environment: Windows / Jupyter Notebook
