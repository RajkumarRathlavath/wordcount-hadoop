# WordCount Hadoop

This is a Java-based Hadoop MapReduce word count application with stopword filtering and sample dataset.

## Run
To run this application, simply follow these steps:

1. Compile the Java classes and package them into a JAR.
2. Upload the input files to HDFS:
   ```bash
   hdfs dfs -put src/Input/* /user/$USER/input
## Run the MapReduce job:
hadoop jar wordcount.jar org.wordcount.WC_Runner /user/$USER/input /user/$USER/output -skip src/stopwords.txt

## View the output:
hdfs dfs -cat /user/$USER/output/part-r-00000

## Features

This application can:

Count word frequencies in large text datasets.

Remove common stopwords during processing.

Work with multiple input files at once.

Output sorted results in HDFS for easy retrieval.

## Data

The src/Input folder contains sample text files (book1–book5) for testing.
The src/stopwords.txt file contains the list of stopwords to exclude from counting.

