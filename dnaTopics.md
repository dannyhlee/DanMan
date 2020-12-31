## Acronyms

POC = Proof of concept   
RACI = Responsible, Accountable, Consulted and Informed   
ITIL = Information Technology Infrastructure Library (volume of best practices)   
COE = Center of Excellence - team/facility/entity provides leadership, best practices, research, support, training.   
TCO = Total Cost of Ownership   
GDPR = General Data Protection REgulation, 2016   

## Numbers

PB = petabytes = 1000 tb = 10^^15   
EB = exabytes = 1000 pb = 10^^18   
ZB = zettabytes = 1000 eb = 10^^21   
YB = yottabytes = 1000 zb = 10^^24   

## Data Operations Services

ICC = I Command Center
IDW = I Data Operations Workbench
DSD = Data Strategy & Diagnostics
SSS = Secure Scalable Stable

## Analytics Workbench

## Genome Solution

## NIA

## Data Stores
#### ODS
Operational Data Store, central database where data is integrated from disparate sources, can be used in front of a data warehouse to aggregate and cleanup data.

#### OLTP
Online Transaction Processing - real-time execution of large numbers of db transactions by large numbers of people.  Transactions are operations like change, insert, delete or query.  Atomicity and ACID characteristics are important.  OLTP systems process relatively simple transactions, very rapidly and available 24/7/365.  Large number of concurrent transactions means that any downtime or data loss can have significant and costly repercussions.  Requires frequent incrememental and whole backups. OLTP uses RDBMS.  Examples: atm/credit card processing/orders and bookings online

#### OLAP 
Online Analytical Processing System - Stores historical data from OLTP.  OLAP is optimized for complex data analysis by data scientists, analysts, BI workers - supports data mining, BI and other decision support applications.  OLAP uses multidimensional databases made up of RDBs.  OLAP queries are complex, on large numbers of records.  OLAP queries are slower than OLTP and do not change data (read-intensive). 

## BI

#### Microsoft Power BI

Is a collection of software services, apps and connectors that work together to turn unrelated sources of data into coherent, visually immersive and interactive insights.

#### Enterprise dashboards

are dynamic digital and visual tools that offer insights into a company's metrics.  Dashboards are tuned to focus on particular KPIs and allow the spotting of trends, weaknesses and develop strategies that will improve performance.

#### Teradata Vantage

Real-time cloud consumption and analytics processing, runs on premise and on cloud platforms by AWS, Azure and GCP.  Infosys solutions:
- DSD (Data Strategy and Diagnostic Solution) - Connects to Teradata and does analysis and diagnosis, extracting data to a Tableau dashboard.
- Data migration assessment and recommendation engine - Used to inventory and recommend a migration approach
- Migration workbench - UI driven framework for schema conversion, data migration and validation
- iTedge - UI based SQL interface generates TPT (Teradata Parallel Transport) control files, imp/exp data thru jdbc and data validation activities
- Judex code review - DDL review tool

---

## ETL Process

#### 1. Capture

To obtain a snapshot of chosen subset of source data.  **static** - at a point in time.  **incremental** - changes since last static

#### 2. Scrub

To cleanse data using pattern recognition and AI to upgrade quality.  **fix errors** - missing fields, nulls, duplicates, misspellings, inconsistencies.  **ai usage** - decoding, reformating, time stamp, error detection, key gen.

#### 3. Transform

Convert from operational system's format to data warehouse format.  **Record level** - Selection (data partitioning), Joining (data combining), Aggregation (summarization).  **Field level** - single field - 1 to 1, multi field - 1 to n, n to 1.

#### 4. Load and Index

Place transformed data into warehouse and create indexes.  **refresh mode** bulk rewrite of target data **update mode** only change are written.

