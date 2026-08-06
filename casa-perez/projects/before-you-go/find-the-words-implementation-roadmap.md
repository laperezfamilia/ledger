---
status: working
owner: jamie
last_reviewed: 2026-08-03
depends_on: ./BYG-GOV-001.md, ../../governance/GOV-004-product-scope-safety-responsible-use.md, ../../governance/GOV-004-escalation-redirect-principles-DRAFT.md
supersedes:
related: ../../governance/GOV-004-escalation-redirect-principles-DRAFT.md, ../../research/ (design research cluster), ../../characters/character-voice-methodology.md
---

# Find the Words — Implementation Roadmap (Working)

**Purpose of this document:** a single reference for the implementation sequencing that's been discussed across several conversations — so it doesn't need re-deriving each time. This is the working plan, not a locked spec; it should be updated as decisions land, not treated as unchangeable.

## Repository & setup sequence

1. **Jamie creates the Find the Words product repository** — not Claude, via API, under whatever account this session happens to hold. Repo ownership is a business-asset decision, not a technical one.
2. **Resolve entity/ownership first, or in parallel** — is there a formal business entity for Casa Pérez yet? Real code, and eventually real revenue, should belong to the company, not a personal account. Flagged as a founder decision, not yet resolved.
3. **First commit: minimal, not a framework scaffold.** A README stating the repo's purpose and linking back to `ledger` as the source of governing philosophy and specs, plus a `.gitignore`. Framework scaffolding follows stack confirmation, not the other way around.
4. **Transition point from `ledger` to the product repo:** once the stack is confirmed and the safety draft has had a founder review pass. `ledger` remains the source of truth for governance, character voice, and product philosophy going forward — the product repo is where implementation happens, built to comply with what's specified here, not to duplicate or drift from it.

## Technology stack (proposed, pending founder confirmation)

- **Next.js (React)** for the app — PWA-capable, deploys cleanly, and if a later move to React Native happens, logic and patterns carry forward more than most alternatives.
- **Vercel** for hosting.
- **Supabase** for database and auth together.
- **Stripe** for payments.
- **Anthropic's API (Claude)** for Sofía's coaching behavior specifically — suited to the nuanced, richly-specified persona instruction this character voice work already requires.
- No separate backend service for v1 — Next.js API routes/server actions are sufficient at this scale.

## Long-term architecture: PWA now, native later

Not "build once, replace later" — **the logic and data layer carries forward; the UI layer gets rebuilt properly when the time comes.** Achieving this requires a deliberate separation between core business logic (Ready Pack generation, Sofía prompt construction, data access) and presentation, held from the very first commit — not something to retrofit later. Tools like Solito or Expo Router exist specifically to bridge Next.js web and React Native once that separation is real.

## "Now it's time to build" — the actual milestone, in two tiers

Not one single gate. Two, because the two halves of the MVP carry different risk:

- **Ready Pack generation** (no live conversation, lowest risk surface): can begin coding as soon as the stack is confirmed and the repo exists. No reason to wait further.
- **Live Sofía coaching** (real-time conversational AI): development can proceed in parallel with the above, but **must not be exposed to any real user until the escalation/redirect safety draft has had real review** — Jamie's review at minimum, genuine clinical/legal input before it's treated as final. Building it isn't gated. Shipping it to a real person is.

This resolves the tension between moving fast and not rushing safety review: the lower-risk half of the product can move immediately; the higher-risk half can be built in parallel but has an explicit, real gate before anyone outside the team talks to it.

## Workstreams

1. **Governance & Safety** — crisis-response draft exists (`../../governance/GOV-004-escalation-redirect-principles-DRAFT.md`), pending founder + clinical/legal review. Blocks Sofía's launch specifically, not Ready Pack development.
2. **Product & Technical Architecture** — stack proposed, pending confirmation; repo not yet created.
3. **Character/Voice Implementation** — translating Sofía's existing Teaching Philosophy and voice methodology into literal system-prompt specs for the bounded coaching context. Not yet started; can begin once stack is confirmed, in parallel with repo setup.
4. **Audience & Growth** — formal workstream from the beginning, running alongside engineering, not after it. Current scope: waitlist/beta cohort and Sofía's YouTube presence. Everything else (TikTok, Instagram, Reddit, referral systems, Shop Casa Pérez) deliberately deferred to post-MVP-validation.

## Open founder decisions, still pending

- Entity/ownership resolution before real assets get created.
- Stack confirmation (or redirection).
- Review of the escalation/redirect safety draft.
