# Laravel Study Guide

## 🧩 Beginner Level

- **Q:** What is Laravel?  
  **A:** A PHP web framework following the MVC pattern, known for its elegant syntax and developer productivity.

- **Q:** What is Composer used for in Laravel?  
  **A:** Dependency management; installs Laravel and its packages.

- **Q:** What are Service Providers?  
  **A:** Central place where Laravel bootstraps components like routes, events, and bindings.

- **Q:** What is Eloquent ORM?  
  **A:** Laravel’s built-in ORM for interacting with databases using models.

- **Q:** What is a Migration?  
  **A:** Version control for database schema; allows schema changes via code.

- **Q:** What are Blade templates?  
  **A:** Laravel’s templating engine that supports layout inheritance and control structures.

- **Q:** What are middleware?  
  **A:** Filters that run before/after requests — used for authentication, logging, etc.

- **Q:** What is the purpose of `.env` file?  
  **A:** Stores environment-specific configuration values.

- **Q:** How do you create a controller?  
  **A:** `php artisan make:controller ExampleController`

- **Q:** What command runs database migrations?  
  **A:** `php artisan migrate`

---

## ⚙️ Intermediate Level

- **Q:** What is dependency injection in Laravel?  
  **A:** Laravel automatically provides class dependencies via the service container.

- **Q:** Difference between `include`, `require`, and Laravel’s Blade `@include`?  
  **A:** Blade `@include` compiles into cached PHP and handles missing files gracefully.

- **Q:** What are queues in Laravel?  
  **A:** Used to defer time-consuming tasks (e.g., sending emails) for background processing.

- **Q:** How does Laravel handle caching?  
  **A:** Unified cache API supports drivers like file, Redis, memcached, database.

- **Q:** What is the purpose of Events and Listeners?  
  **A:** Decouple logic by triggering actions when specific events occur.

- **Q:** Explain Route Model Binding.  
  **A:** Automatically resolves route parameters to model instances.

- **Q:** How do you validate form requests?  
  **A:** Use `FormRequest` classes or `validate()` method in controllers.

- **Q:** What is a Policy?  
  **A:** Class that handles authorization logic for a model.

- **Q:** What are Laravel Collections?  
  **A:** Extended arrays with chainable methods like `map()`, `filter()`, `pluck()`.

- **Q:** What are Accessors and Mutators?  
  **A:** Methods to format attributes when getting/setting model properties.

---

## 🧠 Advanced Level

- **Q:** What are Service Containers used for?  
  **A:** Managing class dependencies and performing dependency injection.

- **Q:** Explain how Laravel’s request lifecycle works.  
  **A:** Request enters `public/index.php` → Kernel → Middleware → Routes → Controller → Response → Middleware → Client.

- **Q:** What is a Repository Pattern?  
  **A:** Abstracts data persistence logic, improving testability and maintainability.

- **Q:** What are Jobs and Workers?  
  **A:** Jobs represent tasks queued for background processing; Workers process them.

- **Q:** How does Laravel handle lazy vs. eager loading in Eloquent?  
  **A:** Lazy loads relationships when accessed; eager loads upfront with `with()` to reduce queries.

- **Q:** What are Laravel’s Broadcasting features?  
  **A:** Real-time event broadcasting using Pusher, Redis, or WebSockets.

- **Q:** How do you optimize performance in Laravel apps?  
  **A:** Cache config/routes/views, optimize queries, use queues, and minimize autoloaded services.

- **Q:** What are macros in Laravel?  
  **A:** Custom methods you can add to classes like Collections, Request, etc.

- **Q:** How does Laravel handle testing?  
  **A:** Built-in PHPUnit integration with `php artisan test`; supports unit, feature, and browser tests.

- **Q:** How would you design a multi-tenant Laravel application?  
  **A:** Use scoped models, database-per-tenant, or schema separation with middleware to set tenant context.

# Laravel - More Advanced Topics

### Service Container / IoC / Dependency Injection

- **Q:** What is the Laravel service container?  
  **A:** A powerful tool that manages class dependencies and performs dependency injection automatically.

- **Q:** What is IoC (Inversion of Control)?  
  **A:** A principle where the framework controls the creation of objects rather than the developer. Laravel’s service container implements IoC.

- **Q:** What is dependency injection (DI)?  
  **A:** A technique where dependencies are “injected” into a class rather than the class instantiating them manually.

- **Q:** What is the difference between constructor injection, method injection, and property injection in Laravel?  
  **A:**

  - Constructor: inject dependencies via class constructor
  - Method: inject into controller/action methods
  - Property: inject via setter or public property (less common)

- **Q:** How do you bind classes/interfaces in the Laravel service container?  
  **A:**

  - `App::bind(Interface::class, Implementation::class)` — new instance each time
  - `App::singleton(Interface::class, Implementation::class)` — shared instance

- **Q:** How do you resolve a class from the service container manually?  
  **A:** `app(ClassName::class)` or `resolve(ClassName::class)`

- **Q:** How does automatic resolution (auto-wiring) work in Laravel?  
  **A:** Laravel inspects type-hinted dependencies in constructors or methods and resolves them automatically from the container.

- **Q:** What is the difference between `bind` and `singleton`?  
  **A:** `bind` creates a new instance every time; `singleton` always returns the same instance.

- **Q:** How do you inject configuration or primitive values?  
  **A:** Use `App::bind` or closures:
  ```php
  App::bind(Foo::class, fn($app) => new Foo(config('app.value')));
  ```

---

### Service Providers

- **Q:** What is a service provider?
  **A:** The central place to register bindings, event listeners, middleware, and perform bootstrapping in Laravel.

- **Q:** What are the main methods of a service provider?
  **A:**

  - `register()`: bind classes and services to the container
  - `boot()`: perform actions after all services are registered

- **Q:** How do you create a custom service provider?
  **A:** `php artisan make:provider MyServiceProvider` and register it in `config/app.php` if not auto-discovered.

- **Q:** How does deferred service providers work?
  **A:** Loaded only when one of their bindings is resolved, improving performance.

---

### Advanced Design Patterns in Laravel

- **Q:** What design patterns are commonly used in Laravel?
  **A:**

  - **Repository Pattern:** abstracts database queries
  - **Strategy Pattern:** swaps algorithms at runtime
  - **Factory Pattern:** creates objects without exposing instantiation logic
  - **Singleton Pattern:** ensures a class has one instance (used in services)
  - **Observer Pattern:** events and listeners
  - **Decorator Pattern:** adds behavior dynamically
  - **Facade Pattern:** provides static interface to services in container

- **Q:** How do facades work in Laravel?
  **A:** Facades are “static proxies” that resolve underlying classes from the service container at runtime.

- **Q:** What is the Repository Pattern?
  **A:** Abstracts the data layer to separate logic for querying models from business logic.

- **Q:** What is the Strategy Pattern and how is it used in Laravel?
  **A:** Define interchangeable algorithms for a task; used in payments, notifications, or report generation.

- **Q:** What is the Observer Pattern in Laravel?
  **A:** Hooks into Eloquent model events (`creating`, `updating`, `deleting`) via observers.

- **Q:** What is the difference between an event and a listener?
  **A:** Event: something that happened; Listener: code that responds to it.

- **Q:** How do Laravel jobs relate to design patterns?
  **A:** Jobs implement the **Command Pattern**, encapsulating actions for queues and delayed execution.

- **Q:** How does middleware relate to the decorator pattern?
  **A:** Middleware wraps request handling, modifying or extending functionality dynamically.

- **Q:** How do you implement dependency injection in controllers?
  **A:** Type-hint dependencies in constructor or methods; Laravel resolves them automatically.

- **Q:** How do you inject services into Form Requests?
  **A:** Type-hint services in the `authorize()` or `rules()` methods; Laravel resolves them via container.

- **Q:** What is the difference between `resolve()` and `app()` helper functions?
  **A:** Both resolve services from the container; `app()` can also bind and check if bound.

---

### Advanced Eloquent & Query Patterns

- **Q:** What is an Eloquent scope?
  **A:** A reusable query snippet defined in a model:

  ```php
  public function scopeActive($query) { return $query->where('active', 1); }
  ```

- **Q:** How do you implement the Repository + Service pattern?
  **A:**

  - Repository handles DB queries
  - Service handles business logic
  - Controller depends on the service

- **Q:** What is the difference between `hasOne`, `hasMany`, `belongsTo`, `belongsToMany`?
  **A:** Defines relationships between Eloquent models; `belongsToMany` handles pivot tables.

- **Q:** How do you implement polymorphic relationships?
  **A:** Use `morphMany`, `morphTo`, or `morphOne` for models that share relationships across multiple types.

- **Q:** What is query caching in Laravel?
  **A:** Store query results in cache to reduce DB load:

  ```php
  Cache::remember('users', 60, fn() => User::all());
  ```

---

### Advanced Features & Best Practices

- **Q:** How do you handle configuration caching?
  **A:** `php artisan config:cache` to improve performance.

- **Q:** How do you handle route caching?
  **A:** `php artisan route:cache` for faster route registration.

- **Q:** How do you manage large projects with multiple services?
  **A:** Use modular architecture: service providers, repositories, service classes, and Laravel packages.

- **Q:** How do you implement API versioning in Laravel?
  **A:** Use route prefixes, middleware, or separate controllers/namespaces per version.

- **Q:** How do you test classes that rely on DI?
  **A:** Use mocking frameworks (PHPUnit + Mockery) and inject mock services via constructor or container.

- **Q:** What are Laravel macros?
  **A:** Dynamically add methods to existing classes like Collections, Response, or Str.

- **Q:** What is the difference between contracts and implementations in Laravel?
  **A:** Contracts (interfaces) define expected behavior; implementations provide concrete logic.

- **Q:** How do you bind interfaces to implementations for testing?
  **A:** Use the service container to swap implementations in `AppServiceProvider` or testing setup.

- **Q:** How do you create a Laravel package?
  **A:** Organize classes, publish config/views/migrations, register a service provider, optionally bind to container.
