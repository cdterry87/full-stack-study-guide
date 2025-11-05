# CSS Study Guide

## 🧩 Beginner Level

- **Q:** What is CSS?  
  **A:** Cascading Style Sheets; used to style HTML elements (colors, fonts, layout).

- **Q:** What are the different types of CSS?  
  **A:** Inline (`style=""`), Internal (`<style>`), and External (`.css` files).

- **Q:** What is the difference between `id` and `class` in CSS?  
  **A:** `id` is unique per page; `class` can be reused on multiple elements.

- **Q:** What are pseudo-classes and pseudo-elements?  
  **A:**

  - Pseudo-class: `:hover`, `:focus` (state of element)
  - Pseudo-element: `::before`, `::after` (parts of element)

- **Q:** What is the difference between `relative`, `absolute`, `fixed`, and `sticky` positioning?  
  **A:**

  - `relative`: moves relative to normal position
  - `absolute`: positioned relative to nearest positioned ancestor
  - `fixed`: positioned relative to viewport
  - `sticky`: toggles between relative and fixed depending on scroll

- **Q:** What is the difference between `inline`, `block`, and `inline-block` elements?  
  **A:**

  - `inline`: flows with text, no width/height control
  - `block`: starts on new line, can set width/height
  - `inline-block`: inline flow but allows width/height

- **Q:** What is the difference between `em`, `rem`, `%`, and `px` units?  
  **A:**

  - `px`: fixed pixels
  - `%`: relative to parent
  - `em`: relative to parent font-size
  - `rem`: relative to root font-size

- **Q:** What is the difference between relative and absolute font sizing?  
  **A:** Relative scales with parent/root; absolute uses fixed units like `px`.

- **Q:** What is the difference between `visibility: hidden` and `display: none`?  
  **A:** `visibility: hidden` hides but occupies space; `display: none` removes element from layout.

- **Q:** What is the difference between `id` and `class` selectors?  
  **A:** `id` uses `#` and is unique; `class` uses `.` and can target multiple elements.

---

## ⚙️ Intermediate Level

- **Q:** What is the difference between `relative`, `absolute`, and `fixed` in z-index context?  
  **A:** Only positioned elements (`relative`, `absolute`, `fixed`, `sticky`) respond to z-index.

- **Q:** What is the difference between `inline`, `block`, and `flex` layout?  
  **A:**

  - `inline`: horizontal flow, no container control
  - `block`: vertical stacking
  - `flex`: flexible box for layout (row/column, alignment, spacing)

- **Q:** What is the difference between `absolute`, `fixed`, and `sticky`?  
  **A:**

  - `absolute`: relative to nearest positioned ancestor
  - `fixed`: relative to viewport
  - `sticky`: behaves like `relative` until scroll threshold, then fixed

- **Q:** What is the difference between `relative` and `absolute` positioning?  
  **A:** `relative` moves relative to original position; `absolute` removes element from normal flow.

- **Q:** What is the difference between inline, inline-block, and block elements?  
  **A:**

  - Inline: flows in text
  - Block: takes full width
  - Inline-block: flows inline but supports width/height

- **Q:** What is the difference between `position: static` and `position: relative`?  
  **A:** `static` is default, no positioning; `relative` allows offset via top/right/bottom/left.

- **Q:** What is the difference between `min-width`, `max-width`, and `width`?  
  **A:**

  - `width`: normal width
  - `min-width`: prevents element from shrinking below a value
  - `max-width`: prevents element from growing above a value

- **Q:** What are media queries?  
  **A:** CSS rules applied conditionally based on viewport size or device characteristics.

- **Q:** What is the difference between `absolute`, `fixed`, and `sticky` in terms of scrolling behavior?  
  **A:**

  - Absolute: scrolls with page
  - Fixed: stays in viewport
  - Sticky: scrolls until threshold, then fixed

- **Q:** What is the difference between relative, absolute, fixed, and sticky in stacking context?  
  **A:** Only positioned elements (`relative`, `absolute`, `fixed`, `sticky`) respond to z-index.

- **Q:** What is the difference between `inline`, `block`, and `flex` layout?  
  **A:** Inline: horizontal, no container control; Block: vertical; Flex: flexible box for alignment and spacing.

- **Q:** What is the difference between absolute, fixed, and sticky?  
  **A:** Absolute: relative to nearest positioned ancestor; Fixed: relative to viewport; Sticky: relative until scroll threshold.

---

## 🧠 Advanced Level

- **Q:** What is the difference between `relative` and `absolute` positioning?  
  **A:** Relative moves relative to normal flow; absolute removes element from flow and positions relative to nearest ancestor.

- **Q:** What is the difference between inline, inline-block, and block elements?  
  **A:** Inline: flows with text; Block: full width; Inline-block: inline but supports width/height.

- **Q:** What is the difference between `vh`, `vw`, `%`, and `px` units?  
  **A:**

  - `px`: fixed pixels
  - `%`: relative to parent
  - `vh`: viewport height
  - `vw`: viewport width

- **Q:** What is the difference between absolute, fixed, and sticky in stacking context?  
  **A:** Only positioned elements (`relative`, `absolute`, `fixed`, `sticky`) respond to z-index.

- **Q:** What are pseudo-classes vs pseudo-elements?  
  **A:**

  - Pseudo-class: selects element states (`:hover`, `:focus`)
  - Pseudo-element: selects part of element (`::before`, `::after`)

- **Q:** What is the difference between CSS Grid and Flexbox?  
  **A:**

  - Flexbox: one-dimensional layout (row or column)
  - Grid: two-dimensional layout (rows + columns)

- **Q:** What is the difference between relative, absolute, fixed, and sticky in CSS stacking and positioning?  
  **A:**

  - Relative: offset from normal flow
  - Absolute: positioned relative to nearest ancestor
  - Fixed: pinned to viewport
  - Sticky: behaves like relative until threshold

- **Q:** What is the difference between rem and em?  
  **A:** `em` is relative to parent font-size; `rem` is relative to root font-size.

- **Q:** How do you prevent layout shift during loading?  
  **A:** Set explicit width/height, use CSS aspect-ratio, or reserve space for images/fonts.

- **Q:** How do you implement a responsive design?  
  **A:** Media queries, flexible units (`%, vw, vh, em, rem`), CSS Grid/Flexbox, and mobile-first approach.

- **Q:** How do you handle browser compatibility?  
  **A:** Vendor prefixes, fallbacks, feature detection, and testing on major browsers.

- **Q:** What is the difference between relative, absolute, fixed, and sticky positioning in modern CSS layouts?  
  **A:** Relative: offset from normal; Absolute: removed from flow; Fixed: viewport pinned; Sticky: toggles between relative and fixed.

- **Q:** How do you optimize CSS for performance?  
  **A:** Minify CSS, remove unused rules, combine files, use shorthand, and avoid deep selectors.
