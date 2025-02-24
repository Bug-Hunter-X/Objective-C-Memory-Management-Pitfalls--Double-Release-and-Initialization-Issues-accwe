# Objective-C Memory Management Pitfalls

This repository demonstrates two common, yet subtle, memory management issues in Objective-C that can lead to crashes and unexpected application behavior.

## Issues Demonstrated

1. **Double Release:** The `bug.m` file shows a scenario where improper handling of `retain` and `release` within a setter method can result in a double release of an object, leading to application crashes.  This is exacerbated in multithreaded environments.

2. **Initialization Issues:** Incorrect use of `self` during initialization can cause objects to be released prematurely or create retain cycles, hindering garbage collection.

## Solutions

The `bugSolution.m` file provides solutions to the demonstrated issues by using modern memory management techniques and best practices, such as avoiding manual `retain`/`release` and using `nonatomic, strong` properties wherever possible.