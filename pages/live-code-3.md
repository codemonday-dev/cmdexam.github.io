## Question 3 (JS/TS)
Given: Collection of users (array of user object).

Find: 
> (a) Find the name of the user who has maximum age.
> 
> (b) Create function to get age by name, e.g., `getAgeByName('Boat')` or `getAgeByName('boat')` will get result `26`
> 
> (c) Transform array and grouping into `[{ 25: ['Win', 'Ton'], 33: ['Jeff'], 26: ['Boat']}]`

#### Input
```js
[
  {
    name: 'Win',
    age: 25
  },
  {
    name: 'Ton',
    age: 25
  },
  {
    name: 'Jeff',
    age: 33
  },
  {
    name: 'Boat',
    age: 26
  }
]
```

#### Expected Output
```
(a) "Jeff" (name of the user who has maximum age)
(b) getAgeByName('boat') will get 26.
(c) [{ 25: ['Win', 'Ton'], 33: ['Jeff'], 26: ['Boat']}]
```