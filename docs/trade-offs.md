# Design Trade-offs

This document outlines the key design trade-offs made in the architecture of the online shopping system.

---

## Monolithic API vs Microservices

### Decision

The system uses a centralized API layer instead of a microservices architecture.

### Trade-off

* **Pros**:

  * Simpler development and deployment
  * Easier debugging and testing
  * Lower operational complexity

* **Cons**:

  * Limited scalability compared to microservices
  * Potential bottleneck at the API layer as traffic grows

### Rationale

For an initial system or small-to-medium scale platform, a centralized architecture provides faster development and easier maintenance.

---

## Relational Database vs NoSQL

### Decision

The system uses a relational database for storing users, products, and orders.

### Trade-off

* **Pros**:

  * Strong consistency for transactions
  * Well-suited for structured data and relationships
  * Reliable for order and payment records

* **Cons**:

  * Less flexible schema compared to NoSQL
  * May require optimization for high read scalability

### Rationale

E-commerce systems require strong consistency for orders and payments, making relational databases a suitable choice.

---

## Third-party Services vs In-house Implementation

### Decision

The system integrates with external services for payment, email, and delivery.

### Trade-off

* **Pros**:

  * Faster development and time-to-market
  * Leverages specialized, reliable services
  * Reduces internal implementation complexity

* **Cons**:

  * Dependency on external service availability
  * Potential latency and integration issues
  * Less control over external systems

### Rationale

Using third-party services allows the system to focus on core business logic while relying on mature solutions for supporting functionality.

---

## Synchronous vs Asynchronous Processing

### Decision

Core operations (e.g., checkout and payment) are handled synchronously, while non-critical tasks (e.g., email notifications) can be asynchronous.

### Trade-off

* **Pros**:

  * Immediate feedback for critical operations
  * Better user experience during checkout

* **Cons**:

  * Increased response time for synchronous operations
  * Requires careful design to avoid blocking

### Rationale

Critical operations must provide immediate results, while non-critical tasks can be decoupled to improve system performance.

---

## Summary

These trade-offs reflect a balance between simplicity, performance, reliability, and scalability. The design prioritizes maintainability and rapid development while allowing room for future evolution.
