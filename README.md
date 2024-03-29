# Amazon Vine Analysis

## Project Overview

### ETL Of Amazon Product Review Data
Using AWS and PostgreSQL via pgAdmin, a database was created and table schemas initialized. In a Google Colab notebook, a dataset containing Amazon product reviews was extracted into a DataFrame using PySpark, and then transformed to match the table schema previously created. The data was then loaded into pgAdmin to populate the tables so that queries could be run.

### Evaluate Potential Bias In Paid Reviews
Using the DataFrames previously created in PySpark, the data was further filtered to create a dataset of product reviews with more than 20 total votes (of which at least 50% were marked as helpful). DataFrames were used to break down the data by whether the review was written by a member of the Amazon Vine program (which pays members to write product reviews). This data was then analyzed to determine if having paid reviews affected the number of 5 star ratings that a product received. 

## Results
### Paid Reviews
Of the 463 reviews written by Amazon Vine members that met the above criteria, 202 (or 43.63%) of them received a 5 star rating
<img width="791" alt="paid_reviews" src="https://user-images.githubusercontent.com/111674383/211768229-e3db4dad-d879-4711-8aa4-7c569d6bc781.png">
### Unpaid Reviews
There were 25,094 unpaid reviews that met the above criteria, of which 12,033 (or 47.95%) received a 5 star rating. 
<img width="760" alt="unpaid_reviews" src="https://user-images.githubusercontent.com/111674383/211768497-5238bc41-bade-4145-9e76-2e2f73820977.png">

## Summary
While it may have been expected that the reviews written by Amazon Vine members (who were paid for their feedback) would have a greater percentage of 5 star reviews, the opposite ended up being true. 47.95% of the unpaid reviews rated a product with 5 stars, compared to 43.63% of the paid reviews. This provides evidence that paying customers to leave product reviews does not bias or skew the overall product rating with an artificially high number of 5 star reviews.

### Further Inquiry
Using the same DataFrames, the data could be further refined by grouping the reviews by US vs. non-US marketplaces. Consumer culture and incentives for reviews may vary across locations, and evaluating if the same results are found when broken down by marketplace would provide additional information about the efficacy or potential bias of the Amazon Vine program.
