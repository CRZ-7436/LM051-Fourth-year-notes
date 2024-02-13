### Part A: Detailed Design

- **Design Guidelines**:
    
    - Emphasize design clarity and use standard design protocols.
    - Avoid overdesigning systems to maintain flexibility for future extensions.
    - Control inheritance hierarchies (suggested maximum of four levels).
    - Keep messages and operations simple, with limited parameters.
- **Design Volatility**:
    
    - Aim for a stable design that can accommodate changes in requirements.
    - Enforce encapsulation to enhance stability.
- **Designing Associations**:
    
    - Focus on navigability and direction of messages in associations between classes.
    - Minimize two-way associations to reduce coupling.
    - Use arrays or collection classes for one-to-many relationships.
- **Integrity Constraints**:
    
    - Ensure referential integrity, dependency constraints, and domain integrity in design.
- **Normalization**:
    
    - Address redundancy and consistency in system models, especially for relational databases.
- **Coupling and Cohesion**:
    
    - Strive for low coupling and high cohesion in design.
    - Focus on interaction coupling and inheritance coupling.
    - Ensure operation and class cohesion, as well as specialization cohesion in inheritance hierarchies.
- **Liskov Substitution Principle (LSP)**:
    
    - Ensure derived classes are substitutable for their base classes without compromising integrity.

### Part B: Component and Deployment Diagrams

- **Package Diagrams**:
    
    - Provide namespace control and hide irrelevant details.
    - Facilitate interaction modeling between packages.
    - Used for specifying and designing components.
- **Component Diagrams**:
    
    - Show dependencies between parts of the code.
    - Components should realize interfaces and depend on interfaces of other components.
- **Deployment Diagrams**:
    
    - Illustrate the physical structure of the runtime system, including hardware configurations.
    - Show physical communication links and relationships between hardware items and resources.
    - Detail artifacts in the physical system and runtime dependencies.

### Suggested Reading

- **Stevens and Pooley**: Chapters 13 and 14.
- **Bennett et al. (Fourth Edition)**: Sections 3 and 4 in Chapter 19.