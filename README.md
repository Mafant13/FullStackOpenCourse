
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
--> |stop| M[is note alredy has a childnode] --> N[remove child]  --> O[insert the list in the html file]
``` 

#Part 6
``` mermaid
  flowchart LR

A[send note] --> |saved as new_note_spa in JSON| B[form = elements with id 'notes_form'] --> C[onsubmit] --> D[prevent the use of the traditional web app] --> E[creates a var note with content and date] -->
F[pushes the note] --> G[clear the input field] --> H[calls the Redrawnotes funcion] -->  I{is readystate= 4 AND is status= 200};
I --> |yes| J[JSON to JS redable format] --> K[execute funcion rewritenotes] --> L{foreach} --> |go| M[create an li] --> N[it appends it to the ul] --> O[adds the note content] --> I
--> |stop| P[is note alredy has a childnode] --> Q[remove child]  --> R[insert the list in the html file] --> S[recalls the funcion sendtoserver] --> T[saves it using POST to the json file] --> U[requests the content-type and the application/json headers] --> V[and it stringifyes the var note, sending it's content]
```
