### WEEK 3:

Gathering Data<br>

**Identifying Data**<br>
- Source of Data
- Type of Data
- Timeframe over which you need the data
- Volume of Data<br>

**Data Sources**<br>
> Data sources can be internal or external to the organization
- Primary: Refers to information obtained directly forth source. Eg. Surveys, observation
- Secondary: Refers to information retrieved form existing sources. Eg. External database
- Third party: Refers to data purchased form aggregators who collect data from various sources and combine it into comprehensive datasets for purpose of selling the data.

> Gathering data form data sources such as databases, the web, sensor data, data exchanges, and several other sources.

**How to gather and import data**<br>
- SQL, or Structured Query Language, is a queuing language used for extracting information from relational databases.
- Non- relational databases can be queried using SQL or SQL like query tools. Like CQL for Cassandra and GraphQL for Neo4j.
- API, Application Programming Interfaces. Are invoked form applications that require the data and access an endpoint containing the data. Endpoints can include databases, web services and data marketplaces.
- Web Scraping (Screen Scraping, Web Harvesting)
- Senior data, Data streams are popular source for aggregating constant streams of data flowing from sources such as Instruments,  IoT devices, Applications and GPS data from cars
- Data Exchange platforms, <br>


*Wrangling Data*<br>
> Data wrangling, also known as data munging, is an iterative process that involves data exploration, transformation, validation, and making it available for a credible and meaningful analysis
1. Discovery
2. Transformation: Structuring, Normalizing and Denormalizing Data, Cleaning Data and Enriching Data 
 * Structurally manipulate and combine the data using Joins and Unions.
* Normalize data, that is, clean the database of unused and redundant data.
* Denormalize data, that is, combine data from multiple tables into a single table so that it can be queried faster. 
* Clean data, which involves profiling data to uncover quality issues, visualizing data to spot outliers, and fixing issues such as missing values, duplicate data, irrelevant data, inconsistent formats, syntax errors, and outliers.
* Enrich data, which involves considering additional data points that could add value to the existing data set and lead to a more meaningful analysis.

3. Validation
4. Publishing

*Tools for Data Wrangling*
* Excel Power Query/ Spreadsheets
* OpenRefine
* Google DataPrep
* Watson Studio Refinery: IBM
* Trifecta Wrangler
* Python: Numpy and pandas
* R: Dplyr, Data table, Jsonlite

*Data cleaning workflow:*
1. Inspection 
2. Cleaning
3. Verification
