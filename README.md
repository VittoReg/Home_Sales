# Home Sales Analysis with PySpark
## Overview
In this challenge I have used PySpark to analyze a large dataset regarding home sales. The project gives a full understanding on how to apply PySpark for data analysis.

## Project Structure
- `Home_Sales.ipynb`: The Jupyter notebook containing the code for the analysis.
- `home_sales_revised.csv`: The dataset used for the analysis (downloaded from an AWS S3 bucket).

## Dataset
The dataset `home_sales_revised.csv` contains information on home sales including attributes such as the number of bedrooms, bathrooms, floors, square footage, year built, and the sale price.

## Analysis Steps

1. **Set Up Environment**: Initialize PySpark and read the dataset into a DataFrame.
2. **Create Temporary Table**: Create a temporary view of the DataFrame for SQL queries.
3. **Run SQL Queries**:
   - Average price for a four-bedroom house sold for each year.
   - Average price of a home with three bedrooms and three bathrooms for each year it was built.
   - Average price of a home with specific features (three bedrooms, three bathrooms, two floors, and at least 2,000 square feet) for each year it was built.
   - Average price of a home per "view" rating for homes with an average price of at least $350,000.
4. **Cache and Uncache Table**: Cache the temporary table and compare query runtimes before and after caching.
5. **Partition Data**: Partition the dataset by the `date_built` field and save as Parquet files. Create a temporary table from the partitioned data and compare query runtimes.
6. **Uncache Table**: Uncache the temporary table and verify.

## Results

The notebook contains the results of the queries and the runtimes for cached and partitioned data queries. The analysis helps in understanding the average home prices based on various features and conditions.

## Conclusion
Finally this project has proved to be challenging especially when it comes to deal with large datasets, and the whole process would't have been as smooth without the aid of Spark SQL for processing large datasets efficiently.
