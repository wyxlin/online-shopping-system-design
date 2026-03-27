# Sample API Requests and Responses

This document provides example API requests and responses for the online shopping system. These examples illustrate how clients interact with the backend API during product browsing, cart management, checkout, and order tracking.

---

## 1. Get Product List

### Request

```http
GET /products
```

### Response

```json
[
  {
    "productId": "P1001",
    "name": "Wireless Mouse",
    "price": 29.99,
    "stock": 120
  },
  {
    "productId": "P1002",
    "name": "Mechanical Keyboard",
    "price": 79.99,
    "stock": 45
  }
]
```

---

## 2. Get Product Details

### Request

```http
GET /products/P1001
```

### Response

```json
{
  "productId": "P1001",
  "name": "Wireless Mouse",
  "description": "Ergonomic wireless mouse with USB receiver",
  "price": 29.99,
  "stock": 120,
  "category": "Electronics"
}
```

---

## 3. Add Item to Cart

### Request

```http
POST /cart/items
Content-Type: application/json
```

```json
{
  "userId": "U123",
  "productId": "P1001",
  "quantity": 2
}
```

### Response

```json
{
  "message": "Item added to cart successfully",
  "cartId": "C456",
  "items": [
    {
      "productId": "P1001",
      "quantity": 2
    }
  ]
}
```

---

## 4. Checkout

### Request

```http
POST /checkout
Content-Type: application/json
```

```json
{
  "userId": "U123",
  "cartId": "C456",
  "paymentMethod": "credit_card",
  "shippingAddress": {
    "street": "123 Main St",
    "city": "Seattle",
    "state": "WA",
    "zipCode": "98101"
  }
}
```

### Response

```json
{
  "orderId": "O789",
  "status": "Confirmed",
  "estimatedDeliveryDate": "2026-04-05"
}
```

---

## 5. Get Order Status

### Request

```http
GET /orders/O789
```

### Response

```json
{
  "orderId": "O789",
  "userId": "U123",
  "status": "Shipped",
  "trackingNumber": "TRK123456",
  "estimatedDeliveryDate": "2026-04-05"
}
```

---

## Notes

* These examples are intended to illustrate API design and client-server interaction.
* They do not represent a production-ready implementation.
* Additional endpoints can be added for authentication, order cancellation, refunds, and inventory updates.
