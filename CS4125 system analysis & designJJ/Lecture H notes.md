### . Activity Diagrams

- **Purpose**: To model business processes/workflows, system functions represented by use cases, and the logic of operations.
- **Characteristics**: Similar to flowcharts, focusing on the flow of activity driven by internal processing within an object.
- **Usage**:
    - Modeling sequences of steps in a use case description.
    - Representing business processes or workflows, like buying a product online.
    - Describing operations or methods.

### 2. Components of Activity Diagrams

- **Synchronization Bar**: Represents fork and join in the flow.
- **Swimlanes (Partitions) and Object Flows**: Divides an activity diagram into different areas of responsibility.
- **Signals and Parameterizing Flows**: Handling events and data flow within the diagram.
- **Expansion Regions**: For complex flows within the diagram.

### 3. State Charts

- **Guard Conditions**: Conditions that control state transitions.
- **States and Events**:
    - The current state of an object is a result of its attributes and links.
    - Movement from one state to another is triggered by events.
- **Overview**: State charts model state-dependent variations in behavior, capturing all possible responses of a single object to all use cases.

### 4. State Charts vs. Activity Diagrams

- **Differences**: State charts focus on the states of an object and transitions triggered by events, while activity diagrams focus on the flow of activities and control.

### 5. State Charts: Detailed Components

- **Triggers**: Types of triggers like change, call, signal, and relative time triggers.
- **Notation**: Standard UML notation for state charts.
- **Composite States**: Representing complex state behavior at different levels of detail.
- **Concurrent States**: Modeling objects with concurrent states.

### 6. Final Statechart for Campaign

- A comprehensive statechart for the Campaign class, illustrating the final version of the statechart.

### 7. Reading Suggestions

- **Recommended Reading**: Chapter 11 in Bennett et al., or Chapters 11 and 12 in Stevens and Pooley.