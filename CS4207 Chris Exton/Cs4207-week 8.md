<span style="color:#00b050">wait groups</span>
1. **Go Channels Philosophy**:
    
    - The slides start by reiterating the Go philosophy of sharing memory by communicating rather than communicating by sharing memory.
2. **WaitGroup Methods**:
    
    - A `WaitGroup` waits for a collection of goroutines to finish.
    - The main goroutine sets the number of goroutines to wait for.
    - Each of the goroutines runs and calls `Done` when finished.
    - `Wait` can be used to block until all goroutines have finished, which is when the number of goroutines reaches zero.
3. **WaitGroup Operations**:
    
    - `Add(int)`: Increases the `WaitGroup` counter by the given integer value.
    - `Done()`: Decreases the `WaitGroup` counter by 1, indicating the termination of a goroutine.
    - `Wait()`: Blocks the execution until its internal counter becomes 0.
4. **Passing WaitGroup by Reference**:
    
    - If a `WaitGroup` is explicitly passed into functions, it should be done by pointer to ensure that the same `WaitGroup` is used across all goroutines.

<span style="font-weight:bold; color:#00b050">goto to go</span>
1. **Goto Statement in Go**:
    
    - The `goto` statement allows for an unconditional jump to a labeled statement within the same function.
    - The label used with `goto` can be any valid identifier that is not a Go keyword.
    - When the `goto` statement is encountered, control is transferred to the referred label, and execution continues from there.
    - Labels are only visible within the function where they are declared, and any reference from outside the function will result in a compilation error.
2. **Goto Example**:
    
    - The slides provide an example of how `goto` can be used in a function to skip certain statements and jump to a label within the same function.
3. **Recommendations on Goto Usage**:
    
    - The use of `goto` is not recommended as it can lead to poor code readability and is a source of many bugs.
    - The slides reference the famous 1968 letter by Edsger Dijkstra titled "Go To Statement Considered Harmful".
    - While `goto` is a keyword in Java, it is not implemented and is explicitly banned.
    - In Go, there is some safety in its implementation since a label has to be created in the same function as the `goto` statement.
    - There is a lot of debate online about if and when `goto` should be used.

<span style="font-weight:bold; color:#00b050">anonymous goroutines and closure</span>
1. **Nested and Anonymous Functions**:
    
    - Go allows functions to be nested within other functions.
    - Anonymous functions are functions defined without a name and can be used for inlining code, especially for goroutines.
2. **Anonymous Goroutine Functions**:
    
    - These are particularly useful for concurrent programming where you want to execute code in a separate goroutine without having to define a separate named function.
    - The slides provide examples of anonymous functions being used with the `go` keyword to initiate concurrent execution.
3. **Syntax of Anonymous Functions**:
    
    - An anonymous function starts with the `func` keyword followed by parameters in parentheses.
    - If there are no parameters, a set of empty parentheses is used.
    - The body of the function is enclosed in braces, similar to a normal function declaration.
4. **Calling Anonymous Functions**:
    
    - After defining an anonymous function, you can immediately call it by including the parameter values enclosed in parentheses after the closing brace.
    - If there are no parameters, a set of empty parentheses is used to call the function.
5. **Closures in Go**:
    
    - Anonymous functions can capture variables from the enclosing scope, known as closures.
    - A closure has access to variables in the scope in which it was created, even if the outer function has finished execution.
6. **Examples of Closures**:
    
    - The slides show how closures can access variables that are not declared within the anonymous function itself.
    - They also demonstrate how the value of a variable in a closure is the value at the time the variable is used, not when it was captured.
7. **Dangers with Closures and Loops**:
    
    - A common pitfall with closures is capturing loop variables, which may lead to unexpected results, such as capturing the final value of an iterator instead of the value at the time of capture.
8. **Solutions to Closure Pitfalls**:
    
    - To avoid issues with closures in loops, the slides suggest passing the loop variable as a parameter to the anonymous function, which ensures that a copy of the variable is made.
9. **Practical Examples**:
    
    - The slides provide practical code examples to illustrate how anonymous functions and closures work, including how to correctly capture loop variables to avoid common mistakes.