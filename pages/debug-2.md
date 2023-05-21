### Debug Problem #2
See the code in ES6 module project below

First file `file1.js`
```js
export default {
  foo: "bar"
}
```

Second file `file2.js`
```js
import obj1 from './file1.js'

// CANNOT EDIT THIS LINE //
obj1.foo = 'baz'

export default {
  a: 1,
  b: 2
}
```

The main file `index.js`
```js
import obj1 from './file1.js'
import obj2 from './file2.js'

console.log(obj1)
console.log(obj2)
```

Now the output of calling `node index.js` are
```
{ foo: 'baz' } // WRONG HERE
{ foo: 'baz', a: 1, b: 2 }
```

### Objective
Fix the code to return the correct `obj1` and `obj2` of
```
{ foo: 'bar' }
{ foo: 'baz', a: 1, b: 2 }
```
