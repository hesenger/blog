---
title: NSequence
date: 2024-01-10
tags:
  - hilo
  - dotnet
  - sequence-generator
---

![[nsequence.webp]]

The first version of NSequence, a simple yet powerful HiLo sequence generator suited for dotnet, was released today. NSequence, designed with simplicity in mind, provides an easy way to generate unique IDs for business items within your applications. What distinguishes this project is its user-friendliness, as it offers a public static method for easy integration, making it a viable option for developers that prefer a clear solution over dependency injection.

In the future, the NSequence package will be smoothly integrated into EventPulse examples. EventPulse is a side project that aims to simplify event sourcing without requiring changes in business classes. We can construct unique identifiers using sequential integers by introducing NSequence into EventPulse use, but with the same practical method that “Guid.NewGuid()” provides.

Nuget Package: https://www.nuget.org/packages/NSequence
Repository: https://github.com/hesenger/NSequence
