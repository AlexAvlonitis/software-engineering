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

Functional requirements describe what the product does, specifying the user features needed for a functional product. For example, a system that accepts credit card payments. In contrast, non-functional requirements describe general quality properties of the system, such as usability and performance.

To gather functional requirements, identify the initial high-level use cases of the software. For example, in an online hotel system, use cases could include allowing online booking or online check-in. Functional requirements break down these use cases into smaller units that can be directly implemented and tested, such as enabling a customer to search for available rooms and view details of each room.

Initially, we need to identify core requirements—those with the highest priority for a usable Minimum Viable Product (MVP). To prioritize requirements, the [MoSCoW](https://en.wikipedia.org/wiki/MoSCoW_method) method can be used, labeling requirements as "must have," "should have," "could have," and "won't have."

One way to capture requirements is through user stories, which can be written in this format: As a [role], I want to [feature], so that [reason]. For example, "As a user, I want to be able to do online check-in so that I can save time on arrival."

There are two distinct types of requirements: User and System. User requirements define the product features and can be used to track progress with stakeholders, but they may lack the details needed by developers. System requirements, on the other hand, define the features from a technical perspective, detailing how a feature should be approached, such as "The system shall display available rooms in order from low to high price." However, system requirements should not dictate the specific algorithms or methods developers should use.

## Analysis

## Design

## Implementation

## Testing

## Deployment
