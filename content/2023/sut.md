---
title: SUT
date: 2023-03-13
tags:
  - tdd
  - legacy-code
  - code-coverage
---

In a previous article I mentioned how SUT class helped us to rebuild the application and business…

This is not a easy work at all, and many other practices like Feature Flags could be mentioned here as very important in the process but I'd like to dig a bit in this specific topic and focus this article in the SUT class.

To address this challenge, one effective approach is to use a System Under Test (SUT) class to abstract the implementation details and build more resilient tests that will still pass when implementation changes. In this article, we will discuss what an SUT class is, why it is useful, and how to use it to build more resilient tests.

![[sut.webp]]

## What is an SUT Class?

An SUT class, or System Under Test class, is a class that represents the system being tested. It provides an interface through which the test code can interact with the system being tested, without having to know the details of the implementation.

In other words, an SUT class is a way to abstract the implementation details of the system being tested and provide a clear and simple interface for testing.

## Why is an SUT Class Useful?

There are several reasons why an SUT class is useful for testing:

## 1. It abstracts the implementation details.

An SUT class abstracts the implementation details of the system being tested. This means that the test code does not need to know how the system works internally, which makes it easier to write and maintain tests.

## 2. It provides a clear and simple interface for testing.

An SUT class provides a clear and simple interface for testing. This means that the test code can focus on testing the behavior of the system, rather than worrying about the implementation details.

## 3. It makes tests more resilient to changes in implementation.

An SUT class makes tests more resilient to changes in implementation. Because the test code interacts with the system through the SUT class, changes to the implementation of the system are less likely to break the tests.

## How to Use an SUT Class to Build Resilient Tests

To use an SUT class to build more resilient tests, follow these steps:

## 1. Define the SUT class.

Define the SUT class to represent the system being tested. The SUT class should provide an interface for the test code to interact with the system, without exposing the implementation details.

## 2. Write tests using the SUT class.

Write the tests using the SUT class. The test code should interact with the system through the SUT class, using the interface provided by the class.

## 3. Test the behavior of the system, not the implementation.

Test the behavior of the system, not the implementation. This means that the test code should focus on what the system does, rather than how it does it.

## 4. Keep the SUT class up-to-date with changes in implementation.

Keep the SUT class up-to-date with changes in implementation. If the implementation of the system changes, update the SUT class to reflect the changes. This will ensure that the tests continue to pass, even when the implementation changes.

## 5. Refactor the SUT class if necessary.

Refactor the SUT class if necessary. If the SUT class becomes too complex or difficult to maintain, consider refactoring it to simplify the interface or break it down into smaller, more manageable classes.

## Conclusion

Using an SUT class to abstract the implementation details of a system can help build more resilient tests that are less likely to break when the implementation changes. By providing a clear and simple interface for testing, an SUT class allows the test code to focus on testing the behavior of the system, rather than worrying about how it works internally.

To use an SUT class effectively, define the class to represent the system being tested, write tests using the class, focus on testing the behavior
