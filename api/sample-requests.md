# API Examples

This document provides example API requests and responses for an online shopping system.

The purpose of these examples is to illustrate how a client might interact with a backend system. These APIs are not implemented and are for learning and documentation purposes only.

---

## Overview

The examples below show how common operations in an online shopping system could be represented using REST-style APIs.

They are simplified and intended to demonstrate structure rather than full implementation.

---

## 1. Get Products

### Request

```http
GET /api/products
```

### Example Response

```json
[
  {
    "id": "p001",
    "name": "Wireless Mouse",
    "price": 25.99
  },
  {
    "id": "p002",
    "name": "Mechanical Keyboard",
    "price": 79.99
  }
]
```

This example shows how a client might request a list of products.

---

## 2. Add Item to Cart

### Request

```http
POST /api/cart
```

### Example Body

```json
{
  "productId": "p001",
  "quantity": 2
}
```

### Example Response

```json
{
  "status": "success",
  "message": "Item added to cart"
}
```

This example illustrates how a cart update request could be structured.

---

## 3. Checkout

### Request

```http
POST /api/checkout
```

### Example Body

```json
{
  "userId": "u123",
  "cartItems": [
    {
      "productId": "p001",
      "quantity": 2
    }
  ],
  "paymentMethod": "credit_card"
}
```

### Example Response

```json
{
  "orderId": "o789",
  "status": "PAID"
}
```

This example demonstrates how a checkout request might look in a typical system.

---

## 4. Get Order

### Request

```http
GET /api/orders/o789
```

### Example Response

```json
{
  "orderId": "o789",
  "status": "SHIPPED",
  "items": [
    {
      "productId": "p001",
      "quantity": 2
    }
  ]
}
```

This example shows how a client could retrieve order information.

---

## Notes

* These APIs are examples only and are not connected to a real backend system
* They are intended to help illustrate how REST APIs can be structured
* Real-world systems would include authentication, validation, and error handling
