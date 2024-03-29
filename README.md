## Project Overview:

The project involves setting up a star-schema data warehouse and creating efficient pipelines for building retail data marts, which are later utilized for business analysis.

## Problem Statement:

A fictitious national department store which decides to build a starschema based sales analysis data warehouse with the dimensions of customer, store, product, Over time, dimension attributes are expected to change, and the requirement is to preserve versions of these changes in the star-schema data warehouse in order to deliver accurate results with queries that relate to prior versions of dimension attributes.

## Data Source:

The data source for populating the star schema is the store's online transaction processing (OLTP) system.

![Data Source](https://github.com/AliMagdy100/Retail-Store-Data-Analysis-And-ETL-using-DataStage/assets/87953057/b3c1b798-77f9-40a4-9957-e0cc646033ab)

## Project Steps:

The primary tool utilized to address the problem is IBM InfoSphere DataStage, serving as an ETL tool.

**1- Building the Physical Data Model:** Constructing a star schema comprising three dimensions: ```product```, ```retail```, and ```customer```, alongside a fact table: ```transactions```.

![Physical Data Model](https://github.com/AliMagdy100/Retail-Store-Data-Analysis-And-ETL-using-DataStage/assets/87953057/a3c63b31-54f2-454d-ae99-4a2e12131774)

**2- Extraction:** Extracting data from the data warehouse, ensuring the inclusion of relevant customer, store, and product information.

**3- Transformation:** Conducting necessary transformations on the extracted data to align it with business requirements, such as converting customer name columns to uppercase.

**4- Data Mart Creation:** Developing a data mart named ```RETAIL_DATA_MART```, containing transaction details for each customer categorized by customer type ("citizen" or "foreign"), product information, and purchased stock.

**5- Loading:** Loading the transformed data into the data mart ```RETAIL_DATA_MART```.

**6- Data Mart Analysis:** Utilizing the ```RETAIL_DATA_MART``` to address various business needs, including:

- Displaying the count of all transactions for each employee in each store.
- Identifying the customer type ("citizen" or "foreign") contributing the highest profit, attributing maximum profit to foreign customers if they make more transactions than citizen customers.
- Awarding bonuses to customers contributing the most to profit.

## Project Files:

- DataStage Jobs: Containing the dsx files for the DataStage jobs.
- Dataset: Holding the data after being modeled in a star schema data warehouse.
- Output_Data: Showcasing samples of the data post-analysis.

