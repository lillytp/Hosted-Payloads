# Bolt's Journal - Critical Learnings

## 2025-06-05 - Performance of Intl.NumberFormat vs Regex
**Learning:** While `Intl.NumberFormat` is standard and handles localization correctly, it can be slightly slower than a simple regex for basic thousand-separator formatting in high-frequency loops (e.g., millions of iterations). However, it is much more robust and safer against ReDoS.
**Action:** Use `Intl.NumberFormat` for its robustness and correctness, but pre-instantiate the formatter outside of high-frequency loops to minimize overhead.

## 2025-06-05 - CSS Containment for Dashboard Performance
**Learning:** Adding `contain: content` to independent UI components like dashboard cards can significantly reduce the cost of layout and paint by limiting the scope of changes to that specific subtree.
**Action:** Always consider `contain: content` or `contain: layout` for modular dashboard elements that update frequently.
