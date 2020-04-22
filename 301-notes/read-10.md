# [The Call Stack](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)

>Call stack - is a mechanism for an interpreter to keep track of its place in a script that calls multiple functions

```js
function greeting() {
   // [1] Some codes here
   sayHi();// runs this function
   // [2] Some codes here
}
function sayHi() {
   return "Hi!";
}

// Invoke the `greeting` function
// this runs first
greeting();

// [3] Some codes here

```
>Whenever we invoke a function, it is automatically added to the Call Stack. Once the function has executed all of its code, it is automatically removed from the Call Stack

Since the `call stack` is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is `synchronous`.

At the most basic level, a `call stack` is a `data structure` that uses the **Last In, First Out** (LIFO) principle to temporarily store and manage function invocation (call).

>When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a `stack frame`. This stack frame is a memory location in the stack

>A `stack overflow` occurs when there is a recursive function (a function that calls itself) without an exit point

In Summary a call stack: 
1. It is single-threaded. Meaning it can only do one thing at a time.
2. Code execution is synchronous.
3. A function invocation creates a stack frame that occupies a temporary memory.
4. It works as a LIFO — Last In, First Out data structure.

# [JavaScript error messages && debugging](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

Type | Description
--- | ---
Reference errors | This is as simple as when you try to use a variable that is not yet declared you get this type os errors. the fact that this happens to let and const is called `Temporal Dead Zone` (TDZ).
Syntax errors | This occurs when you have something that cannot be parsed in terms of syntax
Range errors | Try to manipulate an object with some kind of length and give it an invalid length.
Type errors | Like the name indicates, this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.

> To debug your JS code, the easiest and maybe the most common way its to simply `console.log()`

Using Node.js with Visual Studio Code you can press the debug tab and add a configuration similar to this:

```js

/*
Using Node.js with Visual Studio Code you can press the debug tab and add a configuration similar to this:
*/
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Launch Program",
      "program": "${workspaceRoot}/index.js"
    }
  ]
}

```

>You can run the debugger by `pressing F5` or pressing the green play button.

[JavaScript error reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)

[Main Page](https://will-ing.github.io/reading-notes)