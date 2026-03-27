# Quality Attributes

This document defines the key quality attributes of the online shopping system, including performance, confidentiality, and recoverability. Each attribute is described using scenario-based analysis.

---

## Performance

### Scenario

* **Stimulus Source**: Multiple concurrent users
* **Stimulus**: Users browse products and perform checkout operations simultaneously
* **Environment**: Normal and peak usage conditions
* **Response**: The system processes requests within acceptable response time
* **Response Measure**: Average response time remains within a few seconds

### Design Considerations

* Efficient handling of concurrent requests at the API layer
* Optimized database queries for product and order data
* Potential use of caching for frequently accessed data (e.g., product catalog)

---

## Confidentiality

### Scenario

* **Stimulus Source**: External users or malicious actors
* **Stimulus**: Attempts to access or intercept sensitive user data
* **Environment**: During normal system operation
* **Response**: The system prevents unauthorized access and protects sensitive data
* **Response Measure**: No exposure of confidential information

### Design Considerations

* Secure communication using HTTPS
* Authentication and authorization mechanisms
* Protection of sensitive data such as user credentials and payment information

---

## Recoverability

### Scenario

* **Stimulus Source**: System failure (e.g., server crash, network outage)
* **Stimulus**: The system becomes partially or fully unavailable
* **Environment**: During runtime
* **Response**: The system recovers within a defined time without data loss
* **Response Measure**: System is restored within minutes and data integrity is preserved

### Design Considerations

* Database replication (primary-secondary setup)
* Backup and recovery strategies
* Ability to restart services with minimal downtime

---

## Summary

These quality attributes guide the design decisions of the system and ensure that it meets essential requirements for performance, security, and reliability.
