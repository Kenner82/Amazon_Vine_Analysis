# Amazon Vine Analysis

## Project Overview

### ETL Of Amazon Product Review Data
Using AWS and PostgreSQL via pgAdmin, a database was created and table schemas initialized. In a Google Colab notebook, a dataset containing Amazon product reviews was extracted into a DataFrame using PySpark, and then transformed to match the table schema previously created. The data was then loaded into pgAdmin to populate the tables so that queries could be run.

### Evaluate Potential Bias In Paid Reviews
Using the dataframes previously created in PySpark, the data was further filtered to determine the total number of reviews for a product, , total number
