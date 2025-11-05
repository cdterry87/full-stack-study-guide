# HTML Study Guide

## 🧩 Beginner Level

- **Q:** What is HTML?  
  **A:** HyperText Markup Language; used to structure content on the web.

- **Q:** What is the difference between HTML and XHTML?  
  **A:** XHTML is stricter, requires well-formed markup, and follows XML rules.

- **Q:** What is the difference between block-level and inline elements?  
  **A:**

  - Block-level: occupies full width, starts on new line (`<div>`, `<p>`)
  - Inline: flows within text, does not start on new line (`<span>`, `<a>`)

- **Q:** What is the difference between semantic and non-semantic elements?  
  **A:** Semantic conveys meaning (`<header>`, `<article>`); non-semantic does not (`<div>`, `<span>`).

- **Q:** What are the basic structure elements of an HTML document?  
  **A:** `<!DOCTYPE html>`, `<html>`, `<head>`, `<title>`, `<body>`

- **Q:** What are meta tags and why are they important?  
  **A:** Provide metadata (character set, viewport, SEO, etc.) used by browsers and search engines.

- **Q:** What is the difference between `<section>` and `<div>`?  
  **A:** `<section>` is semantic for content sections; `<div>` is a generic container.

- **Q:** What is the difference between `<span>` and `<div>`?  
  **A:** `<span>` is inline; `<div>` is block-level.

- **Q:** What is the difference between `<a>` with `href="#"` and `href="javascript:void(0)"`?  
  **A:** `#` scrolls to top or stays on page; `javascript:void(0)` does nothing by default.

- **Q:** How do you include images?  
  **A:** `<img src="url" alt="description">`

- **Q:** How do you create a link?  
  **A:** `<a href="url">Link text</a>`

- **Q:** What are HTML forms used for?  
  **A:** Collect user input using elements like `<input>`, `<textarea>`, `<select>`, and `<button>`.

- **Q:** What are HTML lists?  
  **A:**
  - Ordered: `<ol>`
  - Unordered: `<ul>`
  - Definition: `<dl>`

---

## ⚙️ Intermediate Level

- **Q:** What is the difference between `id` and `class` in HTML?  
  **A:** `id` is unique; `class` can be reused for multiple elements.

- **Q:** What is the difference between `<strong>` and `<b>`?  
  **A:** `<strong>` is semantic for importance; `<b>` is only visual bold styling.

- **Q:** What is the difference between `<em>` and `<i>`?  
  **A:** `<em>` is semantic for emphasis; `<i>` is only visual italics.

- **Q:** What is the difference between `<head>` and `<body>`?  
  **A:** `<head>` contains metadata, scripts, and styles; `<body>` contains content visible to users.

- **Q:** How do you include external CSS and JavaScript?  
  **A:**

  - CSS: `<link rel="stylesheet" href="style.css">`
  - JS: `<script src="script.js"></script>`

- **Q:** What are data attributes in HTML?  
  **A:** Custom attributes like `data-name="value"` to store extra information for JS.

- **Q:** What is the difference between `<input type="text">` and `<textarea>`?  
  **A:** `<input>` is single-line; `<textarea>` is multi-line input.

- **Q:** What is the difference between `<script>` in `<head>` and before `</body>`?  
  **A:** `<head>` can block rendering; before `</body>` improves page load performance.

- **Q:** What is the difference between `<iframe>` and `<embed>`?  
  **A:** `<iframe>` embeds an HTML page; `<embed>` embeds external content like PDFs, videos, or apps.

- **Q:** What are ARIA roles?  
  **A:** Accessibility attributes (`role="button"`) to help assistive technologies interpret content.

- **Q:** What is the difference between relative and absolute URLs?  
  **A:** Relative: based on current page path; Absolute: full path including protocol and domain.

- **Q:** What are semantic HTML5 elements?  
  **A:** `<header>`, `<footer>`, `<article>`, `<section>`, `<main>`, `<aside>`, `<nav>`.

- **Q:** What are HTML5 input types?  
  **A:** `email`, `number`, `date`, `color`, `range`, `url`, `tel`, etc., for validation and UI hints.

- **Q:** How do you embed a video?  
  **A:** `<video src="video.mp4" controls></video>`

- **Q:** How do you embed audio?  
  **A:** `<audio src="audio.mp3" controls></audio>`

- **Q:** How do you create a table?  
  **A:** `<table>` with `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`.

---

## 🧠 Advanced Level

- **Q:** What are the differences between `<canvas>` and `<svg>`?  
  **A:**

  - `<canvas>`: pixel-based, procedural drawing, good for games and dynamic graphics
  - `<svg>`: vector-based, scalable, DOM-manipulable, good for icons and charts

- **Q:** How do you make a page accessible (a11y)?  
  **A:** Semantic HTML, ARIA roles, labels for forms, alt attributes for images, keyboard navigation, and proper contrast.

- **Q:** What is the difference between `defer` and `async` on `<script>`?  
  **A:**

  - `async`: script runs as soon as downloaded, may execute out of order
  - `defer`: script waits until HTML parsing is complete, executes in order

- **Q:** How do you structure HTML for SEO?  
  **A:** Proper use of headings (`<h1>`-`<h6>`), meta tags, semantic elements, descriptive URLs, alt text, and structured data.

- **Q:** What is the difference between `<meta name="viewport">` settings?  
  **A:** Controls layout on mobile devices; common: `<meta name="viewport" content="width=device-width, initial-scale=1.0">`

- **Q:** What are HTML templates?  
  **A:** `<template>` holds HTML that isn’t rendered until used via JavaScript.

- **Q:** What are web components in HTML?  
  **A:** Custom reusable elements with encapsulated HTML, CSS, and JS (using `<template>` and Shadow DOM).

- **Q:** How do you prevent cross-site scripting (XSS) in HTML?  
  **A:** Escape user input, use proper context for attributes, use Content Security Policy (CSP).

- **Q:** What are the differences between cookies, localStorage, and sessionStorage in HTML/JS context?  
  **A:**

  - Cookies: sent to server, limited size, persistent if set
  - localStorage: browser-only, persistent
  - sessionStorage: browser-only, cleared on tab close

- **Q:** How do you embed third-party content securely?  
  **A:** Use `iframe` with `sandbox` attribute and proper `CSP` headers.

- **Q:** How do you optimize HTML for performance?  
  **A:** Minify HTML, defer scripts, lazy-load images, use semantic markup, reduce DOM complexity.

- **Q:** What is the difference between progressive enhancement and graceful degradation?  
  **A:**
  - Progressive enhancement: build basic functionality first, add advanced features
  - Graceful degradation: build full-featured app, ensure fallback for older browsers
