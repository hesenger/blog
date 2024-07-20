---
title: Are we writing good tests?
description: A rant about my journey through Acceptance Tests and TDD
date: 2022-11-08
tags:
  - tests
  - tdd
  - acceptance tests
  - rant
---

![[are-we-writing-good-tests.webp]]

In the past few years I became more and more addicted by tests. In the first stage of this disease I remember try to test every single happy and unhappy path of a flow, reach 100% code coverage, running tests against real databases and so on. For sure, it is not ideal and I totally understand the reason today.

Although I was very excited with writing tests and see all the "passes" in the CI, I have not stopped to search for more resources and examples, and one day I came across an article about TDD. I don't recall the exact article and it was not the first time I heard about the topic but that time I was bite.

> I finally landed at a company with everything in place: large code base extensively tested, unit, e2e, integration tests and all sort of those running in the CI for every PR, a dream for my old myself

At that point I was not ready to put TDD in practice, or at least I thought I wasn't, so my journey increasing test coverage and writing as much tests I can to cover edge cases have continued, specially in two occasions where I was leading teams and pushed so hard in that direction. The time goes on and I finally landed at a company with everything in place: large code base extensively tested, unit, e2e, integration tests and all sort of those running in the CI for every PR, a dream for my old myself.

It's not hard to foresee how a large code base, with hundred of developers individually testing each component becomes hard to maintain. Every single change requires fixes in many tests and this started to bother me. Specially in cases where you are working in a new feature, it's supposed you don't need to fix old tests since you are not breaking existing behavior, but this is not what happens in fact.

I came across TDD again, quickly I noticed that we were writing bad tests, tests too tightly coupled to the implementation instead to the behavior. It was not uncommon to have 3 or 4 layers of mocks when writing tests, and now I know that this is result of a bad design, a design without tests in mind, which results in bad components very tangled, in fact it is not a problem with tests but with bad production code.

> we were writing bad tests, tests too tightly coupled to the implementation instead to the behavior […] in fact it is not a problem with tests but with bad production code

**Does TDD lead to good design? Yes, it does. It certainly does because it's impossible to write tangled code, coupled components when you start with tests, and it is due to a simple premisse, we do not write production code hard to test when starting from tests.**

It's just a rant for sure, but I feel like my journey through the Acceptance Tests and TDD is just starting, and to be honest I'm very excited with all of this 😅

References:

- [Continuous Delivery](https://www.youtube.com/channel/UCCfqyGl3nq_V0bo64CjZh8g) — Awesome channel by Dave Farley;

- [Does TDD really lead to good design](https://www.codurance.com/publications/videos/2015-10-03-does-tdd-really-lead-to-good-design);

- Too many others to mention, hopefully I can come back here to do it in follow up rants.
