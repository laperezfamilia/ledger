---
status: working
owner: jamie
last_reviewed: 2026-08-02
depends_on: ./README.md
supersedes:
related: ./README.md, ../educational-philosophy/educational-brief-v1.0-recovered.md, ../character-architecture/README.md
---

# Recognition vs. Evaluation (Working Thesis)

**Status: Emerging Working Thesis, not canon.** Part of the Design Research program (`./README.md`).

## The thesis

Traditional educational products evaluate. Casa Pérez should witness.

> The purpose of data is not judgment. The purpose of data is witness.

Analytics primarily exist to help the people inside the world notice something true about the learner's growth — not to grade them.

## Example

**Generic:** *"Great job!"*

**Casa Pérez:**
- *"A few weeks ago you translated every sentence before answering."*
- *"Today you answered first and checked later."*
- *"I smiled when I realized that."*

The difference is observation rather than praise. Recognition comes from something that genuinely happened, stated concretely — the same "behaviors over adjectives" instinct already established in `../character-architecture/README.md`'s Documentation Convention, applied here to how the product speaks to learners rather than how characters are documented. **This is the fourth independent occurrence of that same underlying instinct** (alongside the dialogue-approval rule, behaviors-over-adjectives, and scene-anchored architectural principles already logged in `../character-architecture/README.md`'s "Why this is the standard" section) — worth treating as real evidence the pattern generalizes, not just a fourth coincidence.

*(`ledger` note: also connects to `../educational-philosophy/educational-brief-v1.0-recovered.md` §2 "Educational Promise" and §12's question "how should learning accumulate across Shorts?" — recognition-as-witness is one candidate answer to how progress gets communicated, not yet reconciled with that document's open questions.)*

## The warmth/surveillance boundary (2026-08-02, emerging — flagged as a future governance question)

A 2026-08-02 pressure-test review surfaced a real risk: "witness" implemented poorly becomes surveillance. Narrating a learner's behavior back to them, however warmly worded, can read as unsettling rather than caring if the underlying observation wasn't something a person could plausibly have noticed.

**Emerging distinction, not yet resolved:** characters should only "notice" things a believable human could reasonably notice through ordinary relationship — not hidden analytics, not microscopic behavioral telemetry. Human-scale observation, not instrumented surveillance.

This is **flagged as a future governance question, not merely a UX question** — `casa-perez/governance/GOV-004-product-scope-safety-responsible-use.md` is scoped tightly to Find the Words' conversational boundaries and currently says nothing about learner data, analytics, or behavioral tracking. Nothing in `ledger` currently governs this. A future GOV-### document may be needed to define the warmth/surveillance boundary before Recognition vs. Evaluation is implemented against real telemetry — see `STATE.md` Org Debt.
