# Activity Diagram – Create Bill

## Workflow
Start → create bill → capture voice → convert speech to text → check clarity → extract items → validate products and prices → calculate totals → preview bill → review and correct → confirm → save/export → end.

If speech is unclear, request repetition or manual correction. If an item or price is missing, request correction before calculation/finalization.

## Mermaid Activity Flow
```mermaid
flowchart TD
  A([Start]) --> B[Create new bill]
  B --> C[Capture voice]
  C --> D[Speech to text]
  D --> E{Text clear?}
  E -- No --> F[Repeat or edit input]
  F --> C
  E -- Yes --> G[Extract items and quantities]
  G --> H[Validate products and prices]
  H --> I{Valid?}
  I -- No --> J[Correct missing details]
  J --> G
  I -- Yes --> K[Calculate totals]
  K --> L[Show bill preview]
  L --> M{Approved?}
  M -- No --> N[Edit bill]
  N --> K
  M -- Yes --> O[Save or export]
  O --> P([End])
```
