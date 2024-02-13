### Q1: What are Non-Functional Requirements? Describe one taxonomy used to classify requirements.

**Solution**:

- **Non-Functional Requirements (NFRs)**: These are requirements that specify criteria that can be used to judge the operation of a system, rather than specific behaviors. They often include aspects like system performance, security, usability, and reliability.
- **Taxonomy for Classifying Requirements**:
    - **FURPS+ Model**: A widely used taxonomy for software requirements. It stands for Functionality, Usability, Reliability, Performance, and Supportability. Additional considerations include design constraints, implementation requirements, interface requirements, and physical requirements.

### Q2: Why are semantics necessary in UML?

**Solution**:

- Semantics in UML (Unified Modeling Language) are necessary because they provide a clear and unambiguous meaning to the modeling elements. Without well-defined semantics, different people might interpret the same UML diagram in different ways, leading to misunderstandings and inconsistencies in the design and implementation of the system.

### Q3: Draw a diagram that illustrates the phases and flows in the Rational Unified Process.

**Solution**:

- The Rational Unified Process (RUP) is divided into four phases: Inception, Elaboration, Construction, and Transition. Each phase consists of one or more iterations where specific activities occur: Business Modeling, Requirements, Analysis & Design, Implementation, Testing, and Deployment. (A diagram should be drawn to reflect these phases and iterative flows.)

### Q4: Write the code for the aggregation shown in Figure 2.

**Solution**:

- The solution would involve writing code that represents an aggregation relationship between two classes. Unfortunately, without the specific details of Figure 2, I cannot provide the exact code. Generally, it involves creating class definitions where one class contains a reference to one or more instances of another class.

### Q5: What is the purpose of a state chart? Illustrate the discussion with a diagram.

**Solution**:

- The purpose of a state chart (or state machine diagram) in UML is to model the dynamic behavior of a system. It shows the life cycle of an object, including its states, the events that cause a transition from one state to another, and the actions that result from a state change. (A diagram should be drawn to illustrate a simple state machine, such as the states of a light switch: on and off.)

### Q6: Write code to implement the Flows relationship in Figure 1.

**Solution**:

- Similar to Q4, without the specific details of Figure 1, I cannot provide the exact code. Generally, implementing a 'Flows' relationship would involve defining classes and methods that facilitate the movement or transfer of data or control from one part of the system to another.


### Q7: Discuss one of the following implementation issues in the Observer Design Pattern.
 Avoiding observer-specific update protocols OR
 Specifying modifications of interest explicitly OR
 Encapsulating complex update semantics

### 1. Avoiding Observer-Specific Update Protocols

In the Observer Design Pattern, a key challenge is avoiding observer-specific update protocols. The pattern typically involves a generic update mechanism where the subject notifies observers of changes without specifying details. However, in complex systems, different observers might need different kinds of updates. Here are some considerations:

- **Generic Update Calls:** The subject can use a generic update call, like `update()`. This simplicity can lead to inefficiencies when observers need to determine what exactly changed, often leading to unnecessary computations or checks.
    
- **Observer-Specific Protocols:** To address this, a more tailored update mechanism can be designed where the subject sends specific information about what changed. However, this can lead to a tight coupling between the subject and its observers, undermining the flexibility and reusability of the pattern.
    
- **Maintaining Balance:** The key is to strike a balance between a too-generic update mechanism and a highly tailored one. This might involve using a broad yet informative event system where updates carry enough information for observers to understand the context of the change without being overly specific.
    

### 2. Specifying Modifications of Interest Explicitly

Another implementation issue is enabling observers to specify which modifications they are interested in, rather than being notified of all changes indiscriminately. This is important for efficiency and relevance.

- **Filtering Mechanism:** Implement a filtering mechanism where observers can register their interest in specific types of updates. This reduces unnecessary notifications and processing.
    
- **Granular Subscription:** Allow observers to subscribe to specific events or state changes. This granularity enhances the system's performance and reduces the likelihood of observers receiving irrelevant updates.
    
- **Dynamic Interest Management:** Observers might need to change their subscriptions over time. Providing a dynamic mechanism for altering interests can be beneficial, though it adds complexity to the observer management.
    

### 3. Encapsulating Complex Update Semantics

The complexity of the update semantics in an observer pattern can vary greatly. In some cases, the logic for what happens during an update can become quite intricate.

- **Complex Dependencies:** When an update in the subject leads to a series of cascading changes across various observers, managing these dependencies becomes challenging. Ensuring that updates occur in a consistent and predictable order is crucial.
    
- **State Consistency:** Ensuring that all observers view a consistent state of the subject can be complicated, especially if updates can occur asynchronously. Strategies like using immutable state snapshots or applying changes in a transactional manner can help.
    
- **Performance Considerations:** Complex update semantics might introduce performance bottlenecks, especially if the updates involve heavy computations or a large number of observers. Efficient data structures, lazy updates, or batching notifications can be employed to address this.


### Q8: Critique and refactor the code in Figure 2.

**Solution**:

- **Critique**: The given code tightly couples the `Button` class with the `CdPlayer` class, making it difficult to extend or modify. It uses explicit checks to determine which button was pushed, which is not scalable.
- **Refactoring**: 
// Command Interface
public interface Command {
    void execute();
}

// Concrete Command for Play
public class PlayCommand implements Command {
    private CdPlayer cdPlayer;

    public PlayCommand(CdPlayer cdPlayer) {
        this.cdPlayer = cdPlayer;
    }

    @Override
    public void execute() {
        cdPlayer.play();
    }
}

// Concrete Command for Stop
public class StopCommand implements Command {
    private CdPlayer cdPlayer;

    public StopCommand(CdPlayer cdPlayer) {
        this.cdPlayer = cdPlayer;
    }

    @Override
    public void execute() {
        cdPlayer.stop();
    }
}

// Receiver Class
public class CdPlayer {
    public void play() {
        System.out.println("Play Button Pushed");
    }

    public void stop() {
        System.out.println("Stop Button Pushed");
    }
}

// Invoker Class
public class Button {
    private Command command;

    public Button(Command command) {
        this.command = command;
    }

    public void push() {
        command.execute();
    }
}

// Client Class
public class GlobalMembersCallback1 {
    public static void main(String[] args) {
        CdPlayer cdPlayer = new CdPlayer();

        Command playCommand = new PlayCommand(cdPlayer);
        Command stopCommand = new StopCommand(cdPlayer);

        Button playButton = new Button(playCommand);
        Button stopButton = new Button(stopCommand);

        playButton.push();
        stopButton.push();
    }
}


### Explanation of the Refactoring:

1. **Command Interface**: This defines a common interface for all commands (`Command` interface with an `execute()` method).
    
2. **Concrete Commands**: `PlayCommand` and `StopCommand` implement the `Command` interface and encapsulate the action to be performed.
    
3. **Receiver**: The `CdPlayer` class contains the actual logic for playing and stopping the CD.
    
4. **Invoker**: The `Button` class acts as an invoker. It is initialized with a command object and will trigger the command's execution when the button is pushed.
    
5. **Client**: The `GlobalMembersCallback1` class sets up the commands, associates them with buttons, and simulates button pushes.
    

This refactoring decouples the `Button` class from the `CdPlayer` class, making the system more flexible and easier to extend or modify. For instance, adding new buttons with different functionalities becomes straightforward without needing to change the existing `CdPlayer` or `Button` classes.

### Q9: Refactor the maze game code to use the Factory Method design pattern.

**Solution**:

**MazeFactory Class:** This is the factory class responsible for creating maze components (Rooms, Walls, Doors).

class MazeFactory {
public:
    virtual Room* MakeRoom(int n) const { return new Room(n); }
    virtual Wall* MakeWall() const { return new Wall(); }
    virtual Door* MakeDoor(Room* r1, Room* r2) const { return new Door(r1, r2); }
};

### Modified Classes

1. **MazeGame Class:** Modified to use `MazeFactory` for creating maze components.


class MazeGame {
public:
    MazeGame(MazeFactory* factory): _factory(factory) {_myMaze = CreateMaze();}
    void Run();
private:
    Maze* CreateMaze();
    Maze *_myMaze;
    MazeFactory* _factory;
};

Maze* MazeGame::CreateMaze() {
    Maze *aMaze = new Maze;
    Room *r1 = _factory->MakeRoom(111);
    Room *r2 = _factory->MakeRoom(222);
    Door *d = _factory->MakeDoor(r1, r2);
    aMaze->AddRoom(r1);
    aMaze->AddRoom(r2);
    r1->SetSide(North, _factory->MakeWall());
    .............
    return aMaze;
}


### Q10: Demonstrate how the Factory Method design pattern supports change.

**Solution**:

class EnchantedRoom : public Room {
public:
    EnchantedRoom(int n) : Room(n) {}
    virtual void Enter() {
        cout << "\n Entering an enchanted room " << GetRoomNumber() << "\n";
    }
    // Additional enchanted room features can be added here
};

class EnchantedDoor : public Door {
public:
    EnchantedDoor(Room* r1, Room* r2) : Door(r1, r2) {}
    virtual void Enter() {
        cout << "\n Entering an enchanted door between rooms\n";
    }
    // Additional enchanted door features can be added here
};

class EnchantedMazeFactory : public MazeFactory {
public:
    virtual Room* MakeRoom(int n) const override { return new EnchantedRoom(n); }
    virtual Door* MakeDoor(Room* r1, Room* r2) const override { return new EnchantedDoor(r1, r2); }
    // Wall creation remains the same, so it's not overridden
};

In this example, the `MazeGame` class remains unchanged, demonstrating the power of the Factory Method pattern. By simply swapping out the factory, we can create a completely different type of maze (in this case, an enchanted one) without any modifications to the `MazeGame` class. This shows how the Factory Method design pattern supports change and makes the system more flexible and extensible.