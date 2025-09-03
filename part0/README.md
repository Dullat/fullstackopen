# contains mermaid diagrams for 0.4, 0.5, and 0.6


## 0.4
```mermaid
sequenceDiagram
    participant user
    participant browser
    participant server

    user->>browser: writes note and clicks "save"
    browser->>server: https://studies.cs.helsinki.fi/exampleapp/new_note_spa: {"content": "dfgfg","date": "2025-09-03T19:11:50.386Z"}
   
```


## 0.5

```mermaid 
sequenceDiagram
    participant browser
    participant server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    server-->>browser: HTML page
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    server-->>browser: spa.js (main)
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server-->>browser: CSS
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server-->>browser: json Data
```

## 0.6
```mermaid
sequenceDiagram
    participant user
    participant browser
    participant server

    user->>browser: writes note and clicks "save"
    browser->>server: Post https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    server-->>browser: Created
    browser->>browser: update the notes list
