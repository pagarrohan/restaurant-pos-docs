# 🧾 Billing Module

The Billing module is the core of the POS. It allows staff to:

- Add items to a bill by category
- Apply discounts or offers
- Add or select customers
- View real-time total, tax, and charges
- Choose payment type (Cash, Card, UPI)
- Print receipts or KOT

## Features

- Order Summary Table
- Quick Pay
- Split Bill
- Hold & Recall Orders
- Print Options (Receipt, KOT)

## API Integration

- `POST /api/orders` – Create new order
- `GET /api/orders/{id}` – Get order details
