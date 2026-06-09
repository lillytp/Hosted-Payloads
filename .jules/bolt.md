## 2026-06-06 - [Ticker DOM Update Optimization]
**Learning:** Frequent use of `innerHTML` for high-frequency UI updates (like tickers or timers) leads to unnecessary DOM re-parsing and layout overhead. Pre-caching DOM element references and using `textContent` is significantly more efficient. Pre-instantiating `Intl.NumberFormat` also avoids repeated constructor overhead and provides cleaner localization.
**Action:** Always cache DOM elements for repetitive updates. Prefer `textContent` over `innerHTML` when only text content changes. Move expensive constructors (like `Intl` formatters) outside of intervals.

## 2026-06-08 - [CSS Containment for Dashboard Performance]
**Learning:** For complex dashboards with multiple independent components (like cards and tickers), the browser often performs global layout and paint operations even if only a small part of the page changes. Using `contain: content` (or `contain: strict`) on these components isolates their internal layout and paint from the rest of the document.
**Action:** Apply `contain: content` to high-level, independent UI containers to minimize layout thrashing and improve rendering efficiency during frequent updates.

## 2026-06-09 - [Consolidated Dashboard Performance Optimizations]
**Learning:** High-frequency dashboard updates (ticker, clock, charts) can be optimized by:
1. Memoizing `CanvasGradient` objects in Chart.js using a `WeakMap` to avoid redundant allocations.
2. Updating data structures (like ticker price arrays) in-place instead of creating new copies with `.map()`.
3. Using `Set` for O(1) lookups in conditional formatting logic.
4. Avoiding redundant DOM mutations by checking if `textContent` or `className` actually changed before assigning.
5. Moving static constants/arrays (like clock days/months) outside of interval callbacks.
**Action:** Apply these patterns to all real-time monitoring interfaces to minimize GC pressure and main-thread work.
