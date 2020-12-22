import java.io.{File, FileNotFoundException, IOException}
import java.nio.file.Paths

import scala.io.Source

// print working directory
val Wd = Paths.get(".").toAbsolutePath

println(Wd)


// get list of files in directory
def getListOfFiles(dir: String):List[File] = {
  val d = new File(dir)
  if (d.exists && d.isDirectory) {
    d.listFiles.filter(_.isFile).toList
  } else {
    List[File]()
  }
}

val myDir = "C:\\tmp"
val files = getListOfFiles(myDir)

println(s"Files in $myDir:")
files.foreach(println)


// Read in a text file and print
val filename = "C:\\tmp\\poems.txt"

// UTF-8 encoding resolves UnmappableCharacterException
val buffered_text_file = Source.fromFile(filename)("UTF-8")

for (line <- buffered_text_file.getLines) {
  println(line)
}

buffered_text_file.close

// Read in as List

val text_file_as_list = Source.fromFile(filename)("UTF-8")
  .getLines
  .toList

// Read in and make into one string

val text_file_as_string = Source.fromFile(filename)("UTF-8")
  .getLines
  .mkString

// try and catch

val non_existent_file = "no-such-file.scala"
try {
  for (line <- Source.fromFile(non_existent_file).getLines) {
    println(line)
  }
} catch {
  case e: FileNotFoundException => println("Couldn't find that file.")
  case e: IOException => println("Got an IOException!")
}

println("done!")
