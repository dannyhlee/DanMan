## https://datameshlearning.com/user-stories/

### ABN AMRO A1
  - Providers
    - Event, batch, API-based publishers => subscribers / read-request response
    - EDA event, message publishers => subscribers
    - API <=> Operational commands/reads 
  - Metadata
    - Data owner/user/application owner
    - Business rules
    - SLA/SLI/SLO
    - Lineage
      - Transforms
      - Source system
      - Source attributes
      - Target system
      - Target attributes
### Adevinta A1
  - Datasets should have
    - description (domain, data it contains, granularity)
    - How and where data can be accessed (SQL, programmatic notebooks, or complex)
    - The schema of the data set, including field types and detailed example for each field
    - Mappings and transforms to generate data set
    - Input freshness, sources, preconditions
    - Data exploration examples (notebook with simple querys, query catalog with SQL query examples.
  - Datasets can be:
    - domain: a specific business domain
    - core: cross-domain data
### AutoZone A1 S1
  - Reducing monitoring risk with data mesh
  - Monitoring data was hard to access
  - Each data product should exhibit:
    - Discoverable
    - Addressable
    - Trustworthy
    - Self-describing
    - Interoperable
    - Secure
### CMC Markets (meetup July 29th)
### Delivery Hero V1
  - BigQuery
  - Kubernetes
  - Airflow
  - Dataproc
### Disney V1 - Caleb Jones
  - Defining domain taxonomy
    -  business or product units
    -  data dependencies
    -  use cases
    -  compute requirements (teams that need many resources)
    -  regulatory requriements (SOX compliance)
  - Graph the interdependencies to find clusters
  - Core Infrastructure/platform capablities
    - Scalable, secure, and governed storage 
    - Encryption standards/configuration/practices
    - Metadata (schema, versioning, governance, lineage, discovery)
    - Anonymozation and deletetion (CCPA/GDPR)
    - Enable data pipeline orchestration
    - Unified access control
    - Monitoring, alerting, logging
    - Federated identity management
    - self-service capabilities
  - Benefits
    - reduce duplication of effort
    - retain scalability of shared services
    - maintains functions that should not be duplicated (governances, identiy management)
  - Levels:
    - Common base lowest level: Common standards, conventions, governance, security, metadata
    - Second level: Common infrastructure, compute, orchestration, streaming, logging, storage
    - Uppermost platform: Platform domains w/cross functional teams, ingest, process, serve
  - Bug reporting infrastructure for core platform
  - Preapproved VPC Configuration (level 1 2 3 -> more secure).  to meet a variety of use cases.
  - Data plane - 1. data store for common data 2. specialized data / GDPR 
  - Meta data capture / directory across domains
  - Metadata and Data Quality as First class citizens
    - input quality and data composability 
  - Federation of data (predefine security levels/VPC to ramp up faster)
  - Paradigm shifts require concensus.  
  - Automation is key - provisioning, CICD, data quality, monitoring
  - Conversations between product and engineering around domain-focus to build a dynamic, ongoing conversation 
  - Group/package cloud accounts (cross-account and cross cloud) account control
  - kafka, nifi
### DPG Media V1 S1 A1 A2 A3
  - Apache sqoop - batch
  - Amazon kinesis - streaming
  - scheduling and transforming data
    - dbt
    - datafy
  - Storage
    - S3
    - Snowflake
    - Elastic search 
  - Data Integration Layer
    - Gluie 
  - Services for API/reporting/data science
    - Looker/qlik/tableau for reporting
    - dataiku/sas/databricks for data science
### FindHotel A1
  - Automation CI/CD Travis data validation
  - Data arrives as JSON datasets, need to be flattened
  - node json processor
  - javascript snoflake UDFs validated contracts
### Gloo A1 A2
### HelloFresh V1
### If Insurance / If P&C A1 A2
### Intuit V1 A1
### JPMorgan Chase A1 V1 (meetup July 8th)
### Kolibri Games V1
### Medtronic V1
### Northern Trust V1
  - CQRS for operational systems
    - realtime, ubiquitous, distributed data architecture achived through DDD
    - delivered through Kafka
    - DDD merged with Event storming
    - Each bounded context should be listed with its metadata:
      - Lineage
      - Business data owner
      - Data steward
      - Technical owner
      - interoperability
      - distributions
### Saxo Bank V1 A1
### Starship Technologies A1
  - Data mesh concepts:
    - Data product: define owner/interface/users
    - Data domain: group by domains representing org structure of company
    - Data platform: empower citizens by standardizing without centralizing data products
    - Data governance: strong personal ownership supported by feedback loops
### WePay A1
  - Four data mesh principles
    - Domain oriented decentralized data ownership and architecture
    - Data as a product
    - Self-serve data infrastracture as a platform
    - Federated computational governance
  - Google Cloud DLP
  - Schema definition tool - protocol buffers/avro/json schema
  - Transformation/transfer tool 
    - Data pipelines - Airflow, Prefect, dbt
    - Stream based - Kafka, flink, outbox pattern
  - Data warehousing tool: snowflake, bigQuery
  - Data catalog: Amundsen, Datahub, Marquez
  - Data plane = data warehouse, data mart and data lake
### Yotpo A1
  - Data catalog - aws glue, hive metastore,, spark, emr, redshift and databricks
  - Data exploration - atlas with ranger, amundsen
  - Execution: Metorikku/Spark
  - Scheduling: Airflow
  - Availability: Apache Hudi
  - Freshness: Structured streaming/flink/CDC and hudi
  - Stability: message broikers/kafka and orchestration plafroms like k8
  - CDC: Debezium
### Zalando V1 V2 V3 V4 V5
  - Legacy => Messaging bus => Data Lake
  - Ingestion layer => Event buss, Data center/DWH, Google analytics (web tracking)
  - Storage layer => object and metastore
  - Serving Layer => Presto (fast query layer), Databricks (Processing platform), Data Catalog
  - Discoverable, Addressable, Self-describing, Secure, Trustworthy, Interoperable
  - Remove bottleneck in the infrastructure
  - Metadata layer (Standardize process to get access of data)
    - BYOB, bring your own bucket - logical distribution through S3 buckets from product groups to the central storage area
    - opt-in data storage in the central archive
    - dedicate resources to understand usage and ensure quality.
### Zenseact S1
  - Data plane: Real-time data sources, enterprise applications, OEM cloud/IoT, cloud applications
  - Ingestion: Event streams, virtualisation, CDC, ETL/Automated ETL, File transfers
  - Data governance, meta data mgmt, data catalogue, data quality, deep learning, data science platform, operational data hub,
  - enterprise data warehouse, master data and reference data mgmt
  - Out: Realtime decision making, dashboards/reporting/grafana, data discovery/self-service/Enterprice KPIs, predictive/performance models
