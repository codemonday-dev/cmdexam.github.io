### Answer Debug #2

### Concept

You need the `factory`.

This is VERY COMMON.

You can find one in the simple express hello world code

```js
const express = require('express') // Import factory function
const app = express() // Instantiate

// Now app is the NEW instance and not MUTATE when used elsewhere

app.get('/', (req, res) => { res.send('Hello') })

app.listen(3000, () => { console.log(`Start`) })
```

### Solution

On `file1.js` the edit will be
```js 
const factory = () => ({ foo: "bar"})

export default factory
```

Then `file2.js` and `index.js` use it as factory
```js
import factory from './file1.js'

const obj1 = factory()

// CANNOT EDIT THIS LINE
obj1.foo = 'baz'

export default {
  obj1,
  a: 1,
  b: 2
}
```
And in the main
```js
import factory from './file1.js'
import obj2 from './file2.js'

const obj1 = factory()

console.log(obj1)
console.log(obj2)
```
