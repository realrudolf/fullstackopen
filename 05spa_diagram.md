sequenceDiagram
    participant Browser
    participant Server

    Browser->>Server: GET /exampleapp/spa (HTML document)
    activate Server
    Server-->>Browser: Returns index.html
    deactivate Server

    Browser->>Server: GET /exampleapp/main.css (CSS file)
    activate Server
    Server-->>Browser: Returns main.css
    deactivate Server

    Browser->>Server: GET /exampleapp/spa.js (JavaScript file)
    activate Server
    Server-->>Browser: Returns spa.js
    deactivate Server

    Browser->>Server: GET /exampleapp/data.json (JSON data)
    activate Server
    Server-->>Browser: Returns JSON data
    deactivate Server

    Browser->>Browser: JavaScript renders the page dynamically