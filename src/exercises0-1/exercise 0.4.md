sequenceDiagram
    participant Browser
    participant Server

    Browser->>Server: POST new note is created
    activate Server
    Server-->>Browser: server redirect to website
    deactivate Server

    Browser->>Server: GET website
    activate Server
    Server-->>Browser: HTML document
    deactivate Server

    Browser->>Server: GET main.js
    Server-->>Browser: Return main.js

    Browser->>Server: GET data.json
    Server-->>Browser: JSON data 

    Browser->>Server: GET main.js(with new appended element) 
    Server-->Browser: Reload with new HTML