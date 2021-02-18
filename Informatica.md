#### Briefly, what is informatica? (2 or 3 sentences)

Informatica is a highly rated suite of products that provide enterprise level data integration and ETL (extract, transform, load) functionality, data quality and management, data lifecycle management, event processing, data masking and does so using workflows stored as Metadata that allows recreation, scheduling and building of pipelines of workflows.  It rated an industry leader by Gartner in 5 categories (Enterprise Integration platform, Data Integration Tools, Data Quality Solutions, Master Data Management Solutions, Metadata Management Soltuions) .
 
#### What is the function of the Designer?

The Designer contains tools to analyze sources, design target schemas and build source-to-target mappings.  

#### What are the parts of the Designer? 
- **Source Analyzer** - imports/creates source definitions.
- **Target Designer** - Import/create target definitions.
- **Transformation Developer** - Develop transformations for use in mappings, user-definied functions can also be used in expressions.
- ** Mapplet Designer** - Create sets of transformations to use in mappings
- ** Mapping Designer** - Create mappings that the Itegration Service uses to ETL data.

#### What is the Integration service?
The Integration service reads workflow information from the repository and runs workflow tasks.  The info the Integration services retrieves includes metadata that tells the Integration service when and how to run ETL tasks.  The Integration service handles the reading of data into a session and writing of transformed data to mapping targets.  THe Integration service can read and write to different platforms and target types.

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


#### Describe a Connected and Unconnected transformations.

A connected transformation has an input or output port that is connected to other transformations in a mapping.  An unconnected transformation receives input from a :LKP expression in an Expression or Aggregator transformation.

https://docs.informatica.com/data-integration/powercenter/10-0/_transformation-guide_powercenter_10-0_ditamap/lookup_transformation/connected_and_unconnected_lookups.html

#### Describe an Active transformation vs Passive transformation

## Active transformations:
#### Source qualifier
#### Ruler
#### Rank
#### Sorter
#### Joiner
#### Union
#### Aggregate
#### Transaction Control
#### Normalize
#### Update strategy
#### SQL

## Passive Transformations:
#### Expression
#### Sequence generated
#### Stored procedure
#### Lookup
#### XML source qualifier
#### SQL

https://www.guru99.com/informatica-interview-questions.html

https://intellipaat.com/blog/interview-question/informatica-interview-questions/
