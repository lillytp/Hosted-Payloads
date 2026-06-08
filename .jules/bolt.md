## 2026-06-06 - [Ticker DOM Update Optimization]
**Learning:** Frequent use of `innerHTML` for high-frequency UI updates (like tickers or timers) leads to unnecessary DOM re-parsing and layout overhead. Pre-caching DOM element references and using `textContent` is significantly more efficient. Pre-instantiating `Intl.NumberFormat` also avoids repeated constructor overhead and provides cleaner localization.
**Action:** Always cache DOM elements for repetitive updates. Prefer `textContent` over `innerHTML` when only text content changes. Move expensive constructors (like `Intl` formatters) outside of intervals.

## 2026-06-08 - [CSS Containment for Dashboard Performance]
**Learning:** For complex dashboards with multiple independent components (like cards and tickers), the browser often performs global layout and paint operations even if only a small part of the page changes. Using `contain: content` (or `contain: strict`) on these components isolates their internal layout and paint from the rest of the document.
**Action:** Apply `contain: content` to high-level, independent UI containers to minimize layout thrashing and improve rendering efficiency during frequent updates.
