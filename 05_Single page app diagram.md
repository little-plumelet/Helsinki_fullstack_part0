# Single page app diagram

``` mermaid 
sequenceDiagram
participant browser
participant server

browser->>server: GET: https://studies.cs.helsinki.fi/exampleapp/spa
server->>browser: server responded with html file
browser->>server: GET: https://studies.cs.helsinki.fi/exampleapp/main.css
server->>browser: server responded with CSS file
browser->>server: GET: https://studies.cs.helsinki.fi/exampleapp/spa.js
server->>browser: server responded with JS file
Note over browser, server: browser executed the code in JS file
browser->>server: GET: https://studies.cs.helsinki.fi/exampleapp/data.json
server->>browser: server responded with JSON file with notes
Note over browser, server: browser parsed JSON file and rendered notes
```
