## Design

After the initial analysis and breakdown of the problem - dealing with *what* needs to be captured - we now need to start thinking about *how* we will implement the solution. Remember, all the steps and designs are not necessary for a software project; we can pick and choose which portions of the problem we want to design, such as a complicated feature, to aid with shared understanding.

### Design by contract

Object-oriented design (OOP) works because it uses real-world objects to build systems. This makes it easier to understand, as we all use this concept subconsciously in our everyday lives, e.g., a car and its parts, such as the engine and doors.

Objects implemented in the design phase can differ from those conceptualized in the analysis models.

As in the real world, contracts form a legal binding by an entity towards another, ensuring that it will perform its duties as laid out in the contract. Similarly, in OOP, the [design by contract (DbC)](https://en.wikipedia.org/wiki/Design_by_contract) approach involves designing objects with a similar contract in mind. A sender/client object sends a message to a receiver/server object, expecting a result back as long as both parties conform to the predefined expectations. If either party does not conform to these expectations, the contract is broken and the service is not supplied. These expectations are in the form of preconditions and postconditions.

Preconditions: what is needed for an operation to be allowed to start?

Postconditions: what will have happened as a result of this operation?

Example: The withdrawing functionality of a banking system could have the following contract.

Precondition: There must be sufficient funds in the account to permit the operation without exceeding the overdraft limit

Postcondition: The account will have been debited the requested amount.

Both of those conditions (contract) will have to be met for the withdrawl to take place.


### Dynamic modelling

So far we have focused on the static modelling of the system, we will now explore the [dynamic modelling](https://www.geeksforgeeks.org/dynamic-modelling-in-object-oriented-analysis-and-design/), which show how the objects interact by sending messages to each other, implementing the required functionality of the system.

To start designing the software solution, we need to have in mind the main design principles that make a good software product, such as encapsulation, low coupling and high cohesion. There are many design patterns that fit better for different situations that could be applied effectively with experience. Even though there are many design patterns that provide general guidance on how to build a product, there are some more practical principles that help solve design problems, [general responsibility assignment software patterns (GRASP)](https://en.wikipedia.org/wiki/GRASP_(object-oriented_design))

Notable *GRASP* principles:

- **Creator** - Creator pattern is a design principle used in object-oriented design to determine which class should be responsible for creating instances of another class. According to this pattern, a class should create an instance of another class if it contains, aggregates, closely uses, or has the initializing data for that object. This helps to ensure that object creation responsibilities are assigned in a way that supports clear and maintainable code, reducing dependencies and promoting encapsulation.

- **Expert** - According to this pattern, a class that has the necessary information to fulfill a task should be the one to carry it out. In other words, the "expert" on a particular piece of information or functionality should be responsible for handling it. This ensures that tasks are assigned to the classes best suited to perform them, leading to more cohesive and maintainable code. By following the Expert Pattern, developers can create systems where responsibilities are logically distributed and encapsulated within the appropriate objects.


**Sequence Diagrams**

A [sequence diagram](https://en.wikipedia.org/wiki/Sequence_diagram) in OOP visually represents the interactions and order of messages between objects over time. It shows how objects collaborate to achieve a specific functionality by depicting the sequence of method calls and the flow of information between them. The diagram typically includes objects represented by lifelines, horizontal arrows indicating messages, and vertical lines showing the passage of time. This helps in understanding the dynamic behavior of the system and the interactions among its components.

![Sequence diagram example](./images/sequence-diagram.png)


**Communication diagrams**

[Communication diagrams](https://en.wikipedia.org/wiki/Communication_diagram), also known as collaboration diagrams, are used in object-oriented design to illustrate the interactions between objects in a system, focusing on the structural organization of these objects and their relationships. Unlike sequence diagrams, which emphasize the order of messages over time, communication diagrams highlight the network of objects and the flow of messages among them.

In a communication diagram, objects are represented as rectangles, and their links (or associations) are depicted as lines connecting these rectangles. Messages exchanged between the objects are shown as arrows on these lines, often numbered to indicate the sequence of interactions. This type of diagram helps in understanding how objects collaborate to perform a specific task and is useful for visualizing and designing the communication pathways within a system.

![Communication diagram example](./images/communication-diagram.png)
