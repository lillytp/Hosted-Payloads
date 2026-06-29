## 2026-06-29 - [Staggered Chart Initialization]
**Learning:** Initializing multiple Chart.js instances synchronously can create a significant long task (>500ms on some devices), blocking the main thread and increasing Total Blocking Time (TBT).
**Action:** Use a recursive `requestAnimationFrame` pattern to stagger chart initializations into separate frames. This breaks the single long task into multiple small tasks, allowing the browser to handle other events and repaints in between, significantly improving page load responsiveness.
