# Decision Log

Append-only. Every significant decision — especially every approved gated
action — gets a dated entry. Never edit or delete past entries; add a new one
that supersedes if needed.

Format:
```
## YYYY-MM-DD — <short title>
- Decision: <what was decided>
- Made by: <operator | orchestrator>
- Context: <why>
- Gated action approved: <yes/no; if yes, what exactly>
```

---

## 2026-07-23 — System initialized
- Decision: Stand up the orchestrator + subagent system; first cycle is
  opportunity selection ("let the agent decide").
- Made by: operator
- Context: Goal of $20K in 90 days on the $200/mo subscription, ~30 min/day
  operator time, legal entity already exists, bank/Stripe not yet set up.
- Gated action approved: no (setup only).

## 2026-07-24 — Budget policy adopted
- Decision: Add `BUDGET.md`. (1) Capacity reinvestment = 2% of trailing-30-day
  revenue ("$200 per $10K"). (2) Graduate always-on workload to metered API
  once trailing revenue ≥ $2,000/mo sustained. (3) Advertising approved as a
  category (e.g. Meta ads) with a revenue-linked, ROAS-guarded envelope:
  no spend until the offer is validated + payment path live + tracking in
  place; $150 test budget; scale while ROAS ≥ 2.0 up to 30% of trailing
  revenue; kill below break-even.
- Made by: operator
- Context: Operator wants spend to scale with revenue and to allow paid
  acquisition once the funnel is proven.
- Gated action approved: yes — advertising and capacity-reinvestment envelopes
  are pre-authorized as policy. Actual spend is still operator-executed, and
  raising a standing cap remains a per-decision approval.
- Defaults (operator-adjustable): API graduation $2,000/mo; ad test $150;
  ROAS scale ≥2.0 / pause 1.0–1.5 / kill <1.0; 14-day attribution; ad cap 30%
  of trailing revenue.
