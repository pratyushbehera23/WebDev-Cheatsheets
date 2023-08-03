# Node.js

JS on pc/server (out of browser)
Use to write Backend code

```js
// Basic nodejs code:

// Import module
const fs = require('fs');

const textIn = fs.readFileSync('./notes/input.txt', 'utf-8');
console.log(textIn);

const textOut = `This is written: ${textIn}, created on ${Date.now()}`;
fs.writeFileSync('./notes/output.txt', textOut);
console.log('File written!');
```

## Synchronous (blocking) vs Asynchronous (non-blocking) code

In nodeJs process there is only one thread

Callback

## Simple web server

```js
const http = require('http');
// server
const server = http.createserver((req, res) => {
    res.end('Hello from server!');
});

server.listen(3000, 'localhost', () => {
    console.log('Listening to requests on port 3000');
});
```

### Routing

```js
const url = require('url');

```

### API

<!-- ------------------------------------------------------------------- -->

## MongoDB

NoSql DataBase

## Conclusion
