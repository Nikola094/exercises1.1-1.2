sequenceDiagram
    participant Browser
    participant Server

    Browser->>Server: GET website
    activate Server
    Server-->>Browser: HTML document
    deactivate Server

    Browser->>Server: GET main.js
    Server-->>Browser: Return main.js

    Note right of Browser: JSON data is fetched

    Browser->>Server: GET data.json
    Server-->>Browser: JSON data

    Note right of Browser: Page doesn't reload -> preventDefault
    