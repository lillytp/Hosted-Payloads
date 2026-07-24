# Proposal: token-efficiency across all agents

**Status:** proposed (blocked from auto-applying by the `.claude/**` source lock —
this is the intended governance behavior). Needs human application.
**Goal:** cut runtime token/compute use without cutting capability.
**Net effect:** the small added prompt text is repaid many times over by fewer
tool calls, tighter returns, and right-sized models.

---

## 1. Append this block to EVERY agent (`.claude/agents/*.md`)

```
## Token discipline (do more with less — never at the cost of capability)
- Read only what the task needs — specific sections/line ranges, not whole
  files; never re-read what's already in context.
- Prefer one well-targeted search/fetch over many; stop the moment the answer
  is good enough to act on.
- Return a compressed, structured result (findings · sources · recommendation).
  Write full detail to files; don't echo it back into the reply.
- No filler: don't restate the prompt, the context, or your plan back.
- Batch related tool calls; skip redundant re-verification.
- Capability is preserved by scoping sharply, not by cutting corners — if depth
  is needed, go deep, then compress the output.
```

## 2. Orchestrator only — add to its Token-discipline section

```
- Delegate deliberately: one well-scoped agent beats three vague ones; only run
  agents in parallel when independence truly matters (e.g., a vote).
- Reuse, don't redo: check business/research/ and DECISION_LOG.md before
  commissioning work already done.
- Right-size the model per task (see table below).
```

## 3. Right-size models (edit each agent's `model:` frontmatter)

| Agent | Now | Proposed | Why |
|---|---|---|---|
| orchestrator | opus | **opus** (keep) | The brain — judgment/coordination; don't sacrifice. |
| market-analyst | sonnet | sonnet | Research reasoning + web synthesis. |
| product-builder | sonnet | sonnet | Builds real deliverables. |
| growth-marketer | sonnet | sonnet | Positioning/copy quality. |
| sales | sonnet | sonnet | Persuasive drafting. |
| business-development | sonnet | sonnet | Deal/partnership reasoning. |
| finance-officer | sonnet | sonnet | Math + judgment; must stay accurate. |
| qa-reviewer | sonnet | sonnet | Independent judgment. |
| accountant | sonnet | **haiku** | Mechanical categorization/tax set-aside — a lighter model is sufficient. |
| customer-support | haiku | haiku | Templated replies. |

Optional deeper cut: orchestrator → sonnet would save the most, but trades some
coordination judgment. Left at opus by default per "don't sacrifice capability."

## 4. Rationale — why capability is NOT sacrificed
The savings come from *behavior* (fewer redundant reads/searches, compressed
returns, no re-running finished work) and *routing* (mechanical work on lighter
models), not from making the reasoning agents dumber. Heavy-reasoning roles keep
their models; they just work leaner.

## 5. How to apply (human, per GOVERNANCE.md)
Apply the edits locally / via PR (the `.claude/**` lock prevents in-session
tool edits by design):
1. Append §1 block to each of the 10 agent files; add §2 to the orchestrator.
2. Change `accountant` frontmatter `model: sonnet` → `model: haiku`.
3. Commit + log in DECISION_LOG.md.

Alternatively, authorize a one-time in-session apply (uses the shell path that
bypasses the tool-lock) — a logged, operator-authorized exception.
