sequenceDiagram
    participant Browser
    participant Server

    Note right of Browser: New element

    Browser->>Server: POST JSON data
    activate Server
    Server-->>Browser: 201 status code added
    deactivate Server

    Note right of Browser: main.js updates with no reload
