

## Write file to HDFS from Spark

#### Resolves Exception:
`Exception in thread "main" org.apache.hadoop.security.AccessControlException: Permission denied: user="spark", access=WRITE, inode="/user/spark":spark:spark:drwxrwxr-x`

---

#### Get HDFS port:
```
$ hdfs getconf -confKey fs.defaultFS
hdfs://localhost:9000
```

#### Create user's directory on HDFS
```
$ hdfs dfs -mkdir /user/<username>
$ hdfs dfs -chmod g+w /user/<username>
```

#### Scala code (eg: Runner.scala)
Write file:
```
df.rdd.saveAsTextFile("hdfs://localhost:9000/user/<username>/<folder or file name>")
```
Read File:
```
//RDD
val rdd = spark.sparkContext.textFile("hdfs://localhost:9000/user/<filename>")
val rdd = spark.sparkContext.wholeTextFiles("hdfs://localhost:9000/user/<filename>)
val df = spark.read.text("hdfs://localhost:9000/user/<filename>")
val ds = spark.read.textFile("hdfs://localhost:9000/user/<filename>")
```

#### Add environment variable 
**warning**: do not use quotes around `<username>`

##### In Intellij Run Menu (->Configurations->Environment variables)
```HADOOP_USER_NAME=<username>```
 
##### As unix shell environment variable
```export HADOOP_USER_NAME=<username>```

---

## Delete HDFS file or directory from Spark

```
import java.net.URI
import org.apache.hadoop.fs.{FileSystem, Path}

 val fs = FileSystem.get(new URI("hdfs://localhost:9000/"), spark.sparkContext.hadoopConfiguration)
 println(spark.sparkContext.hadoopConfiguration)
 val fsStatus = fs.listStatus(new Path("hdfs://localhost:9000/"))
 fsStatus.foreach(x=> println(x.getPath))

 val outputPath = new Path("/user/spark/trends")
 println(fs.exists(outputPath), outputPath)
 if (fs.exists(outputPath))
   fs.delete(outputPath, true)
```
---

## Create SparkSQL Schema for Nested JSON objects using StructType (DataFrames)

##### Spark generated schema  `.printSchema()`
```
     root  
 |-- as_of: string (nullable = true)  
 |-- created_at: string (nullable = true)  
 |-- locations: array (nullable = true)  
 |    |-- element: struct (containsNull = true)  
 |    |    |-- name: string (nullable = true)  
 |    |    |-- woeid: long (nullable = true)  
 |-- trends: array (nullable = true)  
 |    |-- element: struct (containsNull = true)  
 |    |    |-- name: string (nullable = true)  
 |    |    |-- promoted_content: string (nullable = true)  
 |    |    |-- query: string (nullable = true)  
 |    |    |-- tweet_volume: long (nullable = true)  
 |    |    |-- url: string (nullable = true)  
```
#### The proper schema for --^
```
import org.apache.spark.sql.types._

val trendSchema = new StructType()  
  .add("as_of", StringType)  
  .add("created_at", StringType)  
  .add("locations", ArrayType(new StructType()  
      .add("name", StringType)  
      .add("woeid", LongType)  
    ))  
    .add("trends", ArrayType(new StructType()  
      .add("name", StringType)  
      .add("promoted_content", StringType)  
      .add("query", StringType)  
      .add("tweet_volume", LongType)  
      .add("url", StringType)  
    ))  
  
// read JSON and convert to DF with schema
val df = spark.read.schema(trendSchema).json("input-old")
```
 
