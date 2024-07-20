---
title: How we turned old legacy code into shiny well tested code.
date: 2023-03-11
---

Modernizing an old legacy system can be a daunting task for any software development team. One of the biggest challenges is to make changes without disrupting the existing system, which is often complex and difficult to understand. In this article, we will explain how we turned an old 10-year legacy system into a shiny new code by keeping all the data structure intact and writing executable specifications.

![[turning-legacy-into-well-tested-code.webp]]

The legacy system we were tasked to modernize was a C# application with zero test coverage. The first step we took was to copy the entities’ definition, following the exact same data structure defined in the original system. These classes were placed in the “core” or “business” layer, without any logic initially.

Next, we created an application layer and wrote the first specification. We created a simple class called SUT (System Under Test) that mocked the repo interfaces. At this point, the repos were nothing other than simply interfaces defined in the business layer. We wrote the first use case, which was a simple operation depending on three other entities in the system. We created the entities without any constructor or validation, so mocking them and adding to a simple Collection based repo mock was very easy.

> This approach allowed us to quickly iterate and improve the system while ensuring that the changes didn’t break any existing functionality

Writing executable specifications was key to our approach. We wanted to ensure that the system was tested thoroughly while making changes. Instead of writing traditional documentation, we created executable specifications that would test the code. This approach allowed us to quickly iterate and improve the system while ensuring that the changes didn’t break any existing functionality.

As we progressed, we replaced the old logic in the controllers with the new libraries. We created a rudimentary feature flag system and added a guard to the old controllers. Then we added each new use case to be called when the individual feature flag was turned ON. We encountered a few failures, but they were not a cause for worry. We simply turned off the feature, wrote a new specification for the failure case, and fixed it. After the next deployment, all we needed to do was turn the feature flag back ON.

At this point, we had rewritten 70% of the code, with a coverage above 90%. The features introduced to the system since then have been smooth, as we would expect from a well-tested system. Even coming from a zero-coverage codebase, we were able to create a well-tested and reliable system by writing executable specifications.

Modernizing an old legacy system can be a challenging task, but with the right approach, it can be done smoothly. Our approach of keeping all the data structure intact, writing executable specifications, and adding features through feature flags proved to be effective. We were able to rewrite most of the code, increase test coverage to over 90%, and introduce new features to the system without causing any disruption.
