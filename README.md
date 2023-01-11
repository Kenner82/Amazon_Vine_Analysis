# Amazon Vine Analysis

## Project Overview

### ETL Of Amazon Product Review Data
Using AWS and PostgreSQL via pgAdmin, a database was created and table schemas initialized. In a Google Colab notebook, a dataset containing Amazon product reviews was extracted into a DataFrame using PySpark, and then transformed to match the table schema previously created. The data was then loaded into pgAdmin to populate the tables so that queries could be run.

### Evaluate Potential Bias In Paid Reviews
Using the DataFrames previously created in PySpark, the data was further filtered to create a dataset of product reviews with more than 20 total votes (of which at least 50% were marked as helpful). DataFrames were used to break down the data by whether the review was written by a member of the Amazon Vine program (which pays members to write product reviews). This data was then analyzed to determine if having paid reviews affects the number of five star ratings that a product has. 

## Results
