``` mermaid
  flowchart LR

A[send note] --> |saved as new_note in JSON| B[on state change] --> C{is readystate= 4 AND is status= 200};
C --> |Yes| D[JSON to JS redable format] --> E[print data] --> F[add ul with attribute class:notes] --> G[foreach create an li, it appends it to the ul, and adds the note content]
```
