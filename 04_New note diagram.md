
# New note diagram
 
sequenceDiagram
participant user
participant browser
participant server

user->>browser: fill the input with text 'test-note' and press save button
Note over user, browser: <img width="284" alt="image" src="https://user-images.githubusercontent.com/70891441/215975621-9be6d8e3-f6b8-4e64-a258-1934a0e4388b.png">
browser->>server: POST: https://studies.cs.helsinki.fi/exampleapp/new_note
Note over browser, server: server created new note and responded with code 302 (redirect)
browser->>server: GET: https://studies.cs.helsinki.fi/exampleapp/notes and made other requests to layout web page
server->>browser: responded with all requested files
Note over browser, server: browser executes the callback function that renders the notes, including the newly created one 

