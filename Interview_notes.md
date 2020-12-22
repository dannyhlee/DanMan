I am a software engineer specializing in scala and spark, leveraging hadoop, hive and spark to process big data.  I have created my own mapreduce jobs in Scala and have used hive and spark for data filtering and analysis.  I have used AWS EMR to create MapReduce jobs on EC2 clusters using S3 storage.  I have also used Google Cloud Compute VM clusters to process Spark jobs on DataProc.  I have compiled Scala code into JAR files using sbt in the Intellij IDE as well as from the command line. I have used VCS/Git in smaller team projects extensively and on a large project with 20 contributors. I have previous experience building full-stack web applications using Ruby on Rails (backend) and Javascript (frontend).  I have worked on teams at Revature, as well as at Flatiron school and have developed my interpersonal skills and gained confidence in working as a unit and tackling projects and problems head on. 

I have been working with scala since week 1 at revature and I am a big fan of its functional, high-level, statically typed nature.  I also enjoy the type inference system and type-safety because I would rather know at compile time whether my code is reliable than during runtime execution. Scala is also concise and built for a lightweight, readable syntax with rich pattern matching and lazy evaluation.  I was also introduced to intellij and sbt and like working with both.  I'm also excited to learn more about parallel and concurrent programming, and scala is the language to do it.  Its a portmanteau of SCalable Language.

Its functional nature is not much of a shift from the functional style of Javascript I learned at Flatiron school.  The functional pattern of using pure functions with idempotent output and composing functions to build programs, rather than maintaining state or procedural programing feels very comfortable.  I also learned about its many immutable collections (lists, sequences, vectors, sets and maps) as well as mutable collections like listbuffers and arraybuffer.  I'm still learning with Martin Odersky on EPFL courses at Coursera.

What is spark streaming?

Spark streaming is a library built on top of core Spark that provides scalable, high throughput, fault-tolerant stream processing of live data streams.  Streams can be read from HDFS, tcp, Kafka and sent to filesystems, databases and dashboards like kibana.  Spark streaming using DStreams which we access through the streamingContext, which is streaming version of sparkContext.

import org.apache.spark._
import org.apache.spark.streaming._
import org.apache.spark.streaming.StreamingContext._

val conf = new SparkConf().setMaster("local[*]".setAppName("MyApp")
val ssc = new StreamingContext(conf, Seconds(1))

Create Dstream from TCP source, ie connect to socket:
val lines = ssc.socketTextStream("localhost", 9999)

ssc.start() // start computation
ssc.awaitTermination() // wait for end

What is spark sql?
Spark sql is an api built on top of core spark which provides two other apis, dataframes and datasets.  These datasets allow us to structure data so that it can be queried using SQL-like queries.  It includes the catalyst optimizer and the tungsten serializer.  

What is structured streaming?
Stuctured streaming is built on top of spark sql, and offers the advantagesd of sparksql in the same way as sparksql does over using rdds.  Its not as low level but gives you optimizations and serialization.  Instead of working on rdds, we are working with datasets and dataframes.  It also offers fault-tolerance through checkpointing and write-ahead logs.  (provides durability and atomicty)  Can provide exactly-once fault-tolerance.

Three modes of output:  complete, append and update.

Structured streaming can take input from files, kafka, sockets and output them to file sinks, kafka, foreach sinks, console sinks and memory sinks



#### Have you used Scala?

Yes, we've been working with Scala since week 1 and I'm a big fan of its functional, high-level, statically typed nature. I also enjoy the type inference system and type-safety, because I know I have an error at compile time, rather than at run-time.  It is concise and is built for lightweight, readble syntax with rich pattern matching and lazy evaluation.  It was also my introduction to IntelliJ ide and the SBT build tool for scalac. I'm also excited about its potential in parallel procssing, I mean its built to Scale (portmanteau of SCalable Language)

Its not that radical of a shift from the functional programming style I learned at Flatiron school using Javascript with functions as first class citizens and higher order functions like map, filter and reduce.  Learning Ruby, then Javascript, then Java and now Scala worked very well for me and gave me the intuition I needed to be able to fully enjoy and understand Scala's programming style.  The functional pattern of using pure functions with idempotent output and composing them, rather than maintaining vary degrees of state.  I think the concept fits me better than object oriented programming's encapsulation of state that needs to be accounted for.  I also like functional programming over procedural programming because of the ability to organize code into smaller, re-usable functions that are pure and not have to worry about as many side effects.  I learned programming in a procedural style (basic, c, pascal).

We learned about immutability, and common immutable data structures in Scala like Lists, Vectors and Sequences as well as mutable ones like Array.  I was also introduced to Generic types, case classes and some of the syntactic sugar they provide, scala string interpolation, Some() values and flatmap.  I've found a course by Martin Odersky from EPFL on Coursera and started learning about the thought process behind building scala.  I've learned about function currying, which Im still trying to understand to the point I can explain it clearly, though I understand the concept in practice. There's a few other courses on the use of scala in parallel processing and distributed systems.

#### Have you used hadoop?

In project 1 (Twitter data analysis) I used Scala to write a Hadoop driver, a mapper and reducer for Wikipedia Clickstream (1.5gb) and Pageview-ez (40gb) data.  The driver set our configuration, mapper and reducer classes, FileInput and and FileOutput formats and ran our first mapper.  The first mapper read the file, and split on whitespace, then converted each line to a list of columns.  Then using scala pattern matching the relevant data was extracted, which was the article name(string) and the requests (int), the rest dropped and transformed into a tuple and collected and written to the context.  The KV pairs were sent to the reducer to aggregate the request counts for each article.  

The programs were compiled to a java bytecode jar, and along with the data uploaded to hdfs and run in a Hadoop single node cluster.  The results were pulled into Hive.

#### Have you used Hive?

I used Hive in project 1 to pull my data in, convert to external tables and run HQL queries on the data to extract the answers for my questions.

#### Have you used Spark?

#### Have you used Kafka?

#### ACID compliance - database transaction
- Atomicity refers to the integrity of the entire database transaction being one unit.  Atomicity guarantees that the entire transaction 
will be performed as if it were a single operation.  That is, all changes will be performed or none of them.

- Consistency refers to the state of data when a transaction starts, and when it ends.  A transaction must follow the rules of the
database, else it be rolled back to a state which does comply.

- Isolation is the property that ensures that concurrent transactions that are reading and writing to a table at the same time leave
the database in serialized state and as if they were run sequentially.

- Durability is the property that guarantees that once a transaction is successfully committed, it will endure system failures and 
changes to data will persist.

*Strong consistency, focus on "commit", conservative, slower evolution (schema)*


#### BASE consistency model for distributed systems

- Basically Available - availablity is important and reading and writing operations trump consistency guarantees

- Soft state - Because consistency is not guaranteed and data can be in the process of sync'ing state may not match across replications

- Eventual consistency - The data will eventually sync, and will continue to move in to a state of consistency, but as long as data is added, it will be evolving.

*Availability first, best effort, approximate answers should be ok and aggresive.  Simpler, faster, easier evolution.*

#### CAP Theorem - distributed systems (aka Brewer's theorem)

- Consistency - All clients - same data, same time, all nodes.  Every read request gets most recent write or error.  

- Availability - Every request get non-error response, without guarantee is most recent write.

- Partition tolerance - Nodes containue to work, regardless of partitions (communications disruption).

#### Types of NoSQL databases: 

- CP database - Consistency and Partition tolerance, when partition occurs, not available. (ex: mongoDB)

- AP database - Availability and Partition tolerance, when partition occurs, available, but consistency not guaranteed. (ex: cassandra)

- CA database - Consistency and Availability, but cannot handle partitions/fault tolerance.  Not practical in distributed systems.




