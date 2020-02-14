# JS Debugging

# JavaScript book, Ch. 10, “Error Handling & Debugging”
 
### Things to consider
* Order of excution
* Execution contexts
* The stack
* Execution context (2 phases)
  1. Prepare - new scope is created. variables, functions, and arguments are create
  2. Execute - Now it can assign values to variables, reference function and there code, execute statements.
* Hoisting

>if a javascript statement generates an error then it throws an exception. At that point the interpreter stops and looks for exception-handling code.

>Error objects can help you find where your mistakes are and browsers have tool to help you read them.

Property | Descriptions
---- | ----
name | Type of error
message | description
fileNumber | Name of the javascript file
lineNumber | Line number of error

###  **7 types of error objects**

Property | Descriptions
---- | ----
Error | Generic error - the other errors are all based upon this error
Syntax error | Syntax has not been followed
Reference Error | Tried to reference a variable that is not declared
TypeError | an unexpected data type that cannot be coerced
RangedError | numbers not in acceptable range
URIError | encodeURI(), decodeURI(), and similar methods used incorrectly
evalError | eval() functioned incorrectly

>You can handle errors graceully using **try, catch, throw and finally** statements.

```js
try {
  // try to execute this code
} catch (exception) {
  // if there is an exception, run this code
} finally {
  // this always gets executed
}
```


Identify:

1. Where is the problem?
2. what exactly is the problem?

Tools: 
1. `Console Table()` method:
  * objects 
  * arrays that contain other objects

  ```js
var contacts = {
  "london": {
    "tel": "+44 (0)200 948 0128:,
    "country"= "UK"},
  "New Youk": {
    "Tel": "+1 (0)1 555 2104
    "country": "USA"}
}

console.table(contacts);

var city, contactDetails;
contactDetails = '';

$.each(contacts, function(city, contacts){
  contactDetails += city + ': ' + contacts.Tel + '<br />;
});
$('h2').after('<p>' + contactDetails  + '</p>');

  ```

Learn breakpoints --> p476 & p477

Setting multiple breakpoints allows you to step through code.

You can add conditional breakpoints.

Throwing errors

>If you know something might cause a problem for your script, you can generate your own errors before the interpreter creates them.

```js
throw new Error('message')
```

[Main Page](https://will-ing.github.io/reading-notes)
