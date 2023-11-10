<span style="color:#00b050">lecture slide 1 *go channels*</span>
1. **Go Channels Philosophy**:
    
    - Emphasizes the principle of not communicating by sharing memory, but instead sharing memory by communicating.
2. **Concurrency & Go Channels**:
    
    - Channels are a means for two goroutines to communicate and synchronize their execution in a goroutine-safe manner.
    - They have FIFO (First-In-First-Out) semantics and are a type-safe generalization of Unix pipes.
    - Channels are inspired by Hoare's Communicating Sequential Processes (CSP) and are used to coordinate computations through explicit communication, reducing the need for locks, semaphores, and mutexes.
3. **More on Channels**:
    
    - A channel type is declared with the keyword `chan` followed by the type of items that are passed on the channel.
    - The `<-` operator is used for sending and receiving messages on the channel.
    - Channels facilitate not only the communication of typed data but also the synchronization of goroutines.
4. **Synchronization with Channels**:
    
    - Standard channels store a single element and provide FIFO semantics.
    - Messages sent on a channel will wait until the receiving goroutine is ready, thus channels can cause goroutines to block and unblock.
5. **Channel Direction**:
    
    - Channels can be restricted to either sending or receiving by specifying a direction on the channel type.lecture slide 2 <span style="color:#00b050">go comparison</span>
1. **Simple Syntax**:
    
    - Go has only 25 keywords, fewer than Java or C#, which implies less complexity.
    - It has simple scoping rules where the case of the first letter determines the visibility of package-level variables.
    - Go includes built-in garbage collection to simplify memory management.
2. **No Classes**:
    
    - Go does not support traditional classes but does have structures. Consequently, there are no constructors or destructors.
3. **Object-Oriented Programming**:
    
    - Instead of classes, Go uses structs and interfaces.
    - Methods can be defined on any type, and the method receiver can be a direct value or a pointer.
    - Go has two access levels, public and package-private, determined by the case of the first letter of top-level declarations.
4. **No Inheritance**:
    
    - Go avoids issues with multiple inheritance by providing interfaces that are more dynamic.
5. **No Overloading**:
    
    - Function overloading and operator overloading are not supported in Go. Functions and methods must have unique names within the same scope.
6. **No do or while Loops**:
    
    - The language does not contain do-while and while statements; for loops are used exclusively.
7. **No Exceptions**:
    
    - Go uses errors to signify events like end-of-file and run-time panics for run-time errors such as out-of-bounds array indexing.
8. **No Generics**:
    
    - As of the time of the slides, Go did not support generics, although it was a topic of debate and might be considered for future inclusion.
9. **No Implicit Type Conversion**:
    
    - Go requires explicit type conversion for operations that mix different types.
10. **Built-in Types**:
    
    - Strings and hash tables (maps) are built into the language, with strings being immutable.
11. **Pointers and References**:
    
    - Go offers pointers to values of all types and treats arrays as values. Maps, slices, and channels are passed by reference.
12. **Functional Programming**:
    
    - Functions are first-class citizens in Go and can be passed around just like other values.
13. **Complex Numbers**:
    
    - Go has built-in support for complex numbers.
14. **Formatting**:
    
    - Code formatting is standardized by the `gofmt` tool, and `golint` performs additional style checks.
15. **Concurrency**:
    
    - Go uses goroutines as lightweight processes for separate threads of execution.
    - Communication between goroutines is implemented using channels.
    - The `go` keyword is used to start a function in a new goroutine.
    - A channel without these restrictions is known as bi-directional.
    - Bi-directional channels can be passed to functions that take send-only or receive-only channels, but not vice versa.
6. **Buffered Channels**:
    
    - Channels are unbuffered by default, meaning they will only accept sends if there is a corresponding receive ready.
    - Buffered channels can be created with a capacity, allowing them to hold one or more elements before needing a corresponding receive.
    - Buffered channels are asynchronous, meaning sending or receiving a message will not wait unless the channel is full.


lecture slide 2 <span style="color:#00b050">go comparison</span>
1. **Simple Syntax**:
    
    - Go has only 25 keywords, fewer than Java or C#, which implies less complexity.
    - It has simple scoping rules where the case of the first letter determines the visibility of package-level variables.
    - Go includes built-in garbage collection to simplify memory management.
2. **No Classes**:
    
    - Go does not support traditional classes but does have structures. Consequently, there are no constructors or destructors.
3. **Object-Oriented Programming**:
    
    - Instead of classes, Go uses structs and interfaces.
    - Methods can be defined on any type, and the method receiver can be a direct value or a pointer.
    - Go has two access levels, public and package-private, determined by the case of the first letter of top-level declarations.
4. **No Inheritance**:
    
    - Go avoids issues with multiple inheritance by providing interfaces that are more dynamic.
5. **No Overloading**:
    
    - Function overloading and operator overloading are not supported in Go. Functions and methods must have unique names within the same scope.
6. **No do or while Loops**:
    
    - The language does not contain do-while and while statements; for loops are used exclusively.
7. **No Exceptions**:
    
    - Go uses errors to signify events like end-of-file and run-time panics for run-time errors such as out-of-bounds array indexing.
8. **No Generics**:
    
    - As of the time of the slides, Go did not support generics, although it was a topic of debate and might be considered for future inclusion.
9. **No Implicit Type Conversion**:
    
    - Go requires explicit type conversion for operations that mix different types.
10. **Built-in Types**:
    
    - Strings and hash tables (maps) are built into the language, with strings being immutable.
11. **Pointers and References**:
    
    - Go offers pointers to values of all types and treats arrays as values. Maps, slices, and channels are passed by reference.
12. **Functional Programming**:
    
    - Functions are first-class citizens in Go and can be passed around just like other values.
13. **Complex Numbers**:
    
    - Go has built-in support for complex numbers.
14. **Formatting**:
    
    - Code formatting is standardized by the `gofmt` tool, and `golint` performs additional style checks.
15. **Concurrency**:
    
    - Go uses goroutines as lightweight processes for separate threads of execution.
    - Communication between goroutines is implemented using channels.
    - The `go` keyword is used to start a function in a new goroutine.