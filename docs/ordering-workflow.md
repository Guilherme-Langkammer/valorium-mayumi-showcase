# Ordering Workflow

```mermaid
flowchart TD
    A[Browse catalog] --> B[Select product and options]
    B --> C[Review cart]
    C --> D[Choose delivery or pickup]
    D --> E[Choose available schedule]
    E --> F[Submit order]
    F --> G[Server-side validation]
    G --> H[Order registered or rejected]
    H --> I[Administrative order workflow]
```

This is a **conceptual** customer journey based on the showcased product direction. Payment confirmation, external integrations, scheduling constraints and end-to-end production behavior must be verified against the private build before being claimed as released.

## Important considerations

- Validate availability and promotional eligibility on the server.
- Recalculate totals independently of browser-supplied values.
- Keep customer-visible order state consistent with administrative changes.
- Protect customer contact and address information.
- Avoid duplicate submissions and ambiguous payment/order states.
