**CS4337 Big Data Management & Security** _Lecture 6 – Spark (continued)_ _Week 7, SEM 1 2023/24_ _Instructor: Dr. Andrew Ju_

**Agenda – Apache Spark:**

- Recap of Spark's purpose and capabilities.
- Deep dive into Spark RDDs (Resilient Distributed Datasets).
- Exploring Spark operations.
- Discussing scheduling and memory management.
- Example applications of Spark.

**Recap – Why Spark?**

- Spark is a fast, expressive cluster computing system compatible with Apache Hadoop.
- It works with any Hadoop-supported storage system (e.g., HDFS, S3).
- Spark improves efficiency through in-memory computing primitives and general computation graphs.
- It improves usability through rich APIs in Java, Scala, Python, and an interactive shell.
- Spark can be up to 100x faster than Hadoop MapReduce and often requires 2-10x less code.

**Spark RDDs:**

- RDDs are collections of objects that act as one unit and can be stored in main memory or disk.
- They are designed for parallel operations and have fault tolerance without replication due to their lineage.
- RDDs are read-only and distributed either in main memory or disk, with the system automatically deciding their location.
- Users have control over persistence and partitioning strategies, indicating which RDDs they will reuse and choosing a storage strategy for them (e.g., in-memory storage).

**Spark Operations:**

- Spark provides transformations (e.g., map, filter, groupBy, join) to build RDDs from other RDDs and actions (e.g., count, collect, save) that return a result or write it to storage.
- Transformations are lazy operations, meaning they are not executed immediately but only when an action is triggered.
- Spark supports operations on key/value pairs, which are essential for distributed reduce transformations.

**Scheduling and Memory Management:**

- Execution in Spark is triggered when an action operation is invoked.
- The scheduler checks the lineage graph to execute the necessary transformations.
- Memory utilization is essential in Spark, especially for caching.
- Spark offers three storage options for persistent RDDs: in-memory storage as deserialized Java objects, in-memory storage as serialized data, and on-disk storage.
- The Spark process runs within a JVM, and memory usage can be controlled through parameters.

**RDD Fault Tolerance and Recovery:**

- RDDs maintain a lineage graph (Directed Acyclic Graph - DAG) to recompute lost data.
- In case of failure, RDD partitions can be recovered, although recovery can be time-consuming for RDDs with long lineage chains.
- Spark uses a checkpoint mechanism to make some RDDs persistent, which can be user-defined, system-controlled, or driven by workload.

**Example - Page Rank Algorithm:**

- Page Rank is a complex algorithm that benefits from Spark’s in-memory caching and involves multiple stages of map and reduce operations.
- The basic idea is to assign ranks to pages based on links to them, with links from many pages or high-rank pages contributing to a higher rank.
- The algorithm involves multiple iterations over the same data, with each page contributing a portion of its rank to its neighbors and updating its rank based on contributions from other pages.