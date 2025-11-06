# Full-Stack Study Guide

### Table of Contents

- [CSS](css.md)
- [DEVOPS](devops.md)
- [GIT](git.md)
- [HTML](html.md)
- [JAVASCRIPT](js.md)
- [LARAVEL](laravel.md)
- [LINUX](linux.md)
- [MYSQL](mysql.md)
- [OOP](oop.md)
- [PHP](php.md)
- [REACT](react.md)
- [SECURITY](security.md)

---

- [My Real World Examples](EXAMPLES.md)

---

### Overview

## 🏗️ Backend Architecture (PHP/Laravel)

### Service Container & Dependency Injection

- Centralizes object creation and dependency management.
- Constructor, method, and property injection patterns.
- `bind()` vs `singleton()` in the container.
- Auto-resolution of type-hinted dependencies.
- Swapping implementations for testing (contracts vs concrete classes).

### Service Providers

- `register()` vs `boot()` methods.
- Deferred providers for performance.
- Organizing providers for modular apps.

### Design Patterns in Laravel

- **Repository Pattern:** abstracts DB layer from business logic.
- **Service Pattern:** organizes domain/business logic.
- **Observer/Event Pattern:** decoupled event handling.
- **Strategy Pattern:** interchangeable algorithms (e.g., payments, notifications).
- **Command Pattern:** queued jobs or tasks.
- **Decorator Pattern:** dynamically extend object behavior.
- **Facade Pattern:** static interface over container services.

### Eloquent & Database Layer

- Query scopes, polymorphic relations, pivot tables, and many-to-many.
- Optimized eager loading vs lazy loading.
- Repository + Service layer for clean architecture.
- Database caching strategies.
- Migration & seeding best practices.

### Security & Authentication

- Laravel built-in auth (Sanctum, Passport, JWT).
- CSRF, XSS, SQL injection protection.
- Role-based and policy-based authorization.
- Secure password hashing and token management.

### Testing & Quality

- Unit tests (PHPUnit), integration tests, feature tests.
- Mocking dependencies using container binding.
- Test-driven development workflow in Laravel.

---

## 🌐 Frontend Architecture (JS/React)

### Component Architecture

- Functional vs Class components.
- Hooks (useState, useEffect, useReducer, custom hooks).
- Prop drilling vs Context API for state management.
- Lifting state vs global state solutions (Redux, Zustand).

### Design Patterns

- Container/Presentational pattern.
- Higher-Order Components (HOC) vs Render Props.
- Hook-based composition pattern.
- Lazy-loading components for performance.

### State Management & Data Flow

- Centralized store patterns (Redux or Context).
- Optimistic updates, caching, and immutability.
- Handling async API calls with fetch, Axios, or RTK Query.

### Security

- XSS prevention in JSX.
- CSRF handling in SPA + API.
- Authentication flows: JWT, OAuth2, session tokens.

### Performance & Optimization

- Code splitting, lazy loading, memoization (`React.memo`, `useMemo`, `useCallback`).
- Virtualization for large lists.
- Minimizing re-renders and unnecessary state updates.

---

## 💾 Database & API Architecture

### Database Design

- Normalization vs denormalization trade-offs.
- Indexing, query optimization, and foreign keys.
- Polymorphic associations and pivot tables in relational DBs.
- Transactions, optimistic vs pessimistic locking.

### API Design

- RESTful principles: resource-based endpoints, proper status codes.
- GraphQL: queries vs mutations, resolvers, batching.
- Versioning strategies for long-term maintenance.
- Pagination, filtering, and caching for large datasets.

### Security

- Rate limiting and throttling.
- Input validation and output encoding.
- Authentication and authorization strategies (OAuth2, JWT, API tokens).

---

## 🛠️ DevOps & Deployment

### Continuous Integration / Continuous Deployment

- Automated testing pipelines (GitHub Actions, GitLab CI/CD).
- Deployment pipelines: staging → production.
- Rollbacks, blue/green deployments, canary releases.

### Containerization & Virtualization

- Docker for development and production parity.
- Docker Compose for multi-service apps.
- Kubernetes for orchestrating container clusters.

### Monitoring & Logging

- Centralized logging (Monolog, ELK stack).
- Application performance monitoring (New Relic, Blackfire, Sentry).
- Health checks and uptime monitoring.

### Scaling & Load Management

- Horizontal vs vertical scaling.
- Database read replicas and load balancers.
- Caching strategies: Redis, Memcached.

---

## 🧩 Architectural Principles & Patterns

### SOLID Principles

- Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion.

### Clean Architecture

- Separation of concerns: Controllers → Services → Repositories → Models.
- Dependency rule: inner layers unaware of outer layers.

### Modular & Package-based Design

- Reusable modules, Laravel packages, npm packages.
- Service-oriented or microservice architecture considerations.

### Testing & Maintainability

- Test coverage and automation.
- Mocking dependencies and using contracts/interfaces.
- Refactoring strategies and code reviews.

---

## ⚡ Advanced Topics

- CQRS (Command Query Responsibility Segregation) in Laravel apps.
- Event sourcing and audit logging.
- WebSockets and real-time applications (Laravel Echo + Pusher).
- Multi-tenant architecture in Laravel (single DB vs multiple DBs).
- Caching patterns: query caching, fragment caching, full-page caching.
- API rate limiting, throttling, and request validation.
