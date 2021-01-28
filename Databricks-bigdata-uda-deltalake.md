
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



#### What are some challenges when it comes to building big data analytics for business?

#### What are the parts that make up Databricks?

#### What is the Collaborative Data Science Workspace?

#### What is the Unified Data service?  Databricks runtime?  Delta lake?  Databricks injest?

#### What is BI Integration?

#### What is Enterprise Cloud Service?

#### What parts make up a Delta Lake Lakehouse?

#### What are the advantages of Delta lake?

#### What are the disadvantages of Delta lake vs other technologies?

#### What is OLTP?  What is OLAP?  

#### What is an ODS?  What is EDSS Stand for?

#### What does SSOT stand for?

#### What are the 3 pillars of Delta Lake?
