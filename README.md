# PySpark Home Sales Data Analysis

## Overview

This project involves analyzing a home sales dataset using PySpark and SparkSQL. The analysis includes querying the dataset to extract meaningful insights, such as average home prices based on various criteria, and optimizing query performance through caching and partitioning techniques.

## Features

- **DataFrame Creation:** A Spark DataFrame is created from the dataset for efficient data processing.
- **Temporary Tables:** Temporary tables are generated from the DataFrame for SQL querying.
- **SQL Queries:**
  - **Average Price by Year for Four-Bedroom Homes:** Retrieves the average price of four-bedroom homes sold each year, rounded to two decimal places.
  - **Average Price by Year for Three-Bedroom, Three-Bathroom Homes:** Computes the average price of homes with three bedrooms and three bathrooms, categorized by the year they were built.
  - **Average Price by Size:** Returns the average price of homes with three bedrooms, three bathrooms, two floors, and a size of at least 2,000 square feet, categorized by the year they were built.
  - **Average Price by View Rating:** Extracts the average home price for different "view" ratings, limited to homes with an average price of $350,000 or more.
- **Query Optimization:**
  - **Caching:** Caches the temporary "home_sales" table to optimize query performance.
  - **Run Time Comparison:** Compares query run times before and after caching the temporary table.
  - **Partitioning:** Partitions the dataset by the "date_built" field and reads it in a Parquet format to optimize storage and querying.
  - **Performance Testing:** Runs queries on both the cached and partitioned datasets to compare performance improvements.

## Technical Details

- **Data Source:** [Home sales dataset](https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-classroom/v1.2/22-big-data/home_sales_revised.csv)  containing information on various properties, including their prices, sizes, and features.
- **Tools:**
  - **PySpark** for data processing and analysis
  - **SparkSQL** for writing SQL queries
  - **Parquet** for optimized data storage and retrieval
- **Performance Metrics:**
  - **Caching:** Used to reduce the query run time by storing intermediate data.
  - **Partitioning:** Used to improve data access and query performance based on the "date_built" field.

## How to Use

1. **Set Up PySpark:** Ensure that PySpark is installed and properly configured on your system.
2. **Load the Dataset:** Load the home sales dataset into a Spark DataFrame.
3. **Run the Project:**
   - Execute the SQL queries to analyze the home sales data.
   - Compare the query run times before and after caching and partitioning.
   - Use the insights gained from the analysis for further decision-making or reporting.
