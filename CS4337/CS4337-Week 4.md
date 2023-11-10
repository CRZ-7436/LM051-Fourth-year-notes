**CS4337 Big Data Management & Security** _Lecture 4 – Spark_ _Week 4, SEM 1 2023/24_ _Instructor: Dr. Andrew Ju_

**Quiz I:**

- Question about the backup of the master Hadoop node in the event of failure. The correct answer is b. Secondary NameNode.

**Quiz II:**

- Question regarding the common, worker node in a Hadoop system. The correct answer is d. DataNode.

**Agenda – Apache Spark:**

- Understanding the need for Apache Spark and its motivation.
- Exploring the Spark Programming Model.
- Learning about Spark RDDs (Resilient Distributed Datasets).
- Discussing Scheduling and Memory management in Spark.

**Motivation for Apache Spark:**

- **Need for New Infrastructure**: Hadoop has been widely used, but there are reasons to move away from it:
    - MapReduce was great for batch processing, but there are needs for more complex, multi-pass algorithms, interactive ad-hoc queries, and real-time stream processing.
    - Specialized systems are required for these complicated workloads.

**Downsides of Specialized Systems:**

- More systems to manage, tune, and deploy.
- Inability to combine different processing types in one application.
- Data exchange between engines often becomes the dominant cost, especially in pipelines that involve loading data with SQL, then running machine learning.

**Vision for a Generic Efficient Infrastructure:**

- The goal is to create a generic infrastructure that can handle complex multi-pass algorithms, interactive ad-hoc queries, and real-time stream processing efficiently.

**Motivation from the Hardware Side:**

- RAM is becoming much cheaper, leading to commodity machines with gigabytes of RAM.
- Large distributed RAM in clusters suggests that processing, storage, and data transfer should ideally use RAM.

**Summary of Motivation to Use Spark:**

- Provides better support for real-time processing.
- Exploits RAM as much as possible for processing and storage.
- Enables large-scale distribution without reinventing the wheel.

**Spark Overview:**

- Spark Architecture follows a Master/Slave model.
- The Spark Communication Model details how Spark executes a job.