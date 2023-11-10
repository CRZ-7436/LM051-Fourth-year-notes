1. **Nondeterministic vs Deterministic**:
    
    - **Deterministic** algorithms or systems operate in a way where the output is predictable and consistent for a given input every time.
    - **Nondeterministic** algorithms or systems may produce different outcomes for the same input on different executions, often due to elements of randomness or parallelism.
2. **Shared State (Memory) vs Message Passing (Distributed State)**:
    
    - **Shared State (Memory)** refers to a concurrency model where multiple threads or processes share the same area of memory and communicate by reading and writing to these shared variables.
    - **Message Passing (Distributed State)** involves processes or threads that have separate memory and communicate by sending messages to each other. This is common in distributed systems.
3. **Process Synchronization vs Data Access Synchronization**:
    
    - **Process Synchronization** is about coordinating the sequence and timing of processes to ensure correct execution.
    - **Data Access Synchronization** is specifically about ensuring that concurrent access to shared data does not create conflicts or corrupt the data.
4. **Immutable**:
    
    - An **Immutable** object or variable is one that cannot be modified after it is created. This is beneficial in concurrent programming because it eliminates the need for synchronization.
5. **Semaphore**:
    
    - A **Semaphore** is a synchronization primitive that can be used to control access to a common resource by multiple processes in a concurrent system. It uses a counter to control access, which can be incremented or decremented.
6. **Atomic Operation**:
    
    - An **Atomic Operation** is one that is completed in a single step from the perspective of other threads. It cannot be interrupted and is used to prevent race conditions.
7. **Atomic Variable**:
    
    - An **Atomic Variable** is a variable that is read or written atomically. Operations on atomic variables are often used to implement thread-safe data structures without locks.
8. **Deadlock**:
    
    - A **Deadlock** occurs when two or more processes are unable to proceed because each is waiting for the other to release a resource.
9. **Livelock**:
    
    - A **Livelock** is a situation where two or more processes continually change their state in response to changes in the other processes without doing any useful work.
10. **Starvation**:
    
    - **Starvation** happens when a process or thread is perpetually denied necessary resources to proceed with its work, often due to unfair scheduling or resource allocation.
11. **Lock Granularity**:
    
    - **Lock Granularity** refers to the size or amount of data a lock controls. Fine-grained locks protect small amounts of data, while coarse-grained locks protect large sections of data.
12. **Thread Local Storage**:
    
    - **Thread Local Storage (TLS)** is a computer programming method that uses static or global memory local to a thread, ensuring that the data is unique to that thread.
13. **Mutual Exclusion (Mutex)**:
    
    - **Mutex** is a program object that allows multiple program threads to share the same resource, such as file access, but not simultaneously.
14. **Critical Section**:
    
    - A **Critical Section** is a part of a multi-threaded program that must not be executed by more than one thread at the same time to prevent access conflicts.
15. **Thread of Execution**:
    
    - A **Thread of Execution** is the smallest sequence of programmed instructions that can be managed independently by a scheduler.
16. **Thread Safe**:
    
    - A piece of code or program is **Thread Safe** if it functions correctly during simultaneous execution by multiple threads.
17. **Context Switching**:
    
    - **Context Switching** is the process of storing and restoring the state (context) of a CPU so that execution can be resumed from the same point at a later time.
18. **Significance of Lock Order**:
    
    - The **Significance of Lock Order** is a principle that states that locks should always be acquired in a consistent order to prevent deadlocks.
19. **Race Condition**:
    
    - A **Race Condition** occurs when the system's substantive behavior is dependent on the sequence or timing of other uncontrollable events.
20. **Data Synchronization**:
    
    - **Data Synchronization** is the process of establishing consistency among data from a source to a target data storage and vice versa and the continuous harmonization of the data over time.
21. **System Threads vs User-Level Threads (Green, Lightweight Threads)**:
    
    - **System Threads** are managed by the operating system, and the OS kernel performs thread creation, scheduling, and management.
    - **User-Level Threads** or **Green Threads** are managed by a user-level library or runtime, without kernel support, and are lighter weight but may lack certain system-level features.
22. **Concurrency vs Parallelism**:
    
    - **Concurrency** is about dealing with lots of things at once (like handling multiple tasks at the same time).
    - **Parallelism** is about doing lots of things at once (like performing multiple computations simultaneously).
23. **Tightly Coupled vs Loosely Coupled Systems**:
    
    - **Tightly Coupled Systems** are those in which components are highly dependent on each other, often leading to a system where components are hard to isolate and changes in one component can significantly affect others.
    - **Loosely Coupled Systems** are composed of components that do not depend on each other as much. Changes in one component tend to have minimal or no impact on others. This is often seen as a more flexible and maintainable approach.