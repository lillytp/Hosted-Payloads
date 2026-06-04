# Bolt's Journal - Critical Learnings

## 2025-06-04 - DOM Churn in Ticker Updates
**Learning:** Using `innerHTML` for frequent updates (e.g., every 3 seconds) causes unnecessary DOM churn and re-parsing. Granular updates using `textContent` and `className` are much more efficient.
**Action:** Always prefer caching DOM elements and updating their properties directly for high-frequency UI updates.
