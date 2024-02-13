### Part 1: Requirements Engineering (RE) 101

- **Basics of RE**:
    - Functional Requirements: e.g., banking operations like credit and debit.
    - Non-Functional Requirements (NFRs): Availability, reliability, portability, testability, extensibility, performance, etc.
    - Usability: Nielsen’s 5 components - Learnability, memorability, satisfaction, reduction in errors, increase in efficiency/productivity.
- **Roles in RE**:
    - Business Analyst (BA): Models organizational structure, workflows, processes, IT systems.
    - Architect: Focuses on NFRs and Architecturally Significant Requirements (ASRs).

### Use Cases in RE

- **Basics**:
    - Use cases represent tasks with system support.
    - Actors represent roles played by system users.
    - Use case instantiation is a scenario documented in textual descriptions.
- **Use Case Realization**:
    - Iterative development approach with basic functionality in the first iteration.
    - Example: Developing use cases for borrowing and returning books and journals in a library system.

### Moving into Analysis Phase

- **Identifying Classes**:
    - Based on use case descriptions, identify key domain abstractions as classes.
    - Use noun identification technique for candidate classes.
    - Discard poor candidates using heuristics.

### Analysis Phase Class Diagram

- **First Cut**:
    - Use UML class model diagram to illustrate associations and multiplicity.
    - Example: Generalization between MemberOfStaff and LibraryMember.
- **Use Case Stereotypes**:
    - UML stereotypes like <<include>> and <<extends>> for common behavior and variant cases.

### Identifying and Prioritizing Use Cases

- Identify actors and their needs from the system.
- Prioritize use cases based on risk and time required for implementation.

### Problems with Use Cases

- Risks of developing non-object-oriented systems with inadequate class modeling.
- Confusion between design and requirements.

### Creating the Analysis Class Model

- **Steps**:
    - Identify candidate classes from use case descriptions.
    - Use CRC (Class Responsibilities Collaborations) cards for sanity checks.
    - Draw collaboration and communication diagrams.
    - Refine the use case class diagram to yield an analysis class diagram.

### Extending the UML

- Use of stereotypes and profiles for specific modeling needs.

### Recap and Reading Suggestions

- Recap of weeks 1 and 2, covering OOAD using UML, architecture, design patterns, refactoring, and more.
- Suggested reading: Chapters 6 and 7 in Bennett et al. or Chapters 5 - 8 in Stevens and Pooley.