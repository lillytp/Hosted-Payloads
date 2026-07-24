# Budget Policy

The single source of truth for money rules. Two funded envelopes —
**capacity reinvestment** and **advertising** — plus the rule for graduating
to metered API capacity. All figures are defaults the operator can change;
change them here and note it in `DECISION_LOG.md`.

"Trailing revenue" always means **verified revenue in the last 30 days** from
`LEDGER.md`. Only confirmed transactions count — never projections.

---

## 1. Capacity reinvestment (the "$200 per $10K" rule)

Reinvest **2% of trailing-30-day revenue** into agent capacity (Claude
subscription seats and/or metered API). This is the "$200 per $10,000" rule
expressed as a ratio so it scales automatically.

- Floor: the base $200/mo subscription is always covered.
- At $10K trailing revenue → ~$200/mo capacity budget. At $50K → ~$1,000/mo.
- This envelope funds *capacity only* (compute), not ads.

**Capacity graduation to metered API:** while trailing-30-day revenue is below
**$2,000/mo**, stay on the flat $200 subscription and spawn agents
deliberately. Once trailing revenue is **≥ $2,000/mo sustained** (two
consecutive weeks), the operator may move the always-on / background workload
to metered API credits, funded from this 2% envelope. Rationale: below that
line, compute is not the binding constraint and metered spend isn't justified;
above it, API removes the usage-cap ceiling and "2% of revenue" becomes a
literal, tunable budget.

## 2. Advertising budget

Advertising (e.g. Meta ads, and similar paid channels) is an **approved
category** with a revenue-linked, profit-guarded envelope. Ad spend is
fundamentally different from capacity spend: it should scale with *proven
return*, not be capped at a flat ratio.

**Preconditions — no ad spend until all three are true:**
1. The payment path is live (bank + Stripe) so revenue can actually land.
2. The offer is **validated**: at least a few real sales earned organically or
   by hand, proving the funnel converts. Do not pour money into an unproven
   offer.
3. Conversion tracking is in place so ROAS can be measured honestly.

**Test phase:** start with an operator-approved test budget of **$150** on a
single channel to gather real ROAS data. One channel at a time.

**ROAS guardrails** (ROAS = revenue attributable to ads ÷ ad spend, measured
within a **14-day** attribution/payback window):
- **ROAS ≥ 2.0** → the channel is working; may scale (see below).
- **1.0 ≤ ROAS < 1.5** → pause and diagnose before spending more.
- **ROAS < 1.0** (losing money) → **kill the campaign.** No exceptions on hope.

**Scaling cap:** while ROAS stays **≥ 2.0**, the standing ad budget may scale up
to **30% of trailing-30-day revenue**. Raising the standing cap beyond that, or
above the current cap at any time, is an operator-approved decision.

## 2b. Reinvestment allocation (capacity, ads, tooling, people)

The operator has authorized reinvesting a share of revenue back into growth.
Each cycle the finance-officer computes what's available and the orchestrator
may propose an allocation across four buckets:

- **Capacity** — standing envelope, §1 (2% of trailing revenue).
- **Advertising** — standing envelope, §2 (ROAS-guarded, up to 30%).
- **Tooling** — small paid tools/services that clear their own cost. Each new
  paid tool is an operator-approved decision.
- **People (contractors / sales staff)** — see below.

**Guardrail:** reinvestment is funded from realized margin, not hope. The
finance-officer must confirm the business can cover an allocation from actual
trailing revenue before it's proposed — never spend the business toward
insolvency to chase the goal.

**People / sales staff:**
- Proposed **only** once there's a *proven, repeatable* sales motion and the
  unit economics show a human clearly pays for themselves (e.g. a closer whose
  added conversion more than covers their cost).
- **Hiring is always a per-decision operator approval** — it involves a real
  person, payment, and legal/tax commitments. The agent may draft the role, the
  scope, and the comp proposal; the **operator** does the hiring, contracting,
  and paying.
- Start with a bounded trial engagement (defined scope, defined spend), measure,
  then decide to continue. No open-ended commitments.

## 3. How budgets interact with approval gates

These envelopes change *who pre-authorizes the category*, not who executes the
spend:

- The **operator authorizes** each envelope and any increase to a standing cap.
- The **operator executes the actual spend** — configuring billing in the ad
  platform, paying invoices, entering payment details. Agents cannot and do not
  touch payment instruments.
- **Within an approved cap**, agents may *plan, build, and manage* campaigns
  (targeting, creative, budget allocation, optimization) and must report
  performance honestly against the ROAS guardrails.
- Everything outside these two envelopes remains fully gated per
  `APPROVAL_GATES.md`. A new paid tool, a one-off purchase, a price change —
  still individually approved.

## 4. Standing values (edit here)

| Rule | Value |
|---|---|
| Capacity reinvestment | 2% of trailing-30-day revenue |
| API graduation threshold | trailing revenue ≥ $2,000/mo, 2 weeks sustained |
| Ad test budget | $150, single channel |
| ROAS scale threshold | ≥ 2.0 |
| ROAS pause band | 1.0–1.5 |
| ROAS kill threshold | < 1.0 |
| Ad attribution window | 14 days |
| Ad scaling cap | 30% of trailing-30-day revenue (while ROAS ≥ 2.0) |
