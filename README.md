## Project Overview:

The project implements a star-schema data warehouse and make efficient pipelines for creating a retail data marts, which we used later for business analysis.


## Problem Statment:

A fictitious national department store decided to build a star-schema-based sales analysis data warehouse with the dimensions of customer, store, and product. Over time, dimension attributes are expected to change.

The requirement is to preserve versions of all changes in the star-schema data warehouse in order to deliver accurate results with queries that relate to prior versions of dimension attributes.


## Data Source:

The data source for populating the star schema is the store's online transaction processing (OLTP) system.

![242076005-5c80f680-28f9-4289-b900-9c48d26e2256](https://github.com/AliMagdy100/Retail-Store-Data-Analysis-And-ETL-using-DataStage/assets/87953057/b3c1b798-77f9-40a4-9957-e0cc646033ab)

## Project Steps:

The IBM InfoSphere DataStage tool is mainly used as an ETL tool to solve the problem.

**1- Building the Physical Data Model:** A star schema is built with three dimensions: ```product```, ```retail```, and ```customer```. And a fact table: ```transactions```.
![image](https://github.com/AliMagdy100/Retail-Store-Data-Analysis-And-ETL-using-DataStage/assets/87953057/a3c63b31-54f2-454d-ae99-4a2e12131774)

**2- Extraction:** Extract the data from the data warehouse, ensuring the inclusion of relevant customer, store, and product information.

**3- Transformation:** Perform some transformations on the extracted data to align it with the business needs. This includes converting customer name columns to uppercase.

**4- Data Mart Creation:** A data mart named ```RETAIL_DATA_MART``` is developed. It contains each transaction for each customer, categorized by customer type ("citizen" or "foreign"), information about the product, and the stock purchased. 

**5- Loading:** The transformed data will be loaded into the data mart ```RETAIL_DATA_MART```.

**6- Data Mart Analysis:** The data mart ```RETAIL_DATA_MART``` is used to answer some business needs:

- Display the count of all transactions for each employee in each store.
- Identify the customer type ("citizen" or "foreign") that generates the highest profit. For Example: if "foreign" customers make 5 transactions and citizen "customers" make 3 transactions, the maximum profit would be attributed to foreign customers.
- A bonus is given to the customer(s) who contribute the most to the profit.

## Project Files:

- DataStage Jobs: contains the dsx files for the DataStage jobs
- Dataset: contains the data after it is modeled in a star schema data warehouse model.
- Output_Data: contains samples of the data after analyzing it.

