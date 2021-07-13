# Big Data and AI Compendium

### Cloud / Hybrid storage / Containers
### Data warehouse
### Data lake
### SQL Databases
### NoSQL Databases
### Graph Databases
### Data Observability / Data Ops / ML Ops / Lineage
### Stream-processing / Pub-Sub / Messaging 
### Data Ingestion / Data Wrangling / ETL / ELT
### Labeling / Annotation
### Monitoring / Security
### BI / Visualizations
### Notebooks
  - Apache Zeppelin:  A web-based notebook enabling data-driven, interactive data analytics and collaborative documents. (incub. rel. 7/23/2015, 0.9.0 rel 12/26/2020) - https://zeppelin.apache.org/
    - Interpreters:
      - Spark: unified analytics engine for large-scale data processing - (rel. 5/26/2014, lr. 3/2/2021) - https://spark.apache.org/
      - JDBC: Java (API for) DataBase Connectivity - (rel. 2/19/1997, lr. 9/21/2017) https://docs.oracle.com/javase/tutorial/jdbc/basics/index.html
        - PostgreSQL: World's most advanced open-source relational DB - (released 6/1989, last release 5/13/21) - https://www.postgresql.org/
        - MySQL: World's most popular open-source database. (released 5/23/1995, last release 5/11/21) - https://www.mysql.com/
        - MariaDB: A community-developed fork of the MySQL RDBMS. (released 10/29/2009, last release: June 18, 2021) - https://mariadb.org/
        - Redshift: An Amazon data warehouse product handling analytics workloads on big data data sets. Columnar, parallel-processing, high compression with 16 pb cluster sizes. (released Oct 2012) https://aws.amazon.com/redshift/
        - Hive: Open-source Data warehouse facilitating r/w and management of big data data sets stored in distributed storage queried via SQL. (released 10/01/10, last release: Aug 26, 2019) - https://hive.apache.org/
        - Phoenix: OLTP and operational analytics for Hadoop using SQL/ACID transactions, with late-binding, schema-on-read flexibility using HBase (see below)  (released 4/2014, last release: Jun 7, 2021) - https://phoenix.apache.org/
        - Drill: Schema-free SQL query engine for Hadoop, NoSQL and cloud storage (Hbase, MongoDB, MapR-DB/FS, HDFS, S3, Azure Blob, GC, Swift, NAS and local fs. (released 2012, last release: September 5, 2020) https://drill.apache.org/
        - Tajo (retired): Big data relational and distributed warehouse system on Hadoop, queries with SQL. (released 2013, last release: May 18, 2016) - https://tajo.apache.org/
      - Python: An interpreted, high-level, dynamically-typed, garbage-collected general-purpose programming language which supports procerdural, OO and functional programming paradigms - (released, 2/91, last release: 28 June 2021) - https://www.python.org/
      - Hbase: An open-source, Hadoop ecosystem, distributed, scalable big data non-relational database store based on Google BigTable. (released 2008, last release: 	2021/06/14) - https://hbase.apache.org/ 
      - pig: High-level platform built on Hadoop platform and abstracts MapReduce/Apache Tez and Spark complexity using a language similar to SQL with extensibility through user-defined functions (UDFs) written in Java, python, javascrip, Ruby or Groovy (released 2008, last release: 19 June, 2017) -https://pig.apache.org/
      - beam - An open-source unified model for defining both batch and streaming data-parallel processing pipelines, executing said pipelines through a distributed processing back-end (Flink, Spark, GC Dataflow). - https://beam.apache.org/
      - scio - A Scala API for beam and GC Dataflow. - https://spotify.github.io/scio/
      - BigQuery - Serverless, scalable data warehouse with petabyte scale using ANSI SQL.  ML Features for building models, multicloud analytics solution for interaction with AWS and Azure, BI engine to connect to Data Studio or Looker. - https://cloud.google.com/bigquery
      - Livy: Programmatic, fault-tolerant, multi-tenant submission (from web/mobile apps), REST service for Spark.  Spark/Python. - https://livy.incubator.apache.org/
      - HDFS: Hadoop file system - https://hadoop.apache.org/docs/r1.2.1/hdfs_user_guide.html
      - Alluxio: Open source virtual distributed file system (VDFS).  A data orechestration layer between computer and storage, abstracting the files/objects (rel: Apr 8, 2013, lr: 6/23/2021) - https://www.alluxio.io/
      - Scalding: Scala API for Cascading - Scala library on top of Hadoop MapReduce jobs, build on Cascading. https://twitter.github.io/scalding/
      - Elasticsearch: A distributed, multitenant capable, full-text search engine based on the Lucene library, with HTTP web interface and schema-free JSON documents.  (rel: 2/8/2010, lr: 5/25/2021) https://www.elastic.co/elasticsearch/
      - Angular: Typescript-based web application framework by Google / OS community. (rel: 9/14/2016, lr. 6/30/2021)
      - Markdown: Lightweight markup language - https://www.markdownguide.org/
      - Shell
      - Flink: Unified stream and batch processing framework written in java aand scala.  Executes dataflow programs in data-parallel, iterative and pipelined manner. High-throughput, low-latency streaming engine, event-time processing and state management.  Supports exactly-once, java, scala, python and sql. (rel 5/2011, lr, 5/28/2021) - https://flink.apache.org/
      - Cassandra: Open source, NoSQL distributed database trusted for scalability and high availability, without compromising performance.  Linear scalability and fault-tolerant on commodity hardware.  (rel 72008, lr. 2/1/2021) - https://cassandra.apache.org/
      - Geode: In-memory data management platform and distributed data container, which pools resources (memory, CPU, network and opt. disk) to manage them and provide dynamic replication, data partitioning to implement high availbility, performance, scalability, fault-tollerance, rolling-upgrade support, atomic transactions (executed on a single node and distributed afterwards), LRU eviction/expiration.
      - Ignite: Distributed Database for high performance computing with in-memory speed, co-located compute/tasks (java, scala, kotlin, c#, c++), optional distributed ACID, built-in ML tools and integrations, Continuous queries (replacing triggers) (rel- 3/24/2015, lr: 3/15/2021)
      - Kylin: MOLAP engine with SQL interface.  OLAP data warehouse with billion row query at sub-second latency with identification of star/snowflake schemas on Hadoop, cube building (aggregated data) and access via Open DataBase Connectivvity (ODBC)/JDBC/RESTful API).  Connects Hadoop to BI tools (Tableau, PowerBI/Excel, MSTR, QlikSense, Hue and Superset). (rel: 6/10/2015, lr: 9/13/2020)
      - Lens (retired): Unified analytics interface across multiple tiered data stores.  
    - web: https://zeppelin.apache.org/
    - repo: https://github.com/apache/zeppelin
    - twitter: https://twitter.com/ApacheZeppelin
### ML / NLP / Neural Network
### Search Engine
### Data Governance / Regulatory Compliance
