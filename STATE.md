# STATE.md

The Founder Workspace layer: what matters *right now*, as distinct from what is *true* (that's the rest of the repo — see `CLAUDE.md`).

This file is intentionally lightweight. It is not a second knowledge base — it's a pointer layer: current attention, blocked items, recently-added canon worth knowing about, cross-project dependencies, and org debt. Jamie's Reminders/Calendar remain the tools of record for personal task tracking; this file exists for repo-aware, cross-session context that those tools can't hold.

Status: proposed technical home for Founder Workspace, per the Principle of Least Maintenance. Not yet fully confirmed as final — revisit if it stops earning its keep.

---

## Attention

- First real content migration complete: Agrupa project (canon + active operational docs), GOV-004, partial Before You Go material, and the new Casa Pérez Foundation working index are all in `ledger`.

## Blocked

- Solara's read-only GitHub connector (ChatGPT side) was erroring as of the last planning session — needs retry/troubleshooting on her end. Not a repo-readiness blocker.

## Recently added canon

- `ledger` repo initialized: structure, `IDENTITY.md`, `CLAUDE.md`, `STATE.md` (2026-08-01).
- `casa-perez/governance/GOV-004-product-scope-safety-responsible-use.md` — cross-product governance, ingested at Jamie's explicit instruction.
- Agrupa project migrated: Design Constitution, Design Principles v0.1, Authoring Prompt v0.3a (canon); README v2.0, Puzzle Production Ledger, Copy Library, Playtest Log, Master Reference v1.4 (active); Sofía observation bank + character-voice methodology (working, split per Jamie's instruction); Diagnostic methodology notes (working, extracted from an operational sync doc per "archive knowledge, not logistics").
- `casa-perez/FOUNDATION.md` — Solara's Casa Pérez philosophy reconstruction index (working, explicitly non-canonical, distinct from the still-pending Constitution).
- `casa-perez/projects/before-you-go/BYG-DEC-001.md` (Decisions #16–18), `BYG-PRD-001-amendments.md` (§7/§7a), `BYG-UX-001-amendments.md` (continuity surfaces) — all explicitly partial, flagged as such.
- Julie and Denham's Coffee Shop-era playtest feedback recorded in `casa-perez/projects/agrupa/playtest-log.md` (Jamie's recollection, not a contemporaneous transcript) — closes the gap flagged during the earlier migration.
- `casa-perez/brand/branding-style-guide.md` (canon) and `casa-perez/decisions/DEC-CP-001-wreath-permanent-brand-element.md` (canon, first Casa Pérez decision log entry) — transcribed from two image artifacts Jamie located directly, replacing the retired phantom PDF as this content's real source.
- **Correction (2026-08-01):** the BYG-GOV-001 "fulfilled by GOV-004" conclusion above was wrong. Jamie located the actual document — real, distinct, locked (v1.1). `casa-perez/projects/before-you-go/BYG-GOV-001.md` now holds the real content, `status: canon`. GOV-004's lineage note corrected to match: it's a later, additional, cross-product document, not a renamed/evolved BYG-GOV-001. Both stand independently.
- Before You Go's full Foundation v1.1 received and ingested as canon: `BYG-GOV-001.md` (corrected, above), `BYG-DES-001.md` (new), `BYG-PRD-001-foundation-v1.17.md` (new), `BYG-UX-001-foundation-v1.6.md` (new), `BYG-DEC-001-foundation-v1.21.md` (new). All filed under distinguishing filenames rather than overwriting the existing partial-content files, because their content substantially conflicts with what was already there — see Org Debt below.

## Dependencies

- `casa-perez/brand/constitution.md` (pending) and `casa-perez/FOUNDATION.md` (working) are deliberately kept separate per Jamie's decision — the branding style guide's arrival doesn't change this; it's Design System / Logo Guide material, not Constitution material.
- BYG-PRD-001-amendments.md and BYG-UX-001-amendments.md's relationship to their base documents is now an open investigation (see Org Debt) rather than a simple pending-merge — the full base documents arrived, but their content conflicts rather than confirms.
- `casa-perez/brand/design-system-v1.md` and `logo-construction-guide-v2.md` now marked "provisionally satisfied" by `branding-style-guide.md` — kept open, not retired, per Jamie's explicit decision (insufficient evidence yet that fuller versions never existed separately).

## Org debt

- A fuller Design System or Logo Construction Guide (clear-space rules, minimum sizing, misuse examples) — unconfirmed whether one exists beyond the branding style guide now in `ledger`.
- Master Production Tracker (.xlsx) — not yet received.
- Reverie Method Product 1 Etsy listing package + workbook script — not yet received.
- **Investigate lineage: earlier BYG partial content vs. Foundation v1.1 (high priority, per Jamie's explicit instruction not to reclassify either without provenance).** Three pairs of files describe substantially different, apparently incompatible product architectures under the same document IDs and (in DEC-001's case) the same decision numbers:
  - `BYG-DEC-001.md` (#16–18: Edit/Refine Allowance Model, Five-Minute Promise Reclassification, Conversation Continuity/Context model) vs. `BYG-DEC-001-foundation-v1.21.md` (#16–18: Collections, Related Suggestions, CEFR architecture — unrelated topics; Five-Minute Promise never reclassified).
  - `BYG-PRD-001-amendments.md` (§7 Edit Situation/Refine dual allowance, §7a Context/Preparation continuity) vs. `BYG-PRD-001-foundation-v1.17.md` (§7 is a simple 3-refinement ceiling; no Context model anywhere).
  - `BYG-UX-001-amendments.md` (5-screen Context-based continuity structure, "Find the Words" working title) vs. `BYG-UX-001-foundation-v1.6.md` (Prepare/My Ready Packs/Settings navigation, "Before You Go" throughout, no Context concept).
  Possibilities: intentionally superseded exploration, incorporated under different names/structure, or a genuine parallel product-design layer. **Do not treat either source as obsolete based on textual differences alone** — confirm provenance first, then update with explicit lineage notes (superseded / merged / fulfilled / parallel) rather than deleting or quietly reclassifying.
- Sofía Pérez Voice Brief + Addendum, Diagnostic Protocol v0.2, Recognition Model v0.1, PBO Evidence Log, Version 0.2 Early Access Findings — per Solara's reconciliation, these are embedded knowledge distributed across conversation history, not missing standalone artifacts. Not treated as outstanding migration debt unless/until Jamie and Solara decide to formally extract them.
- Repository constitution (governance doc) not yet written — deferred until structure proves itself.
