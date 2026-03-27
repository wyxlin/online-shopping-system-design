# Quality Attributes

This document discusses example quality attributes for an online shopping system design study.

The goal is to show how non-functional requirements can be described using simple scenario-based analysis. These examples are for learning purposes and help illustrate how system quality can influence design decisions.

---

## Performance

### Scenario

- **Stimulus Source:** Multiple concurrent users
- **Stimulus:** Users browse products and perform checkout-related actions at the same time
- **Environment:** Normal and peak usage conditions
- **Response:** The system should respond within an acceptable amount of time
- **Response Measure:** Average response time remains within a few seconds for common operations

### Design Considerations

Possible design considerations for performance include:

- Efficient handling of concurrent requests at the API layer
- Reasonable database query design for product and order data
- Potential use of caching for frequently accessed data such as product catalog information

---

## Confidentiality

### Scenario

- **Stimulus Source:** External users or malicious actors
- **Stimulus:** Attempts to access sensitive user data without authorization
- **Environment:** During normal system operation
- **Response:** The system should protect sensitive information and prevent unauthorized access
- **Response Measure:** No confidential data is exposed

### Design Considerations

Possible design considerations for confidentiality include:

- Secure communication using HTTPS
- Authentication and authorization mechanisms
- Protection of sensitive data such as user credentials and payment-related information

---

## Recoverability

### Scenario

- **Stimulus Source:** System failure, such as a server crash or network outage
- **Stimulus:** Part of the system becomes unavailable
- **Environment:** During runtime
- **Response:** The system should recover within a reasonable amount of time and preserve important data
- **Response Measure:** Service is restored without major data loss

### Design Considerations

Possible design considerations for recoverability include:

- Backup and recovery strategies
- Database replication as a possible reliability measure
- Service restart or failover planning to reduce downtime

---

## Summary

These quality attributes help frame high-level design thinking for an online shopping system.

In a learning project like this, the main value is understanding how performance, security, and recoverability can shape architecture decisions.
