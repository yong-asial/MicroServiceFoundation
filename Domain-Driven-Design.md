# Domain-Driven Design

- If you don't need independent deployability, there is no real reason to go to microservices. If you don't need it, maybe just do DDD in monoliths.

## Bounded Contexts and Entities

- Keep everything context-sensitive and specific
- In the case of bookstore application where we have two context/entities - store for selling book and warehouse for shipping book, instead of having one large Product entity/table, we would have two separate Product table in different databases for each context.

## Orchestrated/Declarative System

![Declarative](./images/Declarative-1.png)

- Synchrounous Services
- One entity tells another entity what to do
- Have a tight relationship between services. Change one service will affect another as it communicate directly.

![Declarative](./images/Declarative-2.png)

## Choreography/Reactive System

- Asynchronous Services
- Eliminates coupling relationships between downstream and upstream services
- Also called a publish-subscribe model. Subscribers are unknown to the publishers. Use a messaging system such as - kafka, rabbitmq, zeromq

![Reactive](./images/Reactive.png)

## Event Storming

- Used to analyze the domain/business
- Used to develop code that is modeling the business
- Collaborative technique with business people
- Design a system that models the structure and flow of activies within the business

### Design

- Focus on a specific story
- Model that part of the system to implement that story
- Get feedback, come back, and extend or move to another events

### Demo

- Create Events, Actions
- Entities (Person): Who do the action
- Context: Domain and businss context
- Context Maps: Show all the bound context in the system
- Entity Maps: Identify classes (services/entities) -> responsibilities -> collaborators. Show all entities in system. relationships by means of event system.
