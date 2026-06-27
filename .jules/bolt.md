## 2026-06-06 - [Ticker DOM Update Optimization]
**Learning:** Frequent use of `innerHTML` for high-frequency UI updates (like tickers or timers) leads to unnecessary DOM re-parsing and layout overhead. Pre-caching DOM element references and using `textContent` is significantly more efficient. Pre-instantiating `Intl.NumberFormat` also avoids repeated constructor overhead and provides cleaner localization.
**Action:** Always cache DOM elements for repetitive updates. Prefer `textContent` over `innerHTML` when only text content changes. Move expensive constructors (like `Intl` formatters) outside of intervals.

## 2026-06-08 - [CSS Containment for Dashboard Performance]
**Learning:** For complex dashboards with multiple independent components (like cards and tickers), the browser often performs global layout and paint operations even if only a small part of the page changes. Using `contain: content` (or `contain: strict`) on these components isolates their internal layout and paint from the rest of the document.
**Action:** Apply `contain: content` to high-level, independent UI containers to minimize layout thrashing and improve rendering efficiency during frequent updates.

## 2026-06-15 - [Minimizing Redundant DOM Mutations with Check-Before-Assign]
**Learning:** Even when using `textContent`, assigning a value to a DOM property that is already set to that same value can still trigger unnecessary browser work or at least consume execution time. Implementing a "check-before-assign" pattern (e.g., `if (el.textContent !== newValue) el.textContent = newValue;`) significantly reduces the overhead during high-frequency update loops, especially when many values remain static between intervals.
**Action:** Always verify if the target DOM property value has changed before performing the assignment in high-frequency update loops.
