# CLAUDE.md

Entry point for any AI session working in this repository. Read this first.

## What this repository is

`ledger` is Casa Pérez's canonical institutional knowledge store — a git repository of plain Markdown files. It answers **"what is true."** It is not the operational "what matters right now" layer; that's `STATE.md`. Do not blur the two.

Obsidian may be used later as an optional editing/viewing layer over this repo. It is never the source of truth — the Markdown files in git are.

## Current state

Version 0.1. The scaffold plus a first real batch of migrated content: Agrupa (game project), GOV-004, and partial Before You Go material are now in place. The original locked artifacts (Constitution, Design System, Logo Guide, Master Production Tracker, Reverie Method package, and the full BYG base documents) are still pending — see "What's in flux" below.

## What's canon right now

- This scaffold itself (structure, `IDENTITY.md`, this file, `STATE.md`)
- `casa-perez/governance/GOV-004-product-scope-safety-responsible-use.md` — Product Scope, Safety & Responsible Use Framework. Cross-product Casa Pérez governance (originated under Before You Go, elevated to cross-product scope by founder decision). Sections 1–5 are the current working-architecture baseline; Section 6 is intentionally deferred to its own design session; Sections 7–11 are not yet drafted — this reflects deliberate sequencing, not incomplete migration. More documents in the GOV-### series are expected.
- `casa-perez/projects/agrupa/design-constitution.md`, `design-principles-v0.1.md`, `authoring-prompt-v0.3a.md` — Agrupa's (formerly "The No-Name Game") locked design canon. The rest of the Agrupa project record (README, Puzzle Production Ledger, Copy Library, Playtest Log, Master Reference v1.4) is filed as `status: active` — current and authoritative, but not locked-canon in the Constitution sense.
- `casa-perez/projects/before-you-go/` — **Before You Go's full Foundation v1.1, Approved Build Authority:** `BYG-GOV-001.md` (Product Constitution), `BYG-DES-001.md` (Voice & Design Language), `BYG-PRD-001-foundation-v1.17.md` (MVP Specification), `BYG-UX-001-foundation-v1.6.md` (Screen & Interaction Design), `BYG-DEC-001-foundation-v1.21.md` (Decision Log & Parking Lot). **Important:** older files also exist in this folder — `BYG-PRD-001.md`/`BYG-PRD-001-amendments.md`, `BYG-UX-001-amendments.md`, `BYG-DEC-001.md` — holding earlier partial content that substantially conflicts with the Foundation v1.1 set above (different product architecture, e.g. a Context/Preparation continuity model absent from the current Foundation). Per Jamie's explicit instruction, **do not treat either set as obsolete** until provenance is investigated — see `STATE.md` Org Debt and the lineage notes inside each affected file.
- `casa-perez/brand/branding-style-guide.md` — primary logo mark, badge variations, tiny icon set, color palette, and typography direction, transcribed from image artifacts Jamie located directly (replaces the retired phantom PDF as this content's source). Source images preserved under `casa-perez/brand/assets/`.
- `casa-perez/decisions/DEC-CP-001-wreath-permanent-brand-element.md` — first entry in the Casa Pérez decision log; the wreath's status as a permanent (not seasonal) brand element.
- Nothing else yet — the locked artifacts named in the Casa Pérez knowledge base plan (Constitution, Design System v1, Logo Construction Guide v2.0, Master Production Tracker, the Reverie Method Product 1 Etsy listing package and locked 14-page workbook script) have stub placeholders under their project folders marked `status: pending-migration` — their actual content has not been migrated into this session and must be pulled from wherever Jamie currently holds it. The branding style guide likely covers most of Design System v1 and Logo Construction Guide v2.0's intended scope — see those stubs for the current assessment.

## What's in flux

- Everything not yet migrated (see `STATE.md` Org Debt for the current list)
- `casa-perez/FOUNDATION.md` — a newly-recognized company-wide-for-Casa-Pérez philosophy layer, explicitly `status: working` and non-canonical (Solara's reconstruction index). Distinct from the still-pending Constitution — see that file's header note.
- Founder Workspace's technical home (`STATE.md` + Reminders/Calendar vs. something else) — proposed, not fully confirmed
- The repository constitution (governance doc: what belongs here, what's canonical, how changes happen) — deferred until the structure has had time to prove itself

## Evolutionary guidance (Jamie/Solara, 2026-08-01 — not yet actionable, don't restructure around these)

Noted for future sessions so this isn't lost to conversation history, per the repo's own "write it down" discipline. None of these require action now:

- **Philosophy and Governance are different layers** and should grow increasingly distinct as the repo matures. Philosophy answers "what do we believe / what should every product feel like" (hospitality first, belonging before instruction, conversation is the product). Governance answers "how are decisions made / what becomes canon / what's authoritative." `casa-perez/FOUNDATION.md` currently holds philosophy-flavored content; keep this distinction in mind as it and GOV-### documents both grow, without forcing a reorg today.
- **Character methodology may eventually outgrow `casa-perez/characters/`.** Concepts like the Three Lenses and the Human Recognition Diagnostic (`casa-perez/characters/character-voice-methodology.md`) are starting to function as company-wide methods for understanding people, not just character-writing tools. Current placement is fine; preserve the flexibility to promote them into a broader methodology layer later without changing their meaning.
- **A future `historical` document status may earn its place** alongside `canon` / `active` / `working` / `pending-migration`, for documents that stop being current but remain historically important (e.g., a superseded master reference). Not being introduced now — the schema's status *values* aren't locked the way its six *fields* are, so this can be added later without a breaking change.

## Roles

- **Founder (Jamie)** — vision, priorities, tradeoffs, final decisions
- **Chief of Staff (Solara, via ChatGPT)** — organizational coherence: founder attention, dependencies, org debt, cross-project awareness, recommending pivots. Read-only GitHub access.
- **Implementation Architect (Claude)** — implementation coherence: doc/implementation drift, repo health, automation, release readiness, implementation debt
- **Together** — governance coherence: watching for principles without mechanisms, untraceable canon, unlinked superseded decisions

Write access flows through Jamie for now: Solara drafts → Jamie relays or approves → Claude commits. This is a deliberate starting posture, not a permanent restriction.

## Operating principles

See [`company/IDENTITY.md`](./company/IDENTITY.md) for the full philosophy layer. The one every session should hold in working memory:

**Principle of Least Maintenance** — before creating anything new, ask: (1) can this be added to an existing artifact, (2) can this be solved with a link, (3) will this reduce future work. If not, don't create it.

## Metadata schema (locked)

Every canonical artifact gets this YAML frontmatter — no more, no fewer fields:

```yaml
---
status:
owner:
last_reviewed:
depends_on:
supersedes:
related:
---
```

Do not add fields speculatively. A field earns its place through demonstrated repeated need.

## Decision logs are append-only

`company/decisions/` (`DEC-CO-###`) and `casa-perez/decisions/` (`DEC-CP-###`). Corrections get a new entry linked via `supersedes` — never a silent edit to an existing one.

## Structure

```
ledger/
  CLAUDE.md
  STATE.md
  README.md
  company/
    IDENTITY.md
    principles/
    governance/
    research-methodology/
    product-process/
    decisions/
  casa-perez/
    FOUNDATION.md
    brand/
    decisions/
    governance/
    research/
    characters/
      character-voice-methodology.md
    projects/
      reverie-method/
      agrupa/
        design-constitution.md
        design-principles-v0.1.md
        authoring-prompt-v0.3a.md
        README.md
        puzzle-production-ledger.md
        copy-library.md
        playtest-log.md
        master-reference-v1.4.md
        sofia-observations-bank.md
        diagnostic-methodology-notes.md
      before-you-go/
      tefs/
```

No `/worlds`, `/engines`, or other future-taxonomy folders — see "design for extension, not scaffolding for speculation" in `IDENTITY.md`. Casa Pérez is the sole implementation priority; a broader "Language Learning Company" shape has been discussed conceptually but is explicitly not being built toward.

## Deferred roles

Not yet built, on purpose, until they emerge from repeated real work: World Architect (waits for at least two genuinely active worlds), Canon Reviewer, Knowledge Curator, Document Link Validator.
