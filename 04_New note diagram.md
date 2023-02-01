
# New note diagram

<p>User fill the form with text 'test-note' and press save button</p>
<img width="284" alt="image" src="https://user-images.githubusercontent.com/70891441/215975621-9be6d8e3-f6b8-4e64-a258-1934a0e4388b.png">

``` mermaid 
sequenceDiagram
participant browser
participant server

browser->>server: POST: https://studies.cs.helsinki.fi/exampleapp/new_note
Note over browser, server: server created new note and responded with code 302 (redirect)
browser->>server: GET: https://studies.cs.helsinki.fi/exampleapp/notes and made other requests to layout web page
Note over browser, server: browser asked for other files, executed JS code and asked for notes
server->>browser: responded with all requested files
Note over browser, server: browser executed the callback function that rendered the notes, including the newly created one 
```
