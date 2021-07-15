ABN AMRO A1
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
Adevinta A1
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
AutoZone A1 S1
  - Reducing monitoring risk with data mesh
  - Monitoring data was hard to access
  - Each data product should exhibit:
    - Discoverable
    - Addressable
    - Trustworthy
    - Self-describing
    - Interoperable
    - Secure
CMC Markets (meetup July 29th)
Delivery Hero V1
Disney V1
DPG Media V1 S1 A1 A2 A3
DWP (Department for Work and Pensions – part of the UK Gov) V1
FindHotel A1
  - Automation CI/CD Travis data validation
  - Data arrives as JSON datasets, need to be flattened
  - node json processor
  - javascript snoflake UDFs validated contracts
Gloo A1 A2
HelloFresh V1
If Insurance / If P&C A1 A2
Intuit V1 A1
JPMorgan Chase A1 V1 (meetup July 8th)
Kolibri Games V1
Medtronic V1
Northern Trust V1
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
Saxo Bank V1 A1
Starship Technologies A1
  - Data mesh concepts:
    - Data product: define owner/interface/users
    - Data domain: group by domains representing org structure of company
    - Data platform: empower citizens by standardizing without centralizing data products
    - Data governance: strong personal ownership supported by feedback loops
WePay A1
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
Yotpo A1
  - Data catalog - aws glue, hive metastore,, spark, emr, redshift and databricks
  - Data exploration - atlas with ranger, amundsen
  - Execution: Metorikku/Spark
  - Scheduling: Airflow
  - Availability: Apache Hudi
  - Freshness: Structured streaming/flink/CDC and hudi
  - Stability: message broikers/kafka and orchestration plafroms like k8
  - CDC: Debezium
  - 
Zalando V1 V2 V3 V4 V5
Zenseact S1
  - Data plane: Real-time data sources, enterprise applications, OEM cloud/IoT, cloud applications
  - Ingestion: Event streams, virtualisation, CDC, ETL/Automated ETL, File transfers
  - Data governance, meta data mgmt, data catalogue, data quality, deep learning, data science platform, operational data hub,
  - enterprise data warehouse, master data and reference data mgmt
  - Out: Realtime decision making, dashboards/reporting/grafana, data discovery/self-service/Enterprice KPIs, predictive/performance models
