# Data Flow Map

**Independent simulation.** Fictional insurer; no real personal data.

```mermaid
flowchart LR
  A["Claimant or policyholder"] -->|"Claim details, photos, documents"| B["Customer portal or phone line"]
  J["Repair garages and third parties"] -->|"Estimates, invoices, contact details"| C
  B --> C["Claims management system"]
  C -->|"Minimised claim data"| D["AI model service (third-party processor)"]
  D -->|"Risk score, priority, explanation"| E["Cloud database"]
  E --> C
  C --> F["Claims handler"]
  F -->|"Final decision, override notes"| C
  C --> G["Claims payment system"]
  G -->|"Bank details"| H["Bank"]
  C --> I["Fraud team (escalations only)"]
  C -.-> K["Audit and access logs"]
```

## Controls at each point
| Flow | Data | Control (proposed) |
|---|---|---|
| Portal to claims system | D01 to D04 | Encryption in transit; input validation |
| Claims system to AI service | D16 (minimised) | Only needed fields sent; contract with processor |
| AI output to handler | D07, D17 | Role-based access; handler can override |
