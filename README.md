# Amazon Vine Analysis

## Overview
The Sellby company has asked to analyze Amazon reviews written by the Amazon Vine Program, a pay-for-review program to determine if there is a bias for favorable reviews. In this analysis, a dataset of over 1.78 million reviews on videogames was selected to perform an ETL process using the following resources. 

Data Source:
- S3 AWS Amazon Review Datasets for US video games <br>

Sofware: 
- PySpark - Spark version 3.0.3
- AWS (Amazon Web Services) RDS (Relational Database Service)
- Google Collab using Python
- PgAdmin 4; PostgreSql 14

## Results
Amazon Review Datasets for US video games was ETL'd (Extract, Transformed and Loaded) using AWS RDS, PySpark, Google Collab using Python and PostgreSQL. 

See code here, https://github.com/Ninax3/Amazon_Vine_Analysis/blob/main/Amazon_Reviews_ETL.ipynb

Vine Table Data
![MechaCar_Statistical_Analysis "total_summary"](https://github.com/Ninax3/MechaCar_Statistical_Analysis/blob/main/total_summary.png)
![Amazon_Vine_Analysis "Vine_Table_df"](

Next, the Vine_Table was used to filter for video game titles that had 20 or more reviews, then filtered for a ratio of "helpful votes" to "total "votes" of 50% or greater. Then votes were counted for "unpaid votes" (non-vine votes) versus "paid votes" (vine votes) and the percentage was calculated for each versus "5-star reviews" per each category. 

See code here, https://github.com/Ninax3/Amazon_Vine_Analysis/blob/main/Vine_Review_Analysis.ipynb

-There were 94 paid (Amazon Vine Program) reviews including 48 "5-star" reviews, for a percentage of 51.1%

-There were 40,471 unpaid reviews including 15,663 "5-star" reviews, for a percentage of 38.7%

## Summary
With 51.1% of the Amazon Vine Program reviews having a "5-star" review versus 38.7% of non-paid reviews having a "5-star" review, the data shows there is a positivity bias for reviews in the Amazon Vine Program. To further confirm this finding, an additional anlaysis is recommended to 
1. perform the same analysis on datasets for "paid" and "unpaid" for "verified purchases" and 
2. compare the statistical distribution (mean and standard deviation) of each review sample. 
