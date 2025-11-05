# React Study Guide

## 🧩 Beginner Level

- **Q:** What is React?  
  **A:** A JavaScript library for building user interfaces using reusable components.

- **Q:** What is JSX?  
  **A:** A syntax extension that allows writing HTML-like code inside JavaScript.

- **Q:** What is a component in React?  
  **A:** A reusable piece of UI logic that returns JSX — can be a function or class.

- **Q:** What is the difference between functional and class components?  
  **A:** Functional components are simpler and use Hooks; class components use lifecycle methods.

- **Q:** What are props?  
  **A:** Read-only inputs passed from parent to child components.

- **Q:** What is state in React?  
  **A:** Mutable data that determines how a component renders and behaves.

- **Q:** How do you handle events in React?  
  **A:** Use camelCase event handlers like `onClick={() => ...}`.

- **Q:** What is the purpose of the `key` prop?  
  **A:** Helps React identify and efficiently update list items.

- **Q:** What does “unidirectional data flow” mean?  
  **A:** Data flows from parent to child components via props.

- **Q:** How do you conditionally render elements?  
  **A:** Using ternary operators or logical AND (`&&`) in JSX.

---

## ⚙️ Intermediate Level

- **Q:** What are Hooks?  
  **A:** Functions like `useState`, `useEffect`, and `useContext` that add state and lifecycle features to functional components.

- **Q:** What does `useState` do?  
  **A:** Declares state variables in functional components.

- **Q:** What does `useEffect` do?  
  **A:** Handles side effects such as fetching data, subscriptions, or DOM updates.

- **Q:** How do you prevent unnecessary re-renders?  
  **A:** Use `React.memo`, `useMemo`, and `useCallback`.

- **Q:** What is `useRef` used for?  
  **A:** Accessing DOM elements or persisting mutable values without re-rendering.

- **Q:** What is context in React?  
  **A:** A way to share state globally without prop drilling (`useContext`).

- **Q:** What is prop drilling?  
  **A:** Passing props down multiple levels unnecessarily.

- **Q:** What are controlled and uncontrolled components?  
  **A:**

  - Controlled: state managed by React
  - Uncontrolled: state managed by the DOM via refs

- **Q:** How does React’s Virtual DOM work?  
  **A:** React creates an in-memory DOM representation and updates only changed elements.

- **Q:** How do you handle forms in React?  
  **A:** Use controlled inputs with `onChange` handlers bound to state.

- **Q:** What are fragments?  
  **A:** Wrapper elements (`<></>`) that let you return multiple children without extra DOM nodes.

- **Q:** What is React Router used for?  
  **A:** Handling client-side navigation in single-page applications.

---

## 🧠 Advanced Level

- **Q:** What is reconciliation in React?  
  **A:** The process of comparing the Virtual DOM to the real DOM and applying minimal updates.

- **Q:** What is the difference between mounting, updating, and unmounting?  
  **A:** Lifecycle stages: creation, re-render, and cleanup of components.

- **Q:** What is the difference between `useEffect` and `useLayoutEffect`?  
  **A:** `useEffect` runs after paint; `useLayoutEffect` runs before paint (blocking render).

- **Q:** What is the purpose of `useReducer`?  
  **A:** Manages complex state logic, similar to Redux-style reducers.

- **Q:** What is React Suspense?  
  **A:** A feature for handling asynchronous rendering and lazy loading components.

- **Q:** What is code splitting?  
  **A:** Breaking bundles into smaller chunks using dynamic `import()` to improve load performance.

- **Q:** What are React portals?  
  **A:** Render children into a DOM node outside the parent hierarchy (useful for modals).

- **Q:** How does React handle rendering performance?  
  **A:** Diffing algorithm, batching updates, and reconciliation optimizations.

- **Q:** What is the difference between server-side rendering (SSR) and client-side rendering (CSR)?  
  **A:** SSR renders HTML on the server; CSR renders content in the browser.

- **Q:** What is hydration in React?  
  **A:** Attaching event listeners to server-rendered markup on the client.

- **Q:** What is React Fiber?  
  **A:** The internal engine introduced in React 16 for incremental rendering and better scheduling.

- **Q:** What are custom hooks?  
  **A:** Reusable logic functions that encapsulate stateful behavior.

- **Q:** What are keys to optimizing large React apps?  
  **A:** Memoization, lazy loading, pagination, selective rendering, and state normalization.

- **Q:** What is a higher-order component (HOC)?  
  **A:** A function that takes a component and returns an enhanced version of it.

- **Q:** How does React 18 improve performance?  
  **A:** Introduces concurrent rendering, automatic batching, and the `useTransition` hook.

- **Q:** What are some common React anti-patterns?  
  **A:** Direct state mutation, excessive re-renders, prop drilling, and overusing context.
