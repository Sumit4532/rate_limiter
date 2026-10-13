# Rate Limiter — Low-Level Design in Java
A Java-based Rate Limiter project demonstrating object-oriented design, multiple rate-limiting algorithms, user-tier-based limits, and concurrent request handling.


## Features

- Implements multiple rate-limiting algorithms:
  - Token Bucket
  - Fixed Window
  - Sliding Window Log
- Uses a factory to create rate-limiter implementations.
- Centralized `RateLimiterService` to process requests.
- Supports `FREE` and `PREMIUM` user tiers with different rate limits.
- Demonstrates concurrent requests using Java concurrency utilities.

## Design Overview

### 1. RateLimiterService
Coordinates rate-limit checks and manages the rate-limiter configuration.

### 2. RateLimiterFactory
Creates the appropriate rate-limiter implementation based on the selected algorithm.

### 3. Rate-Limiting Algorithms
Each algorithm encapsulates its own request-allowance logic.

### 4. User Tiers
`FREE` and `PREMIUM` users can have different request limits and time windows.

## Example Configuration

The example demonstrates:

- FREE users: 10 requests per 60 seconds.
- PREMIUM users: 100 requests per 60 seconds.
- Concurrent requests for the same user to demonstrate rate-limit behaviour.

Actual results may vary depending on concurrent execution.

## How to Run

1. Clone the repository:

2. Open the project in a Java IDE.
3. Configure a compatible JDK.
4. Run `Main.java` to execute the examples.

## Concepts Demonstrated

- Object-Oriented Programming
- Abstraction and Encapsulation
- Factory Design Pattern
- Extensible class design
- Concurrency and synchronization concepts
- Rate-limiting algorithm trade-offs

## Future Improvements

- Add unit tests for algorithm boundaries.
- Add more concurrency tests.
- Implement Sliding Window Counter.
- Add a REST API using Spring Boot.
- Build an interactive web interface to visualize allowed and rejected requests.
- Add Maven or Gradle build configuration.

## Scope

This project focuses on Low-Level Design and rate-limiting algorithms. Distributed rate limiting and production deployment are outside the current scope unless implemented separately.
