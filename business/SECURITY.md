# Security & Secrets Policy

How sensitive information is handled. The short version: **secrets never enter
this repo and never enter the chat with Claude.** They live only in a secret
store the operator controls.

## The core rule

Anything typed into a Claude conversation is processed by the model and
Anthropic's systems. Anything committed to this repo can end up on GitHub.
Therefore:

> **Do not paste banking credentials, payment-processor keys, tax IDs, or any
> real secret into the chat or into a committed file. Ever.**

The agents are designed so they **never need** these. All money movement is
executed by the operator (see `APPROVAL_GATES.md`). Agents only record that a
transaction happened, after the fact.

## Where secrets actually live

Use a real secret store that Claude cannot read:
- A password manager (1Password, Bitwarden, etc.), or
- Your OS keychain / a cloud secret manager, or
- At minimum, a local `.env` file **on your own machine** that is git-ignored
  and never pasted anywhere.

The repo's `.gitignore` already blocks `.env`, `secrets/`, key files, and
`credentials*.json` from being committed.

## What may live in the repo

| Item | In repo? |
|---|---|
| Public business name, tagline, public-facing email, website URL | Yes — `business/state/company.example.json` → copy to `company.json` |
| Marketing copy, product files, drafts | Yes |
| Confirmed transaction amounts/dates (no account numbers) | Yes — `LEDGER.md` |
| Bank account/routing numbers, card numbers | **No** |
| Payment-processor API keys / secret keys | **No** — secret store only |
| EIN / tax IDs, SSN | **No** |
| Login passwords, 2FA seeds | **No** |
| Customer personal/payment data | **No** — stays in your processor (e.g. Stripe) |

## If a secret is ever exposed

If a credential is accidentally pasted or committed: treat it as compromised.
Rotate/revoke it at the source immediately (bank, Stripe, etc.), then remove it.
Do not assume deletion from a repo or chat is enough — rotate first.

## Handling the info the operator offered to provide

The operator offered banking and company information. Response:
- **Banking info:** don't send it. The agents don't need it. Keep it in your
  own secret store; you personally use it when executing a gated money action.
- **Non-sensitive company info** (public business name, public email, site):
  put it in `company.json` (copied from the example) so agents can use it in
  copy and invoices. Nothing sensitive goes there.
