# Event-sourcing
# Event Sourcing Architecture

*  Event Sourcing Architecture an application it state are stored as a series of events 

* We can always reply event to get the state at any point of time
best example of this is-  git commit

* Everything that happens to our system from the inside and from the outside is actually an atomic action

 * Event sourcing involves modeling the state changes made by applications as an immutable sequence

* Event sourcing as an application architecture pattern is rising in popularity.

## Benfit of Event Sourcing Architecture
_____
 * It is Low cost flexibility in changing data models<br>
 * It is enables statistics for the  isolation between  services and domains<br>
 * It is future-proof for use cases<br>
 * It is application changes
___
## How to use event source
____
* First we create then insert ofter that read and then delete we can not update .
* For very large objects/streams, consider using a consumer to store point in time state in another solution to eliminate the need for repeated and costly “replays”.
 * It is use to To determine current state, replay a series of events.  Think “blockchain”.
 _____
 ## Architecture of event sourcing
 _____
 * We are going to Design our e-commerce Architecture with applying Event Sourcing architecture<br>
 <br>
 <br>
 * Now We can Design our Ordering microservices databases
 <br>
 * I write database for relational concerns<br>
 * I read database for querying concerns<br>
 When user create or update an order, I am going to use relational write database, and when user query order or order history, I am going to use no-sql read database. and make consistent them when syncing 2 databases with using message broker system with applying publish.<br>
 ______
 *The following diagram illustrates how the seat reservation subsystem of the conference management system might be implemented using event sourcing.

 ## Advantages of Event Sourcing
 ___
 * It is follow CRUD (create,read,updata,delete) rule.<br>
 * Event Sourcing is one of the patterns that enables concurrent, distributed systems to achieve high performance, scalability and resilience.<br>
 * Event-sourced systems are easy to test and debug. Commands and events can be simulated for test purposes.<br>
 * we can add new views on our system’s activity without making the write-side more complicated<br>
 ____
## Disadvantage of Event Sourcing<br>
_____
* It is very complex like that some programming languages like Scala have very rich collection library that is very flexible to produce some seriously complex<br>
* It is take High disk space usage <br>
* Event stores store events as serialized objects which means we can't query the content of events in the event store which is discouraged anyway
* It is follow Longer bootup time.
___
## Why we use event sourcing
___
* It is represent how we think about any situation<br>
* is removed from a user's cart? Simply count the EventRemovedFromCart events.<br>
* We can generate an audit log that shows exactly how a system got into a state.<br>
____
 ## Refrences
 [Microsoft Documentation](https://docs.microsoft.com/en-us/azure/architecture/patterns/event-sourcing)
