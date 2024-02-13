### Q1: Non-Functional Requirements

**Non-Functional Requirements (NFRs)** refer to the criteria that judge the operation of a system, rather than specific behaviors. They are not about what the system does, but how the system performs its functions. These requirements are crucial for ensuring the usability, reliability, performance, and security of the system. Examples include scalability, performance, legal compliance, and usability.

**Taxonomy for Classifying Requirements:** One common taxonomy used to classify requirements is the **FURPS+ model**, developed by Robert Grady at Hewlett-Packard. FURPS+ is an acronym that stands for:

- **F**unctionality
- **U**sability
- **R**eliability
- **P**erformance
- **S**upportability
- **+** (Plus) includes additional concerns like design constraints, implementation requirements, interface requirements, physical requirements, etc.

In this model, non-functional requirements are primarily categorized under Usability, Reliability, Performance, Supportability, and the '+' categories.

### Q2: critisms of UML
- bloat/redundency
- poorly defined semantics
- doesnt work with agile
- weak extensibility

### Q3: RUP Diagram


### Q4: Purpose of a controll class
In the context of use case realization, particularly when drawing communication diagrams, a **control class** plays a crucial role. The primary purpose of a control class is to **mediate the interaction between the user interface and the underlying business logic or data model**. Here are the key functions of a control class in this scenario:
- **Facilitate Communication**
- **Handle Business Logic
- **Coordinate Activities**
- **Enhance Modularity**
- **mprove Clarity**

### Q5: List three interaction operators.
- **Message passing**
- **Event handling**
- **Data Flow**


### Q6:
![[Pasted image 20231212015202.png]]

### Q7:
- **event handling
- ***MVC architectural pattern

### Q8:

see previous notes

### Q9:
a) **Single Responsibility Principle (SRP)**:

The Single Responsibility Principle states that a class should have only one reason to change, meaning it should have only one responsibility or job. When a class has multiple responsibilities, changes to one of them may require modifications to the others, leading to code that is difficult to maintain and understand.

**Design Pattern Example**: The **Observer Pattern** illustrates the SRP. In this pattern, the subject (or observable) class has the responsibility of managing a list of observers and notifying them of changes. The observers, on the other hand, have the responsibility of responding to these changes. This separation of responsibilities allows for easier maintenance and extension of the code.

(b) **Open/Closed Principle (OCP)**:

The Open/Closed Principle states that software entities (e.g., classes, modules, functions) should be open for extension but closed for modification. This means that you should be able to add new functionality to a software component without altering its source code. This principle promotes code stability and reusability.

**Design Pattern Example**: The **Strategy Pattern** exemplifies the OCP. In this pattern, you define a family of algorithms, encapsulate each one in a separate class (strategy), and make these strategies interchangeable. The context class that uses these strategies is open for extension because you can add new strategies without modifying the context class. This allows you to introduce new behavior without changing existing code, adhering to the OCP.

### Q10:
1. **Rigid Price Code Logic:** The `Movie` class uses integer constants (`CHILDRENS`, `NEW_RELEASE`, `REGULAR`) to represent different price codes. This approach is rigid and makes it difficult to add new pricing strategies or modify existing ones without altering the `Movie` class.
    
2. **Switch Statement in `Customer` Class:** The `statement` method in the `Customer` class uses a switch statement to calculate charges based on the movie's price code. This design violates the Open/Closed Principle as any change in pricing logic requires modifications to the `Customer` class.
    
3. **Lack of Encapsulation:** The pricing logic is not encapsulated within the `Movie` class. Instead, it's spread across the `Customer` class, leading to a violation of the Single Responsibility Principle. The `Customer` class is handling both customer-related responsibilities and pricing logic for different types of movies.
    
4. **Frequent Renter Points Calculation:** The logic for calculating frequent renter points is also embedded within the `Customer` class. This further complicates the `Customer` class and mixes different concerns.

Diagram:
![[Pasted image 20231212015742.png]]
