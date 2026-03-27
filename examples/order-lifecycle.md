# Order Lifecycle

This document describes the lifecycle of an order in the online shopping system, from creation to final delivery and completion.

## Overview

An order progresses through multiple states after a successful checkout. These states reflect the order’s processing status across payment, fulfillment, and delivery.

---

## Order States

An order can move through the following states:

1. **Created**

   * The order is created after successful payment.
   * Order details are stored in the database.

2. **Confirmed**

   * The system confirms that the order has been successfully recorded.
   * A confirmation email is sent to the customer.

3. **Processing**

   * The system prepares the order for shipment.
   * This may include packaging and internal handling.

4. **Shipped**

   * The order is handed over to the delivery or logistics provider.
   * A tracking number may be generated.

5. **Delivered**

   * The order is delivered to the customer’s address.

6. **Completed**

   * The order is marked as completed after successful delivery.
   * The system may trigger post-delivery processes (e.g., feedback request).

---

## State Transitions

* Created → Confirmed → Processing → Shipped → Delivered → Completed

Each transition represents a change in the order’s status and may trigger additional system actions.

---

## Failure Scenarios

### Payment Failure

* If payment fails, the order is not created and no lifecycle begins.

### Delivery Failure

* If delivery fails, the order may be marked as failed or returned.
* The system may allow re-delivery or refund processing.

### System Failure

* If a failure occurs during processing, the system should be able to resume from the last known state.

---

## Design Considerations

* Order state transitions should be clearly defined and stored persistently.
* The system should support tracking and querying order status at any time.
* External services (e.g., delivery providers) may affect state transitions.
* The system should ensure consistency between order status and actual delivery progress.

---

## Future Improvements

* Introduce event-driven architecture for order state transitions
* Add real-time tracking updates for users
* Support order cancellation and refund workflows
