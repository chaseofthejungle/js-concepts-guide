# JavaScript Concepts Guide

**Methods:** Methods play an essential role in JavaScript (JS), as well as other Object-Oriented Programming (OOP) languages. Tasks such as optimizing the performance of code, manipulating/transforming data (such as String, Array, and Object data), and empowering the user to interact via interfaces are common purposes of JS methods.

* String Method examples...
  + `charAt()` returns the character positioned at a specified index in a string.
  + `includes()` verifies if a string contains a specified substring or element.
  + `indexOf()` retrieves the first position in a string in which a specified value is found.
  + `length()` retrieves the total number of characters from a string.
  + `replace()` swaps characters in a string with other characters (as specified).
  + `slice()` returns characters of a specified position range from a string.
  + `split()` divides a string into parts based on a specified delimiter.
  + `substring()` extracts characters occurring between two specified positions of a string and returns a new value.
  + `toLowerCase()` and `toUpperCase()` are self-evident.
    - A sample usage would be `console.log("SAMPLE".toLowerCase());`, which would produce an output of `sample`.
  + `trim()` removes spaces from string values.
* Array Method examples...
  + `filter()` retrieves elements based on a specified condition.
  + `forEach()` executes a specified action for all elements in an array.
  + `map()` generates a new array in which all elements have been manipulated by a specified function. 
* Object Method examples...
  + `entries()` retrieves an array of an object's key/value pairs without modifying the object itself.
  + `keys()` is similar, but retrieves all of the keys instead.
  + `values()` retrieves all of the values from a specified object.
  
<hr />

**Asyncs and Awaits:** These are used in tandem with promises (see the 'Promises' section below). If the keyword `async` is written before a function, then the function is intended to return a promise. If the keyword `await` is written inside of an async funtion, then the program will wait until after the promise is fulfilled.

**Applying/Binding/Calling:** Apply and call are similar methods that enable developers to alter the contexts of invoked functions. While call methods can replace a value inside of a function with a new specified `this` value, apply methods use arrays instead of individual values as arguments. Bind methods create/return new functions that can be executed later (and will utilize user-specified `this` values).
  
**Callbacks (Callback Functions)**: Functions that are executed after other functions are finished running. This is set up when functions are passed as arguments to other functions. Callback functions can be especially useful with asynchronous (async) functions, in which a function should logically wait upon another function to perform.
  
**Currying:** Transforms a multi-argument function into a series of nested functions (a function chain), with each function accepting a single argument until all arguments have been handled.
  
**Memoization:** It is no secret that process management can (and does!) put a heavy burden on CPUs. The good news is that there are software and hardware based approaches to mitigating the problem. This brief guide focuses on memoization: an optimization technique that gets tasks (and their apps) executing faster and with greater processing cost efficiency. Simply put, *Memoization* handles output data via temporary *cache memory* storage, reducing the need for redundant algorithmic processing because the logic has already been handled and stored in memory for ready retrieval/reuse. It does so by performing a boolean-style function check as to whether the necessary logic is already stored in cache. If it is in there, then output is delivered faster and with less processing burden.

There are two *special functions* for performancing memoization:  

* Closures
  + A closure is a function plus the lexical environment (contains local variables, other functions within the current scope, and references to other scopes) that the function was declared within.
* Higher Order Functions
  + These are functions that operate upon various other functions, either by returning them or through accepting them as arguments).

**Promises:** These are JS objects that will eventually produce values. It is good practice for a failing promise to produce a self-documenting reason as to why it failed.  

**Strict Mode [ECMAScript 5 standard and later]:** The directive `"use strict"` (a literal expression, rather than a statement) toggles on the JavaScript strict mode. It prevents undeclared variables from being usable and requires stricter error handling and parsing during runtime.

TODO #1: Add code examples for each section.  
TODO #2: Add sections on Debouncing, Hoisting, IIFEs, Polyfills, Scopes, and Throttling.  
TODO #3: Add and explain methods for the following categories: Arrays, Dates, JSON, Math, Objects, Promises.  
TODO #4: Add information on: arrow functions, shortening assignment operator statements, shortening conditions, shortening mathematical power operations, shortening variable declarations, template literals, and ternary operator usage.  
TODO #5: Add section on how JS can imitate/simulate multi-threading.
