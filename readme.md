## mermain practice file

I can use mermain on github now, this markdown its a practice.


Create a similar diagram depicting the situation where the user creates a new note on page https://studies.cs.helsinki.fi/exampleapp/notes when writing something into the text field and clicking the submit button.

If necessary, show operations on the browser or on the server as comments on the diagram.

The diagram does not have to be a sequence diagram. Any sensible way of presenting the events is fine.

primeiro: eu vou destrinchar os passos:
submitting (clicando no botão do form), ele vai mandar o user input para o servidor:
isso gerou 5 HTTPS REQUEST (pediu 5 endereços para o servidor): new_note, notes, main.css, main.js, data.json
servidor respondeu com um status code 302(isso é um URL redirect) no qual o servidor pede pro browser para fazer um NOVO http get request
server -> browser new HTTP get request in Location /notes
browser reload /notes -> 3 new HTTP request (fetching the css main.css; the js code main.js) and the raw data notes (data.json)


browser     server
submitting
HTTP POST /new_note --> SERVER
HTTP status code 302 <-- Server
do a new request
HTTP GET /notes --> Server
HTML code <---- Server
HTTP GET /main.css ---> Server
main.css <--- Server
HTTP GET /main.js ---> Server
main.js <--- Server
HTTP GET /data.json ---> Server
data.json <---- Server




```mermaid
sequenceDiagram
    participant browser
    participant server
    browser: submit form
```
