# Operating Strategy

**Status:** the commoditization pressure-test has returned
(`research/commoditization-pressure-test.md`). Verdict: the generic
"receptionist, done-for-you" pitch is **not** durably defensible (it races
vendors' own onboarding automation, ~0–18 months of runway); the durable wedge
is **bespoke integration & cross-system workflow automation for SMBs on
fragmented/legacy software stacks** (2–5 year durability, because the constraint
is the client's non-uniform software, which no vendor onboarding wizard can
fix). **A repositioning to that wedge is RECOMMENDED but NOT yet decided —
awaiting the operator's go.** Sections 1–2 below still describe the pre-verdict
positioning and will be finalized once the operator decides. This document
breaks the business into its three operating layers: **the orchestrator**, **the
agents**, and **the human in the middle**.

---

## 1. The thesis (and the honest caveat)

**We are not a product company and will not out-build funded AI-receptionist
startups.** We are a **done-for-you automation + integration service** for
small businesses in a chosen high-value vertical. We ride existing best-in-class
infrastructure (voice AI, workflow tools) and sell what the SMB won't do itself:
setup, deep vertical customization, integration into their existing systems
(CRM, scheduling, dispatch, intake), and ongoing optimization.

**Why we can compete (none of it is technology):**
- **Narrowness** — we go deep on one vertical's real workflow; horizontal
  products go a mile wide.
- **Done-for-you** — self-serve means the owner must set it up; most never
  will. The service *is* the product.
- **Integration depth** — bespoke wiring into a client's specific stack is
  inherently hard to productize, which is our defense against commoditization.
- **Reachability** — targeted, personal go-to-market to an underserved segment
  a generic SaaS funnel reaches poorly.

**The caveat we hold in view:** this moat is thin and time-limited. The
implementation gap we ride is closing as tools get more self-serve. This is a
strong near-term cash engine, not a durable tech moat. We optimize accordingly
and re-validate continuously (that's what the pressure-test is for).

---

## 2. The offer & positioning

- **Beachhead offer:** done-for-you AI missed-call/receptionist + lead-follow-up
  automation, deeply integrated into one vertical's stack.
- **Expansion:** once trust is established, broaden into bespoke back-office
  automation for the same client (intake, scheduling, follow-up, reporting) —
  the higher-margin, harder-to-commoditize work.
- **Target verticals (highest missed-call ROI + reachable):** law firms,
  dental/medical/med-spa, restoration, multi-truck home-service operators.
- **Price:** $1,500–$10,000 setup + $400–$2,000/mo retainer. Fewer, higher-value
  accounts over high-volume cheap ones (see `STRATEGY.md`).

---

## 3. The three-layer operating model (who does what)

| Layer | Owns | Never does |
|---|---|---|
| **Orchestrator** | Planning, prioritization, delegation, gate enforcement, daily brief, state | Specialist work; executing gated actions |
| **Agents** | All the *making*: research, building, drafting, books | Publishing/sending; spending; contacting people |
| **Human** | All the *authorizing & trust*: gated actions, KYC, contracts, key calls | The day-to-day making (that's delegated) |

The governing rule: **agents make; the human authorizes; the orchestrator
directs.** Everything that spends money, goes public, contacts a real person, or
creates a legal/financial commitment stops at the human (`APPROVAL_GATES.md`).

---

## 4. What the ORCHESTRATOR does

- Runs the **daily loop** (§7): reads state, produces the brief, collects the
  human's decisions, delegates the day's work, records outcomes.
- **Prioritizes** against the 90-day goal and the phase plan — decides the next
  highest-leverage move, not everything at once.
- **Delegates** to the right agent with a self-contained brief (each agent
  starts cold) and a definition of done. Spawns/parallelizes agents
  deliberately to respect the usage budget.
- **Enforces approval gates** — prepares gated actions fully, then routes them
  to the human for a yes/no; never lets an agent self-authorize.
- **Synthesizes** agent outputs (via qa-reviewer) into decisions and a clear
  ask for the human.
- **Keeps state honest** — updates `kpis.json`, `LEDGER.md` (via
  finance-officer), `backlog.md`, `DECISION_LOG.md`.
- **Escalates** pivots/kill signals early and truthfully.
- Does **not** do specialist work itself and **cannot** touch source code or
  secrets (`GOVERNANCE.md`, `SECURITY.md`).

## 5. What each AGENT does (mapped to this business)

- **market-analyst** — ongoing demand/vertical validation, competitor and
  pricing watch, the commoditization pressure-test, "which vertical next" calls.
- **product-builder** — builds the actual deliverables: the demo agent, client
  integrations/workflows, onboarding assets, reusable templates. The core
  value-creation engine.
- **growth-marketer** — positioning, the inbound funnel, landing page, content,
  marketplace profile/gig copy, social — all as ready-to-publish **drafts**.
- **sales** — pipeline from lead to paid: qualification, proposals, outreach and
  follow-up sequences — all as **drafts** to send.
- **business-development** — partnerships and channels (field-service SaaS,
  trade associations, referral/affiliate deals) — proposals **drafted**, never
  committed.
- **customer-support** — onboarding docs, FAQ, and client reply **drafts**;
  flags recurring issues back to product.
- **finance-officer** — unit economics, the exact client-count-to-$20K math,
  ledger integrity, and enforcement of `BUDGET.md` (reinvestment, ROAS gates).
- **accountant** — clean categorized books, tax set-aside, compliance readiness;
  never touches banking credentials.
- **qa-reviewer** — independent quality/policy/gate check on every output before
  it reaches the human.

## 6. What the HUMAN in the middle does

**The ~30 min/day approval + decision session** (the daily check-in), plus:

**Gated actions only the human can do:**
- Set up and operate the **bank account + Stripe** (the revenue unblocker).
- **Create and identity-verify** all accounts (marketplaces, email/domain,
  phone numbers, tools) — KYC is inherently human.
- **Publish** anything public; **send** every outreach message and client reply
  (batched, from agent drafts).
- **Take the calls** that require a human voice (early sales, especially before
  there's a track record).
- **Sign** contracts/SOWs; **execute** any spend or ad budget; **approve** any
  paid-tool signup, any AI-synthesized use of their likeness, and any hire.

**Trust the human carries (irreducible):** being the accountable party, the
early founder-led sales, the relationships. This is highest at the start and
shrinks as reviews/case studies accumulate — and shrinks further if a paid
human closer is added later (`BUDGET.md` §2b).

---

## 7. The daily loop (how a day runs)

1. Human opens a session, says "run the daily check-in."
2. Orchestrator reads state → delivers the **brief** (money, what happened,
   blockers, decisions needed).
3. Human makes decisions / approves gated items in one batched sitting.
4. Orchestrator delegates the day's tasks to agents; qa-reviewer checks outputs.
5. Orchestrator records results; queues tomorrow. Human is done for the day.

## 8. The deal flow (designed for minimal human involvement)

1. **Agents create** the inbound funnel: demo agent on a live number, landing
   page, content, marketplace listings.
2. **Human publishes** them (batched approval).
3. **Prospect self-qualifies** by experiencing the live demo.
4. **Prospect pays** via a self-serve Stripe link (no negotiation call where
   possible); or, for larger accounts, the human takes one call.
5. **Agents build** the client's integration from an onboarding form; **human
   approves go-live.**
6. Human's per-deal touch: publish, maybe one call, approve go-live. The rest is
   agent work.

## 9. 90-day phase plan

- **Phase 0 — Select (done).** Niche chosen by 3-agent vote; pressure-test in
  progress.
- **Phase 1 — First dollar (wk 1–3).** Human sets up bank/Stripe + accounts.
  Agents build the demo + funnel + one integration template. Land 1–2 small,
  even underpriced, accounts *for the case study*.
- **Phase 2 — Repeatable sales (wk 4–8).** Turn the one channel that worked into
  a repeatable motion. Raise price with proof. Most of the $20K is earned here.
  Begin ad spend only if the offer is validated and ROAS-positive.
- **Phase 3 — Scale or pivot (wk 9–13).** Double down on what compounds; expand
  landed clients into bespoke automation. If the trajectory can't reach the
  goal, say so early and pivot or recommend stopping.

## 10. Money math (the reality check)

$20K/90d needs roughly **5–7 higher-value accounts** ($5K setup + ~$1.5K/mo) or
a mix — not dozens of cheap ones. Recurring retainers are the compounding asset;
setup fees fund the present. Full table in `STRATEGY.md`.

## 11. Metrics & kill criteria

- **Leading:** demos experienced, qualified leads, proposals sent, reply rate.
- **Lagging:** paying accounts, setup revenue, MRR, cumulative vs. the goal line.
- **Kill/pivot signals:** no paying customer by end of Phase 1; reply/conversion
  far below plan with no fixable cause; commoditization erodes pricing power
  faster than we can land accounts. A validated "no" early is a win, not a loss.

## 12. Honest risks

- **Commoditization** — the central risk; being pressure-tested now.
- **Cold-start trust gap** — first sales are the hardest; involvement is
  front-loaded.
- **Delivery risk** — automations touching a client's live systems can break
  real things; requires careful testing and a liability-aware SOW.
- **Compliance** — call-recording consent / TCPA for any voice + outreach; run
  past a professional before going live.
- **The 90-day goal is a stretch, not a forecast** — realistic range is wide
  ($8K–$20K); we report the truth as it develops.
