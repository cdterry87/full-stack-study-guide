# PHP Study Guide

## 🧩 Beginner Level

- **Q:** What is PHP?  
  **A:** A server-side scripting language designed for web development.

- **Q:** What does PHP stand for?  
  **A:** “PHP: Hypertext Preprocessor.”

- **Q:** How do you declare variables in PHP?  
  **A:** Prefix with `$`, e.g. `$name = "Chase";`.

- **Q:** Difference between `==` and `===`?  
  **A:** `==` compares values; `===` compares values _and_ types.

- **Q:** How do you define constants?  
  **A:** `define('NAME', 'value');` or `const NAME = 'value';`.

- **Q:** What are superglobals?  
  **A:** Predefined variables like `$_GET`, `$_POST`, `$_SESSION`, available anywhere.

- **Q:** How do you include other files?  
  **A:** `include`, `require`, `include_once`, `require_once`.

- **Q:** What is the difference between `include` and `require`?  
  **A:** `require` causes a fatal error if the file is missing; `include` only warns.

- **Q:** What is type juggling?  
  **A:** Automatic type conversion during operations.

- **Q:** How do you handle errors in PHP?  
  **A:** Using `try...catch` for exceptions or custom error handlers.

---

## ⚙️ Intermediate Level

- **Q:** What are namespaces in PHP?  
  **A:** Used to group related classes and avoid name collisions.

- **Q:** Explain autoloading.  
  **A:** Automatically loads class files using `spl_autoload_register()` or Composer PSR-4.

- **Q:** What are traits?  
  **A:** Mechanism for code reuse across classes without inheritance.

- **Q:** Explain interfaces vs. abstract classes.  
  **A:** Interfaces define method contracts; abstract classes can define both contracts and partial implementations.

- **Q:** What are magic methods?  
  **A:** Special methods like `__construct`, `__get`, `__set`, `__call`, `__toString`.

- **Q:** What are closures?  
  **A:** Anonymous functions that can capture variables from the parent scope.

- **Q:** Difference between `self` and `static` in PHP OOP?  
  **A:** `self` refers to the current class; `static` allows late static binding for child overrides.

- **Q:** How does PHP handle sessions?  
  **A:** Stores data across requests using `$_SESSION` and cookies with a session ID.

- **Q:** What’s the difference between `array_map`, `array_filter`, and `array_reduce`?  
  **A:** `map` transforms, `filter` removes elements, `reduce` accumulates values.

- **Q:** How do you connect to a database in PHP (without frameworks)?  
  **A:** Using `PDO` with prepared statements for security.

---

## 🧠 Advanced Level

- **Q:** What is the difference between `==` and `===` with type coercion?  
  **A:** `==` converts types before comparison; `===` enforces type integrity.

- **Q:** Explain SOLID principles in PHP.  
  **A:**

  - **S:** Single Responsibility
  - **O:** Open/Closed
  - **L:** Liskov Substitution
  - **I:** Interface Segregation
  - **D:** Dependency Inversion

- **Q:** What are design patterns commonly used in PHP?  
  **A:** Singleton, Factory, Repository, Strategy, Observer, Dependency Injection.

- **Q:** What is the difference between composition and inheritance?  
  **A:** Composition uses contained objects for behavior; inheritance extends behavior.

- **Q:** What is the use of generators in PHP?  
  **A:** `yield` keyword returns data lazily, saving memory in large iterations.

- **Q:** How do you use the `match` expression in PHP 8+?  
  **A:** Cleaner alternative to `switch`, supports strict comparisons and returns values.

- **Q:** What are union types in PHP 8?  
  **A:** Allow multiple accepted types, e.g. `function foo(int|float $num)`.

- **Q:** What are attributes (annotations) in PHP 8?  
  **A:** Metadata defined with `#[Attribute]` instead of docblocks.

- **Q:** How do you manage dependencies in modern PHP?  
  **A:** With Composer and semantic versioning (`composer.json`).

- **Q:** How do you handle asynchronous or parallel tasks in PHP?  
  **A:** Using libraries like `amphp`, `ReactPHP`, or via queues and workers in frameworks.

- **Q:** How would you improve PHP application performance?  
  **A:** Use OPcache, caching layers, optimized queries, autoload optimization, and profiling with Xdebug or Blackfire.

- **Q:** How does PHP-FPM improve performance?  
  **A:** Manages worker processes efficiently for concurrent request handling.

- **Q:** How does PHP 8’s JIT compiler affect performance?  
  **A:** Compiles bytecode to native machine code for faster execution in CPU-bound tasks.

# PHP - Advanced OOP & Design Patterns

### Classes & Objects

- **Q:** What is the difference between `abstract class` and `interface`?  
  **A:**

  - Abstract class: can contain implemented methods and properties; can have constructor.
  - Interface: only method signatures; no properties; multiple interfaces can be implemented.

- **Q:** What is the difference between `public`, `protected`, and `private` visibility?  
  **A:**

  - Public: accessible everywhere
  - Protected: accessible in class + subclasses
  - Private: accessible only within class

- **Q:** What are traits in PHP?  
  **A:** Reusable sets of methods to include in multiple classes (horizontal inheritance).

- **Q:** What is the difference between `static` and instance methods/properties?  
  **A:** Static belongs to the class itself, not the object; instance belongs to the object.

- **Q:** What is late static binding?  
  **A:** Refers to the called class at runtime (`static::method()`) instead of the class where method is defined.

- **Q:** What are magic methods in PHP?  
  **A:** Special methods with `__` prefix (`__construct`, `__destruct`, `__get`, `__set`, `__call`, `__toString`).

- **Q:** How do you implement cloning in PHP?  
  **A:** Use `clone` keyword; optionally define `__clone()` to customize behavior.

- **Q:** What is type hinting and return type declarations?  
  **A:** Enforces argument and return types for methods/functions (`function foo(User $user): string {}`).

- **Q:** What are namespaces and why are they important?  
  **A:** Organize classes, avoid name collisions, and allow autoloading (PSR-4).

---

### SOLID Principles

- **Q:** What does SOLID stand for?  
  **A:**

  - **S:** Single Responsibility
  - **O:** Open/Closed
  - **L:** Liskov Substitution
  - **I:** Interface Segregation
  - **D:** Dependency Inversion

- **Q:** What is the Single Responsibility Principle?  
  **A:** A class should have one reason to change; one responsibility only.

- **Q:** What is the Open/Closed Principle?  
  **A:** Classes should be open for extension, closed for modification.

- **Q:** What is the Liskov Substitution Principle?  
  **A:** Subclasses should be usable wherever parent classes are expected.

- **Q:** What is the Interface Segregation Principle?  
  **A:** Avoid fat interfaces; break interfaces into smaller, specific ones.

- **Q:** What is the Dependency Inversion Principle?  
  **A:** High-level modules should depend on abstractions (interfaces), not concrete classes.

---

### Design Patterns

- **Q:** What is the Factory Pattern?  
  **A:** Creates objects without exposing instantiation logic; centralizes creation.

- **Q:** What is the Singleton Pattern?  
  **A:** Ensures only one instance of a class exists; accessed via a static method.

- **Q:** What is the Strategy Pattern?  
  **A:** Encapsulates interchangeable algorithms; selects behavior at runtime.

- **Q:** What is the Repository Pattern?  
  **A:** Abstracts data layer logic; separates DB queries from business logic.

- **Q:** What is the Observer Pattern?  
  **A:** Objects (observers) subscribe to events emitted by a subject; Laravel events are an example.

- **Q:** What is the Decorator Pattern?  
  **A:** Dynamically adds responsibilities to objects without altering original class.

- **Q:** What is the Command Pattern?  
  **A:** Encapsulates a request as an object; allows queuing, logging, and undo operations (used in Laravel Jobs).

- **Q:** What is the Adapter Pattern?  
  **A:** Converts one interface to another expected interface; useful for integrating legacy code.

- **Q:** What is the Facade Pattern?  
  **A:** Provides a simplified static interface to a complex subsystem (used extensively in Laravel).

- **Q:** What is the Dependency Injection Pattern?  
  **A:** Pass dependencies to a class instead of creating them internally (constructor or setter injection).

- **Q:** What is the Template Method Pattern?  
  **A:** Defines a skeleton algorithm in a base class and lets subclasses override steps.

- **Q:** What is the Proxy Pattern?  
  **A:** Provides a surrogate or placeholder to control access to another object.

---

### Advanced PHP Techniques

- **Q:** How does autoloading work in modern PHP?  
  **A:** PSR-4 autoloading maps namespaces to folder structures; Composer handles autoloading automatically.

- **Q:** How do you handle dependency injection manually in plain PHP?  
  **A:** Instantiate dependencies outside and pass them into the constructor of the dependent class.

- **Q:** How do you implement immutable objects?  
  **A:** Private properties with no setters; only set values via constructor; return new instances on change.

- **Q:** What are closures and anonymous functions?  
  **A:** Functions without names; can be assigned to variables and passed as callbacks.

- **Q:** What are generators and why use them?  
  **A:** Yield values one at a time for memory-efficient iteration over large datasets.

- **Q:** What are PHP attributes (annotations)?  
  **A:** Metadata attached to classes, methods, or properties for reflection-based processing.

- **Q:** How do you handle errors and exceptions in modern PHP?  
  **A:** Use `try/catch` blocks; create custom exception classes; use type-safe error handling.

- **Q:** What is the difference between `include`, `require`, `include_once`, `require_once`?  
  **A:** `require` throws fatal error if file missing; `include` warns; `_once` ensures single inclusion.

- **Q:** How do you implement PSR standards in PHP?  
  **A:** Follow PSR-1/PSR-12 for coding style, PSR-4 for autoloading, PSR-7 for HTTP messages, PSR-11 for containers.

- **Q:** How do you test OOP classes in PHP?  
  **A:** Use PHPUnit or Pest; mock dependencies with Mockery; isolate logic for unit tests.
