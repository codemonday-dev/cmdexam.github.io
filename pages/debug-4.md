### Debug 4

Inspect the code below in the main Express controller

```js
...
app.get('/', async (req, res) => {
  const result = handlerFunction(req.body)
  res.json(data)
})
...

```
Then the `handler.js` code
```js
export default function handlerFunction() { 
  try {
    const data = await func1()
    const result = func2(data)
    return result
  } catch(error) {
    await func3()
    console.log(error)
    return null
  }
}
```

### Question
1. What happen when `func1` error?
2. Are there a way to know if error is from `func1` and `func2`?
3. Are there a chance that unhandled error will happen?
