# Object-Oriented Programming (OOP) Study Guide

## 🧩 Beginner Level

- **Q:** What is Object-Oriented Programming?  
  **A:** A paradigm that structures code into objects containing data (properties) and behavior (methods).

- **Q:** What are the four main principles of OOP?  
  **A:** Encapsulation, Inheritance, Polymorphism, Abstraction.

- **Q:** What is a class?  
  **A:** A blueprint for creating objects that defines their properties and methods.

- **Q:** What is an object?  
  **A:** An instance of a class.

- **Q:** What is encapsulation?  
  **A:** Restricting direct access to data; achieved using access modifiers (`private`, `protected`, `public`).

- **Q:** What is inheritance?  
  **A:** The ability of a class to derive from another class, reusing and extending its functionality.

- **Q:** What is polymorphism?  
  **A:** The ability of different classes to define methods with the same name but different implementations.

- **Q:** What is abstraction?  
  **A:** Hiding complex implementation details and exposing only essential features.

- **Q:** What is a constructor?  
  **A:** A special method that initializes an object when it’s created.

- **Q:** What is a destructor?  
  **A:** A method automatically called when an object is destroyed.

---

## ⚙️ Intermediate Level

- **Q:** What are access modifiers?  
  **A:** Keywords controlling visibility: `public`, `protected`, and `private`.

- **Q:** What are getters and setters?  
  **A:** Methods used to access or modify private properties safely.

- **Q:** What is method overriding?  
  **A:** Redefining a parent class’s method in a child class.

- **Q:** What is method overloading?  
  **A:** Defining multiple methods with the same name but different parameters (PHP does not support this natively, but can be simulated).

- **Q:** What is the difference between an abstract class and an interface?  
  **A:** Abstract classes can have concrete methods; interfaces define only method signatures.

- **Q:** What are static methods and properties?  
  **A:** Belong to the class rather than any instance; accessed using `ClassName::method()`.

- **Q:** What is the difference between composition and inheritance?  
  **A:** Composition builds classes from other objects; inheritance extends from a base class.

- **Q:** What are magic methods in OOP?  
  **A:** Special methods like `__construct()`, `__get()`, `__set()`, `__toString()`, `__call()` for dynamic behavior.

- **Q:** What is late static binding?  
  **A:** Allows static references in inherited methods to use the child class context (`static::` vs. `self::`).

- **Q:** What is the purpose of interfaces?  
  **A:** To define a contract that implementing classes must follow.

---

## 🧠 Advanced Level

- **Q:** What are SOLID principles?  
  **A:**

  - **S:** Single Responsibility — one reason to change
  - **O:** Open/Closed — open to extension, closed to modification
  - **L:** Liskov Substitution — subclasses must be replaceable for their base class
  - **I:** Interface Segregation — many small, specific interfaces
  - **D:** Dependency Inversion — depend on abstractions, not concretions

- **Q:** What is the Dependency Injection principle?  
  **A:** Providing dependencies externally rather than creating them inside the class.

- **Q:** What is the difference between tight coupling and loose coupling?  
  **A:** Tight coupling means classes depend heavily on each other; loose coupling increases flexibility and testability.

- **Q:** What are design patterns?  
  **A:** Reusable solutions to common software design problems (e.g., Singleton, Factory, Strategy, Observer).

- **Q:** Explain the Factory Pattern.  
  **A:** Encapsulates object creation logic in a single place to decouple instantiation from use.

- **Q:** Explain the Strategy Pattern.  
  **A:** Allows switching algorithms or behaviors at runtime using interchangeable objects.

- **Q:** Explain the Observer Pattern.  
  **A:** Defines a one-to-many dependency so that when one object changes state, others are notified.

- **Q:** What is the difference between an interface and a trait?  
  **A:** Interfaces define contracts; traits provide reusable code for multiple classes.

- **Q:** What is the purpose of the Repository Pattern?  
  **A:** Abstracts data access logic, providing a consistent API for working with data sources.

- **Q:** What is an example of violating the Single Responsibility Principle?  
  **A:** A class that handles both database logic and email notifications.

- **Q:** What is a Data Transfer Object (DTO)?  
  **A:** A simple object used to carry data between layers without business logic.

- **Q:** What are anti-patterns in OOP?  
  **A:** Poor practices like God Objects, Spaghetti Code, or overuse of Singletons.

- **Q:** How can you achieve polymorphism without inheritance?  
  **A:** By using interfaces or dependency injection to swap implementations.

- **Q:** What’s the difference between aggregation and composition?  
  **A:** Composition = strong ownership (child destroyed with parent); Aggregation = weak ownership (child exists independently).

- **Q:** What is the Law of Demeter?  
  **A:** “Talk to friends, not strangers” — a method should only interact with direct dependencies.

- **Q:** How do you test OOP code effectively?  
  **A:** Use dependency injection, mock interfaces, and write unit tests for isolated logic.
