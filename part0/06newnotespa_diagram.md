```mermaid
sequenceDiagram
    participant User
    participant Browser
    participant Server

    User->>Browser: Enters text in the input field
    User->>Browser: Clicks the 'Save' button
    Browser->>Server: HTTP POST /new_note with note content
    activate Server
    Server->>Server: Saves the note (e.g., in database)
    Server-->>Browser: Sends confirmation (e.g., JSON with the new note)
    deactivate Server

    Browser->>Browser: JavaScript updates the note list dynamically
