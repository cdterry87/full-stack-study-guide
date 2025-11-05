# JavaScript Study Guide

## 🧩 Beginner Level

- **Q:** What is JavaScript?  
  **A:** A high-level, interpreted programming language used for web interactivity and application logic.

- **Q:** What are the different data types in JavaScript?  
  **A:** Primitive: `string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`; Non-primitive: `object`.

- **Q:** What is the difference between `var`, `let`, and `const`?  
  **A:**

  - `var`: function-scoped, hoisted
  - `let`: block-scoped, reassignable
  - `const`: block-scoped, not reassignable

- **Q:** What is `NaN`?  
  **A:** Represents “Not-a-Number,” returned from invalid numeric operations.

- **Q:** What does `typeof null` return?  
  **A:** `"object"` — a historical bug kept for backward compatibility.

- **Q:** What is `undefined` vs `null`?  
  **A:** `undefined` = variable declared but not assigned; `null` = intentional empty value.

- **Q:** How do you check equality in JavaScript?  
  **A:** `==` for loose comparison (type coercion), `===` for strict comparison (no coercion).

- **Q:** What is the difference between `for`, `for...in`, and `for...of`?  
  **A:**

  - `for`: numeric iteration
  - `for...in`: iterates keys
  - `for...of`: iterates values

- **Q:** What is a function expression?  
  **A:** Assigning a function to a variable, e.g., `const greet = function() {};`.

- **Q:** What are arrow functions?  
  **A:** Shorter syntax for functions that don’t bind their own `this`.

---

## ⚙️ Intermediate Level

- **Q:** What is the difference between `==` and `===`?  
  **A:** `===` checks both type and value; `==` performs type coercion.

- **Q:** What are closures?  
  **A:** Functions that capture variables from their outer lexical scope even after that scope has closed.

- **Q:** What is the `this` keyword?  
  **A:** Refers to the object that owns the function being executed (context-dependent).

- **Q:** How does hoisting work?  
  **A:** Declarations are moved to the top of their scope before execution (for `var`, functions).

- **Q:** What are promises?  
  **A:** Objects representing the eventual completion or failure of an asynchronous operation.

- **Q:** What is async/await?  
  **A:** Syntactic sugar over Promises for writing asynchronous code that looks synchronous.

- **Q:** What is the event loop?  
  **A:** Mechanism that handles asynchronous callbacks via the call stack, event queue, and microtask queue.

- **Q:** What are template literals?  
  **A:** Strings using backticks that support interpolation: `` `Hello ${name}` ``.

- **Q:** What is destructuring?  
  **A:** Extracting values from arrays/objects into variables:  
  `const {name, age} = user;`

- **Q:** What are rest and spread operators?  
  **A:**

  - **Rest (`...args`)** collects values into an array
  - **Spread (`...array`)** expands iterable values

- **Q:** What is a callback function?  
  **A:** A function passed as an argument to be executed later.

- **Q:** What is the difference between shallow and deep copy?  
  **A:** Shallow copies reference nested objects; deep copies duplicate all levels.

- **Q:** What is the difference between `null`, `undefined`, and undeclared variables?  
  **A:** `null`: empty value, `undefined`: no value assigned, undeclared: not defined at all.

---

## 🧠 Advanced Level

- **Q:** What is prototypal inheritance?  
  **A:** JavaScript objects inherit directly from other objects via the prototype chain.

- **Q:** Difference between classical and prototypal inheritance?  
  **A:** Classical uses classes (blueprints), prototypal uses objects as prototypes.

- **Q:** What is the difference between `call()`, `apply()`, and `bind()`?  
  **A:**

  - `call`: invokes function with arguments
  - `apply`: same but arguments as array
  - `bind`: returns a new function with `this` bound

- **Q:** What is event delegation?  
  **A:** Using a single event listener on a parent to handle events for child elements.

- **Q:** How does the `this` keyword behave in arrow functions?  
  **A:** It’s lexically bound (inherits from the parent scope).

- **Q:** What are higher-order functions?  
  **A:** Functions that take other functions as arguments or return them.

- **Q:** What are modules in ES6?  
  **A:** Reusable code units that use `export` and `import` syntax.

- **Q:** What are generators?  
  **A:** Functions that can pause and resume execution with `yield`.

- **Q:** What is currying?  
  **A:** Transforming a function with multiple arguments into a series of single-argument functions.

- **Q:** What is memoization?  
  **A:** Caching function results to improve performance.

- **Q:** Explain the difference between synchronous and asynchronous JavaScript.  
  **A:** Synchronous executes line by line; asynchronous defers tasks using callbacks, promises, or async/await.

- **Q:** What is the difference between stack and heap memory in JavaScript?  
  **A:** Stack = primitive values and execution context; Heap = reference types (objects, arrays).

- **Q:** What is the difference between shallow equality and deep equality?  
  **A:** Shallow checks references; deep checks nested object structure and values.

- **Q:** What are WeakMap and WeakSet used for?  
  **A:** Store weakly referenced keys (no memory leaks) — useful for caching or private data.

- **Q:** How does garbage collection work in JavaScript?  
  **A:** Removes objects with no references (mark-and-sweep algorithm).

- **Q:** What are microtasks and macrotasks?  
  **A:**

  - **Microtasks:** Promise callbacks
  - **Macrotasks:** setTimeout, setInterval, I/O

- **Q:** How can you improve JavaScript performance?  
  **A:** Minimize DOM operations, debounce/throttle events, memoize, lazy-load, and use Web Workers.
