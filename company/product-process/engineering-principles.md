---
status: working
owner: jamie
last_reviewed: 2026-08-06
depends_on:
supersedes:
related: ../../casa-perez/projects/before-you-go/find-the-words-implementation-roadmap.md, ../research-methodology/character-architecture/README.md, ../research-methodology/educational-philosophy/participation-loop-working-hypothesis.md
---

# Engineering Principles (Founder-Approved)

Company-wide engineering principles — distinct from any single product's implementation details. Filed here, not in a product-specific roadmap, because the reasoning applies to any future product that integrates an AI model or a specific infrastructure vendor, not just Find the Words.

## 1. No application code should directly depend on a specific LLM provider

All AI interactions pass through a provider abstraction layer, so the underlying model can be replaced without application-wide changes. Concretely: application code calls an internal interface (e.g. `getSofiaResponse(context)`); the provider-specific API call lives inside that one module, not scattered through the codebase. Tools like the Vercel AI SDK formalize this pattern rather than requiring it be built from scratch.

**Origin:** proposed by Jamie & Solara during Find the Words' technology stack review (2026-08-03), in response to Claude's recommendation to use Anthropic's API for Sofía's coaching behavior — the distinction drawn was "don't use Claude" vs. "don't let the application *know* it's Claude." Founder-approved, elevated from a single-product recommendation to a company-wide principle.

## 2. Character voice and behavior specifications live as structured data, not application logic

Sofía's Teaching Philosophy, correction style, and any future character's equivalent specifications should live as reviewable, structured content — the same kind of artifact already maintained in `company/research-methodology/character-architecture/` — not hard-coded into prompts scattered through implementation code.

**Why this is a second, related principle rather than a restatement of the first:** principle 1 protects against dependency on a specific *model*. This one protects against dependency on a specific *implementation* — even with a perfect provider-abstraction layer, a character's actual voice could still end up buried and fragmented across application code, making it hard to review, hard to keep faithful to what Character Architecture actually established, and hard to carry forward if the implementation itself is ever rebuilt (e.g., the PWA-to-native transition already planned for Find the Words). Keeping the character specification as portable data means the *identity* stays Casa Pérez's own, independent of both which model runs it and which codebase implements it.

## 3. Recognition/Witness is never a reward mechanic

Any product surface where a character notices or names a learner's growth (Sofía's coaching, future Family Chat surfaces, etc.) must be triggered by what a believable, attentive person could plausibly remember and notice — never by a counter, streak, threshold, or dashboard. If stating the observation accurately would require consulting a log rather than genuine relational memory, it has crossed into surveillance/gamification territory and should not ship as written, regardless of whether the underlying data exists.

**Origin:** Founder Decision (2026-08-06), `company/research-methodology/educational-philosophy/participation-loop-working-hypothesis.md` — Casa Pérez is designed around Participation + specific relational Witness, explicitly *not* a participation→reward model. Filed here because it is a real implementation constraint (no streak counters, no engagement-triggered praise logic, no notification-driven "you haven't practiced in 3 days" mechanics) that applies to any product surface with a character-facing recognition moment, not only Find the Words.

## Why these are company-level, not Find the Words-specific

Both principles apply to any future product that talks to an AI model — Sofía AI, the Family Chat, future character AIs — not only the first one built. Filing them here rather than in `find-the-words-implementation-roadmap.md` keeps them from needing to be rediscovered per product.

*(`ledger` note: this connects directly to something already established elsewhere in this repo — the broader founder instinct, voiced explicitly during this same conversation, that "Casa Pérez shouldn't depend permanently on any single model, engineer, or platform." These two principles are the first concrete engineering-level expression of that instinct, not a new value — the value already existed; this is where it started getting implemented.)*
