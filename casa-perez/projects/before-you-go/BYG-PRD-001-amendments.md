---
status: working
owner: jamie
last_reviewed: 2026-08-01
depends_on: ./BYG-DEC-001.md
supersedes:
related: ./BYG-PRD-001.md, ./BYG-UX-001-amendments.md, ../../governance/GOV-004-product-scope-safety-responsible-use.md
---

# BYG-PRD-001 — Amendment Sections From This Thread

**Migration status:** This file holds only §7 (revised) and §7a, drafted within one thread. **It is NOT the complete PRD** — v1.17's other sections have not been migrated into `ledger`. Do not treat this as replacing `./BYG-PRD-001.md` (the base-document stub); once the complete PRD is located, these sections should be merged into it and this amendments file retired/superseded.

---

## §7 (revised) — Post-Capture Decision Tree & Edit/Refine Allowances
*Scope: States 1–4 only. State 5 (safety-sensitive interception) is explicitly out of scope for this amendment — see GOV-004 §6.*

**Post-capture states:**
1. **Ready to Generate** — sufficient, clear, relevant context present. Proceeds directly to generation. No confirmation step.
2. **Clarification Needed** — situation type identified, but one variable exists that would materially change phrase content. System asks exactly one focused question, framed as a continuation of the original submission, not a modal or separate flow.
3. **Essential Information Missing** — system cannot identify a situation type at all. System asks conversationally for the minimum needed to proceed.
4. **Unsupported Situation** — request exceeds intended MVP scope (taxonomy lives in GOV-004 §4–5). App explains the boundary warmly and redirects toward an appropriate everyday-conversation use case; does not manufacture confidence or produce an unreliable Pack.

**Clarification evaluation standard** (applied uniformly across States 2–3): *Was the question necessary, quick to answer, and valuable enough to justify interrupting direct generation?*

**Edit/Refine allowance model** (per Decision #16): Edit Situation — 1 per Ready Pack, corrects a misunderstood/changed situation, regeneration replaces the prior Pack. Refine — 1 per Ready Pack, adjusts an otherwise-valid Pack. Independent tracking; unused allowance survives an Edit Situation replacement. Once exhausted, learner is guided to a fresh Ready Pack.

**Five-Minute Promise** (per Decision #17): Positioning principle, not a measured guarantee — no clock, no defined start event. UX obligations: respect urgency, minimize unnecessary steps, cap clarification at one question, deliver usable value quickly, allow exit before full-pack completion.

**Note on State 5:** Safety-sensitive interception remains a required, separately-scoped product and policy pass (GOV-004 §6), intentionally not defined here.

---

## §7a — Conversation Continuity (Decision #18, extends Decision #16)

**7a.1 Purpose.** Many conversations recur with the same people, places, and relationships over time. Continuity allows earlier preparation to make future preparation better, without requiring the learner to manage versions, categories, or setup.

**7a.2 Contexts.** A Context is a learner-confirmed grouping representing a recurring real-life situation. Contexts are never created through a formal setup flow. The app may suggest a label after detecting a soft match between a new submission and a prior one; the learner confirms or edits it. No automatic entity merging or splitting occurs. If multiple Contexts satisfy the match threshold ambiguously, no suggestion is shown.

**7a.3 Preparations and relation types.** Each Preparation belongs to at most one Context and carries a relation_type: origin, occurrence, or level_variant. A level_variant does not require Context membership. Each Preparation independently carries its own Edit and Refine allowances under Decision #16.

**7a.4 Actions.**
- Edit Situation and Refine modify the current Preparation, governed entirely by Decision #16.
- Review reopens an existing Preparation read-only. No allowance consumed.
- Add for Next Time creates a new Preparation (relation_type = occurrence) with fresh Decision #16 allowances. Learner is prompted only for what is different ("What's different this time?"); prior Context content is not restated.
- Try Another Level creates a new Preparation (relation_type = level_variant) with fresh allowances. Free and uncapped. Learner's default level is unaffected.
- Continue Preparing is navigation only, no generation. Available actions depend on entry point: from Home continuation card includes Review; from within an open Preparation omits Review.

**7a.5 Same-occurrence resolution.** When a new submission closely matches the most recent unresolved Preparation within a single candidate Context (not globally), the learner is asked whether this is the same upcoming conversation or a new occurrence. If dismissed without a choice, defaults to new occurrence. A Preparation is presumed resolved after a defined time window even without explicit reflection.

**7a.6 Variant staleness.** When Edit Situation replaces a Preparation, derived level_variant Preparations become stale (explicit variant_status field). Stale variants remain available in history but are not current. Opening one displays a factual notice with the option to create an updated version (free) or view anyway. A variant's source_preparation_id always resolves within the same context_id as its origin.

**7a.7 Context lifecycle.** Archive (default, reversible, one-tap) or Permanent Delete (separate, explicitly confirmed, irreversible). Archived Contexts excluded from soft-match and Home continuation-card eligibility; reactivation requires intentional learner action. Rename/Archive/Permanent Delete accessed via secondary menu, not primary list.

**7a.8 Recognition and retrieval surfaces.** My Preparations is the complete saved-history retrieval surface for every Preparation, grouped or standalone. Your Life in Spanish is Context-only — plain list of Context labels and factual counts, no charts/percentages/streaks/scores/AI-generated interpretation.

**7a.9 Trust model.**
1. Memory may assist by default.
2. Recognition must be invited.
3. Confidence is earned, never declared.
4. The learner names their life.

**7a.10 Home continuation card.** Most-recently-active, non-archived Context within a bounded, tunable recency window (~30 days initial default). Nothing shown if ambiguous. Copy generated from a fixed, deterministic template waterfall — never LLM-generated. Dismissal persists until new activity occurs within that Context.
