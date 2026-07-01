## 2026-06-25 - Staggering Chart.js Initialization
**Learning:** Simultaneous initialization of multiple Chart.js instances creates a significant long task (>500ms) that blocks the main thread during page load. Breaking these up using nested `requestAnimationFrame` calls allows the browser to remain responsive between renders.
**Action:** Use a recursive or loop-based `requestAnimationFrame` pattern to stagger heavy synchronous UI initializations.

## 2026-06-25 - Check-before-assign for DOM Updates
**Learning:** High-frequency updates (like a 30s clock or 3s ticker) can cause unnecessary DOM churn if the content hasn't actually changed.
**Action:** Implement a "check-before-assign" pattern (comparing `textContent` or `innerHTML`) before performing DOM mutations to minimize layout and paint overhead.
