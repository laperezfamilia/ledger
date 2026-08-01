---
status: canon
owner: jamie
last_reviewed: 2026-08-01
depends_on: ./BYG-GOV-001.md
supersedes:
related: ./BYG-PRD-001-foundation-v1.17.md, ./BYG-UX-001-foundation-v1.6.md, ./BYG-DEC-001-foundation-v1.21.md
---

# BYG-DES-001: Before You Go — Voice & Design Language

**Version 1.1 | Status: Locked**
Companion documents: BYG-GOV-001 (Constitution), BYG-PRD-001 (MVP Specification), BYG-DEC-001 (Decision Log & Parking Lot)

---

## 1. Purpose
This document governs *how* Before You Go's language behaves — not what the product does (BYG-PRD-001) or what it values (BYG-GOV-001), but how it sounds and thinks. It is a design-language decision, not a Constitution amendment: nothing here changes BYG-GOV-001, and any future addition to this document should be checked against the Constitution's Personality clause (§7) rather than treated as a path around it.

## 2. Voice Principle #1: Partner, Not Interpreter
**Speak as a trusted preparation partner, not an AI interpreter.**

**Avoid** reflective AI language that sounds like the app checking its own homework:
- "It sounds like…"
- "Based on your input…"
- "I understand that…"
- "You appear to…"
- "Your request indicates…"

**Prefer** language that moves directly into partnership:
- "We'll focus on…"
- "Let's get you ready for…"
- "We'll make sure you're ready if…"
- "First we'll cover…"
- "We'll also prepare for…"

The difference is psychological, not stylistic: one voice analyzes, the other accompanies. This is the brand.

## 3. Design Rule: Advance, Don't Echo
**Never repeat the learner's words. Advance them.**

If the learner says *"I'm going to Spain,"* the app does not answer *"It sounds like you're going to Spain."* It advances: *"We'll get you ready for the airport first, then help you feel confident getting to your hotel."*

Every sentence should move the learner one step closer to feeling prepared — not confirm what they already told the app.

**Worked example (locked reference case):**
> Generic AI: *"It sounds like you'd like help talking to Athena during your walk and having a conversation if you meet a neighbor."*
> BYG: *"We'll focus on talking with Athena during your walk, and we'll also get you ready in case a neighbor stops to chat."*

Note the side effect, not itself a hard rule: an advancing sentence like this one also gives the learner an implicit mental roadmap of what the Ready Pack will cover (Athena, then neighbor) before they've seen any content. Good BYG copy tends to organize as a side effect of advancing rather than needing a separate "here's what's coming" summary.

## 4. Voice Filter (The Four-Job Test)
Every sentence in BYG's language should accomplish at least one of these:
1. **Prepare**
2. **Encourage**
3. **Clarify**
4. **Guide**

If a sentence does none of those, delete it. No filler, no AI self-commentary, no unnecessary acknowledgement.

## 5. Internal Confirmation Stays Internal
The app may still need to privately confirm it understood the learner's situation correctly before generating — BYG-PRD-001 §17's Understanding Checkpoint Rule describes this as *advancing* the learner's stated situation into a clear preparation plan (or, where technical precision matters more than voice, *translating* it into one). That confirmation step is internal; it is not user-facing language. Per §2–3 above, the *output* the learner sees should always be advancing language ("We'll get you ready for…"), never a reflective checkpoint ("Did I understand correctly?" / "It sounds like…").

**General design law:** internal architecture or framing terms — "Understanding Loop," "Understanding Checkpoint Rule," or similar — must never appear in UI copy. The learner should never need to know a confirmation step happened; they should simply feel understood. Invisible design is the goal.

## 6. Relationship to Other Documents
- **BYG-GOV-001** governs identity and values (why); this document governs voice (how it sounds carrying out that why). Consistent with §5 (Emotional Position) and §7 (Personality) — this document is an implementation layer under those, not a parallel authority.
- **BYG-PRD-001** governs functional requirements (what). §17's Understanding Checkpoint Rule now uses this document's preferred verb (*advance*) directly, rather than reflective phrasing — see Decision Log for the wording-reconciliation record.
- **BYG-DEC-001** records this as a locked decision (see log) and is where design-language questions that don't rise to Constitution-level get parked.

This document changes only when a voice/design principle proves inconsistent with real usage or with the Constitution — not to accommodate individual copy preferences. New copy ideas go to BYG-DEC-001 as parking-lot items until they earn a place here.
