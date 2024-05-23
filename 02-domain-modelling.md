## Domain Modelling

**Business rules** and **business processes** are required to be understood in order to start designing our project.
Business rules reflect the way the business works, independently of any new system being introduced in that business domain. Business processes define what is done in the business, by whom and with what consequences.

For example in a lending book company we could extract these business rules,

- There is a limit in the number of books a member can take out.
- Late returns incur a fine.

And these business processes,

- Issue a book
- Return a book

Business rules need to be *verified* and *validated* to ensure the solution is correctly developed and satisfies the business requirements. Verification can be performed automatically to ensure that the rules match what is developed. Validation can be performed by stakeholders to confirm that the rules meet the business needs.

We will explore how different business processes, rules, and scenarios can be modeled with UML and specific descriptions.

### Activity Diagrams

Business processes can be represented as [UML Activity Diagrams](https://en.wikipedia.org/wiki/Activity_diagram). Activity diagrams help us understand the business situation before any decisions are taken about the software solution and its boundaries. They model the behavioural aspect of the domain.

Notable design blocks for activity diagrams:

 - **Start/End nodes**: The start node is where the diagram begins (initial state), and the end node is where it ends (final state). They are represented by filled circles.
 - **Activities**: These are the main building blocks of activity diagrams, shown as rounded boxes. They represent each process as an isolated task.
 - **Transitions**: These go hand in hand with activities. They are the arrowed lines connecting the activities. Each activity will have an incoming and an outgoing transition. The end of an activity will transition to the start of the next.
 - **Synchronization bars**: These are denoted by thick black horizontal lines. The upper bar indicates a *fork*, and the lower one a *join*. This means activities within the synchronization bars can run in parallel, and at the end, they will all have to complete (join) before the next activity, outside the bars, can start.
 - **Decision nodes**: When there are two or more alternative paths an activity might take (like an if statement), a decision node can denote that. They are represented as diamond shapes, and the *guards* (their boolean pathways) are written inside square brackets on their outgoing transitions.
 - **Merge nodes**: Every decision node's outgoing transitions *must* converge in a merge node. A merge node is represented the same way as a decision node, as a diamond.
 - **Swimlanes**: With activity diagrams, we might want to represent different roles or different services of the product. We can design that distinction with swimlanes, where a bordered, titled column can represent each role. Each activity will belong within that columned section, and each transition can go from one role to the other.

![activity-diagram](./images/activity-diagram.png)


### Use case models

After capturing the understanding or the problem domain with activity diagrams, the next step is to understand the the requirements for the system that will be a solution for that domain.

[Use cases](https://en.wikipedia.org/wiki/Use_case_diagram) is a way of capturing functional requirements. It's a way of breaking down the analysis further and starting to think of who does what, defining what the system should do from a user's perspective. During the exploration of the problem domain, we will identify different *actors* - roles or external dependencies - which could be associated with different business events. The same business event can be slightly different for different kinds of users; therefore, these decisions need to be captured.

Use cases focus on user-centered design, and each design is also called a *task*. Use cases represent functional requirements, but non-functional ones are equally important. The non-functional requirements can be captured as well in the form of notes.

We can represent use cases in the form of UML designs, which are simple and intuitive enough to be understood by stakeholders. They can also be represented as textual descriptions that include finer details.

Notable design blocks for use case UML diagrams:

- **Actors**: Different actors are represented by stick figures.
- **Use cases**: The actual use cases are shown as ovals.
- **Associations**: The connections between actors and the use cases are shown as straight lines.
- **System boundary**: This is shown as a solid box encapsulating all the use cases for a particular system, representing the scope of the software solution. Actors are outside of the box.
![Use case diagram](./images/use-case.png)

**Describing use cases**

Use case diagrams alone do not include a lot of details that would need to be taken into consideration when building the software solution. That's why there needs to be some textual description that accompanies the design, describing additional important information.

For example, if the diagram shows an actor and an associated "make reservation" use case, it would be missing important information, such as what the actor needs in order to make a reservation, or what the system needs from the actor.

There is a formal textual representation describing use cases with the following notable sections:

- **Goal**: The purpose of the use case to meet its goal for its associated actor(s).
- **Preconditions**: What needs to hold true before the use case can happen.
- **Postconditions**: What will happen after the use case completes.
- **Main success scenario**: The "happy path" scenario, explains the steps that need to happen for the use case to succeed.
- **Inclusion**: When two or more use cases share a common task, that task can be associated with them via an inclusion association, shown as a dotted line with an arrow and with the *<<include>>* *stereotype*.
- **Extension**: Extensions represent alternative paths to the main success scenario, shown as a dotted line with an arrow and with the *<<extends>>* stereotype. Since extensions indicate alternative paths, a *note* box is also included and connected with a dotted line explaining the condition leading to that extension.

*Example of "make a room reservation" use case:*

**Identifier and name**: UC1 *make reservation*

**Initiator**: Guest or receptionist

**Goal**: A room in the hotel is reserved for a guest

**Preconditions**: None (for this particular use case)

**Postconditions**: A room will have been reserved for the guest for the requested period. The room will no longer be free for that period.

**Assumptions**: The guest or receptionist is using a web browser, and is already known to the system

**Main success scenario**

1. The guest chooses to make a reservation
2. The receptionist selects the desired hotel, dates and room type
3. The system provides the availability and price for the request (An offer is made).
4. The guest accepts the offer
5. The guest provides personal information for the reservation
6. The guest provides payment details
7. The system creates the reservation and gives an identifier
8. The system show the identifier to the guest
9. The system creates a confirmation of the reservation and sends it to the guest.

**Extensions**

3.a. *room not available*

3.a.1 The system offers
alternative dates and type of room

3.a.2 The guest selects the alternative or declines the offer

5.a Guest already on record

5.a.1 Resume at step 6


**Conclusion**

Finally, all the described techniques for domain modeling can be used in parallel and are only tools that help understand the domain and aid communication with the stakeholders. Therefore, each model must be kept simple enough, and if the domain is complex, instead of creating a single complex use case, we can always create smaller, simpler ones.
