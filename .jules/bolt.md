## 2026-06-24 - [Ticker DOM Update Optimization]
**Learning:** Using 'innerHTML' for high-frequency updates causes significant DOM churn and re-parsing. Direct 'textContent' updates are much more efficient.
**Action:** Always prefer 'textContent' and cached DOM references for periodic UI updates.

## 2026-06-24 - [CSS Containment for Dashboard Performance]
**Learning:** 'contain: content' limits the browser's layout/paint scope to independent components, which is critical for dashboards with multiple updating charts and tickers.
**Action:** Apply 'contain: content' to independent dashboard cards to reduce layout thrashing.
