# Governance: source access & change control

Two rules that keep the system honest and prevent it from quietly rewriting
itself.

## 1. Agents do not have access to their own source code

The "source" of this system — the agent definitions (`.claude/agents/*.md`),
`CLAUDE.md`, `.claude/settings.json`, and config — is **off-limits to the
running agents**. At runtime they operate only on the `business/` workspace
(data, drafts, ledgers), never on the code that defines them.

Enforcement (layered, strongest first):
1. **Physical separation (recommended for a hardened deployment).** Run the
   agents against a checkout / working directory that does **not** contain the
   `.claude/` source. If the file isn't on disk in the agent's workspace, no
   tool can reach it. This is the only *airtight* guarantee.
2. **Permission deny rules (`.claude/settings.json`).** `Read`, `Edit`, and
   `Write` are denied on `.claude/**`, `CLAUDE.md`, and config. This blocks
   the file tools from touching source.
3. **Policy.** No agent prompt instructs reading or editing source; the
   orchestrator delegates work, it doesn't re-author the roster.

**Honest limitation:** deny rules govern the file tools well, but any agent with
a shell (`Bash`) could in principle read a file that physically sits in its
working directory. So rule #1 (keep the source out of the runtime workspace) is
what makes "no access to source" a guarantee rather than a strong policy. The
deny rules make casual/accidental access fail closed.

## 2. All code changes require human approval

Any change to the agent system's code — new agents, edited prompts, changed
permissions, changed gates — is a **human-reviewed, human-applied** change:

- An agent may **propose** a change: describe what and why, ideally as a diff,
  written into `business/proposals/`. It does **not** apply it.
- A **human reviews and applies** it through normal git (edit + commit, or a
  pull request that a person merges). The deny rules mean the agent literally
  cannot self-apply, so approval isn't optional — it's structural.
- The change is recorded in `DECISION_LOG.md`.

## Reconciling with "the orchestrator can spin up agents"

"Spin up agents" means the orchestrator **delegates work to the existing
roster** and can run **multiple instances/tasks in parallel** as needed — that's
runtime behavior, always allowed. It does **not** mean authoring new agent
*types* on its own. A genuinely new agent type is a code change: the
orchestrator proposes it, a human approves and adds it.

## What agents CAN freely read/write (not source)

Everything under `business/` except secrets: ledger, KPIs, backlog, decision
log, research, product, marketing, sales, bizdev, accounting, support, and
proposals. That's the workspace. Source and secrets are out of bounds.
