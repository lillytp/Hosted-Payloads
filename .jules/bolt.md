## 2026-06-19 - [Staggered Chart.js Initialization]
**Learning:** Simultaneous initialization of multiple complex Chart.js instances on page load creates a significant long-task (>500ms) that blocks the main thread, increasing Total Blocking Time (TBT) and delaying interactivity.
**Action:** Stagger chart initializations using `requestAnimationFrame` or `setTimeout` to break up the synchronous work into smaller chunks, allowing the browser to paint frames in between and improving perceived performance.
