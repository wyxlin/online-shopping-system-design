# Order Lifecycle Example

This document illustrates an example order lifecycle in an online shopping system.

The goal is to show how an order might move through different states from creation to completion. This document is for learning and documentation purposes only.

---

## Overview

In a typical online shopping system, an order may go through several states during its lifecycle.

A simplified example includes:

- `CREATED`
- `PAID`
- `PROCESSING`
- `SHIPPED`
- `DELIVERED`
- `CANCELLED`

The exact states can vary depending on the business model and system design.

---

## Example State Transitions

### 1. CREATED

This is the initial state after the user submits an order and the order record is created.

At this stage:
- The order exists in the system
- Payment may still be pending
- Inventory may not yet be finalized

---

### 2. PAID

If payment succeeds, the order may move to the `PAID` state.

At this stage:
- Payment has been confirmed
- The order is ready for internal processing

---

### 3. PROCESSING

After payment confirmation, the order may move into a processing stage.

This can represent activities such as:
- Inventory confirmation
- Picking and packing
- Preparing the shipment

---

### 4. SHIPPED

Once the package has been handed off to a delivery provider, the order may move to `SHIPPED`.

At this stage:
- A tracking number may be available
- The user may receive a shipping notification

---

### 5. DELIVERED

When the package reaches the customer, the order may be marked as `DELIVERED`.

This usually indicates that the main order flow has been completed.

---

### 6. CANCELLED

In some cases, an order may move to `CANCELLED`.

Possible reasons include:
- User cancellation
- Payment failure
- Inventory shortage
- Operational issues

A cancelled order would typically stop moving through the normal fulfillment flow.

---

## Example Transition Paths

Some possible lifecycle paths include:

- `CREATED → PAID → PROCESSING → SHIPPED → DELIVERED`
- `CREATED → CANCELLED`
- `CREATED → PAID → CANCELLED`

These are simplified examples used to illustrate order state changes.

---

## Design Considerations

When documenting an order lifecycle, common design considerations may include:

- Which states are needed
- When state transitions are allowed
- How failures or cancellations are handled
- How users are informed of status changes

---

## Summary

This example provides a simplified view of how an order lifecycle can be documented in a system design project.

The main purpose is to practice describing state transitions clearly at a high level.
