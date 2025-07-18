# Kitchen Order Ticket (KOT)

## Overview
The Kitchen Order Ticket (KOT) module is responsible for capturing and sending customer orders to the kitchen. It ensures smooth communication between front-of-house staff and kitchen staff.

---

## Features

- Create new KOTs for each order.
- Print KOTs directly to kitchen printers.
- Support for dine-in, take-away, and delivery modes.
- Group items by course or category.
- Multiple KOTs per table/session (incremental).
- Track KOT preparation status (Preparing, Ready, Served).
- Real-time KOT updates on Kitchen Display System (KDS).
- Custom kitchen notes per item (e.g., "Less Spicy", "No Onion").

---

## Workflow

1. **Order Placement**  
   Server inputs order using POS → Clicks “Print KOT” → KOT generated.

2. **KOT Dispatch**  
   KOT sent to:
   - Kitchen Printer (ESC/POS format)
   - Kitchen Display App (KDS)

3. **Kitchen Processing**  
   Chef marks item as "Preparing" → "Ready"

4. **Order Serving**  
   Waiter serves the order → KOT marked as "Served"

---

## Data Model

```json
{
  "kotId": "KOT12345",
  "orderId": "ORD12345",
  "tableNo": "T3",
  "waiterName": "Ravi",
  "timestamp": "2025-07-18T13:00:00Z",
  "items": [
    {
      "itemName": "Paneer Butter Masala",
      "quantity": 2,
      "notes": "Less Spicy",
      "status": "Preparing"
    },
    {
      "itemName": "Tandoori Roti",
      "quantity": 4,
      "status": "Pending"
    }
  ],
  "kotStatus": "Pending"
}
