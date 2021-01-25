#### What are Staging areas?

Staging areas is a place where we put things temporarily, before moving them to a stable location.  In a real world warehouse, we have loading bays with marked areas where cargo is held until it is loaded or unloaded.  In old school data warehouses, a staging database is a database where data is retrieved from the transactions database, manipulated if needed and transformed in the staging database, before moving the data to the reporting database.

#### Stages in Snowflake

The stages in Snowflakes are more like folders, similar to the way you interact with FTP and FTP servers. There are two types of stages, External and Internal stages.  Internal stages are held on Snowflake local storage.  External stages use the storage of Amazon AWS S3 and MS Azure BLOB (Binary Large Object Storage) and Google Cloud Platform Storage Buckets.  They are stored securely and Snowflake requires access credentials from the cloud provider and you need to define a Stage Definition in Snowflake.

#### Pre-Stage Data Movement

For example, Amazon provides 3 ways to transfer data to Staging.  

- Amazon Transfer for SFTP
- Amazon CLI
- Amazon Web browser interface

Also, files can be loaded using APIs.  

Watch folders or folder syncing can be used to automate updates.

#### What is Data Movement Staging Lifecycle?

#### Code Sample for `COPY INTO`
```
COPY INTO ~TABLE NAME~
FROM ~@MY_S3_BUCKET/load/~
FILES = ( 'weight.txt' )
FILE_FORMAT = ( FORMAT_NAME = USDA_FILE_FORMAT )
FORCE = TRUE;
``` 


#### Data Storage Structures

- Presentation layer
- Data storage layer (eg. author, subject, title)
  - ERDs - entity relationship drawings
  - Normalized Relational Database Model
    - Different entities stored in separate tables
    - Same info not repeated
    - Unique IDs for each row

#### Sequences in Snowflakes 

Similar to auto-incrementing, primary keys (counters).  Created in the `Sequences` tab of Database menu.  Need to set:
- Initial value
- Interval (of increment)

#### Semi-Structured Data 
- JSON: Lightweight text-based transport and storage format for data. Easy to read and write for both man and machine.  Built of either objects (key:value pairs surrounded by curly braces) or an ordered list of values (array).
- XML: markup language that defines a structural set of rules for human/machine readable documents.  Is transportable and extensible, but more verbose and redudant than other text-based data transport formats (e.g. JSON)
- Parquet: column based, predicate push down, up to 87% data storage savings vs CSV, 99% less data scanned, 34x faster queries.  Dictionary encoding, bit packing and RLE (run length encoding).  Reading is faster that writing, updating data is slow.
- Avro: Data serialization system with rich data structures; compact/fast binary format; schema resolution; row based
- ORC: columnar storage format with compression, fast read/write, predicate pushdown, both compressed/uncompressed storage available
  
  
