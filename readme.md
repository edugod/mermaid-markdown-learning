## mermain practice file

I can use mermain on github now, this markdown its a practice.


Create a similar diagram depicting the situation where the user creates a new note on page https://studies.cs.helsinki.fi/exampleapp/notes when writing something into the text field and clicking the submit button.

If necessary, show operations on the browser or on the server as comments on the diagram.

The diagram does not have to be a sequence diagram. Any sensible way of presenting the events is fine.


```mermaid
sequenceDiagram
    participant BROWSER
    participant SERVER
    BROWSER->>SERVER: HTTP POST https://studies.cs.helsinki.fi/exampleapp/notes
    SERVER-->>BROWSER: status code 302, do a new HTTP GET with adress notes
    BROWSER->>SERVER: HTTP GET https://studies.cs.helsinki.fi/exampleapp/notes
    SERVER-->>BROWSER: HTML code
    BROWSER->>SERVER: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
    SERVER-->>BROWSER: main.css
    BROWSER->>SERVER: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.js
    SERVER-->>BROWSER: main.js
    BROWSER->>SERVER: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
    SERVER-->>BROWSER: data.json
```

