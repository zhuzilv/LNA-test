# LNA-test
github page lna test

# if you want use this page , you should open a server eg:
```
const http = require('http')

http.createServer((req, res) => {
  console.log(req.method, req.url, req.headers)

  const headers = {
    'Access-Control-Allow-Origin': '*',
    'Access-Control-Allow-Methods': 'GET,POST,OPTIONS',
    'Access-Control-Allow-Headers': 'content-type',
    'Access-Control-Allow-Private-Network': 'true'
  }

  if (req.method === 'OPTIONS') {
    res.writeHead(204, headers)
    return res.end()
  }

  res.writeHead(200, {
    ...headers,
    'Content-Type': 'application/json'
  })

  res.end(JSON.stringify({ ok: true }))
}).listen(18080, '127.0.0.1')

```
