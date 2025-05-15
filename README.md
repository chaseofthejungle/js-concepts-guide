# JavaScript Concepts Guide

#### Table of Contents:

1. [Primitive Data Types](#primitive-data)
2. [Undefined versus Null](#undefined-versus-null)
3. [Arrays](#arrays)
4. [Methods](#methods)
5. [Miscellaneous JS Topics](#miscellaneous)
6. [Application Programming Interface (API)](#api)
7. [Shorthand Coding Techniques](#shorthand)
8. [Development Pitfalls](#pitfalls)
9. [Supplemental Resources](#supplemental)
  
<hr />

## 1. <a name="primitive-data">Primitive Data Types</a>
  
**Primitive Data Types:** Primitive data types in JavaScript (JS) are unchangeable and unalterable (in developer lingo: immutable). This includes variables of the types: *String*, *Boolean*, *Number*, *BigInt*, *Symbol*, *Null*, and *Undefined*. Unlike objects (e.g., functions, arrays), primitive variables store by value rather than reference.
  
**String code example:**  
`let name = "Joe"; // literal character sequence. single quotes are also acceptable`  

**Boolean code example:**  
`let isEmployee = true; // true or false values only`  

**Number code example:**  
`let price = 67.35; // can be an integer or decimal value, stored as a floating-point`  

**BigInt code example:**  
`let x = 9999999999999999999n; // JS integers are <= 15 characters. Trailing 'n' is BigInt syntax`  

**Symbol code example:**  
`let sym = Symbol("abc"); // Unique value even if another 'abc' String or Symbol is created`  

**Null code example:**  
`let selectedValue = null; // indicates no value is selected`  

**Undefined code example:**  
`let x; // variable is declared but not initialized`

<hr />
  
## 2. <a name="undefined-versus-null">Undefined versus Null</a>
  
**Definitions/Overview:** An *undefined variable* in JS is one in which the variable was declared but not yet given a value (in other words, not yet initialized). JS automatically assigns the type of 'undefined' to variables of this context. In comparison, a *null variable* is one that purposely and deliberately lacks an object value (this is commonly done to reset the value of a variable, or otherwise clear it out). Nulls are of the type 'object'.
  
**'undefined' code example:**  
```
let x;  
console.log(x); // would output 'undefined', since variable was declared but not initialized  
```
  
**'null' code example:**  
```
let x = null;  
console.log(x); // would output 'null', as variable has been defined by developer to be null  
```
  
<hr />
  
## 3. <a name="arrays">Arrays</a>
  
**Arrays:** Arrays contrast with variables in that arrays allow for multiple values to be stored in one structure. Examples of items arrays can collect include objects, strings, numbers, and other arrays (essentially, if an item has a data type, it can be stored in an array). There are two common ways to create a JS array:
  
```
let pets = ["cat", "dog", "turtle"];  
let pets = new Array("cat", "dog", "turtle");
```
  
Individual array values/items are referred to as 'elements'. The first element in an array is considered the '0th' item in an array.  
  
```
let pets = ["cat", "dog", "turtle"];  
console.log(pets[0]); // Returns: 'cat'   
console.log(pets[1]); // Returns: 'dog'  
console.log(pets[2]); // Returns: 'turtle'
```
  
Array elements can be modified by accessing their index numbers. For example:
  
```
let pets = ["cat", "dog", "turtle"];  
pets[2] = "hamster";  
console.log(pets); // Returns: ["cat", "dog", "hamster"]  
```
  
<hr />
  
## 4. <a name="methods">Methods</a>
  
**Methods:** Methods play an essential role in JS, as well as other Object-Oriented Programming (OOP) languages. Tasks such as optimizing the performance of code, manipulating/transforming data (such as String, Array, and Object data), and empowering the user to interact via interfaces are common purposes of JS methods.

* **String Method examples...**
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
* **Array Method examples...**
  + `filter()` retrieves elements based on a specified condition.
  + `forEach()` executes a specified action for all elements in an array.
  + `map()` generates a new array in which all elements have been manipulated by a specified function. 
* **Object Method examples...**
  + `entries()` retrieves an array of an object's key/value pairs without modifying the object itself.
  + `keys()` is similar, but retrieves all of the keys instead.
  + `values()` retrieves all of the values from a specified object.
    
<hr />
  
## 5. <a name="miscellaneous">Miscellaneous JS Topics</a>
  
**Asyncs and Awaits:** These are used in tandem with promises (see the 'Promises' section below). If the keyword `async` is written before a function, then the function is intended to return a promise. If the keyword `await` is written inside of an async funtion, then the program will wait until after the promise is fulfilled.

**Applying/Binding/Calling:** Apply and call are similar methods that enable developers to alter the contexts of invoked functions. While call methods can replace a value inside of a function with a new specified `this` value, apply methods use arrays instead of individual values as arguments. Bind methods create/return new functions that can be executed later (and will utilize user-specified `this` values).
  
**Callbacks (Callback Functions)**: Functions that are executed after other functions are finished running. This is set up when functions are passed as arguments to other functions. Callback functions can be especially useful with asynchronous (async) functions, in which a function should logically wait upon another function to perform.
  
**Currying:** Transforms a multi-argument function into a series of nested functions (a function chain), with each function accepting a single argument until all arguments have been handled.
  
**Memoization:** It is no secret that process management can (and does!) put a heavy burden on CPUs. The good news is that there are software and hardware based approaches to mitigating the problem. This brief guide focuses on memoization: an optimization technique that gets tasks (and their apps) executing faster and with greater processing cost efficiency. Simply put, *Memoization* handles output data via temporary *cache memory* storage, reducing the need for redundant algorithmic processing because the logic has already been handled and stored in memory for ready retrieval/reuse. It does so by performing a boolean-style function check as to whether the necessary logic is already stored in cache. If it is in there, then output is delivered faster and with less processing burden.

There are two *special functions* for performancing memoization:  

* **Closures**
  + A closure is a function plus the lexical environment (contains local variables, other functions within the current scope, and references to other scopes) that the function was declared within.
* **Higher Order Functions**
  + These are functions that operate upon various other functions, either by returning them or through accepting them as arguments).

**Promises:** These are JS objects that will eventually produce values. It is good practice for a failing promise to produce a self-documenting reason as to why it failed.  
  
Several JS promise methods include:  

* `promise.all() // if any promise fails, entire result is rejected`
* `promise.allSettled() // returns array of all settled promise results, whether accepted or rejected`
* `promise.any() // neglects rejected promises but resolves as soon as any promise is accepted`
* `promise.catch() // specifies callback for handling a rejected promise`
* `promise.finally() // specifies callback for a settled promise, whether accepted or rejected`
* `promise.race() // determines overall result or rejection status based on how first promise is settled`
* `promise.reject() // initializes a promise with a specified error`
* `promise.resolve() // initializes a promise to a specified value`
* `promise.then() // specifies callbacks for a promise, whether accepted or rejected`
  
**Strict Mode [ECMAScript 5 standard and later]:** The directive `"use strict"` (a literal expression, rather than a statement) toggles on the JavaScript strict mode. It prevents undeclared variables from being usable, prevents accidental declaration of global-level variables, and requires stricter error handling and parsing during runtime.
  
<hr />
  
## 6. <a name="api">Application Programming Interface (API)</a>
  
**API and the fetch() method:**
  
JS utilizes the *Fetch API* for the purpose of creating web (HTTP) requests and satisfying them with processed responses/return data. The Fetch API relies upon *promises* (discussed in the previous section of this document) to generate results. Request status verification and response body extraction can be processed through a variety of data formats (e.g., JSON, XML).
  
In practice, a fetch implementation might look something like:
  
```
fetch('https://example.com/directory/submit', {  
  method: 'POST',  
  body: data  
});
```

Objects can be utilized to make more compelling fetch statements: the *Request*, *Headers*, and *Response* objects.

The *Request* object is used to create API requests, such as:
  
```
const myRequest = new Request('url', {  
  headers: myHeaders,  
  credentials: myCredentials  
});  
    
fetch(myRequest).then(...);
```
  
*Headers* sets headers, as well as reuse them across requests. This object can be used in many ways and various formats, such as:
  
```
myHeaders.append("Authorization", token);  
myHeaders.append("Content-Type", "text/xml");
```
  
The *Response* object clones response bodies, to be reused:

```
let myResponse = null;  
  
fetch("/api/v4/endpoint", {  
  headers: myHeaders  
}).then(response => {  
  myResponse = response.clone();  
  return response.json();  
});
```
  
The above code samples are deliberately simple illustrations of what the objects can do. Please consult the [Mozilla Fetch API documentation](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) for additional details.
  
<hr />
  
## 7. <a name="shorthand">Shorthand Coding Techniques</a>
  
Shorthand coding techniques can be utilized to write simpler, more easily readable, and more cost efficient programs. Such techniques include...

**When declaring multiple variables at once...**

Instead of typing:

```
let a;
let b;
let c = '3';
```
  
Try accomplishing all of that with one statement:
  
```
let a, b, c = '3';
```
  
<br />
  
**When checking if a variable is true...**

Instead of typing:

`if (sampleVar === true) {}`

Try getting rid of the explicit 'true' altogether:

`if (sampleVar) {}`
  
<br />
  
**When referencing a character in a string...**
  
Instead of typing:  

`"exampleString".charAt(2);`

Try skipping the method call altogether:

`exampleString[0];`
  
<br />
  
**When initializing elements of an array...**
  
Instead of typing:  

```
let exampleArray = new Array();
exampleArray[0] = "lizard";
exampleArray[1] = "hippo";
exampleArray[2] = "rat";
exampleArray[3] = "squirrel";
```
   
Try doing it all on the same line:
  
`let exampleArray = ["lizard", "hippo", "rat", "squirrel"];`

<br />
  
**When writing out conditional logic...**
  
Instead of typing:  

```
let passingScore;

if (score < 60) {
  passingScore = false;
} else {
  passingScore = true;
}
```

Try using the ternary operator:

`let passingScore = score < 60 ? false : true;`
  
<br />
  
**When doing math...**

Instead of typing:
  
```
a = a + b;
a = a - b;
```
  
Try using assignment operators like this:
  
```
a += b;
a -= b;
```
  
<br />
  
**When calculating exponents...**
  
Instead of typing:
  
`Math.pow(2,4);`
  
Try sticking to asterisks:
  
`2**4;`
  
<br />
  
**When using a function to display text to screen...**

Instead of typing:
  
```
function sayHi(name) {
  console.log("Hello there " + name);
}
```
  
Try using a one-line arrow function statement:

```
const sayHi = name => console.log("Hello there " + name);
```
  
<br />
  
**When printing out multiple variables...**

Instead of typing:
  
```
const name = "Billy";
const subject = "Math";

const favorite = "Did you know that " + name + " really likes to study " + subject + "?";
```

Try using template literals:
  
```
const name = "Billy";
const subject = "Math";

const favorite = `Did you know that ${name} really likes to study ${subject}?`;
```
  
<hr />
  
## 8. <a name="pitfalls">Development Pitfalls</a>
  
*Some common pitfalls in JS development include:*
  
* Decreased performance and readability from not utilizing arrow functions, promises, the forEach() method, the spread operator, strict equality (comparing both values *and* their type), and/or destructuring.  
* Forgetting to enable strict mode.  
* Needlessly declaring functions and variables globally (causing every JS file included within a page to execute within the same scope).  
* Not modularizing functions (failing to write functions so that they only perform one task at a time).  
* Only using `var` instead of `let` and `const` for variable declarations, potentially leading to redeclarations and variables declared outside of proper scope.
* Poor loop performance due to reading array length attribute at each iteration (solvable by storing length within a variable and accessing it as necessary).
  
<hr />

## 9. <a name="supplemental">Supplemental Resources</a>
  
* *[Intro to MERN and MEAN Stack Overview Guide](https://github.com/chaseofthejungle/intro-to-mern-and-mean-stack)*
* *[JavaScript Event Handling Guide](https://github.com/chaseofthejungle/js-event-handling-guide)*
* *[Node.js JavaScript Runtime Environment Official Website](https://nodejs.org/en)*
  
<hr />
  
TODO #1: Add sections on: Arrow Functions, Debouncing, Destructuring, Hoisting, IIFEs, Inheritance, Multi-threading (as in Imitating/Simulating multi-threading), Plug-ins, Polyfills, Prototyping, Scopes, the Spread Operator, Strict Equality (versus Loose Equality), and Throttling.  
TODO #2: Add and explain methods (with code samples) for the following categories: Arrays, Dates, JSON, Math, Objects.  
TODO #3: Add Axios to API section, as an alternative to the fetch method.  
