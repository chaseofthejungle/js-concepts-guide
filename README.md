# JavaScript Concepts Guide

**Asyncs and Awaits:** These are used in tandem with promises (see the 'Promises' section below). If the keyword `async` is written before a function, then the function is intended to return a promise. If the keyword `await` is written inside of an async funtion, then the program will wait until after the promise is fulfilled.

**Callbacks (Callback Functions)**: Functions that are executed after other functions are finished running. This is set up when functions are passed as arguments to other functions. Callback functions can be especially useful with asynchronous (async) functions, in which a function should logically wait upon another function to perform.
  
**Memoization:** It is no secret that process management can (and does!) put a heavy burden on CPUs. The good news is that there are software and hardware based approaches to mitigating the problem. This brief guide focuses on memoization: an optimization technique that gets tasks (and their apps) executing faster and with greater processing cost efficiency. Simply put, *Memoization* handles output data via temporary *cache memory* storage, reducing the need for redundant algorithmic processing because the logic has already been handled and stored in memory for ready retrieval/reuse. It does so by performing a boolean-style function check as to whether the necessary logic is already stored in cache. If it is in there, then output is delivered faster and with less processing burden.

There are two *special functions* for performancing memoization:  

* Closures
  + A closure is a function plus the lexical environment (contains local variables, other functions within the current scope, and references to other scopes) that the function was declared within.
* Higher Order Functions
  + These are functions that operate upon various other functions, either by returning them or through accepting them as arguments).

**Promises:** These are JS objects that will eventually produce values. It is good practice for a failing promise to produce a self-documenting reason as to why it failed.  

**Strict Mode [ECMAScript 5 standard and later]:** The directive `"use strict"` (a literal expression, rather than a statement) toggles on the JavaScript strict mode. It prevents undeclared variables from being usable and requires stricter error handling and parsing during runtime.

TODO #1: Add code examples for each section.  
TODO #2: Calling/Binding/Applying, Currying, Debouncing, Hoisting, IIFEs, Polyfills, Scopes, and Throttling.
