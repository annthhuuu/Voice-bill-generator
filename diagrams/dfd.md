# Data Flow Diagram

## Context (Level 0)
External entity: Cashier / Shopkeeper. The user provides voice commands, corrections, and confirmation. The system returns recognized text, validation feedback, bill preview, and saved/exported bill.

## Level 1 Processes
1. Capture voice input.
2. Recognize speech and produce text.
3. Parse product names and quantities.
4. Validate products and retrieve prices.
5. Calculate line totals and bill total.
6. Present preview and save after confirmation.

## Data Stores
- D1: Product Catalogue
- D2: Confirmed Bill Records

## Mermaid Data-Flow Sketch
```mermaid
flowchart LR
  U[Cashier] -->|Voice| P1[Capture audio]
  P1 --> P2[Speech to text]
  P2 --> P3[Extract items]
  P3 --> P4[Validate products]
  D1[(Product catalogue)] --> P4
  P4 --> P5[Calculate bill]
  P5 --> P6[Preview and confirm]
  U -->|Corrections / approval| P6
  P6 -->|Confirmed bill| D2[(Bill records)]
  P6 -->|Preview / result| U
```

This is a conceptual model; update it to match the final architecture.
