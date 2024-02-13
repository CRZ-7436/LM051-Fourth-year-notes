### Part 1: The Factory Method Design Pattern (DP)

- **Definition**: A creational design pattern that provides an interface for creating objects in a superclass but allows subclasses to alter the type of objects that will be created.
- **Usage**:
    - When a class can't anticipate the class of objects it must create.
    - To delegate creation to subclasses and localize the creation process.
- **Example**: Trace interface for error reporting with different implementations like `FileTrace` and `SystemTrace`.

### Part 2: Singleton, Composite, and State Design Patterns

- **Singleton DP**: Ensures a class has only one instance and provides a global point of access to it.
- **Composite DP**: Allows you to compose objects into tree structures to represent part-whole hierarchies.
- **State DP**: Allows an object to alter its behavior when its internal state changes.

### Part 3: Overview of Design Patterns

- **Design Patterns**: Solutions to common problems in software design, providing a way to reuse successful designs and architectures.
- **Classification**:
    - Creational Patterns: Concerned with the construction of object instances.
    - Structural Patterns: Deal with the composition of classes or objects.
    - Behavioral Patterns: Characterize the ways in which classes or objects interact and distribute responsibility.

### Factory Method DP in Detail

- **Factory Method**: Used to create a family of objects, decoupling the instantiation process from the client.
- **Extensibility**: Demonstrated through scenarios like creating different types of mazes in a game using factory methods.

### Singleton DP in Detail

- **Usage**: When a single instance of a class is needed to control the action throughout the execution.
- **Example**: A company class where information is stored in one place and accessible by all other objects.

### Composite DP in Detail

- **Usage**: To treat individual objects and compositions of objects uniformly.
- **Example**: Graphical applications where both atomic objects (like circles) and composite objects (like a group of circles) are treated similarly.

### State DP in Detail

- **Usage**: To handle state-dependent variations in behavior.
- **Example**: Different states of a campaign in a business system, each with distinct behavior.

### General Overview of Design Patterns

- **Purpose**: To capture knowledge about problems and solutions in software development.
- **Flexibility**: Patterns provide a means to extend and modify software components without major changes.