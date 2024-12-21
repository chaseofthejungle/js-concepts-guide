# js-memoization-basics
  
**Definition/Overview:** It is no secret that process management can (and does!) put a heavy burden on CPUs. The good news is that there are software and hardware based approaches to mitigating the problem. This brief guide focuses on memoization: an optimization technique that gets tasks (and their apps) executing faster and with greater processing cost efficiency. Simply put, *Memoization* handles output data via temporary *cache memory* storage, reducing the need for redundant algorithmic processing because the logic has already been handled and stored in memory for ready retrieval/reuse. It does so by performing a boolean-style function check as to whether the necessary logic is already stored in cache. If it is in there, then output is delivered faster and with less processing burden.

There are two *special functions* for performancing memoization:  

* Closures
  + A closure is a function plus the lexical environment (contains local variables, other functions within the current scope, and references to other scopes) that the function was declared within.
* Higher Order Functions
  + These are functions that operate upon various other functions, either by returning them or through accepting them as arguments).

TODO: Add code example.
