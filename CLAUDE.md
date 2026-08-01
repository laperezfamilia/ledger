# CLAUDE.md

Entry point for any AI session working in this repository. Read this first.

## What this repository is

`ledger` is Casa Pérez's canonical institutional knowledge store — a git repository of plain Markdown files. It answers **"what is true."** It is not the operational "what matters right now" layer; that's `STATE.md`. Do not blur the two.

Obsidian may be used later as an optional editing/viewing layer over this repo. It is never the source of truth — the Markdown files in git are.

## Current state

Version 0.1. This repo was just scaffolded. Almost nothing has been migrated yet — only the artifacts listed in "What's canon" below. Everything else referenced in conversation, chat history, or other tools (Notion, Docs, etc.) is **not yet canon** until it's migrated here with proper frontmatter.

## What's canon right now

- This scaffold itself (structure, `IDENTITY.md`, this file, `STATE.md`)
- Nothing else yet — the locked artifacts named in the Casa Pérez knowledge base plan (Constitution, Design System v1, Logo Construction Guide v2.0, Master Production Tracker, Before You Go's three locked foundation docs, the Reverie Method Product 1 Etsy listing package and locked 14-page workbook script) have stub placeholders under their project folders marked `status: pending-migration` — their actual content has not been migrated into this session and must be pulled from wherever Jamie currently holds it.

## What's in flux

- Everything not yet migrated
- Founder Workspace's technical home (`STATE.md` + Reminders/Calendar vs. something else) — proposed, not fully confirmed
- The repository constitution (governance doc: what belongs here, what's canonical, how changes happen) — deferred until the structure has had time to prove itself

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
    brand/
    decisions/
    research/
    characters/
    projects/
      reverie-method/
      agrupa/
      before-you-go/
      tefs/
```

No `/worlds`, `/engines`, or other future-taxonomy folders — see "design for extension, not scaffolding for speculation" in `IDENTITY.md`. Casa Pérez is the sole implementation priority; a broader "Language Learning Company" shape has been discussed conceptually but is explicitly not being built toward.

## Deferred roles

Not yet built, on purpose, until they emerge from repeated real work: World Architect (waits for at least two genuinely active worlds), Canon Reviewer, Knowledge Curator, Document Link Validator.
