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
