# Amazon_Vine_Analysis
UTMCC DataViz Module 16 Challenge Amazon Vine Analysis

---

## Contents 
  * Overview
    - Purpose
    - Resources
  * Results
  * Summary
 

---  

## Overview 
  In continued work with SellBy, this project focusses on the analysis of Amazon product reviews. The reviews are a component of the Amazon Vine program, a service that allows suppliers of products to receive reviews written by members of the paid Vine program. Companies can elect to pay a fee to Amazon, and to provide example products to Vine members, who then are required to publish a written review within the Amazon system. 

   ### Purpose
   To prepare a statistical analysis on a chosen Vine review category, downloaded from the Amazon cloud. Using PySpark and working within Colab notebook, and using AWS S3 storage and AWS RDS with a hosted PostgreSQL database, an ETL and transform process was performed on selected data. The analysis was to determine if any favorable bias exists with reviews in the data between Vine-paid reviews versus reviews that were not in the Vine program. 
  
   The deliverables are: 
   - Deliverable 1: Perform ETL on Amazon Product Reviews
   - Deliverable 2: Determine Bias of Vine Reviews
   - Deliverable 3: A Written Report on the Analysis (this README.md).
   
  
   ### Resources
  * Data/content sources: amazon_reviews_us_Grocery_v1_00.tsv.gz dataset https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Grocery_v1_00.tsv.gz
  * Software: Windows10, Python 3.8.3, Google Colab Notebook, Apache Spark 3.0.1, PySpark, PostgreSQL, pgAdmin 4.24
  * Services: AWS S3 data storage, AWS RDS database hosting. 
  

--- 

## Results


### Deliverable 1: Perform ETL on Amazon Product Reviews
   * DataFrames were transformed from the Amazon Vine Review dataset, and loaded into PostgreSQL. The dataset chosen for this analysis was "us_Grocery".
   * Please see files: `Amazon_Reviews_ETL.ipynb`  and  `Module16_Challenge_Amazon_Reviews.sql` 
   
   
   **All four PostgreSQL tables, as shown using pgAdmin:**  <br>
   | **customers_table** | **products_table** | **review_id_table** | **vine_table** |
   | :---: | :---: | :---: | :---: | 
   | ![customers_table.png](https://github.com/larrydodson/Amazon_Vine_Analysis/blob/main/customers_table.png) | ![products_table.png](https://github.com/larrydodson/Amazon_Vine_Analysis/blob/main/products_table.png) | ![review_id_table.png](https://github.com/larrydodson/Amazon_Vine_Analysis/blob/main/review_id_table.png) | ![vine_table.png](https://github.com/larrydodson/Amazon_Vine_Analysis/blob/main/vine_table.png) | 
 
.

### Deliverable 2: Determine Bias of Vine Review 
  * Using PySpark and Colab notebook.  .  Please see: `Vine_Review_Analysis.ipynb`  
  * Filters on the data: 
    1) Reviews that were ≥ 20 total_votes recorded, and 
    2) Reviews where the ratio of helpful_votes to total_votes was ≥ 50 percent.  After these filters were made, the following analysis was performed.

      **Information from the dataset original file used for extraction, and the above two filters used on us_Grocery,  `amazon_reviews_us_Grocery_v1_00.tsv.gz`:** 
      
     | **Item** | **Quantity**, `.count` | 
     | :--- | ---: | 
     | Total number of original Reviews | 2,402,458 | 
     | Number of Reviews post filter for ≥20 total_votes | 31,518 |  
     | Number of Reviews post filter for ≥50% helpful_votes | 28,348 | 



**Questions:**  Using bulleted lists and images of DataFrames as support, address the following questions:
  *1. How many Vine reviews and non-Vine reviews were there?*
  
     | **Quantity of Vine Reviews** | **Quantity of non-Vine Reviews** |
     | :---: | :---: |
     | ![]() <br>334,443 | ![]() <br>787,555 |  
 
 
  *2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?*
 
     | **Quantity of 5-Star Vine Reviews** | **Quantity of 5-Star non-Vine Reviews** |
     | :---: | :---: |
     | ![]() <br>cde  | ![]() <br>fgh  | 
 
 
  *3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?*
  
     | **Percentage of 5-Star Vine Reviews** | **Percentage of 5-Star non-Vine Reviews** |
     | :---: | :---: |
     | ![]() <br>abc  | ![]() <br>abc  | 
     | ![]() <br>abc  | ![]() <br>abc  | 
 
 
.

### Deliverable 3: A Written Report on the Analysis (*this README.md*)
  
<br>

---

# Summary

### Questions and Replies 
  *1. state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement.* 
  
  
  *2. provide one additional analysis that you could do with the dataset to support your statement.*





.

.end
