# Big Data and AI Compendium

### Cloud / Hybrid storage
  - Amazon AWS
    - S3: Simple Storage Service. Object storage.  Industry-leading performance, scalability, availability and durability. - https://aws.amazon.com/s3
    - EFS: Elastic File System.  Cloud-native, elastic, scalable, serverless, fully managed POSIX-compliant file system.  - https://aws.amazon.com/efs
    - EBS: Elastic Block Store.  High performance, block-storage for use with EC2 (Elastic Computer Cloud). - https://aws.amazon.com/ebs/
    - Backup and Glacier: Low cost. - https://aws.amazon.com/backup/
    - DataSync: Online data transfer automation -https://aws.amazon.com/datasync
    - Storage Gateway: On-premises, hybrid cloud services providing access to virtually unlimited cloud storage - https://aws.amazon.com/storagegateway
    - Snow Family: Physical devices to migrate data into and out of AWS.  Also Edge computing services and storage - https://aws.amazon.com/snow
  - Google Cloud Storage
    - Cloud Storage: Object storage - https://cloud.google.com/storage
    - Block Storage: Persistent and local (ephemeral) ssd. Integrated with Compute Engine and GKE (Google Kubernetes Engine) - https://cloud.google.com/persistent-disk
    - FileStore: File storage, easily mountable to Compute Engine VMs - https://cloud.google.com/filestore
    - Archival Storage: Low cost. - https://cloud.google.com/storage
    - Storage Transfer Service: Secure, low-cost services to transfer data to the cloud or on-premises - https://cloud.google.com/storage-transfer-service
  - Azure Storage
    - Azure Disks: Block-level storage volumes for Azure VMs - https://azure.microsoft.com/en-us/services/storage/disks/
    - Azure Blobs: Massively scalable object store, support for Data Lake Storage Gen2 - https://azure.microsoft.com/en-us/services/storage/blobs/
    - Azure Data Lake Storage: Massively scalable, secure data lake for high-performance analytics workloads - https://azure.microsoft.com/en-us/services/storage/data-lake-storage/
    - Azure Files: Managed file shares for cloud or on-premises deployment - https://azure.microsoft.com/en-us/services/storage/files/
    - Azure NetApp Files: Enterprise file storage, powered by NetApp - https://azure.microsoft.com/en-us/services/netapp/
      - NetApp: Hybrid cloud data services and data management company - https://www.netapp.com/
    - Azure Data Box: Appliances and solutions for offline data transfer to Azure - https://azure.microsoft.com/en-us/services/databox/
    - MS Azure Confidential Ledger: Store unstructured data, completely tamper-proof and can be cryptographically verified - https://azure.microsoft.com/en-us/services/azure-confidential-ledger/
  - IBM Storage
    - IBM Cloud Object Storage: Flexible, cost-effective, scalable storage for unstructured data - https://www.ibm.com/cloud/object-storage
    - IBM Cloud Backup: Fully encrypted backup and recovery across multiple datacenters - https://www.ibm.com/cloud/backup
    - IBM Cloud Block Storage: The lowest latency, highest redundancy data storage option - https://www.ibm.com/cloud/block-storage
    - IBM Cloud File Storage: The simplest solution for data organized into files and folders - https://www.ibm.com/cloud/file-storage
    - IBM Cloud Mass Data Migration: Secure hardware to physically ship petabytes of data to IBM Cloud - https://www.ibm.com/cloud/mass-data-migration

### Data warehouse
  - Amazon Redshift: Integrated with AWS ecosystem, high performance, with AQUA (Advanced Query Accelerator, Petabyte-scale warehousing and analytics, secure and compliant (SOC1, SOC2, SOC3, PCI DSS Lvl 1)
  - Google BigQuery: Petabyte scale, serverless, ML built-in, BigQuery Omni allows access to multi-clouds (AWS and Azure) using standard SQL, BI Engine and integration with Google Data Studio, Looker. - https://cloud.google.com/bigquery
    -  BigQuery ML: Create and execute ML models using standard SQL queries via GC console, bq CLI, REST API, or external notebooks - https://cloud.google.com/bigquery-ml/docs/
    -  BigQuery Omni: Query AWS and Azure from BigQuery UI using standard SQL, powered by Anthos. - https://cloud.google.com/blog/products/data-analytics/introducing-bigquery-omni
      -  Anthos clusters: Enterprise-grade conformant kubernetes services across hybrid and multi-cloud environments. - https://cloud.google.com/anthos/clusters
    -  BigQuery BI Engine - https://cloud.google.com/bi-engine/docs
    -  Google Data Studio - https://analytics.google.com/analytics/academy/course/10
    -  Google Looker - Cloud based BI/Analytics platform.  Unified metrics, permissioning, version-control, security, cloud and best-in-class APIs.  Multicloud, abstraction of underlying data complexity to operationalize BI for everyone, rapid time to value and leading-edge AI/ML and advanced analytics.
  - Microsoft Azure Synapse Analytics: Unified analytics platform, serverless/dedicated options, enterprise data warehouse, integrated with Spark and SQL engines (T-SQL), code-free visual ETL/ELT ingestion connectors, Cloud-native HTAP (Hybrid Transactional/Analtyical Processing), Integrated AI/BI with Azure ML, Azure Cognitive Services and Power BI.  Languages: T-SQL, Python, Scala, Spark SQL and .Net. - https://azure.microsoft.com/en-us/services/synapse-analytics
                
### Data lake
### SQL Databases
### NoSQL Databases
  - DataStax: Multi-cloud DBaaS built on Cassandra, and multi-cloud Streaming-as-a-Service built on Pulsar. (Founded 3/31/2010, lf: Venture, May 2021)
  - 
### Graph Databases

### Data Observability / Data Ops / ML Ops / Lineage
  - Monte Carlo: No-code integration to identify data issues (freshness/recency, volume, schema, distribution of duplicates and nulls, lineage to understand how data evolves), assess impact and alert teams. (Founded 2019, lf: Series B, Feb 2021) https://www.montecarlodata.com/
  - 
### Stream-processing / Pub-Sub
  - Amazon Kinesis: Collect, process and analyze video and data streams in real time.  Ingest Data Streams =>  Kinesis Data Analytics, Spark on EMR, EC2, AWS Lambda, custom apps. - https://aws.amazon.com/kinesis/
  - Spark Streaming
  - Kafka 
  - Beam
  - Pulsar
  - Flink
  - Storm
  - nifi (Apache): Niagara Files - a dataflow management tool to collect, route, enrich, transform and process data in a reliable and scalable manner.  NiFi developed by NSA.  Web based UI, high configurability, back pressure handling, runtime flow modification.  Data provenance (lineage tracked from start to end). Designed for extension.  SSL/SSH/HTTPS/encrypted, policy management, mult-tenant authorization - https://nifi.apache.org/
  - RocketMQ (Apache) Unified messaging engine, lightweight data processing platform.  Low latency, trillion-level message capacity guaranteed, finance oriented with high availablity and auditing features.  - https://rocketmq.apache.org/
  - Confluent - Cloud-native service for fully managed, self-serve provisioning, elastic scaling, Apache Kafka - https://www.confluent.io/confluent-cloud
  - Google Dataflow (Beam) - Unified stream and batch data processing that is serverless, fast and cost effective.  Fully managed, auto provisioning and management.  Horizontal autoscaling of worker resources, OSS innovation w/ Apache beam SDK, reliable/consistent exactly-once processing. https://cloud.google.com/dataflow
  - Azure Stream Analtytics - End to end analytics pipeline, serverless, elastic, rapid scalability, enterprise grade reliability.  C#/JAvascript/SQL. - https://azure.microsoft.com/en-us/services/stream-analytics
  - IBM streams - Real time analytics, java/scala/python, connect to nearly any data source and integrate with hadoop/spark/etc. - https://www.ibm.com/cloud/streaming-analytics
  - Pandio - Distributed messaging built on Apache Pulsar.  Serverless, reliable, performant, flexible deployments, managed, streams/queues and pub/sub.  Distributed SQL query engine. - https://pandio.com/
  - Apex (Apache): (Retired) Enterprise grade unified stream and batch processing engine.  Event-time windowing and high-level API.  https://attic.apache.org/projects/apex.html
  
 ### Messaging  Queue
  - IBM MQ - Enterprise grade messaging,  https://www.ibm.com/products/mq
  - Amazon SQS - Simple Queue Service, fully managed MQ for microservices, distributed systems and serverless apps https://aws.amazon.com/sqs/
  - Amazon MQ - fully managed service OS message brokers using Apache Active MQ- https://aws.amazon.com/amazon-mq
  - Google Pub/Sub - Messaging and ingestion for event-driven systems and streaming analytics.  Scalable, in order message delivery with pull and push modes.  Auto scale and auto provisioning, with support for 0 to hundreds of GB/sec.  
  - RabbitMQ - most widely deployed open source message broker - https://www.rabbitmq.com/
  - Azure Service Bus - Reliable cloud message as a service (MaaS) and simple hybrid integration - https://azure.microsoft.com/en-us/services/service-bus/
  - ZeroMQ - Open source universal message library.  pub-sub/push-pull/client-server.  Async I/O, tiny library.  Multi-transport inproc, IPC, TCP, UDP, TIPC, multicast and WebSocket - https://zeromq.org/
  - MQTT - The standard of IoT messaging - https://mqtt.org/

### Data Ingestion / Data Wrangling / ETL / ELT
  - Trifacta: Open, interoperable, low-code/no-code visualized data preparation, transformation and ingestion.  GDPR/SOC2 Type II/CCPA Compliant. (Founded 2012, lf: Series E, Sept 2019) https://www.trifacta.com/
  - Amazon Glue: Serverless data integration service.  Data discovery and ETL via visual and code-based interfaces.  (Preview) Elastic views to combine and replicate data across multiple data stores using SQL. - https://aws.amazon.com/glue/
  
### Labeling / Annotation
  - Labelbox: Configurable platform to enable teams to create and manage ML training data.  Used to annotate data, manage p&p (people and processes) and iterate. - https://labelbox.com/
  - Hive: Data labelling, model building and complete end-to-end solutions.  https://thehive.ai/
  - Google Vertex Labeling: Request human labelers - https://cloud.google.com/vertex-ai/docs/datasets/data-labeling-job
  - Amazon SageMaker Ground Truth - offers access to public and private human labelers - https://aws.amazon.com/sagemaker/groundtruth/


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


### Containers
  #### Providers
    - Amazon EKS
    - Google Cloud
    - Azure Container Service (AKS)
    - Cisco Container Platform (CCP)
  #### Frameworks
    - RedHat
    - SUSE
    - VMWare - vSPhere
    - Mesosphere
    - Docker
    - Rancher
    - Ballerina
    - Cloud FOundary
  #### Monitoring
    - Datadog
    - Sumologic
    - New Relic
    - AppDynamics
    - Buoyant
    - Turbonomic
    - Grafana
    - Instana
    - Dyantrace
    - Prometheus
    - Fluentd
  #### Management
    - Spotinst MCS
    - DigitalOcean
    - Giant Swarm
    - Kublr
    - Envoy
  #### Load Balancing
    - AVI Networks
    - HAProxy
    - Nginx
  #### Security
    - Aqua
    - Black duck 
    - Cilium
    - Twistlock
    - Alcide
  #### Tools
    - Jfrog
    - CloudBees
    - Univa
    - Bitnami
    - Aspen mesh
    - GitLab
    

### Definitions
- Exabyte: 1000 PB / 1 Million TB / 1 Billion GB 
- Petabyte: 1000 TB / 1 Million GB / 1 Billion MB
