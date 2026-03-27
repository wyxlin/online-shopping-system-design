# Design Trade-offs

This document discusses example design trade-offs for an online shopping system.

The goal is not to claim that a full implementation was built, but to show how common architecture choices can be compared at a high level during the design process.

---

## Centralized API Layer vs Microservices

### Example Decision

For a learning-oriented design, it is often easier to start with a centralized API layer rather than a full microservices architecture.

### Trade-off

**Pros:**

- Simpler to understand and document
- Easier to test and reason about at a high level
- Lower operational complexity

**Cons:**

- Less flexible scalability than a well-designed microservices approach
- A single API layer could become a bottleneck as traffic grows

### Rationale

For an early design study or a small-to-medium scale system, a centralized architecture is often easier to explain and maintain conceptually.

---

## Relational Database vs NoSQL

### Example Decision

A relational database is often a reasonable choice for storing users, products, and orders in an online shopping system.

### Trade-off

**Pros:**

- Strong consistency for transactional data
- Well-suited for structured data and clear relationships
- Easier to reason about order and payment records

**Cons:**

- Less schema flexibility than many NoSQL systems
- High read scalability may require additional optimization

### Rationale

Because e-commerce systems often involve transactional records, relational databases are commonly discussed as a suitable option in high-level designs.

---

## Third-party Services vs In-house Implementation

### Example Decision

External services can be used for capabilities such as payment processing, email notifications, and delivery support.

### Trade-off

**Pros:**

- Faster development at a conceptual level
- Leverages specialized external services
- Reduces the need to design every supporting capability from scratch

**Cons:**

- Dependency on external service availability
- Possible latency or integration complexity
- Less control over external systems

### Rationale

In many real-world systems, it makes sense to rely on established providers for supporting functions instead of designing everything internally.

---

## Synchronous vs Asynchronous Processing

### Example Decision

Critical operations such as checkout confirmation are often discussed as synchronous, while non-critical tasks such as email notifications can be treated as asynchronous.

### Trade-off

**Pros:**

- Immediate feedback for user-facing critical actions
- Better user experience for operations like checkout

**Cons:**

- Synchronous operations may increase response time
- Additional design work is needed to avoid blocking or delays

### Rationale

A common design approach is to keep user-critical actions immediate while moving less critical follow-up tasks into asynchronous processing.

---

## Summary

These examples show how system design often involves balancing simplicity, scalability, reliability, and maintainability.

For this study project, the main purpose is to practice thinking through these trade-offs and documenting them clearly.
