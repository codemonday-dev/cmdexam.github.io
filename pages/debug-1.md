### Debug Problem #1
See the code below

```js
const express = require('express')
const app = express()
const port = 3030
const axios = require('axios')

app.get('/data', (req, res) => {
  const data = { a: 1, b: 2}
  res.json(data)
})

app.get('/', (req, res) => {
  const { data } = axios.get(`http://localhost:${port}/data`)
  res.json(data)
})

app.listen(port, () => { console.log(`[DEBUG] ${Date.now()} listening`) })

```

Now the output of calling `GET localhost:3030/` are
```
{}
```
when calling from the browser or command line like `curl http://localhost:3030`

### Objective
Fix the code to return json data of
```
{ a: 1, b: 2 }
```
