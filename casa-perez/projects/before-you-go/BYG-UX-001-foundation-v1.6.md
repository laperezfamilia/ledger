---
status: canon
owner: jamie
last_reviewed: 2026-08-06
depends_on: ./BYG-GOV-001.md, ./BYG-PRD-001-foundation-v1.17.md, ./BYG-DES-001.md
supersedes:
related: ./BYG-UX-001-amendments.md, ./BYG-DEC-001-foundation-v1.21.md, ./placeholder-library-v0.1.md
---

# BYG-UX-001: Before You Go — Screen & Interaction Design

**Version 1.6 | Status: Locked (Teaching Architecture, Home Screen, Placeholder Library Constitution)**
Companion documents: BYG-GOV-001 (Constitution), BYG-PRD-001 (MVP Specification), BYG-DES-001 (Voice & Design Language), BYG-DEC-001 (Decision Log & Parking Lot)

**Lineage note (2026-08-01):** filed under this distinguishing filename, not `BYG-UX-001.md` (no such base file existed), because `BYG-UX-001-amendments.md` already holds earlier content (a 5-screen continuity structure: Home / Preparation / Continue Preparing / Your Life in Spanish / My Preparations, with Context/Preparation entities) that **does not match this document** — this document's navigation is "Prepare | My Ready Packs | Settings" with no Context-grouping concept anywhere. Per Jamie's explicit instruction, both sources are preserved as-is, unreconciled, until provenance is investigated. See `./BYG-UX-001-amendments.md` for the earlier material and its matching note. Tracked in `STATE.md` org debt.

---

## 0. Purpose & Scope
This document records screen-level layout, hierarchy, and interaction state — distinct from BYG-PRD-001 (what the product does functionally) and BYG-DES-001 (how the app's language sounds). As Track A produces first-pass UX for each screen, it gets recorded here rather than accumulating inside the PRD as ad hoc detail.

*Documentation home judgment call: today's Claude Update said "PRD and/or UX documentation." Creating this as a new companion document, mirroring the BYG-DES-001 precedent, rather than folding full screen hierarchy into the PRD. If you'd rather this live inside BYG-PRD-001 instead, that's a one-message change — flagging the choice rather than assuming it.*

---

## 1. Teaching Architecture: Implicit vs. Explicit Teaching
Before You Go teaches through two complementary, deliberately separated systems. This governs every future screen recorded in this document, not just Home.

**Implicit Teaching** — the learner absorbs it naturally, without feeling taught:
- Placeholder Library (§2.5)
- Screen hierarchy
- Voice (BYG-DES-001)
- Progressive disclosure

**Explicit Teaching** — for learners who want a deeper understanding on demand:
- "Using Before You Go" (Settings — BYG-PRD-001 §21)
- Short coaching cards

**Why the separation matters:** it supports different learner personalities — some want to just start typing, others want to understand the product first — without forcing either group through the other's path, and without letting explicit help content bloat the primary (implicit) experience. When recording a new screen in this document, classify its teaching role explicitly: is it implicit (modeling, ambient) or explicit (opt-in, on-demand)? Don't let the two blend on one screen.

## 2. Home Screen

**Purpose:** the beginning of every preparation journey. Its job is not to teach the learner how the app works — it's to help the learner immediately feel *"I'm in the right place,"* reducing friction before they type a single word.

### 2.1 Returning Learner Hierarchy
1. **Greeting:** *"Hi, [Name]."*
2. **Primary heading (locked):** *"What's coming up?"* (matches BYG-PRD-001 §1)
3. **Supporting copy:** *"Describe what's ahead. We'll help you feel ready."*
4. **Input field**, placeholder (light gray, instructional): rotates through a **curated example library** (§2.5), not a single fixed string — intentionally instructional, giving the learner permission to write naturally rather than feeling they must engineer a prompt.
5. **Current default CEFR level** displayed below the input (e.g., *"Beginner • A1"*, matching BYG-PRD-001 §18's level labels) with a simple **Change** action → Settings → Learning Preferences.
6. **Primary button** (current preferred wording, not yet fully locked): *"Create Ready Pack."*
7. **Recently Prepared** — appears below the primary flow, never competing with it visually. A preview surface into My Ready Packs (BYG-PRD-001 §13), not a separate library.

**Primary navigation:** Prepare | My Ready Packs | Settings (BYG-PRD-001 §15) — unchanged.

### 2.2 First-Time Home
Same overall layout — not a separate tutorial screen. Instead of Recently Prepared (nothing to show yet), a gentle prompt:
> *"Not sure where to start? Try telling us where you're going, who you may speak with, and what you'd like to feel ready for."*

Goal: teach natural input through example, not instructions or an onboarding tutorial.

### 2.3 UX Principles Confirmed
The Home screen should:
- Feel calm rather than busy.
- Begin a conversation, not present a form.
- Invite natural language rather than prompt engineering.
- Keep one clear primary action.
- Ensure every visible sentence has a distinct purpose — Prepare, Encourage, Clarify, or Guide (BYG-DES-001 §4).
- Follow "Advance, Don't Echo" — avoid repeating the same idea in multiple ways (BYG-DES-001 §3). Today's refinement deliberately separated invitation, guidance, and action into distinct elements rather than restating one idea three ways.

### 2.4 Emotional Goal
Arrival state: *"I have something coming up."*
Exit state, Home screen only: *"I'm in the right place."*

**Deliberately not stated here:** *"I can do this."* That deeper emotional destination belongs to the Ready Pack experience itself (BYG-PRD-001 §2–§3), not the Home screen — the app earns confidence rather than declaring it prematurely (BYG-GOV-001 §5, §6).

### 2.5 Placeholder Library Constitution (Locked Philosophy)
The Placeholder Library is a **first-class teaching surface** (Implicit Teaching, §1), not decorative placeholder text. Purpose: reduce blank-page anxiety by modeling authentic moments from real life that inspire learners to naturally describe their own situations. This section is the governing philosophy for **all future placeholder writing** — the batch itself is drafted against these principles, not ad hoc.

**Locked principles:**
- The placeholder is the learner's first teacher.
- It teaches through modeling, not instruction.
- Every placeholder tells a tiny story, not a generic category.
- The learner is always the narrator ("I…"), making it easy to mentally substitute their own life.
- Placeholders sound like something a real person would naturally type — never prompt engineering, never a textbook exercise.
- The library reflects the full range of real communication: spoken conversations, texting, online interactions, travel, work, family, pets, healthcare, errands, celebrations, awkward moments, everyday life.
- Specificity is a design strength — small, authentic details create mental pictures that inspire personalization, not vague generic prompts.
- Every placeholder must earn its place by inspiring, modeling, reassuring, or expanding the learner's understanding of what BYG can help with.

**Behavior (mechanism, locked separately from content):** rotates through a curated library over time — not randomly generated text, not a single fixed string, not user-personalized in V1. Purpose: demonstrate both immediate and future-practice input framing without added explanation, teach the product's breadth through repeated exposure, reinforce natural-language description over prompt engineering.

**QA Principle — The Conversation Test (locked):** a placeholder isn't successful merely because it describes a meaningful life moment. It must also naturally imply a communication opportunity that would realistically lead someone to open BYG — speaking, texting, calling, greeting, thanking, apologizing, introducing, asking, comforting, celebrating, small talk, requesting help. A beautiful life moment without a communication opportunity generally belongs elsewhere. The strongest placeholders sit at the intersection of authentic life and authentic communication.

**Working observations for future drafting (guidance, not hard rules):**
- Recurring people/pets (e.g. a named dog) should appear *lightly* across independently rotating examples, not as a mascot showing up everywhere. *Flagged distinction, since this borders a locked non-goal: GOV-001 §10 excludes "characters or narrative continuity." Light recurrence across unconnected, standalone examples (no storyline, no relationship arc between appearances) stays on the right side of that line. If future drafting starts giving a recurring figure a continuing story across placeholders, that crosses into the excluded territory — worth remembering as the library grows.*
- Rotating placeholders should feel like glimpses into different people's lives, not systematic category coverage.
- Emotional variety (ordinary, funny, awkward, stressful, joyful, meaningful) makes the rotation feel alive rather than uniform.
- The Placeholder Library is a meaningful product differentiator and should be treated as a long-term curated content asset, not disposable UI copy.

**Content status: Foundational Working Library, Draft Batch 1 (Version 0.1) — supersedes the provisional 6-example set below.** Approximately 100 draft placeholders (Foundation Batch) now exist as the first working library, validated against the constitution above. **Architecture and governing philosophy are locked; individual placeholder wording remains intentionally editable** through future QA passes — this is candidate content, not locked production copy.

*Note (updated 2026-08-06): the actual placeholder entries were originally tracked only in an external spreadsheet, not reproduced in this governance document — this section recorded the governing decisions the batches were drafted against and QA'd with, not the content itself. Jamie has since recovered that content; it now lives at `./placeholder-library-v0.1.md` (171 active entries, verified against Decisions #25-31's documented counts and rewrites before being committed). This section remains the governing philosophy; that file is the content.*

**Provisional starting set (pre-dates this constitution — superseded by Draft Batch 1 above, kept here for history only):**
- "I'm grabbing a coffee before my train…" *(immediate)*
- "I want to practice talking to my neighbors." *(future practice)*
- "I'm taking Athena to the vet tomorrow." *(immediate)*
- "I'd like to practice checking into a hotel." *(future practice)*
- "I'm meeting my boyfriend's parents for dinner." *(immediate)*
- "I need to return something at a store." *(immediate)*

*Flags from the prior draft of this section, now verified against the actual Foundation Batch (Claude ran QA once the real 100 items were shared):* **(1) immediate/future-practice balance — confirmed, not resolved:** all 100 Foundation Batch entries are immediate-framed; zero use future-practice framing. This was the single most important finding of that QA pass — one of BYG's two locked input intents (PRD §1, Decision #5) was entirely unrepresented. **(2) communication-range coverage — partially assessed:** 2 exact duplicates found (#46/#66, #54/#75) and 1 near-duplicate (#59/#64); 3 entries flagged as borderline against the Conversation Test below (#28, #31, #98 — describe a life moment without clearly naming a communication opportunity). Full QA detail lives in the tracked content asset (§2.5 note above), not this document.

### 2.6 Future Practice & Relationship Collections (Draft Batch 2)
Added directly in response to the Foundation Batch QA finding above. Two new working collections, ~40 candidates each, ~180 total across the library. Same status as Draft Batch 1: architecture/philosophy locked, individual wording editable, not production copy.

**Future Practice Collection:** dedicated collection developed to give future-practice framing its own emotional voice, rather than sprinkling a few examples into the existing set. **Key insight, now part of the Placeholder Library Constitution's practical guidance:** future-practice placeholders must not read like learning objectives.
> Weak: *"I'd like to practice making phone calls."*
> Strong: *"I'd like to practice ordering tacos at a food truck."*

Immediate placeholders say *"Life is happening."* Future-practice placeholders say *"I'm growing into this."* Both must still tell tiny stories from a real person — never a lesson objective.

**Relationship Collection:** placeholders centered on human connection — spouses/partners, dating, parents, children, grandparents, siblings, extended family, friendship, encouragement, gratitude, apology, affection, reconnecting. Deliberately not "romance prompts" — about connection broadly, spanning family and friendship as much as romantic partners.

**QA findings on this batch (Claude, against the actual 80 items):**
- **Balance resolved by volume, not yet by ratio:** the library is now 100 immediate : 80 future-practice. The zero-representation gap is closed; whether 100:80 is the right long-term ratio is a separate, open question.
- **Structural note:** the Relationship Collection is not a third intent. Every Relationship entry is also future-practice-framed ("I'd like to…") — Relationship and Future Practice split the library by *topic*, not by *intent*. For intent-balance accounting, treat all 80 new entries as future-practice.
- **4 exact duplicate pairs across the two collections:** identical text appears in both Future Practice and Relationship (e.g. "I'd like to say more sweet things to my husband in Spanish" appears in both, word-for-word). Plus 2 near-duplicate pairs.
- **10 entries read as generic learning objectives**, not specific scenes — the exact pattern the Future Practice section's own "weak example" warns against (e.g. "I'd like to get better at keeping conversations going" — no scene, no person, no moment).
- **Conversation Test:** this batch passes structurally far more consistently than the Foundation Batch — the "I'd like to [communication verb]" construction inherently names a communication act.
- Full row-by-row detail (which entries, which pairs) lives in the tracked content asset.

**Product framing (documented, not Constitution — see BYG-DEC-001):** *"Before You Go doesn't just prepare people for conversations. It prepares people for connection. Conversation is the vehicle. Connection is the destination."*

### 2.7 Editorial Standard — The Tiny Story Test (locked)
Added to the Placeholder Library Constitution (§2.5) as a primary editorial test for all future placeholder writing, alongside the Conversation Test.

**The Tiny Story Test:** a strong placeholder reads like a real thought someone has about their own life. If it sounds like a lesson objective, a curriculum heading, a communication category, or a language exercise, it should be revised until it becomes a believable personal moment. Success signal: the learner thinks *"Oh… I could type something like that,"* not *"That sounds like a lesson."*

**Editorial rewrite principle:** whenever possible, rewrite generalized goals into specific future moments — not by adding detail for its own sake, but by giving the learner a moment to picture themselves in.
> Weak: *"I'd like to get better at asking for help."* → Strong: *"I'd like to feel more confident asking for help at the pharmacy."*
> Weak: *"I'd like to practice making phone calls."* → Strong: *"I'd like to call my grandmother more often in Spanish."*

**Standing QA workflow rule:** in future passes, Claude continues flagging generalized wording, weak mental imagery, curriculum-style phrasing, exact/near duplicates, and Conversation Test failures — **without rewriting unilaterally**. Edits happen only after Jamie & Solara review and direct specific action, as in Editorial Pass 1 below. This preserves the collaborative editorial loop rather than Claude silently reshaping content.

**Editorial Pass 1 — executed (per explicit direction, not unilateral):**
- **6 exact-duplicate rows removed** (marked Removed, not hard-deleted, for audit trail): Foundation Batch #66 (kept #46), #75 (kept #54); Future Practice FP-11/18/19/23 (kept the Relationship-collection versions — thematically stronger home for that content).
- **3 near-duplicate rows archived** (recoverable, not deleted): Foundation Batch #64 (kept #59), FP-14 (kept REL-11), FP-26 (kept REL-35).
- **10 rows rewritten** per the Tiny Story Test. Two used Solara's own worked examples verbatim (FP-30, FP-39); the other 8 are Claude's rewrites following the same pattern.

**Editorial Pass 2 — review and final resolution (Jamie & Solara):**
- **9 of the 10 Pass 1 rewrites approved as-written** (FP-20, FP-27, FP-35, FP-36, FP-38, FP-39, REL-7, REL-10, REL-38).
- **FP-30 required a second revision:** the Pass 1 rewrite ("I'd like to keep chatting instead of ending the conversation too soon") was judged more human than the original but still lacking a concrete setting. Final approved wording: *"I'd like to keep chatting after I meet someone new instead of ending the conversation too soon."*
- **The 3 Conversation Test borderline entries resolved**, not left open: each rewritten to make the communication opportunity explicit rather than only implying a life moment.
  - #28: *"Athena made a new dog friend at the park, and I want to ask if they come there often."*
  - #31: *"I'm boarding my flight in an hour, and I want to ask if I can switch to an aisle seat."*
  - #98: *"I'm going to my first concert in Spain, and I want to chat with people while we wait in line."*
- **Round 1 QA status: all flags resolved.** Duplicates, learning-objective drift, and Conversation Test borderlines from Decisions #28–#29 are closed.
- **Active working library: 171 entries** (180 drafted, 6 removed, 3 archived). Full row-level detail — every rewrite, every original wording, both revision passes where they occurred — lives in the tracked QA spreadsheet's Notes column and Status field (Active / Active — Revised, Approved / Archived / Removed).

**First-Time Home (§2.2):** the "Not sure where to start?" prompt remains as specified; the curated library governs the input field's placeholder behavior on both first-time and returning Home, not a replacement for that prompt.
