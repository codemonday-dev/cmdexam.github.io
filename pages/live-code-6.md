## Question 6 (JS/TS)
It is famous that once there is an NPM module which is very easy to implement yet most downloaded so when the author took down the module many sites also went down.
https://www.npmjs.com/package/left-pad by now Node.js has already implemented the `padStart` function just like in the browser. Still there are many people who keep downloading this.

In real life, we tend not to download NPM modules like this since it will make our repository grow extremely big with too many dependencies.

We would like you to implement this easy function `leftPad` by yourself to showcase your basic programming skill.

```
 leftPad('foo', 5)
// => "  foo"
 
leftPad('foobar', 6)
// => "foobar"
 
leftPad(1, 2, '0')
// => "01"
 
leftPad(17, 5, 0)
// => "00017"

leftPad(17, 5, 'X')
// => "XXX17"