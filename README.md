

## 🏠 Home Sales Data Analysis with PySpark
This project demonstrates the use of PySpark SQL for analyzing home sales data. The project involves reading and processing large datasets, performing data analysis using SQL queries, and optimizing performance using PySpark features such as caching and partitioning.

## 📑 Table of Contents
Project Overview
Technologies Used
Features and Objectives
Dataset Description
Setup Instructions
Analysis Steps
Results and Insights
Repository Structure
Contributing
License

##🔍 Project Overview
This project analyzes home sales data to answer key business questions and optimize queries using advanced PySpark SQL techniques. The analysis includes:

Calculating average home prices based on various filters.
Exploring performance improvement through caching and partitioning.
Comparing runtime performance for cached and uncached datasets.

## 💻 Technologies Used
Programming Language: Python
Framework: PySpark
Libraries: PySpark SQL, pandas, time
Data Format: CSV and Parquet
Development Environment: Google Colab and local Git repository
Version Control: Git and GitHub

## 🎯 Features and Objectives
SQL Analysis:

Determine average prices for homes with specific attributes.
Group and aggregate data by year and other fields.
Performance Optimization:

Cache and uncache data for faster query execution.
Partition datasets for efficient querying.
Query Performance Comparison:

Measure runtime differences between cached and uncached queries.
Use Parquet files for improved query performance.

## 🗂 Dataset Description
The dataset used for this analysis is home_sales_revised.csv. It contains the following columns:

Date Built: The year the home was built.
View: A rating for the home view.
Price: The selling price of the home.
Bedrooms: Number of bedrooms.
Bathrooms: Number of bathrooms.
Square Footage: Total area of the home.

## ⚙️ Setup Instructions
Clone the repository to your local machine:

git clone https://github.com/Hannah-61/Home_Sales.git
Install dependencies (e.g., PySpark):

pip install pyspark
Open the Home_Sales.ipynb notebook in your preferred environment (e.g., Google Colab or Jupyter Notebook).
Load the dataset home_sales_revised.csv into the notebook.
Run the cells in the notebook sequentially to perform the analysis.

## 📋 Analysis Steps
-- Data Loading:

Load the CSV file into a PySpark DataFrame.
Temporary Table Creation:

Create a temporary table home_sales for SQL queries.
SQL Queries:

Query 1: Average price of four-bedroom homes sold each year.
Query 2: Average price of three-bedroom, three-bathroom homes by year built.
Query 3: Average price of homes with 3 beds, 3 baths, 2 floors, and ≥2,000 square feet by year built.
Query 4: Average home price by "view" rating (with prices ≥ $350,000).
Caching and Optimization:

Cache the home_sales table and rerun Query 4 to compare runtimes.
Partition data by date_built and save in Parquet format for better performance.
Uncache Table:

-- Verify the uncaching of the home_sales table.

## 📊 Results and Insights
The average prices for different types of homes and conditions were calculated.
Query performance improved significantly when using caching and partitioned data.
Runtime comparisons demonstrated the efficiency of caching and Parquet formats for data storage and querying.

## 📂 Repository Structure
bash
Copy code
Home_Sales/
├── Home_Sales.ipynb           # Jupyter Notebook containing analysis and results
├── home_sales_revised.csv     # Dataset used for analysis
├── README.md                  # Project documentation
