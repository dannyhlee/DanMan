
## Introduce yourself based on your technical background -- 60 - 90 seconds, do not rush
  - Name, basic information, college experience (graduation year and degree)
  - Talk about any previous technical experience
  - Explain technologies you know and worked with
  - Explain your reason for going into technology (i.e. your motivations)

##  Walk me through your latest project
  - Purpose of the project -- Reason for the project
  - Make sure your thought process is linear - explain the who, what and why of the application
  - Explain any methodologies you followed Agile or otherwise, and go a little into how that helped your project progression
  - Include information as to whether it was inherited code you were working off of or new source code

## Explain the complete data flow through your last project
  - Different data access layers and any design patterns used for the data flow
  - Also include the technologies used and how you maintained version control
  
## What was your role in the project? 
  - Specific Role you took
  - How did you role help other groups? How did you manage your time constraints during the sprint?

## What was the biggest challenge during the project?
  - Talk about a challenge that you overcame and how you overcame it and how you would prevent it from happening in the future
  - Important to not be overly negative about the challenge
  
---
# Projects:

## Project 3

### COVID Dataset Analysis
Project 3 involves a series of data analysis questions about the 2020 COVID pandemic. Analysis is performed using Spark applications (predominantly Spark SQL) on static and streaming data sources, making use of a Spark cluster and a Kafka cluster running on Amazon's cloud. 

#### Analysis questions and goals follow: 
1. Which Regions handled COVID-19 the best assuming our metrics are change in GDP by percentage and COVID-19 infection rate per capita. (Jan 1 2020 - Oct 31 2020)? 
2. Find the top 5 pairs of countries that share a land border and have the highest discrepancy in covid-19 infection rate per capita. Additionally find the top 5 landlocked countries that have the highest covid-19 infection rate per capita. 
3. Live update by Region of current relevant totals from COVID-19 data. 
4. Is the trend of the global COVID-19 discussion going up or down? Do spikes in infection rates of the 5-30 age range affect the volume of discussion? 
5. When was COVID-19 being discussed the most? 
6. What percentage of countries have an increasing COVID-19 Infection rate? 
7. What are the hashtags used to describe COVID-19 by Region (e.g. #covid, #COVID-19, #Coronavirus, #NovelCoronavirus)? Additionally what are the top 10 commonly used hashtags used alongside COVID hashtags? 
8. Is there a significant relationship between a Region’s cumulative GDP and Infection Rate per capita? What is the average amount of time it took for each region to reach its first peak in infection rate per capita?

#### Roles / Responsibilities

 - Point person for Elastic Stack to be implemented for Spark, Kafka, Amazon S3, and Hadoop/HDFS.    
 -  Implemented Beats data ingesters, LogStash from Kubernetes Clusters, with Pods running Docker Containers.
 - Fed log data to ElasticSearch, and then to Kibana.   
 - Ran Spark jobs on Google DataProc using Google Cloud Storage.
 - Utilized Amazon S3 to store Datasets and Spark JARs     
 - Ran Spark jobs on Amazon EMR in Cluster mode as well as Step Execution mode.   
 - Collaborated using Git on Github to manage source control between   multiple teams.
 - Sourced documents, sample files, and wrote documentation for ELK,    DataProc, and Kubernetes/Docker.

 
#### Environment / Technologies
Scala , sbt, Parquet, Spark SQL, Spark Streaming, Spark, EMR, DataProc, EMR, git

---

## Project 2

### Twitter Geographic Trend Analysis (Team 6 Project 2)
Using Big Data technologies, and Twitter's Trend API endpoint, project 2 consists of retrieving responses from Twitter with the Spark Structured Streaming API at 10 minute intervals, transforming the response with Spark by converting a single object with a location value and an array of 50 trends into 50 row entries and writing them to CSV format The output is then analyzed using Spark SQL to extract trend patterns to find the trends average rank, highest rank, hours trending, number of tweeets about the trend and top trends. The output of the project include Spark jarfiles, both pre and post processed datasets and documentation to repeatable and used on larger datasets and datasets that streamed on an ongoing basis. 

#### The questions examined follow: 

 1. Can we identify patterns in trending topics being popular in one    
    location and then moving to others?  
 2. If so, can we identify separate regions for these patterns? (ex.:   
    North American patterns, East Asian patterns, etc.)
 3. What about global scale patterns for specific events? ex.: Burning of   Notre Dame-how did this topic travel according to twitter usage?

#### Roles / Responsibilities

 - Utilized Postman and it's Collection Runner functionality to script
   the automated retrieval of Twitter Trend API events.
 - Designed a Scala Spark Runner program to input raw JSON response   files for processing.
 - Extracted Twitter's JSON Trend Api response and fitted it to a Spark   schema.
 - Transformed the data from one object with a Location and fifty Trend   topics to fifty objects with a Trend topic at that location.
 - Exported data into the local file system as CSV.
 - Destructured SparkSQL query function into separate Scala modules and packaged them as individual JAR files.
 - Tested functionality of SparkSQL JAR files in Google DataProc.
 - Produced and reported on analysis results.
 - Implemented Scala, Spark on Windows, and Ubuntu Linux.
 - Source control and versioning handled using Git and GitHub.

#### Environment / Technologies
Scala , sbt, YARN, Parquet, Spark SQL, Spark Streaming, Spark, Google DataProc, Google Cloud Storage

---

## Project 1

### Wikipedia Big Data Analysis

Project 1's analysis consists of using big data tools to answer questions about datasets from Wikipedia. There are a series of basic analysis questions, answered using Hive or MapReduce. The tool(s) used are determined based on the context for each question. The output of the analysis includes MapReduce jarfiles and/or .hql files so that the analysis is a repeatable process that works on a larger dataset, not just an ad hoc calculation. Assumptions and simplfications are required in order to answer these questions, and the final presentation of results includes a discussion of those assumptions/simplifications and the reasoning behind them. In addition to answers and explanations, this project requires a discussion of any intermediate datasets and the reproduceable process used to construct those datasets. Finally, in addition to code outputs, this project requires a simple slide deck providing an overview of results. 

#### The questions follow:

1. Which English wikipedia article got the most traffic on October 20, 2020? 
2. What English wikipedia article has the largest fraction of its readers follow an internal link to another wikipedia article? 
3. What series of wikipedia articles, starting with Hotel California, keeps the largest fraction of its readers clicking on internal links? 
4. Find an example of an English wikipedia article that is relatively more popular in the UK, then find the same for the US and Australia. 
5. How many users will see the average vandalized wikipedia page before the offending edit is reversed? 
6. Run an analysis you find interesting on the wikipedia datasets we're using.

#### Roles / Responsibilities

 - Developed Scala Hadoop mappers to filter and normalize data.
 - Loaded, extracted fields, and output TSV and CSV format files to
   HDFS.
 - Constructed filtered aggregations of data using Hadoop MapReduce.
 - Loaded restructured data into both external and managed tables in
   Hive.
 - Designed custom Hive schema to fit data.
 - Generated Hive HQL queries to seek meaningful data.
 - Produced and reported on analysis results.
 - Deployed Hadoop, Hive, and Spark jobs on Windows and Ubuntu Linux, using HDFS and Yarn.
 - Source control and versioning handled using Git and GitHub.
 - Utilized curl, gzip, tar, UNIX shell to retrieve Wikipedia data.

#### Environment / Technologies

Scala , sbt, HDFS, YARN, MapReduce, Hadoop, Hive
