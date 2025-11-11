
#Part 4
``` mermaid
  flowchart LR

A[send note] --> |saved as new_note in JSON| B[it continues to listen to a new change in the data.json file] --> C[on state change]-->D{is readystate= 4 AND is status= 200};
D --> |Yes| E[JSON to JS redable format] --> F[print data] --> G[add ul with attribute class:notes] --> H{foreach} --> |go| I[create an li] --> J[it appends it to the ul] --> K[adds the note content] --> H
--> |stop| L[insert the list in the html file] --> B
```
#Part 5


#Part 6
