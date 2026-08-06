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

## Technology stack (2026-08-03 — Founder Decision, mostly confirmed)

- **✅ Next.js (React)** — approved. Deciding factor: ecosystem size, given Casa Pérez is building with an AI-assisted engineering workflow specifically — a larger ecosystem means stronger AI-coding-assistant performance over the company's lifetime, not just more documentation.
- **✅ Vercel** — approved, with the lock-in tradeoff explicitly acknowledged and accepted for the MVP stage. Named as the layer to revisit first if the company grows significantly; Netlify remains the known fallback if that becomes live.
- **✅ Supabase** — approved. Standard PostgreSQL underneath keeps the data layer portable, consistent with the same anti-proprietary-silo instinct already governing this whole repo's own choice of Git and Markdown.
- **✅ Paddle (Merchant of Record)** — resolved, replacing the earlier Stripe-only recommendation. Changed by a real Founder Decision: Casa Pérez is globally available from day one, not US-first. EU VAT applies near-immediately regardless of volume, unlike US sales tax's more forgiving economic-nexus thresholds — global-from-day-one plus a three-person team with no in-house tax/accounting capacity point toward Merchant of Record together, not against each other. Paddle specifically substitutes for the accountant the team doesn't have, rather than requiring one — this decision doesn't need professional sign-off precisely because choosing Paddle is what avoids needing it.
- **✅ Anthropic's API (Claude)** for Sofía's coaching behavior — approved, specifically *behind a provider abstraction layer* (see `company/product-process/engineering-principles.md`, new). No separate backend service for v1 — Next.js API routes/server actions are sufficient at this scale.

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

- Review of the escalation/redirect safety draft (Jamie's pass, then real clinical/legal input).
- Entity/ownership resolution — self-serve, see checklist below.

## Professional review checklist (2026-08-03)

**Context:** the team currently has no retained outside legal, clinical, or accounting advisors. That doesn't remove the need for real professional input in a few places — it means that input should be scoped and one-time where possible, not assumed to require an ongoing relationship. Distinguishing genuine launch blockers from decisions the team can reasonably make itself now, revisiting later as the company scales.

**Requires real professional input before launch — no responsible way around it:**
- The escalation/redirect crisis-response protocol, before live Sofía coaching reaches any real user. Build the draft from established public guidance (e.g. the 988 Suicide & Crisis Lifeline publishes free resources on exactly this), then get one scoped, one-time paid consultation with a mental health professional to check the actual language before it ships — not a retainer, a single session.

**Reasonable to decide and act on now — revisit with real professional input later, not before launch:**
- **Business entity formation.** Self-service formation (e.g. direct state filing, or a reputable formation service) is fine for a solo founder with no co-founders or investors yet. Real legal counsel becomes clearly worth the cost once there's equity to split or outside investment to structure — not required for a simple single-owner LLC.
- **Privacy Policy and Terms of Service.** Draft carefully now from credible frameworks and templates. Real legal review matters before this scales meaningfully past the initial beta cohort, not before the first user.
- **Payment processor choice.** Resolved above — Paddle was chosen specifically because it substitutes for the accountant the team doesn't have, not because professional sign-off was obtained.

**Flagged for later, not urgent, not blocking anything now:**
- Trademark protection for "Casa Pérez" and character names — worth doing before someone else registers it, but doesn't block building.

## Repository status (2026-08-03)

- GitHub Organization created: `casa-perez-hq`.
- Product repository created: `find-the-words`, private, README initialized, Node `.gitignore` added.
- `ledger` remains under the personal account, not yet transferred — deliberately sequenced after confirming the organization itself works, per the migration plan in `STATE.md`.
