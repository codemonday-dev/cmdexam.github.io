### Debug 3

This Question test you the basic tool of functional programming in JS

The code below intend to sum the score of Team A. Fill in the function in `___A___` then `B` and `C`

```js
const data = [
  { team: 'a', score: 12 },
  { team: 'b', score: 82 },
  { team: 'b', score: 49 },
  { team: 'a', score: 33 },
  { team: 'a', score: 12 },
  { team: 'c', score: 65 }
]

const result = data
  .___A___(score => score.team === 'a')
  .___B___(teamA => teamA.score)
  .___C___((prev, curr) => prev + curr, 0)

console.log(result)

```
