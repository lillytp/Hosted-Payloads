## 2026-06-25 - [Staggered Chart Initialization]
**Learning:** Synchronous initialization of multiple Chart.js instances can block the main thread for over 500ms, leading to high Total Blocking Time (TBT). Using `requestAnimationFrame` to stagger initializations effectively breaks these into smaller tasks across separate frames, improving responsiveness. A recursive or loop-based approach is more maintainable than nesting callbacks.
**Action:** Use `requestAnimationFrame` with a maintainable scheduling pattern to stagger heavy UI initializations on dashboard loads.
