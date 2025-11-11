``` mermaid
  flowchart LR

A[send note] --> |saved as new_note| B[on state change] --> C{is readystate= 4 AND is status= 200}
```
