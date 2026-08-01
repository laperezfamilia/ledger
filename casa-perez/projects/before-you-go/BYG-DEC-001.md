---
status: canon
owner: jamie
last_reviewed: 2026-08-01
depends_on:
supersedes:
related: ./BYG-PRD-001-amendments.md, ./BYG-UX-001-amendments.md, ../../governance/GOV-004-product-scope-safety-responsible-use.md, ./BYG-DEC-001-foundation-v1.21.md
---

# BYG-DEC-001 — Before You Go Decision Log

**Migration status:** This is an append-only decision log. **Decisions #1–15 have not yet been migrated into `ledger`** — only Decisions #16–18, drafted and locked in the thread that produced them, are present below. This is expected of an append-only log rather than a gap to apologize for; earlier decisions should be appended above this note (in original order) whenever their source content is located, never inserted out of order or edited in place.

**Unresolved lineage flag (2026-08-01):** a complete document self-identified as "BYG-DEC-001, Version 1.21, Round 22" was later received and filed at `./BYG-DEC-001-foundation-v1.21.md`. Its own Decisions #16–18 are "Collections final classification," "Related Ready Pack Suggestions," and "CEFR and Multi-Level Ready Pack architecture" — **different topics under the same numbers** as the #16–18 below. Its Decision #3 (Five-Minute Promise) is never reclassified by anything later in that log, contradicting this file's Decision #17 claim. Per Jamie's explicit instruction, both sources are preserved as-is, unreconciled, until provenance is investigated (tracked in `STATE.md` org debt). Do not assume this content is superseded, incorporated, or still current relative to the newer document — this may represent an earlier/parallel exploration (possibly connected to "Find the Words," referenced in the related UX-001 amendments) that was not carried into the Foundation v1.1 reconciliation, but that is not confirmed.

---

## Decision #16 — Edit/Refine Allowance Model
*Supersedes Decision #6 in full.*

- Two independent allowances per Ready Pack: one Edit Situation, one Refine.
- Edit Situation corrects a misunderstood or changed underlying situation. Refine adjusts an otherwise-valid Pack. These serve different jobs and are tracked independently — using one does not consume or remove the other.
- Each allowance may be used once per Ready Pack. Once a specific allowance is used, that same action is unavailable again within that Pack — but the other, if unused, remains available.
- Edit Situation regeneration replaces the prior Pack rather than preserving it, since the original was based on an incorrect or changed premise.
- Any unused Refine allowance carries over to the replacement Pack created by an Edit Situation regeneration.
- Once both allowances are exhausted — or the learner requests an additional Edit or Refine beyond the limit — the learner is guided to create a fresh Ready Pack rather than continue iterating within the same Pack.

## Decision #17 — Five-Minute Promise Reclassification
*Supersedes the measurable "time-to-usable-Ready-Card" definition established in Decision #3.*

- The Five-Minute Promise is reclassified from a measurable service definition to a positioning and product-experience principle.
- Communicates that the product delivers fast, practical preparation shortly before a real conversation.
- Not a timed guarantee, stopwatch, measured service level, or defined technical clock. No formal timing mechanism is implemented or implied.
- UX obligations: respect urgency; minimize unnecessary steps; permit no more than one focused clarification; deliver usable preparation quickly; allow the learner to leave with value before consuming the entire Pack.
- Clarification evaluation standard: *Was the question necessary, quick to answer, and valuable enough to justify interrupting direct generation?*

## Decision #18 — Conversation Continuity Model
*Cross-referenced to Decision #16. Does not supersede #16; extends the governance boundary alongside it.*

**Relationship to Decision #16:**
- Decision #16 governs modifications to the current Preparation within a single occurrence: one Edit Situation, one Refine.
- Decision #18 governs actions outside that boundary: new occurrences, level variants, Context history, and continuity navigation.
- Add for Next Time and Try Another Level each create a new, distinct Preparation record with fresh Decision #16 allowances of their own. Neither consumes the Edit or Refine allowance of the Preparation it originates from.
- Try Another Level is free and uncapped as an action — it is not treated as Refine.

**Data model:**
- Two entities: Context (id, label, category, created_at, last_active_at, status: active/archived) and Preparation (id, context_id nullable, situation_text, cefr_level, created_at, relation_type: origin/occurrence/level_variant, source_preparation_id nullable, variant_status: current/stale — applies to level_variant only, edit_used bool, refine_used bool, reflection nullable).
- A level_variant is a full Preparation record, not a nested child object. Does not require Context membership.
- No stored "dormant" status — derived at read time from last_active_at.

**Context creation and lifecycle:**
- Contexts are never created through a formal setup workflow. The app may suggest a label after detecting a soft match between a new submission and a past one; the learner confirms or edits it.
- No automatic entity merging or splitting occurs. The learner names their life.
- If multiple Contexts match ambiguously, no suggestion is shown.
- Declined suggestions may be offered again after a later strong match, always with explicit confirmation, never silently.
- Archive: default, one-tap, fully reversible. Hides the Context and its Preparations from the primary view while preserving label and grouping.
- Permanent Delete: separate, explicitly confirmed, irreversible action. Removes the Context and all linked Preparations. No detached/orphaned state exists.
- Archived Contexts are excluded from soft-match suggestion candidates and Home continuation-card eligibility. Reactivation requires the learner to intentionally reopen the archived Context (silent reactivation on manual return).
- A level_variant's source_preparation_id always resolves within the same context_id as its origin — no cross-Context variant relationships.

**Same-submission vs. new-occurrence detection:**
- Uses the same soft-match logic as Context suggestion — one shared matching mechanism.
- Scoped per-Context, not globally across a learner's history.
- When a close match is detected against a Preparation that hasn't been reflected on or treated as having occurred, the learner is asked whether this updates the same upcoming conversation or prepares for another occurrence.
- If the learner dismisses the prompt without choosing, the system defaults to "Prepare for another time" (new occurrence). Working principle: *when uncertain, preserve history.*
- Deterministic time-based fallback: a Preparation is presumed resolved after a defined window even without explicit reflection.

**Variant staleness:**
- Tracked via an explicit variant_status field (current/stale), not derived from replacement lineage.
- When Edit Situation replaces a Preparation, all level variants sourced from it become stale: remain available in history, not treated as current, not carried forward into future occurrences.
- A stale variant displays a factual notice when opened, with the option to create an updated version at the same level — free, does not consume an Edit or Refine allowance. The new variant's source_preparation_id points to the new current Preparation and is marked current, with its own fresh Decision #16 allowances.

**Home continuation surfacing:**
- Shows the most-recently-active, non-archived Context within a bounded, tunable recency window (initial default ~30 days).
- If no Context is unambiguously most recent, nothing is shown.
- Card copy is templated/deterministic from stored fields — never LLM-generated. Fallback waterfall: quoted short phrase (fixed length limit) → Context-label statement → Context-label-and-level statement.
- Dismissal persists until new activity occurs within that Context, not on a calendar-based reset.

**Governing trust rules (behavioral, not just architectural):**
1. Memory may assist by default.
2. Recognition must be invited.
3. Confidence is earned, never declared.
4. The learner names their life.
