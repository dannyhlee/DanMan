#### Briefly, what is informatica? (2 or 3 sentences)

Informatica is a highly rated suite of products that provide enterprise level data integration and ETL (extract, transform, load) functionality, data quality and management, data lifecycle management, event processing, data masking and does so using workflows stored as Metadata that allows re-creation, scheduling and building of workflow pipelines.  Its an industry leader according to Gartner in 5 categories (Enterprise Integration platform, Data Integration Tools, Data Quality Solutions, Master Data Management Solutions, Metadata Management Soltuions).
 
#### What is the function of the Designer?

The Designer contains tools to analyze sources, design target schemas and build source-to-target mappings.  

#### What are the parts of the Designer? 
- **Source Analyzer** - imports/creates source definitions.
- **Target Designer** - Import/create target definitions.
- **Transformation Developer** - Develop transformations for use in mappings, user-definied functions can also be used in expressions.
- **Mapplet Designer** - Create sets of transformations to use in mappings
- **Mapping Designer** - Create mappings that the Itegration Service uses to ETL data.

#### What is the Integration service?
The Integration service reads workflow information from the repository and runs workflow tasks.  The info the Integration services retrieves includes metadata that tells the Integration service when and how to run ETL tasks.  The Integration service handles the reading of data into a session and writing of transformed data to mapping targets.  It can read and write to different platforms and target types.

#### What is a Session?
A session includes instructions on how to extract data from sources, transform the data and load the data into mapping targets.

#### WHat is a workflow? 
A workflow is a set of instructions that tells an Integration Service how to run tasks.

#### What is the PowerCenter Workflow Monitor?

This product allows users to monitor workflows and tasks that are run on nodes or grids.

#### What is a node?

A node represents a machine in a domain.  A node can be a gateway or a worker.  A node can have a compute role or a service role or both.  By default, it is both.

#### What is a grid?  

A grid is an alias for a group of nodes.  A load balancer distributes tasks to nodes.

#### What is the PowerCenter Workflow Manager

Here you define a set of instructions to execute tasks, such as sessions, emails and shell commands.  This set is called a workflow.  THere are three tools:
- Task developer: Create tasks (session, email, shell)
- Worklet designer: Create worklets.  Worklets are a group of tasks, can be nested in workflows.
- Workflow designer: Connected tasks in order of execution and time to execute.

#### Describe a Connected and Unconnected transformations.

A connected transformation has an input or output port that is connected to other transformations in a mapping.  An unconnected transformation receives input from a :LKP expression in an Expression or Aggregator transformation.

https://docs.informatica.com/data-integration/powercenter/10-0/_transformation-guide_powercenter_10-0_ditamap/lookup_transformation/connected_and_unconnected_lookups.html

#### Describe an Active transformation vs Passive transformation

An active transformation is one that either:
- Changes the number of rows that pass-thru (ex: filters, reduces rows according to predicate)
- Changes the transaction boundary (ex: commit or rollback based on expression_
- Changes the row type (ex: insert, delete, update or reject flags)

note: You cannot connect two active transformations or an active and passive to the same downstream transformation or transformation input group.

A Passive transformation does not change the number of rows that passthru, maintains the transactional boundary and row type.  Thus, you can connect multiple transformations to the same downstream transformation group.

#### What are Native and Non-Native Transformations?

Native transformations are provider by Designer.  Non-native are created using the Custom transformation.  A few are provided by Designer (Java, SQL, and Union)

## Active transformations:
#### Aggregator
(Active, connected, native) Performas aggregate calculations.

#### Filter
(Active, connected, native) Filters data

#### Java 
(Active or passive, connected, non-native) Executes user logic in java, byte code stored in repository.

#### Joiner
(active, connected, native) Joins data from different db and flat fiels.

#### Normalizer
(active, connected, native) Source qualifier for COBOL sources.  Can also use in pipeline to normalize relational and flat files.

#### Rank
(active, connected, native) Limits record to top or bottom of a range.

#### Router
(active, connected, native) Routes data into multiple transformation based on group conditions

#### Sorter
(active, connected, native) Sorts data based on a sort key

#### Source qualifier
(Active, connected, native) Represents the rows that the IS (Integration service) extractsfrom a relational or flat file

#### SQL
(active or passive, connected, non-native) Executes SQL queries against db

#### Transaction Control
(active, connected, native) Defines commit and rollback transactions.

#### Union
(active, connected, non-native) Merges data from different db and flat file systems with identical schema.

#### Update strategy
(active, connected, native) Determines whether to insert, delete, update or reject rows

#### XML Generator 
(active, connected, native) Reads data from input port and outputs XML through single output port

#### XML Parser 
(active, connected, native) Reads XML from one input and outputs data to one or more outputs

#### XML Source Qualifier
(active, connected, native) Represents the rows that the IS reads from an XML source


## Passive Transformations:
#### Data Masking
(passive, connected, non-native) Replaces sensitive production data with realistic test data for non-production envs

#### Expression
(passive, connected, native) Calculates a value

#### External procedure
(passive, connected or unconnected, native)  Calls a procedure in a shared lib or COM layer of windows

#### HTTP
(passive, connected, non-native) Connects to HTTP server to read or update data

#### Input or Output
(passive, connected, native) Defines mapplet input or output rows from Mapplet designer

#### Lookup
(active or passive, connected or unconnected, native)  Look up and return data from flat file, rel. table, view or synonym.

#### Sequence generator
(passive, connected, native) Generates primary keys

### Stored procedure
(passive, connected or unconnected, native) Calls a stored procedure

https://www.guru99.com/informatica-interview-questions.html

https://intellipaat.com/blog/interview-question/informatica-interview-questions/
