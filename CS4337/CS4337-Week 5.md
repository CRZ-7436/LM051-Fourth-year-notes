**CS4337 Big Data Management & Security** _Lecture 5 – Spark (continued)_ _Week 5, SEM 1 2023/24_ _Instructor: Dr. Andrew Ju_

**Agenda – Apache Spark:**

- Recap of Spark's purpose and capabilities.
- Deep dive into Spark's programming model.
- Understanding Spark RDDs (Resilient Distributed Datasets).
- Exploring Spark operations.
- Discussing scheduling and memory management in Spark.

**Recap – Why Spark?**

- Spark is a fast, expressive cluster computing system compatible with Apache Hadoop.
- It can work with any Hadoop-supported storage system (e.g., HDFS, S3).
- Spark improves efficiency through in-memory computing and general computation graphs.
- It also improves usability with rich APIs in Java, Scala, Python, and an interactive shell.
- Spark can be up to 100x faster than traditional systems and often requires 2-10x less code.

**Spark Architecture:**

- Master/Slave setup.
- Detailed communication model explaining job execution.

**Running Spark:**

- Locally on multicore systems as a library in your program.
- On EC2 using scripts for launching a Spark cluster.
- On a private cluster using Mesos, YARN, or standalone mode.

**Languages Supported:**

- APIs available in Java, Scala, and Python.
- Interactive shells provided for Scala and Python.

**Spark – Key Ideas:**

- Work with distributed collections similarly to local ones.
- RDDs are immutable collections of objects spread across a cluster.
- RDDs are built through parallel transformations (e.g., map, filter) and are automatically rebuilt on failure.
- Persistence of RDDs is controllable, such as caching in RAM.

**Operations in Spark:**

- Transformations: Lazy operations like map, filter, groupBy, join to build RDDs from other RDDs.
- Actions: Operations like count, collect, save that return a result or write it to storage.

**Example Use Case:**

- Mining Console Logs: Load error messages from a log into memory, then interactively search for patterns.

**RDD Fault Tolerance:**

- RDDs track their lineage (the transformations used to build them) to recompute lost data.

**Behavior with Less RAM:**

- The lecture may have discussed strategies for when there is insufficient RAM for operations.

**Spark Memory Management:**

- Memory utilization is crucial in Spark, especially for caching.
- The Spark process runs within a JVM (Java Virtual Machine).

**High-Level Coding in Spark:**

- Use high-level coding to build workflows in Scala/Java or Python.
- Code compiles to distributed parallel operations.
- Two abstraction units in Spark:
    - RDDs: Resilient Distributed Datasets.
    - Parallel Operations: Executed across the cluster.

**Language Recommendations:**

- Standalone programs can be written in Java, Scala, or Python, but the console is only for Python & Scala.
- Python developers can use Python for both standalone and console.
- Java developers might consider using Scala for the console to learn the API.
- Performance: Java/Scala will generally be faster due to static typing, but Python can perform well for numerical work with libraries like NumPy.