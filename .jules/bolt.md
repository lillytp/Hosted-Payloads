## 2026-06-28 - [Staggered Chart.js Initialization]
**Learning:** Initializing multiple Chart.js instances synchronously during page load can cause significant main-thread blocking (e.g., >500ms), leading to poor Total Blocking Time (TBT) and high First Input Delay (FID).
**Action:** Stagger heavy synchronous initializations like Chart.js using nested `requestAnimationFrame` calls. This breaks up the work into separate frames, allowing the browser to handle user input between tasks and significantly reducing TBT (e.g., from ~515ms to ~95ms).
