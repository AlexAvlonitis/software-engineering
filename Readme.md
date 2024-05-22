# Software Engineering

A summary on how to approach the creation of a software project "by the book", from the initial conception to the actual implementation. Following the [Unified Process (UP)](https://en.wikipedia.org/wiki/Unified_Process) for building object oriented, iterative and incremental enterprise software using [UML](https://en.wikipedia.org/wiki/Unified_Modeling_Language).

**Table of content**
1. [Requirements gathering and domain modelling](#requirements-gathering-and-domain-modelling)
    - [Functional requirements](#functional-requirements)
2. [Analysis](#analysis)
3. [Design](#design)
4. [Implementation](#implementation)
5. [Testing](#testing)
6. [Deployment](#deployment)

## Requirements Gathering and Domain Modelling

To decide what features the software needs, we must gather requirements in collaboration with clients, stakeholders, and other beneficiaries. Requireme/nts describe various aspects of the system, including its behavior, constraints, and other properties.

### Functional Requirements

Functional requirements describe what the product must do, specifying the features needed for a functional product. For example, a system that accepts credit card payments. In contrast, non-functional requirements describe general quality properties of the system, such as usability and performance.

To gather functional requirements, identify the initial high-level use cases of the software. For example, in an online hotel system, use cases could include allowing online booking or online check-in. Functional requirements break down these use cases into smaller units that can be directly implemented and tested, such as enabling a customer to search for available rooms and view details of each room.

Initially, we need to identify core requirements—those with the highest priority for a usable Minimum Viable Product (MVP). To prioritize requirements, the [MoSCoW](https://en.wikipedia.org/wiki/MoSCoW_method) method can be used, labeling requirements as "must have," "should have," "could have," and "won't have."

One way to capture requirements is through user stories, which can be written in this format: As a [role], I want to [feature], so that [reason]. For example, "As a user, I want to be able to do online check-in so that I can save time on arrival."

There are two distinct types of requirements: User and System. User requirements define the product features and can be used to track progress with stakeholders, but they may lack the details needed by developers. System requirements, on the other hand, define the features from a technical perspective, detailing how a feature should be approached, such as "The system shall display available rooms in order from low to high price." However, system requirements should not dictate the specific algorithms or methods developers should use.


### Non Functional Requirements

Non-functional requirements describe the qualities of that the system should have, such as being secure, reliable, fast etc...
An alternative way to think of non-functional requirements would be as constraints of the functional ones. For example a functional requirement would be to allow customer to check-in and the non-functional would be, for this action to complete within 1 second.

A list of non-functional requirements exists to help with choosing what needs to be taken into account when building a project:

**Look-and-feel requirements** is about the general style of the interface. For example: The product shall use only two colours.

**Usability and humanity requirements** measure how easy can users perform tasks with minimal errors, in terms of intuitive user interface. For example: The system should comply with the Disability Discrimination Act, or it should be possible to pay in different currencies.

**Performance requirements** measure how fast, safe, accurate, available and reliable all the functionality would be. For example: the product shall handle 10 concurrent users, or the product shall complete the check-in of a user within 1 second.

**Operational and environmental requirements** measure the environment the product should operate under, could be underwater or on top of a mountain, or any other extreme environment and also the installation requirements. For example: The product shall be usable in up to x meters below the sea level or the product will need to be installed in 100 locations in all the continents within 1 month by 10 semi-skilled workers.

**Maintainability and support requirements** specify how easy a product can change and the time it takes to apply them. For example: The product shall be operatable in operating systems used in our remote branch, or the product shall comply with any new law requirements occuring about every 6 months.

**Cultural requirements** specify the appropriate tone and formalities of the interface depending the region the product operates on. For example: The pictures shown for the UAE region should not show any exposed bodies.

**Legal requirements** specify all the law requiremnts the product must comply with. Such as country specific regulations, such as [EU GDPR](https://en.wikipedia.org/wiki/General_Data_Protection_Regulation) and any other product specific regulations that should apply for that country, for example a medical product should not sell products to people under 18 years old. These requirements should be consulted by specialised lawyers.

**Security requirements** specify simply specify the security and confedentiality of the product. Reminder, that requirements do not specify exact technologies and specific implementations, but rather the general idea we need to take to secure our product. Security requirements can be broken down to different categories to help us cover all aspects of it, such as:

  * *Access*: Authorised users can access their data

  * *Privacy*: Authorised users can view only their data and noone else's.

  * *Integrity*: Data does not get corrupted

  * *Audit*: Any chosen action can be traced back for analysis

  * *Immunity*: The product is protected against hacking attacks.

## Analysis

## Design

## Implementation

## Testing

## Deployment
