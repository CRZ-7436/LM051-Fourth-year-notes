**CS4337 Big Data Management & Security** _Lecture 3 - Hadoop_ _Week 3, SEM 1 2023/24_ _Instructor: Dr. Andrew Ju_

**Introduction to Hadoop:**

- **Key Questions:**
    - Why Hadoop?
    - What is Hadoop?
    - How to use Hadoop?
    - Example of Hadoop usage.

**Recap of Big Data:**

- Big Data is a term for collections of datasets so large and complex that traditional data processing applications are inadequate.
- Everyday statistics of data generation:
    - 500 million tweets sent
    - 294 billion emails sent
    - 4 petabytes of data created on Facebook
    - Data from IoT connected cars
    - 65 billion WhatsApp messages
    - 5 billion Google searches

**The Problem with Big Data:**

- Massive data volumes
- Reliability of storing petabytes of data
- Various failures: disk, hardware, network
- Increased probability of failures with more machines

**Solution: Hadoop**

- Offers redundant, fault-tolerant data storage
- Provides a parallel computing framework
- Handles job coordination

**Hadoop's Advantages:**

- Manages file location
- Handles failures and data loss
- Divides computation
- Simplifies programming for scaling

**Real-world Example:**

- The New York Times used Amazon EC2 and S3 to convert 4 TB of TIFF images to PDF files, making their entire archive available online.

**Hadoop's History:**

- Open-source implementation based on Google's File System (GFS) and MapReduce
- Created by Doug Cutting and Mike Cafarella in 2005
- Donated to Apache in 2006

**Who Uses Hadoop?**

- Primarily entities that generate Big Data

**Hadoop Stack:**

- Distributed file system (HDFS)
- Execution engine (MapReduce)

**Hadoop Architecture:**

- Master-slave, shared-nothing architecture

**Hadoop Resources:**

- Apache Hadoop Documentation
- Data Intensive Text Processing with MapReduce
- Hadoop: The Definitive Guide

**Hadoop Distributed File System (HDFS):**

- Motivation: Store data on multiple machines using commodity hardware
- Master/Slave Architecture:
    - NameNode: Manages file system namespace and block mappings
    - DataNode: Handles block operations and replication
    - Secondary NameNode: Checkpoint node

**HDFS Inside:**

- Blocks: Fixed-size, easy to manage, replicate, and balance load
- Read/Write Operations: Clients interact directly with DataNodes for efficiency and scalability
- Rack-awareness for network topology optimization

**MapReduce (Distributed Programming):**

- Users provide "Map" and "Reduce" functions
- Job Tracker (Master node) manages task assignments and execution
- Task Tracker (Slave node) runs tasks and reports progress

**Properties of MapReduce Engine:**

- Handles Key/Value pairs interface
- Shuffling and Sorting: Groups similar keys for reducers
- Developer's responsibility to decide on keys and values

**MapReduce Phases:**

- Developer decides what will be the key and what will be the value

**Examples:**

- Word Count: Count occurrences of each word in a dataset
- Colour Count: Count occurrences of colors (specific example not detailed)