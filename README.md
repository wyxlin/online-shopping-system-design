# Online Shopping System Design

A system design case study for a scalable online shopping platform that supports web and mobile clients, secure checkout, and integration with external services such as payment, email, and delivery.

## Overview

This repository presents the high-level design of an online shopping system using the C4 model. It shows how a modern e-commerce platform can be structured to support user-facing applications, backend services, external integrations, and deployment planning.

The project focuses on practical software engineering concerns such as system decomposition, quality attributes, design trade-offs, client-server interaction, and end-to-end business workflows.

## Architecture

The system is documented using three C4 views:

* **System Context Diagram** – shows how users interact with the platform and external systems
* **Container Diagram** – illustrates internal components such as the web app, mobile app, API layer, and database
* **Deployment Diagram** – describes infrastructure and runtime deployment

See [`diagrams/`](./diagrams) for architecture diagrams.

## Key Components

* **Web Application (SPA)** – user interface for browsing products and checkout
* **Mobile Application** – mobile client for accessing the platform
* **API Layer** – handles business logic and client requests
* **Database** – stores users, products, and order data
* **External Services**

  * Payment provider
  * Email service
  * Delivery / logistics system

## Design Documentation

Detailed design documents are available in [`docs/`](./docs):

* [`architecture.md`](./docs/architecture.md) – system structure, core components, and deployment overview
* [`quality-attributes.md`](./docs/quality-attributes.md) – performance, confidentiality, and recoverability requirements
* [`trade-offs.md`](./docs/trade-offs.md) – key engineering decisions and architectural trade-offs

## Example Workflows

Key system behavior is described in [`examples/`](./examples):

* [`checkout-flow.md`](./examples/checkout-flow.md) – end-to-end checkout process
* [`order-lifecycle.md`](./examples/order-lifecycle.md) – order states from creation to completion

## API Design

This project includes lightweight API examples to illustrate client-server interaction.

See [`api/`](./api):

* [`sample-requests.md`](./api/sample-requests.md) – example API requests and responses for products, cart, checkout, and orders

## Repository Structure

```text
online-shopping-system-design/
├── api/         # API interaction examples
├── diagrams/    # C4 architecture diagrams
├── docs/        # Design documentation
├── examples/    # Business workflow examples
└── README.md
```

## Design Goals

* Provide a clear and scalable architecture for an online shopping platform
* Demonstrate integration with external services
* Highlight key quality attributes and engineering trade-offs
* Show how design artifacts connect to business workflows and API interaction

## Purpose

This project is intended to demonstrate system design and software engineering thinking for entry-level software engineering roles, including architectural design, system decomposition, and technical communication.
