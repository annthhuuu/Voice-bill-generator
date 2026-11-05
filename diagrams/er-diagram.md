# ER Diagram

## Entities
**Product**: product_id (PK), name, unit, unit_price, active_status.

**Bill**: bill_id (PK), bill_number, created_at, subtotal, tax_amount, discount_amount, grand_total, status.

**BillItem**: bill_item_id (PK), bill_id (FK), product_id (FK), quantity, unit_price_at_sale, line_total.

**User** (optional): user_id (PK), name, role.

## Relationships
- One Bill contains one or more BillItems.
- One Product can appear in many BillItems.
- Each BillItem belongs to one Bill and references one Product.
- If accounts are implemented, one User may create many Bills.

## Mermaid ER Diagram
```mermaid
erDiagram
  PRODUCT ||--o{ BILL_ITEM : appears_in
  BILL ||--|{ BILL_ITEM : contains
  USER ||--o{ BILL : creates
  PRODUCT {
    int product_id PK
    string name
    string unit
    decimal unit_price
  }
  BILL {
    int bill_id PK
    string bill_number
    datetime created_at
    decimal grand_total
    string status
  }
  BILL_ITEM {
    int bill_item_id PK
    int bill_id FK
    int product_id FK
    decimal quantity
    decimal unit_price_at_sale
    decimal line_total
  }
  USER {
    int user_id PK
    string name
    string role
  }
```

The User entity is optional. Finalize the schema during detailed design.
