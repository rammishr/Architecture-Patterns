# Circuit Breaker Pattern

## Introduction
The Circuit Breaker pattern is a design pattern that helps to manage failures and improve the resilience of distributed systems. It provides a way to detect and handle failures in a controlled manner, by isolating the faulty system component and preventing cascading failures.

## Problem
In a distributed system, calls to remote services or APIs can fail for various reasons such as network issues, service unavailability, or other errors. When a remote service fails, it can lead to a cascading failure, where the calling service also fails, leading to more failures in other services. This can cause a complete system outage and affect the end-user experience.

## Solution
The Circuit Breaker pattern provides a solution to this problem by introducing a middleware component between the caller and the remote service. This middleware component is responsible for monitoring the remote service and detecting failures. When a certain number of failures occur, the middleware "trips" the circuit, preventing any further calls to the remote service. The middleware can also provide a fallback mechanism, such as returning cached data or providing a default response.

    There are popular open-source libraries, like Netflix’s Hystrix or Reselience4J, that can be used to implement this pattern very easily.    
More detail about Hystrix can be found at [How-it-Works](https://github.com/Netflix/Hystrix/wiki/How-it-Works).

The Circuit Breaker pattern typically involves three states:
- **Closed state**: In this state, the circuit is closed and calls to the remote service are allowed to pass through the middleware.
- **Open state**: When a certain number of failures occur, the circuit "trips" and enters the open state. In this state, all calls to the remote service are blocked and a fallback mechanism is used instead.
- **Half-open state**: After a certain amount of time has passed, the circuit enters the half-open state. In this state, a limited number of requests are allowed to pass through to the remote service to test if it has recovered. If the test is successful, the circuit returns to the closed state. Otherwise, it returns to the open state.
<img width="370" alt="image" src="https://user-images.githubusercontent.com/43367262/235586000-ad29abbe-57e1-49fb-9e07-2d999a8815e0.png">

## Example
A detailed working example can be found at https://howtodoinjava.com/spring-cloud/spring-hystrix-circuit-breaker-tutorial/. 
Sample working files compressed as zip can be found in this folder.

## Benefits
The Circuit Breaker pattern provides several benefits:
- Improved resilience: By isolating failures and preventing cascading failures, the Circuit Breaker pattern improves the resilience of distributed systems.
- Graceful degradation: The Circuit Breaker pattern provides a fallback mechanism for handling



