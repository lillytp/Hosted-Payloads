
## 2026-06-14 - Ticker DOM and Formatter Optimization
**Learning:** High-frequency DOM updates using `innerHTML` and repeated `Intl.NumberFormat` instantiation can lead to measurable main thread overhead and GC pressure. Switching to `textContent` with cached DOM references, pre-instantiated formatters, and dirty checking (only updating if values changed) significantly reduces update execution time.
**Action:** Always cache DOM nodes and pre-instantiate locale-aware formatters outside of high-frequency loops or intervals, and implement dirty checking before DOM mutations.
