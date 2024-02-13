### . Design Overview: Transition from Analysis to Design

- **Process Separation**: Analysis determines what the system should do, while design focuses on how it should be implemented.
- **System vs. Detailed Design**: System design deals with overall architecture and standards, while detailed design focuses on individual components.

### 2. System Design Activities

- Identification of sub-systems and major components.
- Architecture decisions, including client-server distribution.
- Data management, security strategy, and human-computer interface standards.
- Development of test plans and code development standards.

### 3. System Design and Architecture

- **Importance of Architecture**: Defines the structure of the system, including software elements and their relationships.
- **Subsystems**: Division into smaller units for development, maximizing component reuse, and managing complexity.

### 4. Layering and Partitioning in System Design

- **Layering**: Different sub-systems represent different levels of abstraction.
- **Partitioning**: Focuses on different aspects of system functionality.
- **Layered Architecture**: Commonly used in business-oriented information systems to eliminate tight coupling between interfaces and data representation.

### 5. Model-View-Controller (MVC) Architectural Pattern

- **Components**: Separation into models (functionality), views (user interface), and controllers (update management).
- **Benefits**: Facilitates maintenance, portability, and the ability to present information in different formats.
- **MVC Architecture**: Solves update issues by separating core functionality from the interface.

### 6. Broker and Concurrency in System Design

- **Broker Pattern**: Used in distributed systems for decoupling components.
- **Concurrency**: Handling objects that operate concurrently, often on different logical processors.

### 7. Reading on Architectural Patterns

- **Quote**: "All architecture is design, but not all design is architecture."
- **Suggested Reading**: Chapters 8, 12, 13, 14, and 15 in Bennett, McRobb, and Farmer (4th Edition).