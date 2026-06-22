## 2026-06-21 - Optimized Ticker DOM Updates
**Learning:** Replacing `innerHTML` with direct `textContent` and `className` updates, combined with a "check-before-assign" pattern, eliminates unnecessary DOM thrashing and layout reflows in high-frequency UI components like stock tickers. Caching DOM element references outside the update loop further reduces selection overhead.
**Action:** Use specific child element selectors and cache them at initialization for periodic UI updates. Always verify that a value has actually changed before performing a DOM write.
