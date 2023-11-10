<span style="color:#00b050">read write mutex</span>
1. **Critical Sections**:
    
    - Critical sections are bottlenecks in a program that are not good for liveness but sometimes necessary for safety.
    - Entering and exiting a critical section is expensive in terms of processing overhead.
    - Programmers should minimize the time spent in critical sections, and one approach is to reduce the cross-section of the critical section.
    - Different threads may require different access types, some need read access while others need write access.
2. **Read/Write Synchronization**:
    
    - A Read/Write lock allows concurrent access for read-only operations, while write operations require exclusive access.
    - Multiple threads can read data in parallel, but an exclusive lock is needed for writing or modifying data.
    - When a writer is writing the data, all other writers or readers will be blocked until the writing is finished.
3. **Read/Write Synchronization and Starvation**:
    
    - Read/Write locks can be designed with different priority policies for reader vs. writer access, affecting concurrency and starvation.
    - Policies can be read-preferring, write-preferring, or unspecified with regards to priority.
4. **Write Lock Starvation**:
    
    - Write lock starvation is a problem where read locks are shared, and if a read lock is present, subsequent threads can add a read lock.
    - However, if a thread with a read lock is locked, a thread trying to add a write lock will be blocked, resulting in write lock starvation.
5. **Go's Guarantees**:
    
    - Go ensures that writers cannot be starved, readers cannot be starved, and no thread shall be allowed to starve.
6. **The sync Package**:
    
    - Contains various synchronization primitives like WaitGroup, Mutex, RWMutex, Cond, Once, and Pool.
7. **sync.RWMutex**:
    
    - Conceptually the same as a Mutex as it guards access to memory.
    - However, RWMutex gives more control over the type of access, allowing an arbitrary number of readers to hold a reader lock as long as nothing else is holding a writer lock.
8. **sync.RWMutex Methods**:
    
    - Methods used by readers: `Rlock` and `RUnlock`.
    - Methods used by writers: `Lock` and `Unlock`.
9. **sync.RWMutex Protocol**:
    
    - Once a writer calls `Lock()`, new readers are blocked.
    - The writer waits for the current set of readers to finish their jobs, and once done, the writer can proceed.
    - After the writer ends, previously blocked readers and then writers are resumed.
    - It is important to ensure that neither readers nor writers get starved.

<span style="font-weight:bold; color:#00b050">go mutex</span>
1. **Mutex Philosophy**:
    
    - Go encourages the principle of not communicating by sharing memory, but instead sharing memory by communicating.
2. **Mutex - Mutual Exclusion**:
    
    - Sometimes it is necessary to ensure that a block of code manipulating a data structure is executed by only one thread at a time to avoid conflicting accesses to shared data, such as read/write or write/write conflicts.
    - A mutex is a type used to enforce mutual exclusion, i.e., a critical section.
    - Mutexes are one kind of lock, with others including read/write locks and reentrant locks.
3. **Mutex Operations**:
    
    - When a thread locks a mutex, if the lock is unlocked, the thread takes the lock and continues execution. If the lock is locked, the thread blocks and waits until the lock is unlocked.
    - If multiple threads are waiting for a lock, they all wait until the lock is unlocked, and one will receive the lock.
    - When a thread unlocks a mutex, it continues normally, and a waiting thread (if any) takes the lock and is scheduled to run.
4. **Critical Sections With Mutexes**:
    
    - Critical sections can be bottlenecks and are not good for liveness, so it is advised to keep critical sections as small as possible.
    - Critical sections design can be coarse-grained, which leads to poor scalability, or fine-grained, which can be hard to write.
5. **Mutex in Go (sync.Mutex)**:
    
    - Go's standard library provides mutual exclusion with `sync.Mutex` and its two methods: `Lock` and `Unlock`.
    - A block of code can be defined to be executed in mutual exclusion by surrounding it with a call to `Lock` and `Unlock`.