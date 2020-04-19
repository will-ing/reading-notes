# Refactoring

## [functional programming](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

> `Functional programming` is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data

> Pure functions - It returns the same result if given the same arguments

Properties -
  - It returns the same result if given the same arguments 
  - It does not cause any observable side effects

```js
// global object that was not passed as a parameter to the function.
let PI = 3.14;

const calculateArea = (radius) => radius * radius * PI;

calculateArea(10); // returns 314.0


// This is a the pure function example
let PI = 3.14;

const calculateArea = (radius, pi) => radius * radius * pi;

calculateArea(10, PI); // returns 314.0
```

>Immutability - Unchanging over time or unable to be changed.



## [strategies for easier code](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)

- return early from functions
- Cache variables so functions can be read like sentences
- Check for Web APIs before implementing your own functionality



[Main Page](https://will-ing.github.io/reading-notes)