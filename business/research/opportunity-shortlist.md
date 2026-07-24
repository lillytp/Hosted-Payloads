# Opportunity Shortlist — Phase 0

**Prepared by:** market-analyst
**Date:** 2026-07-24
**Constraints applied:** near-zero starting capital + $200/mo subscription; no
ad budget until an offer is validated; ~30 min/day operator time; operator
willing to use personal brand/voice on social (per `BRAND_MEDIA_POLICY.md`);
legal entity exists, bank/Stripe not yet set up; almost all execution must be
agent-doable, with the human handling money/legal/publishing/outreach-sending.

**Method:** Web search for pricing benchmarks, live marketplace demand
(Upwork/Fiverr listings), and buyer-side discussion. Where a source is a
vendor's own marketing blog selling the exact service being priced, I flag it
as **weak/self-interested evidence** rather than independent proof — pricing
anchors are still useful, demand claims from those sources are not treated as
fact. Where I could not verify a claim, I label it an **assumption**.

**A note on what I don't know:** I have no information about the operator's
specific professional background, skills, or existing network/audience. All
options below assume a *generalist* operator directing AI agents, not a
subject-matter expert in any one field. If the operator has relevant expertise
(e.g., a technical background, an existing audience, or domain credibility),
several of these options — especially the consulting/ghostwriting ones — get
meaningfully easier and should be re-scored. This is flagged per-option below.

---

## Reality check (from `STRATEGY.md`)

$20,000 / 90 days ⇒ at $20/sale you need **1,000 sales** (no ad budget, no
audience — not plausible); at $200/sale, **100 sales**; at $2,000/sale, **10
sales**. Every option below is deliberately priced at $300+ per transaction,
mostly $1,000+, to keep required volume in a channel-plausible range.

---

## Option A — Done-for-you AI Automation & Agent Build-Outs for SMBs (RECOMMENDED)

**The offer:** Build custom workflow automations (n8n/Zapier/Make) and simple
AI chatbots/lead-capture agents for small businesses, sold as fixed-price
projects ($1,200–$3,000), with an optional $300–$800/mo maintenance retainer.

**Why now (demand signal):**
- Live, current job postings for exactly this work exist on Upwork right now,
  e.g. "N8N Automation Developer" for a material-handling company and "n8n
  Automation Expert for Account Scoring" (posted Feb 2026) — [Upwork n8n job
  search](https://www.upwork.com/nx/search/jobs/?nbs=1&q=n8n+automation).
- Upwork's own 2026 in-demand-skills report (investor press release, a
  primary/credible source, not a vendor blog) shows AI-integration job growth
  of **+178% YoY** and AI chatbot development **+71% YoY** —
  [Upwork's In-Demand Skills 2026](https://investors.upwork.com/news-releases/news-release-details/upworks-demand-skills-2026-demand-top-ai-skills-more-doubles-ai).
- Fiverr has active, high-volume sellers in this exact niche — one automation
  seller shows **1,137+ reviews** with a 5.0 rating, and multiple dedicated
  gig categories exist (`n8n`, `n8n-ai-agent`, `ai-agent-automation`) with
  starting prices around $80–$300+ — [Fiverr n8n agent
  gigs](https://www.fiverr.com/gigs/n8n-agent), [example
  listing](https://www.fiverr.com/experttdevelopr/build-ai-agent-n8n-automation-n8n-ai-automation-n8n-workflow-n8n-ai-agent).
  This is real transaction-volume evidence, not just a pricing claim.
- Agency-side pricing benchmark: $500–$3,000/mo per client in recurring
  revenue is cited as typical for automation agencies —
  [LearnForge, n8n agency guide](https://learnforge.dev/blog/n8n-automation-agency/)
  (vendor-adjacent source, used only as a pricing anchor, not a demand proof).

**Path to first dollar:** Create an Upwork profile + Fiverr gig (one-time
gated "publish/create account" action) targeting "n8n workflow automation"
and "AI chatbot setup." Bid on live jobs; take a small first project
(~$200–500) specifically to earn a review, then raise price. In parallel, the
agent can compile a hand-built list of local SMBs and draft cold-outreach
messages for the operator to batch-approve and send (gated per
`APPROVAL_GATES.md`).

**90-day revenue math:** ~11 projects at $1,800 average ≈ $19,800. Or a mix:
a few $300–500 reputation-building jobs early, then 8–9 projects at
$2,000–2,500 once reviews exist. **Plausibility:** the channel has confirmed
live demand and real transacting sellers, so the volume is plausible — but a
brand-new seller with zero reviews typically needs several weeks and
below-market pricing before landing repeat-rate jobs (see below), so the
realistic 90-day range is wide: **$8K–$20K** depending on how fast the first
2–3 reviews land.

**Startup cost:** $0 cash to list on Upwork/Fiverr. n8n self-hosted (free) or
free-tier cloud is sufficient for delivery. Upwork "Connects" (bid tokens)
have a small per-bid cost beyond the free monthly allotment — flag as a
possible future micro-expense requiring approval, not assumed here.

**Agent-executability:** High. Agents can design and build the actual
workflows/chatbots (this is software), write proposals, draft case
studies/portfolio pieces, and draft outreach messages. The human must: create
and verify the Upwork/Fiverr accounts (identity verification is inherently
human), approve/send messages and proposals, take any client calls, and
handle payment collection once Stripe/bank exist.

**Top 3 risks:**
1. **New-seller trust gap** — zero reviews means low win-rate on early bids;
   could stall first dollar past week 2–3.
2. **Scope creep** — clients often expect ongoing "IT support" beyond the
   fixed project, eroding margin if not contained by a clear SOW.
3. **Production risk** — an automation touching a client's live email/CRM/
   payment systems can break something real; needs careful testing and a
   liability-aware SOW (no promises beyond what's tested).

**Score: 20/25** (Evidence 4, Speed-to-$1 4, 90-day plausibility 4, Margin/
agent-exec 4, Risk-adjusted 4)

---

## Option B — AI Readiness Audit (one-time diagnostic)

**The offer:** A structured 1–2 week "AI opportunity audit" for a small
business ($1,500–$2,500 flat fee), delivering a prioritized roadmap of where
automation/AI saves them time or money.

**Why now (demand signal):** Multiple consulting sites price this exact
deliverable at $2,000–$8,000 for an SMB-scale engagement, with one provider
anchoring lower at $397 flat/async —
[ConsultKit](https://www.consultkit.ai/blog/how-to-price-an-ai-readiness-assessment-what-the-market-actually-pays-in-2026-1773479248460),
[Agentpro AI $5K diagnostic](https://agentpro.ai/services/ai-readiness-audit),
[For The TECH Of It, $397](https://www.forthetechofit.com/ai-readiness-audit).
**Caveat:** every source found for this option is a firm marketing its own
identical service — self-interested pricing pages, not independent
buyer-side data. I found no forum thread, review, or third-party report
confirming real purchase volume at these prices. **Treat demand here as an
assumption, not a confirmed signal** — weaker evidence than Option A.

**Path to first dollar:** Cold outreach (LinkedIn/email) to SMB owners, or
LinkedIn posts under the operator's name positioning the audit. No
marketplace/inbound assist exists for this niche the way Upwork/Fiverr assist
Option A.

**90-day revenue math:** Only **10 sales at $2,000** needed — the lowest
volume requirement of any option here. But selling an intangible,
unfamiliar diagnostic cold, with no case studies, no reviews, and (per the
evidence above) no confirmed market of buyers actively searching for this
exact service, is a harder sale than a marketplace listing with live
inbound demand.

**Startup cost:** $0.

**Agent-executability:** High for delivery (research, roadmap drafting);
the sale itself is cold-outreach-heavy, i.e. more human-gated messages per
dollar earned than Option A.

**Top 3 risks:**
1. **Weakest independent evidence in this shortlist** — may describe an
   aspirational category more than a proven one.
2. **Cold-outreach-only motion** — no inbound channel, so it's slower and
   consumes more of the operator's gated "approve this message" time per sale.
3. **No natural repeat/referral loop** — an audit alone doesn't build
   anything; without pairing it with implementation (i.e., feeding into
   Option A) it's a one-off with no recurring upside.

**Score: 13/25** (Evidence 2, Speed 2, Plausibility 3, Margin/agent-exec 4,
Risk-adjusted 2)

*Best use: not a standalone bet — a possible lower-commitment front-end offer
that upsells into Option A, if Option A gets traction.*

---

## Option C — LinkedIn Ghostwriting Retainer for B2B Founders/Execs

**The offer:** Managed LinkedIn content (research + AI-drafted posts + light
human/agent editing) for a B2B founder or exec, $1,500–$2,500/mo, ~8–12
posts/month.

**Why now (demand signal):** Multiple 2026 pricing guides converge on
$1,000–$5,000/mo as the going rate, with "most founders hiring for the first
time" landing in the $1,500–$3,000/mo band —
[Foundera, 2026 pricing guide](https://www.foundera.co/blog/linkedin-ghostwriting-pricing-guide-2026),
[Windmill Growth](https://windmillgrowth.com/blogseo/linkedin-ghostwriter-cost).
**Caveat:** nearly all sources are ghostwriting agencies pricing their own
service — pricing anchors are usable, the "34% YoY growth in the executive
creator economy" claim from one source could not be independently verified
and is **not** used as fact here.

**Path to first dollar:** This is the hardest cold-start in the set. Buyers
of ghostwriting evaluate the writer partly on the writer's *own* visible
voice/track record. With no existing portfolio or audience on record for
this operator (assumption — unknown), landing a $1,500+/mo retainer cold is
unlikely early. The faster real path is the operator posting under their own
name first (unpaid) to build a portfolio, which delays revenue.

**90-day revenue math:** ~8–13 client-months needed at $1,500–2,500 (e.g. 4
clients × $1,700/mo × 3 months ≈ $20,400). Plausible only if 3–4 retainer
clients close in the first month, which is optimistic without samples.

**Startup cost:** $0.

**Agent-executability:** High for drafting; the sale needs human
trust-signals (voice/samples), and ongoing tone-matching review adds
recurring human time beyond the 30-min/day budget if it scales.

**Top 3 risks:**
1. **Cold-start trust problem** — no one hands over their executive voice to
   an unproven writer with no samples.
2. **Retainer churn** — one off week of content and the client cancels;
   revenue is fragile MRR, not banked project fees.
3. **Time cost creep** — quality ghostwriting needs real human review per
   client per week; doesn't scale cleanly within 30 min/day past 2–3 clients.

**Score: 13/25** (Evidence 3, Speed 2, Plausibility 3, Margin/agent-exec 3,
Risk-adjusted 2)

---

## Option D — Productized AI Website/Landing Page Build for Local Small Businesses

**The offer:** A fast-turnaround (48–72hr), AI-assisted one-page or small
website for local service businesses with a poor/no web presence, $800–$1,800
flat.

**Why now (demand signal):** The pricing gap is real and sourced: a designer
+ copywriter build normally costs $2,000–$5,000 and takes weeks —
[SuperDupr](https://superdupr.com/blog/ai-chatbot-cost) (cost context for
custom builds), general landing-page tool market context via
[Involve.me](https://www.involve.me/blog/best-ai-landing-page-builders). But
I found **no buyer-side evidence** — no forum thread, no marketplace order
volume — of small businesses actually paying a third party $800–1,800 for
this specific niche today; my searches mostly returned AI website-builder
*tool vendors* (Wix-style DIY products), which points to a real risk (below),
not confirmation of the service model.

**Path to first dollar:** Fiverr/Upwork gig + local outreach (Chamber of
Commerce lists, Google Maps businesses with no/outdated sites, local
Facebook groups).

**90-day revenue math:** ~12 sites × $1,500 ≈ $18,000. Volume is
theoretically plausible (local small businesses are abundant) but local
sales cycles and trust-building are typically slower than Upwork/Fiverr
inbound.

**Startup cost:** $0 (free tiers of AI site-building tools).

**Agent-executability:** High for the build itself; local sales/relationship
work is the bottleneck and is more human-heavy than a marketplace listing.

**Top 3 risks:**
1. **DIY substitution** — the same AI tools that would let us build fast are
   marketed directly to the small-business owner for $20–50/mo; the pitch
   has to be "we save you time," a harder, more discretionary sell than
   Option A's "we fix a business problem."
2. **Local sales cycle is slower** than marketplace inbound — cold-visiting
   or emailing local businesses has a lower, slower response rate than
   bidding on live Upwork jobs.
3. **Ongoing support creep** — clients expect free tweaks/hosting help after
   launch, eroding margin on a one-time fee.

**Score: 14/25** (Evidence 2, Speed 3, Plausibility 3, Margin/agent-exec 4,
Risk-adjusted 2)

---

## Option E — AI-Assisted Content-as-a-Service for B2B SaaS

**The offer:** Managed blog/content production (AI-drafted, human/agent
edited, structured for both SEO and AI-search visibility) for a B2B
SaaS/professional-services company, $1,500–$2,500/mo for ~4 posts.

**Why now (demand signal):** Established agencies charge $5,000–$25,000/mo
for this exact service, leaving clear room to underprice as a new entrant —
[TheRankMasters, SaaS content pricing](https://www.therankmasters.com/insights/service-playbooks/saas-content-marketing-pricing).
More independently sourced than most options here: Forrester's 2024 Buyers'
Journey Survey found **89% of B2B buyers now use generative AI in research**,
and Gartner projected traditional search volume would drop ~25% by end of
2026 (both cited via secondary summary, original reports not directly
fetched — flag as second-hand citation) — this creates a genuine, timely
reason for "AI-search-optimized content" specifically, not just generic blog
writing.

**Path to first dollar:** Cold outreach + LinkedIn content showing sample
work to SaaS marketing leads. No confirmed inbound marketplace channel found
for this specific niche (Upwork has a general "content writer" category but
was not separately verified for this niche's volume).

**90-day revenue math:** Same shape as Option C — ~8–13 client-months at
$1,500–2,500 needed. Same cold-start problem: no case studies yet, and this
field is more competitive than automation (many existing well-reviewed
agencies).

**Startup cost:** $0.

**Agent-executability:** Very high for production; sales still needs
human-approved cold outreach.

**Top 3 risks:**
1. **Crowded, established competitive field** — multiple agencies with case
   studies and track records already serve this exact niche.
2. **Portfolio-less cold sell** into an AI-content-fatigued buyer market —
   "another AI content agency" is a weak differentiator without proof.
3. **Retainer churn**, same dynamic as Option C.

**Score: 14/25** (Evidence 3, Speed 2, Plausibility 3, Margin/agent-exec 4,
Risk-adjusted 2)

---

## Scoring Summary

| # | Option | Evidence | Speed-to-$1 | 90d Plausibility | Margin/Agent-exec | Risk-adj | Total /25 |
|---|---|---|---|---|---|---|---|
| A | AI Automation & Agent Build-Outs | 4 | 4 | 4 | 4 | 4 | **20** |
| D | AI Website/Landing Page Build | 2 | 3 | 3 | 4 | 2 | 14 |
| E | Content-as-a-Service (B2B SaaS) | 3 | 2 | 3 | 4 | 2 | 14 |
| B | AI Readiness Audit | 2 | 2 | 3 | 4 | 2 | 13 |
| C | LinkedIn Ghostwriting Retainer | 3 | 2 | 3 | 3 | 2 | 13 |

## Recommendation

**Lead with Option A — Done-for-you AI Automation & Agent Build-Outs for
SMBs.** It has the strongest and most independently-verifiable demand
evidence of the set (live current Upwork job postings, a real high-volume
Fiverr seller with 1,137+ reviews, and Upwork's own investor-reported skill-
growth data), the fastest realistic path to first dollar (inbound marketplace
demand instead of cold-outreach-only), the best fit to the strategy's
higher-ticket/no-ad-budget preference, and the highest agent-executability
(the actual deliverable — a workflow or chatbot — is software an agent can
build; the human's job is accounts, approvals, and payment).

**Sequencing suggestion for the operator:**
1. Start Option A as the primary bet — create the Upwork/Fiverr presence
   (gated account-creation approval) and get the first, even underpriced,
   project done to earn a review.
2. Hold Option B (AI Readiness Audit) in reserve as a **front-end upsell
   offer** once Option A has 1–2 reviews/case studies — it's the same buyer,
   same skill set, and turns a weak standalone bet into a strong add-on.
3. Deprioritize C and E for now — both require a portfolio/audience the
   operator doesn't yet have on record, and both compete against established
   players. Revisit C specifically if the operator wants to build a personal
   LinkedIn presence anyway for Option A's outreach — the content could double
   as a ghostwriting portfolio later.
4. D (website builds) is a reasonable secondary channel test if A stalls,
   but carries a real DIY-tool substitution risk that A does not.

**What would change this recommendation:** if the operator has specific prior
expertise, an existing audience, or professional credibility in a narrower
domain (e.g., a regulated industry, a technical specialty, existing
executive-coaching clients), that materially strengthens the
consulting/ghostwriting options and should be weighed against this
generalist-operator analysis.

## Open assumptions to flag to the operator

- I do not know the operator's professional background/skills; this shortlist
  assumes a generalist operator directing AI agents. Please correct if false.
- Vendor-authored pricing pages (marked above) were used only for price
  anchoring, never as proof of transaction volume.
- No claim in this document should be read as a guarantee — all 90-day math
  is arithmetic on assumed prices/volumes, not a forecast.
