1. **Concurrency and Parallelism in Software Development**:
    
    - Sequential programs have a single thread of control, known as a process.
    - Concurrent programs have multiple threads of control, which may be executed as parallel processes.
2. **GO or Golang**:
    
    - An open-source language created by Google to address common criticisms of other languages while maintaining their positive characteristics.
    - It is compiled, concurrent, imperative, and designed to support networking and multiprocessing.
3. **GO Language Design**:
    
    - Similar to C but with improved brevity and simplicity.
    - Features include concise variable declaration, fast compilation, and a toolchain that produces statically linked native binaries.
4. **Distributed Systems and Concurrency**:
    
    - The module considers distribution, concurrency, and parallelism, often with overlapping design issues.
5. **Moors Law and Multi Processors**:
    
    - Reference to Intel Quad Core 2 Extreme QX6700 as an example of a multi-processor system.
6. **Advantages of Concurrent Programming**:
    
    - Includes efficiency through speed-up execution on multiple CPUs, reactive programming, asynchronous invocation, real-time programming, simulation, and distribution.
7. **What is a Thread**:
    
    - A thread is an encapsulation of the flow of control in a program, with multithreaded programs having several threads running simultaneously.
8. **Threads and Processes**:
    
    - Threads are lightweight processes with shared data except for the stack and registers, making context switches less costly than between processes.
9. **Implementing Processes - The OS View**:
    
    - A heavyweight process in an OS is represented by its code, data, and machine registers, with multiple stacks to support lightweight threads.
10. **Threads versus Goroutine**:
    
    - Comparison between threads managed by operating systems and goroutines managed by the Go runtime, including differences in hardware dependency, communication medium, scheduling, startup time, and stack management.
11. **Parallelism**:
    
    - Describes the execution of threads in a multi-threaded process, with the potential for parallelism on a single CPU machine through interleaving.
12. **Concurrency and Parallelism**:
    
    - Discusses the difference between real and pseudo-concurrent execution on single and multiple CPU systems.
13. **Difficulties with Concurrent Applications**:
    
    - Includes challenges such as safety, liveness, non-determinism, and run-time overhead.
14. **Safety and Liveness**:
    
    - Safety ensures consistency, while liveness ensures progress, with properties to prevent deadlock and starvation.
15. **Expressing Concurrency**:
    
    - A programming language must provide mechanisms for process creation, communication, and synchronization.
16. **Communication and Synchronization**:
    
    - Differentiates between shared variable approaches, which require explicit synchronization, and message passing approaches, which combine communication and synchronization.
17. **Message Passing (The Go Way)**:
    
    - Message passing in Go combines communication and synchronization, with different modes such as asynchronous, buffered, and synchronous transfers.