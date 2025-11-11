``` mermaid
  flowchart LR

A[send note] --> |saved as new_note in JSON| B[on state change] --> C{is readystate= 4 AND is status= 200};
C --> |Yes| [JSON to JS redable format] --> D[print data] --> E[add ul with attribute class:notes] --> F[foreach create an li, it appends it to the ul, and adds the note content]
```
