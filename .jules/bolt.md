## 2026-07-02 - Staggering Chart.js Initialization to reduce TBT
**Learning:** Initializing multiple Chart.js instances synchronously on page load can create significant long-tasks (>200ms) that block the main thread and increase Total Blocking Time (TBT). Breaking these up using a recursive `requestAnimationFrame` pattern allows the browser to paint and respond to user input between renders, improving load responsiveness.
**Action:** Stagger heavy synchronous UI initializations across multiple animation frames using `requestAnimationFrame`.
