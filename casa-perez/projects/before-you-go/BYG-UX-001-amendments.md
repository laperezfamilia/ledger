---
status: working
owner: jamie
last_reviewed: 2026-08-01
depends_on: ./BYG-PRD-001-amendments.md, ./BYG-DEC-001.md
supersedes:
related: ./BYG-PRD-001.md, ./BYG-UX-001-foundation-v1.6.md
---

# BYG-UX-001 — Amendment Sections From This Thread

**Migration status:** This file holds only the continuity surface amendments drafted within one thread. **It is NOT the complete UX-001 document** — v1.6's other sections have not been migrated into `ledger`. No base `BYG-UX-001.md` stub exists yet in this repo (UX-001 was not part of the original three-artifact Before You Go migration list — Jamie added it as real content that should be preserved). Once the complete UX-001 is located, create the base file and merge these sections into it, retiring this amendments file.

**Unresolved lineage flag (2026-08-01):** a document self-identified as "BYG-UX-001, Version 1.6, Locked" was later received in full and filed at `./BYG-UX-001-foundation-v1.6.md`. Its navigation is "Prepare | My Ready Packs | Settings" with no Context/Preparation continuity structure — it **does not contain** this file's 5-screen continuity architecture (Home / Preparation / Continue Preparing / Your Life in Spanish / My Preparations) in any form. Per Jamie's explicit instruction, this content is preserved as-is, unreconciled with the newer document, until provenance is investigated (tracked in `STATE.md` org debt). Do not assume this content is superseded, incorporated, or still current relative to the newer document.

**Naming-timeline correction (2026-08-01, per Solara):** the "Naming note" below, written at the time this content was drafted, describes "Find the Words" as a newly-adopted working name — which read, at first glance, like an earlier phase preceding "Before You Go." Per Solara, that direction is backwards: **Before You Go was the original working title; Find the Words is the later/current internal project name.** This corrects the naming timeline only — it does not resolve whether this file's Context/Preparation content is a later evolution of Foundation v1.1, a parallel/experimental branch, or was superseded before implementation.

---

## Screen 1 — Home
Two entry points, unchanged relative priority.
- **Continue Where You Left Off:** optional, dismissible, factual card per PRD §7a.10. Dismiss is a low-emphasis close control, not a competing button. If no Context is eligible, this section is simply absent — no empty-state placeholder shown.
- **What's Coming Up?:** unchanged existing input and 171-item rotating placeholder library.

## Screen 2 — Preparation
Unchanged core content surfaces (Ready Card, full preparation, rehearsal, audio, learner note). Edit Situation and Refine remain primary, Decision #16-governed. Secondary "Continue Preparing" entry opens Screen 3b.

## Screen 3 — Continue Preparing
Navigation only, no generation. Displays the Context's learner-confirmed label as a visible title. One underlying screen, two entry variants via an entry parameter:
- **3a (from Home card):** Review, Add for Next Time, Try Another Level, Previous Preparations.
- **3b (from within an open Preparation):** Add for Next Time, Try Another Level, Previous Preparations — Review omitted as redundant.

**Add for Next Time** opens a lightweight, empty free-text prompt: "What's different this time?" Prior Context content is not restated.

**Try Another Level** opens a level selector; current level shown but not actionable, with copy: "This won't change your usual level."

**Previous Preparations** displays history using plain-language labels (date + level, "· Another level" for variants, "· Needs updating" for stale) — schema terms never learner-facing. Stale entries carry only a quiet list indicator; opening one surfaces the full factual notice ("This version was created before the situation changed") with "Create an updated version" (free) and "View anyway" options. If there are no Preparations beyond the current one, this section is omitted entirely rather than shown empty.

## Screen 4 — Your Life in Spanish
Plain list of active Context labels with factual Preparation counts only — no charts, bars, percentages, streaks, or AI-generated interpretation. Archived Contexts excluded by default; secondary "View Archived" path available. Empty state: "Your recurring conversations will appear here as they grow." Archived empty state: "Nothing archived yet." Standalone Preparations not shown here.

## Screen 5 — My Preparations (existing surface, clarified scope)
Complete retrieval index for every Preparation, whether grouped into a Context or standalone. Where ungrouped Preparations remain reachable; continuity does not replace or duplicate this surface. Distinct purpose from Your Life in Spanish — retrieval vs. reflection — neither a subset or superset of the other.

## Context Management
Rename, Archive, and Permanent Delete accessed via a secondary menu on the Context detail screen, not the primary Your Life in Spanish list. Archive is one-tap, reversible. Permanent Delete requires an additional explicit confirmation step, removes the Context and all linked Preparations irreversibly.

## Confirmed State Flows
| Interaction | Flow |
|---|---|
| Home continuation entry | Card shown (if eligible) → tap → Screen 3a (Review included) |
| In-Preparation Continue Preparing | Tap from Screen 2 → Screen 3b (Review omitted) |
| Add for Next Time | Tap → empty "What's different this time?" field → submit → new occurrence Preparation, fresh allowances |
| Try Another Level | Tap → level selector (current level disabled) → select → new level_variant Preparation, free, uncapped |
| Previous Preparations | Tap from Screen 3 → plain-language list → tap entry → opens read-only (stale entries show full notice + actions on open) |
| Stale variant opening | Open from list → factual notice + "Create an updated version" (free, becomes new current) or "View anyway" |
| Context archive | One tap, no confirmation, fully reversible, excluded from soft-match/continuation-card eligibility going forward |
| Context restore | Learner navigates to archived view, reopens intentionally → silently reactivates |
| Context permanent deletion | Secondary menu → explicit additional confirmation → irreversible removal of Context + all linked Preparations |

## Naming note
Product title updated to "Find the Words" as internal working name for development consistency (not a locked public brand name — pending planned audience validation). "Ready Pack" / "Create Ready Pack" remain intentionally provisional terminology, unchanged.
