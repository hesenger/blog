---
title: "Don’t Jump the Gun: Understanding DDD Before Applying CQRS"
date: 2023-04-05
tags:
  - ddd
  - cqrs
---

Modern software development frequently uses the architectural design pattern known as Command Query Responsibility Segregation (CQRS), which divides a system’s commands (write actions) and queries (read operations).

Software development using the DDD methodology places a strong emphasis on the value of modeling the business domain within the system.

![[ddd-cqrs.webp]]

Developers run the danger of building an unnecessarily complex system that is hard to comprehend and manage when they attempt to deploy CQRS from scratch without understanding DDD. CQRS is not a panacea, and it shouldn’t be used without taking into account the particular needs of the business domain.

One of the key advantages of CQRS is that it enables programmers to separately optimize a system’s read and write pathways. This enables read-heavy systems to scale separately from write-heavy systems, enhancing efficiency and cutting costs. Yet in order to achieve this separation, a well-designed domain layer is necessary, which can be extremely difficult without a firm grasp of DDD.

> it needs to have closed boundaries which aims to hide objects from the surface — so how to list entities that are not even exposed by their aggregate root?

A well-designed domain layer is usually a bad readable model, though. It's inherently to the way we plan it: it needs to have closed boundaries which aims to hide objects from the surface — so how to list entities that are not even exposed by their aggregate root?

Although the domain layer’s goal is to provide a clear separation of concerns and a representation of the business domain, this does not always convert into a user-friendly interface or a model that non-technical stakeholders can easily grasp.

This issue is resolved by CQRS, which separates read and write processes so that programmers can separately optimize each. This means that although the write model can be tuned for speed and consistency, the read model can be created expressly for simple consumption by users or other systems.

As a result, even while CQRS is a powerful design that can considerably help software systems, it shouldn’t be implemented randomly without a solid understanding of DDD.
