
// process lines of an RDD read from a wikipedia log file gzip.
// reference: Brian Clapper - RDDs, DataFrames and Datasets in Apache SPark - NE Scala 2016
// url:                       https://youtu.be/pZQsDloGB4w?t=2324

pagecounjtsRDDs.flatmap { line => 
  line.split("""\s+""") match {
    case Array(project, page, numRequests, contentSize) => Some((project, page, numRequests.toLong))
    case _ => None
  }
}.
filter { case (project, page, numRequests) => project == "en" }.
map { case (project, page, numRequests) =-> (page, numRequests) }.
reduceByKey(_ + _).
sortBy({ case (page, numRequests) => numRequests }, ascending = false).
take(100).
foreach { case (page, totalRequests) => println(s"$page: $totalRequests") }


// number of Mebibytes of a data set
// https://umbertogriffo.gitbook.io/apache-spark-best-practices-and-tuning/sparksqlshufflepartitions_draft
// number Of Megabytes = M = (N*V*W) / 1024^2

//     N  =  number of records
//     V  =  number of variables
//     W  =  average width in bytes of a variable

---

arr.zipWithIndex.filter(_._2 %2 == 1).map(_._1)

---

// val readInt = scala.io.StdIn.readInt()
import scala.io.StdIn.{readInt}

def f(num:Int) : List[Int] = {
  val list = (1 to num).toList
  list
}

---

def f(arr:List[Int]):List[Int] = {
    (for (i <- (arr.length - 1) to 0 by -1) yield arr(i)).toList
}

---

 def f(arr:List[Int]):Int = {
     arr.filter(_ % 2 != 0).sum
 }
 
 ---
 
 def f(arr:List[Int]):Int = {arr.map(_=>1).sum}
 
 ---
 
// readline 
val a = io.StdIn.readInt()

(1 to a).foreach { i => 
  val j = io.StdIn.readInt()
  val list = (1 to j).map(x => io.StdIn.readline.split("\\s+")(0)).toList
}

---
// readline
    def functionTest() : Unit = {
        // read number of pairs in this test case
        val X = scala.io.StdIn.readInt()        
        // Read each line of (x,y) pairs
        val data = Iterator.continually(scala.io.StdIn.readLine())
        .take(X) // take X number - read above
        .collect(_.split(" ") match // split the pair on spaces and test against
        { case Array(s1, s2) => (s1.toDouble, s2.toDouble)}) // this case and collect
        .toList                                       // the results, before toList

        //println("data: ", data)
        //println("data.toMap.size: ", data.toMap.size)
        //println("data.toMap print: ", data.toMap.foreach(println))
        //println("data.length: ", data.length)

        // toMap converts the array 2 tuple to a map entry.  The key value remains
        // the same, but if the value varies in different test case pairs, then the
        // value will get rewritten and size of the map will not match the original
        // data.length 
        println(if (data.toMap.size == data.length) 
                "YES" else "NO")
    }

    def main(args: Array[String]) {
        val N = scala.io.StdIn.readInt()
        for (_ <- 1 to N) {
            functionTest
        }
    }


