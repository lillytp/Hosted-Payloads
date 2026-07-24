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

## 2026-07-24 — Social media, personal brand, and staffing authorized
- Decision: (1) Social media approved as a channel (organic + paid). (2)
  Operator's voice and image approved as brand assets, at the orchestrator's
  discretion. (3) Reinvestment may fund contractors / sales staff when the
  economics justify it. New file `BRAND_MEDIA_POLICY.md`; `BUDGET.md` §2b added.
- Made by: operator
- Context: Operator wants the fastest legitimate path to $20K and is willing to
  use a personal brand and to reinvest in growth (ads, tooling, people).
- Gated action approved: category-level yes for social and personal brand;
  publishing still gated per action. NOT blanket-approved: any AI-synthesized
  likeness of the operator (per-use approval, disclosed, non-deceptive) and any
  hiring (per-decision approval — real person, payment, legal).

## 2026-07-24 — Added agents; set secrets policy
- Decision: Add `accountant`, `sales`, and `business-development` agents;
  clarified `growth-marketer` is the marketing agent. Established a secrets
  policy: banking/company secrets are never pasted into chat and never
  committed. Added `SECURITY.md`, `.gitignore`, `.env.example`, and
  `company.example.json`.
- Made by: operator (requested agents + secure storage)
- Context: Operator offered to provide banking/company info and required it be
  stored securely, off the public internet, and not shared with Claude.
- Key point recorded: Claude processes everything typed in chat, so the
  banking info must NOT be sent here. Agents don't need it — the operator
  executes all money movement. Secrets live in the operator's own secret store.
- Gated action approved: no new spend. Non-sensitive public company info may go
  in `company.json` (git-ignored); nothing sensitive in repo or chat.

## 2026-07-24 — Governance: no self-modification + code-change approval
- Decision: Agents have no access to their own source; all code changes are
  human-reviewed and human-applied. Added `GOVERNANCE.md`, `RUNBOOK.md`
  (topology + laptop run instructions), and `.claude/settings.json` deny rules
  blocking Read/Edit/Write on `.claude/**`, `CLAUDE.md`, config, and secrets.
- Made by: operator
- Context: Operator required that at run the agents never access source code and
  that any code change be human-approved.
- Note: "orchestrator spins up agents" = delegate to / parallelize the existing
  roster; authoring a NEW agent type is a code change requiring human approval.
- Gated action approved: n/a (governance/config only).

## 2026-07-24 — Opportunity-selection cycle kicked off
- Decision: Start Phase 0 — delegate to market-analyst for a validated shortlist
  of 3-5 business options fitting the constraints.
- Made by: operator
- Context: System fully specified; first real work begins.
- Gated action approved: no (research only; no spend, no publishing).

## 2026-07-24 — Niche selected by 3-agent independent vote
- Decision: NICHE = AI automation services for SMBs. Per operator's rule ("if
  two of three independent agents agree, that's the pick"), the vote decided it.
  Result: unanimous (3/3) on the AI-automation category; 2/3 (agents 2 & 3)
  independently converged on the sub-niche: done-for-you AI voice-receptionist /
  missed-call recovery for home-service trades (HVAC/plumbing/electrical),
  ~$1,500-2,500 setup + $400-700/mo retainer. Analyses: vote-agent-{1,2,3}.md.
- Made by: operator's pre-stated decision rule (3-agent majority vote)
- Context: Operator asked to spin up three independent research agents and adopt
  the niche any two agreed on.
- Gated action approved: none. Phase 1 gated items (bank/Stripe, marketplace
  account creation, outreach sending, any paid voice-infra signup) still require
  explicit operator approval. 90-day clock not started until go-to-market begins.
