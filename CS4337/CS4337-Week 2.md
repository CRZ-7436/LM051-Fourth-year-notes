**CS4337 Big Data Management & Security** _Lecture 2 - Big Data_ _Week 2, SEM 1 2023/24_ _Instructor: Dr. Andrew Ju_

**Scalability of Database Systems:**

- **Scale Out**: Utilize more resources to distribute workload in parallel. This approach typically incurs higher data access latency as data is more distributed.
- **Scale Up**: Efficient use of the resource through architecture-aware algorithm design.

**Agenda:**

- Focus on Big Data and its implications.

**Big Data Techniques:**

- Massive Parallelism
- Huge Data Volumes Storage
- Data Distribution
- High-Speed Networks
- High-Performance Computing Task and Thread Management
- Data Mining and Analytics Data Retrieval
- Machine Learning
- Data Visualization

**Typical Scenario vs. Big Data:**

- **Application Development**:
    - Traditional: Specialized developers skilled in high-performance computing, performance optimization, and code tuning.
    - Big Data: Simplified model using distributed file systems, programming models, databases, and scheduling within frameworks like Hadoop.
- **Platform**:
    - Traditional: High-cost massively parallel processing (MPP) computers with high-bandwidth networks and massive I/O devices.
    - Big Data: Scalable and elastic virtualized platforms using clusters of commodity hardware or cloud-based services.
- **Data Management**:
    - Traditional: File-based or relational database management systems (RDBMS) with standard row-oriented data layouts.
    - Big Data: NoSQL models offering a variety of methods for managing information to suit specific business needs, like in-memory data management, columnar layouts, and graph databases.
- **Resources**:
    - Traditional: Large capital investment in high-end hardware managed in-house.
    - Big Data: Deployment on virtualized platforms like Hadoop in cloud-based environments, more cost-effective for small and medium businesses.

**Why is Big Data a Big Deal now?**

- Increased data collection and storage.
- Availability of open-source code.
- Use of commodity hardware and cloud services.
- Advances in Artificial Intelligence.

**Big Data and AI/ML:**

- The lecture slides may have detailed the relationship between Big Data and AI/ML, highlighting how big data fuels AI algorithms and machine learning models.

**Some Big Stats:**

- Facebook's use of public Instagram photos for AI training.
- Predicted growth of the big data analytics market.
- Data generation rates per person.
- Daily internet data generation.
- The necessity for businesses to manage unstructured data.
- Organizational investment in big data and AI.
- Netflix's savings on customer retention using big data.
- Increase in cyber scams during the pandemic.
- Projected data creation growth.

**Importance of Data:**

- Data likened to oil by Clive Humby in 2008, emphasizing its value when refined and analyzed.
- Recommended resources for understanding data's influence: "The Social Dilemma" and "AlphaGo The Movie".

**Impact of Big Data Analytics:**

- This section was marked "TBA" (To Be Announced), indicating upcoming content on the impact of big data analytics.

**Example – Google Case Study:**

- Google's use of MapReduce to process large amounts of data.
- The necessity of a distributed system for storage and parallel processing.
- Challenges of parallel programming, communication between nodes, scaling, and handling machine failures.

**MapReduce:**

- Google's solution for big data processing.
- Features automatic parallelization, distribution, I/O scheduling, load balancing, network and data transfer optimization, fault tolerance, and handling of machine failures.
- Emphasizes scaling out with commodity servers rather than scaling up with specialized servers.

**Classic Word Count Example:**

- A typical problem solved by MapReduce, demonstrating the process of reading data, mapping, shuffling, sorting, reducing, and writing results.

**Summary:**

- MapReduce is a programming paradigm for data-intensive computing.
- It allows for distributed and parallel execution.
- It is simple to program and automates many tasks such as machine selection and failure handling.