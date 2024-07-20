---
title: Uncovering the Essence of Event Sourcing in Everyday Systems
date: 2024-01-09
---

![[uncovering-event-sourcing.webp]]

The idea of “event sourcing” has long felt very complicated to many in the software development industry. For many, it could seem like a paradigm change, but in reality, most systems are far closer to Event Sourcing than they may think.

CRUD operations are frequently used in traditional systems to handle data. Beneath the surface, though, these systems can be thought of as being predicated on estimates produced by the event sourcing pattern. To put it another way, instead of keeping the events themselves, CRUD-based systems retain their consequences, like a change in state or an action. On the other hand, event sourcing promotes the archiving of real-world occurrences, offering a chronological account of activities.

> For many, it could seem like a paradigm change, but in reality, most systems are far closer to Event Sourcing than they may think.

Developers can use pre-existing systems and make little changes to the persistence layer to implement Event Sourcing. The system may recreate the exact same records in the CRUD tables using the stored events, as opposed to storing the resultant state directly. This method permits a more accurate portrayal of the system’s history in addition to offering a more thorough audit trail.

This method’s flexibility is what makes it so great — it lets developers gradually implement Event Sourcing ideas. Developers can progressively move from a CRUD-centric approach to one based on the concepts of Event Sourcing by incorporating event storage into an existing system.

However, there appears to be a disconnect between the ideal scenario suggested by classic Domain-Driven Design (DDD) and the implementation of commonly used Event Sourcing frameworks. DDD advises separating any persistence-related issues from the domain layer to provide a clear and manageable architecture.

Many event sourcing frameworks are not up to par with this goal in practice. Developers are often obliged to adopt a less elegant solution, inheriting and contaminating the domain layer with event persistence architecture. This tampers with the domain layer’s purity, raising a number of issues that may impede code clarity and maintainability.

To summarize, event sourcing is not a strange notion to developers working with CRUD-based systems. Recognizing the value of recording events rather than merely their effects allows for a more realistic representation of system history. It's critical to be aware of potential flaws in widely used frameworks, which may need a compromise in the separation of concerns advocated by basic DDD. The ability to strike the proper balance between historical accuracy and clean design will surely determine the future of event-driven programming.
