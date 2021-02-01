
#### What is a Data warehouse?

A data warehouse is a data management system designed to be a "single source of truth" for business intelligence (BI) activities like analytics.  They are usually build by deriving data from multiple sources.  They hold data that is meant to be queried upon and often contain large amounts of historical data.  The centralization and consolidation of data from multiple resources allows organizations to extract valuable business insights to improve decision making.  Some benefits of using a data warehouse include:
- Extracting insights to make better decisions
- Bringing together data from multiple sources and conforming them to the desired structure
- Being able query over and analyze large amounts of historical data
- By using ETL processes we can ensure that the data is consistent, accurate and of high quality (aka "Golden records")
- Disconnects analytical processing with the storage to improve performance.
- Schema can be implicitly or explicitly implemented.  If defined prior to ingestion, it is schema-on-write.  At the time of analysis, or reading, it is schema-on-read.

#### What is a Data lake?

A data lake a repository for all types of data (structured, semi-structured and unstructured data) at any scale.  Data is stored as-is and can be in a raw state, and as opposed to hiearchial structure of a warehouse (folders, files) data lakes store data in a flat architecture where data is given a unique identifier/meta data and often stored as objects (S3/Azure blob).  Cloud storage options are cheap, but the raw nature makes Data lake data harder to work with.  Querying over structureless data can take longer.  

#### What is a Data lakehouse?
Data lakehouse is a new design proposed by Databricks to bridge the gaps between data warehouses and data lakes.  Provides storage on low-cost cloud storage used for data lakes, but provides Transactional ACID support, Schema enforcement and governance, BI Support, support for a wide variety of data type and workloads, along with support for streaming and batch processing.

Delta lake decouples compute and storage, and provides scalability and availability.  Its a performant and reliable, ACID compliant, with optimizations that make DL best in class solution for object storage in the cloud.

![warehouse vs lake vs lakehouse](https://databricks.com/wp-content/uploads/2020/01/data-lakehouse.png)
(Image hosted at https://databricks.com/glossary/data-lakehouse)

#### What is a Unified Data Platform?

Unified Data brings together data from disparate sources, cleans and transforms it into a format that can be analysed to extract analytical data.  These platforms provide fast data ingestion, real-time streaming analytics, historical analytics, predictive analytics, and prescriptive analytics.    The uniformed data platform is capable of moving data throughout an organization, regardless of volume, velocity or variety of data types, by ingesting from internal and external sources, enriching, munging, and/or transforming the data, making it available to consumers, and then persisting it in storage.

#### What is Artificial Intelligence?
AI encompasses the entire realm of what it means for "machiens that respond to stimulation consistent with traditional responses from humans, given the human capacity for contemplation, judgment, and intention.” Researchers Shubhendu and Vijay described AI as software systems that “make decisions which normally require [a] human level of expertise”. John Allen and Darrell West argued AI systems have three qualities that define them: intentionality, intelligence, and adaptability.  An example is the Turing test.

#### What is Machine Learning?
A subset of AI, that includes that includes applications and algorithms that learns on its own, when given enough data, will retrain itself to be more accurate.  It works well with structured data and recognizes patterns.  Predicts the likelihood of something being or not being.  ML is also a method of data analysis based in automated, self-teaching by developing analytics models that can identify patterns and make decisions.  The models accuracy is verified by humans.

#### What is Deep Learning?

A subset of ML, made up of applications that teach themselves to perform a task with increasing accuracy without human interaction.  Uses neural networks (sets of algorithms modelled on the human brain).  

#### What is Data Science?

Data Science brings together the fields of math, statistics and business and uses tools and workflows to (process, manage and analyze) data to extract insights that inform business decisions.   The workflow consists of:
- Identifying the business need
- Ingestion of data (as a stream or batch, often raw and messy)
- Munge the data (cleanse it and make it safe)
- Data Analysis
- Sharing the insights gleaned from data through visual dashboards, presentations, emails, etc.

#### What is the role of: Data engineers, Data Scientists, Data analysts and Platform administrators?

Data Engineers develops, tests and maintains system for data systems (data pipelines) to improve data quality, efficiency and reliability.  They provide the data in ready to use form for the data scientist.  The data scientist writes machine learning algorithms, and statistical methods to develop the predictive model to answer business needs.  Data scientists test and track ML models using python, R, SQL and ML libraries. Business analysts generate different types of records, using sql, Tableau, PowerBI, looker to extract insights and to make informed business decisions.  Platform administrators setup the infrastructure, updates and maintains the software, does health checks, implements best practices and monitors usage.

#### What are the advantages of Big Data Analytics for Business?

- Understand the customers better
  - Who are they?
  - How do they use the product?
  - What do they like?
- Improve the product
  - What do customers like most?
  - Should we make changes?
  - What changes should we make?
- Protect the business
  - Are we investing in the right things?
  - Will the risks we take pay off?
- Stay ahead of the competition
  - Who are the competitors?
  - What are the trends?
  
#### What are some challenges when it comes to building big data analytics for business?

1. Siloed workflows and data: The data engineers, data scientists and data analysts work in separate spheres which can cause confusion, poor data consistency
2. Securing data: Data security must comply with laws such as GDPR, HIPAA and various laws, in different regions.  Once customer trust is lost, it may never be regained or at the very least, it will take a long time to regain.
3. Other challenges:
  - combining batch and streaming adta
  - older architectural patterns may be a struggle to adapt
  - designing and implementing a single souce of truth
  - guaranteeing data availability

#### What are the parts that make up Databricks?

- Collaborative Data science workspace 
- BI Integrations
- Unified Data Servicec
- Enterprise cloud service

#### What is the Collaborative Data Science Workspace?

The Collaborative Data Science Workspace is where data scientists, data engineers and data analysts can work together in collaborative notebooks and with managed ML flow.  The notebooks support real-time comments, sharable notebooks, automated versioning, rules to automate processes.  The managed ML Flow provides experiment tracking and centrally managed models, with the ability to monitor and tune models and deploy them to production.

#### What is BI Integration?

Provides integrations to easily connect popular BI tools such as Power BI, tableau, QlikQ, looker, TIBCO, SQL Workbench/J to Databricks clusters and SQL endpoints.  This allows the BI tools to use the power Databricks to analyse their data and prepare reports and visualzaiotns.

#### What is the Unified Data service?  Databricks runtime?  Delta lake?  Databricks injest?

The Unified Data service is made up of the Databricks runtime, Delta Lake and Databricks injest.  

The Databricks runtime is made up of an optimized version of Spark, which is more performant than the Open Source version, which runs on an auto-scaling infrastructure with auto termination after a certain amount of idle time. A powerful engine that can scale up or scale down as needed, and also shuts down when not being used so you pay for the power you need.

Delta lake adds intelligence to data lake storage via a transaction log, which provides transactional performance and brings ACID properties to data lake storage. Delta lake is a reliable, historical version tracking and performant warehouse layer that includes connections to viz tools and cleans up data.

Databricks injest brings data together from different sources and allows real-time incrementaion to Delta Lake.

#### What is Enterprise Cloud Service?

The Enterprise Cloud Service provides Security features and allows enterprises to retain control over data by storing data in their own cloud account (encrypted as needed).  It creates isolated and compliant (GDPR/HIPAA) workspaces and can be implemented with OKTA corporate directories and SSO for long.  Admins can onboard and offboard users, control costs, set alerts and Enterprise Cloud Service has auditting fucntionality to track user access and usage.

#### What parts make up a Delta Lake Lakehouse?

Delta Lake Lakehouse is made up of Delta Tables, Delta Files and the Delta transactionlog. The delta files are held in object stores (parquet format) with data version tracking, metadata and transaction logs.  The delta tables are a Hive metastore.  And Delta transaction log is stored with the delta files in the object store. Currently Delta storage is able to work with ADLS (Azure Data Lake Storage) and AWS s3)

#### What are the advantages of Delta lake?

A Delta lakehouse is a warehousing option that decouples computer from storage, provides scalability and availability with lower cost.  Spark handles the load & compute, while DL takes care of the permentant storage. DL is a performant and reliable with ACID transactions and optimizations that make DL best in class solution for object storage in cloud.  Developer time costs more than compute, so building a solution with Databricks can reduce the amount of dev time needed to get up and running.

#### What are the disadvantages of Delta lake vs other technologies?

Delta lake and Databricks charge for compute is a surcharge on Ec2 instances.  Its more than AWS EMR might be, and you have more control if you develop a custom solution.  With databricks you are limited to altering your isntances to be high CPU or high memory.  

#### What is OLTP?  What is OLAP?  

OLTP or Online Transaction Processing is a category of data processing that focuses on tasks like inserting, updating or deleting small amounts of data (large volume, simple transactions).  Generally needs to handle high volume, and multiple simultaneous users and uses ACID transactions to record events and can be required to operate on a continuous basis (24/7/365).  OLTP workloads are write intensive, but generally don't need that much storage space, but they do need constant (or concurrent) backups.

OLAP or Online Analytics Processing is the performance of complex data analysis, designed by data scientists and business analysts to support data mining, analysis and other DSSs.  OLAP require multidimensional databases, that can handle complex queries, involving large amounts of records.  OLAP processing is orders of magnitude slower and updates to data are low or none.  OLAP workloads are read intensive.  OLAP have significant storage requirements, and need backups less frequently

#### What is an ODS?  What is EDSS Stand for?

An ODS, or Operation Datastore, is a centralized storage database that aggregates transactional data from one or more data sources that are doing transactional processing and consolidates, performs munging or ETL to prepare that data to be used in conjunction with BI tools to aid in tactical Decision making.  It provides an alternative to a DSS which is connected directly to the data sources that are performing transaction processing.  An ODS performs OLTP.

And EDSS stands for a Enterprise Decision Support System, and contains all versions of data and a history of all transactions.  They can be on-premise or in the cloud, leveraging data lake, data warehouse or data lakehouse technology.  An EDSS performas OLAP.

#### What does SSOT stand for?

The Single Source of Truth is a practice in the design and implementation of Information systems so that everybody accessing data, code, configuration or other assets are all accessing the same resource.   Rather than storing duplicated data, in multiple siloed repositories, we make sure they are all the same.  When we duplicate data, we increase the chance of errors and inconsistencies in data.

#### What are the 3 pillars of Delta Lake?

The 3 pillars of Delta lake are: 
1. Clean, Quality Data - ACID transactions, schema enforcement during ingestion and evolution, exactly once semantics, time travel (rollback, audit trails, reproduccable ml experiments)
2. Consistent views across stream and batch workloads - isolates snapshots which allows simulatenous r/w, mixed streaming/batch data, can handle both.  Acts as a batch table and a streaming source/sink.
3. Optimized and easy to adapt - uses sparks distributed processing power to work with meta data, works with on-premise hdfs, compatible with spark APIs, open source, no data lock-in, local dev possible, in-place import from parquet to delta.
