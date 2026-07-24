# Autonomous Business Orchestrator

A human-supervised, AI-run business system. A lead **orchestrator** agent plans
the work and delegates to specialized subagents; you (the operator) approve the
things that legally or practically require a human and give a ~30-minute daily
check-in.

**Goal:** $20,000 in verified revenue within 90 days.
**Budget:** the $200/mo Claude Max subscription. No API bankroll.
**Decision point:** if the goal is met, keep it. If not, reassess or shut down.

## Read this first: what this is and isn't

**It is** a force multiplier. The agents do the heavy lifting — research,
building, writing, bookkeeping, support drafting — so your 30 minutes a day go
to decisions, not typing.

**It is not** a money printer that runs with zero human involvement. Three
honest constraints shape everything here:

1. **A business legally needs a human.** Bank account, payment processor,
   contracts, taxes — an AI can't own or sign these. You already have the legal
   entity; the agents will hand you a checklist for the rest (bank + Stripe).
2. **The $200 plan is usage-capped.** Agents are spawned deliberately, not
   continuously. This is not a 24/7 always-on API service (that would cost
   metered $/token and blow past $200 fast). Once revenue justifies it, we
   graduate the background workload to metered API and reinvest a slice of
   revenue into capacity — see `BUDGET.md` (the "$200 per $10K" rule and the
   $2,000/mo graduation threshold).
3. **$20K in 90 days is ambitious.** This system gives it a real, honest shot
   and tells you the truth about where it stands — including when to pivot or
   stop.

## How to run it

Start a session and talk to the orchestrator. A normal day:

1. Say "run the daily check-in" (or invoke the orchestrator agent).
2. It reads state, gives you a **daily brief**, and asks for any decisions.
3. You approve/decline gated actions and pick direction where needed.
4. It delegates the day's work to subagents and updates the ledgers.

The first cycle is **opportunity selection** — you chose "let the agent
decide," so the market-analyst will bring you a shortlist to pick from before
anything gets built.

## The agents

| Agent | Role |
|---|---|
| `orchestrator` | General manager. Plans, delegates, enforces gates, reports daily. |
| `market-analyst` | Opportunity research, demand validation, pricing. |
| `product-builder` | Builds the actual sellable asset. |
| `growth-marketer` | Positioning, copy, channels; drafts (publishing is gated). |
| `customer-support` | Drafts customer replies and help docs (sending is gated). |
| `finance-officer` | Honest books, unit economics, runway. |
| `qa-reviewer` | Independent quality/policy check before anything reaches you. |

## The files

- `APPROVAL_GATES.md` — exactly what requires your yes before it happens.
- `BUDGET.md` — money rules: capacity reinvestment, API graduation, ad budget.
- `STRATEGY.md` — the 90-day plan and how the goal breaks down.
- `LEDGER.md` — every real dollar in and out.
- `DECISION_LOG.md` — append-only record of decisions.
- `DAILY_BRIEF_TEMPLATE.md` — the shape of each day's report.
- `state/kpis.json` — machine-readable metrics.
- `state/backlog.md` — prioritized work queue.
- `research/`, `product/`, `marketing/`, `support/` — where agents put outputs.
