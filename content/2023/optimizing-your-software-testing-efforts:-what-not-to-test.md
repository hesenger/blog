---
title: Optimizing Your Software Testing Efforts: what not to test?
---

![[optimizing-your-software-testing-efforts.webp]]

Testing is an essential part of software development, and it is crucial to ensure that the code being developed is functional and reliable. While testing is important, it is equally important to focus on what to test and what not to test. Testing every single component of a software system can be time-consuming, expensive, and unnecessary. In this article, we will discuss why it is not necessary to test 3rd party libraries, implementation details, and system calls.

## Third-Party Libraries

Third-party libraries are often used in software development to save time and effort. These libraries are developed by other developers and are designed to perform specific functions. For example, a web developer may use a third-party library for managing forms, or a mobile app developer may use a third-party library for displaying ads. These libraries are usually well-tested and have been used by many other developers before.

When it comes to testing, it is not necessary to test third-party libraries. These libraries are already tested by the developers who created them, and they are also used by many other developers in their projects. It is unlikely that there are any significant bugs or issues with these libraries. However, it is important to ensure that the library is compatible with the software system being developed. This can be done by testing the integration of the library with the system.

## Implementation Details

Implementation details are the internal workings of the software system. These details include things like the data structures used, the algorithms used, and the code optimization techniques used. These details are not visible to the end-users of the software, and they do not affect the functionality of the software system.

It is not necessary to test implementation details because they do not affect the functionality of the software system. However, it is important to ensure that the implementation details are correct and efficient. This can be done through code reviews and other techniques.

## System Calls

System calls are the interface between the software system and the operating system. System calls are used to perform operations such as file I/O, process management, and memory allocation. System calls are essential for the functioning of the software system, but they are not part of the software system itself.

It is not necessary to test system calls because they are part of the operating system and are already tested by the developers of the operating system. However, it is important to ensure that the software system is using the system calls correctly and efficiently. This can be done through code reviews and other techniques.

In conclusion, testing is an essential part of software development, but it is important to focus on what to test and what not to test. Third-party libraries, implementation details, and system calls do not need to be tested extensively, as they are already well-tested and do not affect the functionality of the software system. Instead, it is important to focus on testing the integration of these components with the software system and ensuring that they are being used correctly and efficiently.
