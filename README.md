
#Part 4
``` mermaid
  flowchart LR

A[send note] --> |saved as new_note in JSON| B[it continues to listen to a new change in the data.json file] --> C[on state change]-->D{is readystate= 4 AND is status= 200};
D --> |Yes| E[JSON to JS redable format] --> F[print data] --> G[add ul with attribute class:notes] --> H{foreach} --> |go| I[create an li] --> J[it appends it to the ul] --> K[adds the note content] --> H
--> |stop| L[insert the list in the html file] --> B
```
#Part 5
``` mermaid
  flowchart LR

  A[load the HTML] --> B[load the CSS] --> C[load the JS file] --> D[load the JSON file] --> E[execute the JS] --> F{is readystate= 4 AND is status= 200};
F --> |yes| G[JSON to JS redable format] --> H[execute funcion rewritenotes] --> I{foreach} --> |go| J[create an li] --> K[it appends it to the ul] --> L[adds the note content] --> I
--> |stop| M[is note alredy has a childnode] --> N[remove child]  --> [insert the list in the html file]
``` 

#Part 6
