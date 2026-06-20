## 2026-06-19 - [Staggered Chart.js Initialization]
**Learning:** Simultaneous initialization of multiple complex Chart.js instances on page load creates a significant long-task (>500ms) that blocks the main thread, increasing Total Blocking Time (TBT) and delaying interactivity.
**Action:** Stagger chart initializations using `requestAnimationFrame` or `setTimeout` to break up the synchronous work into smaller chunks, allowing the browser to paint frames in between and improving perceived performance.

## 2026-06-20 - [Efficient Ticker Updates with DOM Caching]
**Learning:** High-frequency DOM updates (e.g., a ticker every 3s) using `innerHTML` cause significant layout thrashing and garbage collection pressure due to repeated string parsing and object allocations.
**Action:** Use a 'Profile-Cache-Mutate' pattern: cache DOM element references once, pre-instantiate `Intl.NumberFormat` for data formatting, and use a 'check-before-assign' pattern with `textContent` to minimize redundant DOM mutations and browser reflows.
