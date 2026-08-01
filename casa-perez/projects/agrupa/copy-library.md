---
status: active
owner: jamie
last_reviewed: 2026-08-01
depends_on: ./README.md
supersedes:
related: ./puzzle-production-ledger.md
---

# Agrupa Copy Library

**Status:** Working canonical document. **Structure and governing rules approved (Jamie/Solara).** First acknowledgment-pool approvals and the primary Restaurant Reflection line are now **Approved** (this revision) and ready for implementation. Remaining lines are **Proposed** or **Retired**, per the tables below. Governed by Master Reference Section 4A / README Section 4A (Sofía's Voice in Agrupa) — every conversational line must pass the full Conversational Voice Test before status advances to Approved.

## Purpose

Canonical home for approved Sofía-voice copy across Agrupa: correct-group acknowledgments, One Away variations, duplicate-guess messages, Reflection copy, World-completion messages, and future UI dialogue requiring her conversational register. Functional-register copy (buttons, labels, navigation) does not belong here — see README Section 3/9 for shipped functional strings.

## Structural Decisions (locked, this revision — Jamie's decision)

1. **Correct-group acknowledgments use position-aware rotation, not one flat pool and not four rigid scripts.** Three pools: First Correct Group, Middle Correct Groups (shared by groups 2 and 3), Final Correct Group.
2. **Reusable acknowledgment pools are World-agnostic — never name the Moment or World.** Reusability, freedom from templating errors, and brevity all depend on this. The solved cards already reveal the Moment title; repeating it adds nothing.
3. **World- and Moment-specific Sofía dialogue belongs in each puzzle's authored Reflection copy, individually written per puzzle — never generated from a reusable template.** This includes the final-group acknowledgment, which stays generic; World-specific voice arrives only at Reflection.

## Two Fundamentally Different Categories of Copy (confirmed by Solara — critical distinction, not optional framing)

This Library holds two categories of content that must never be treated as interchangeable:

**1. Reusable interaction pools** — correct-group acknowledgments (First/Middle/Final), ordinary-incorrect feedback, One Away, duplicate-guess, and reveal-transition copy. These are World-agnostic, rotate to avoid repetition within a session, and are approved once as a pool rather than per puzzle.

**2. Puzzle-specific authored Reflection notes** — one individually authored note per puzzle, responding to that specific World or lived experience. **This is not a rotating pool.** Each note is drafted and approved on its own, exactly like a puzzle's Tile content — see the Governing Rules for Reflection Notes below.

Confusing these two categories — for example, treating Reflection as something that could be generated from a template or drawn from a shared rotation — would undo the entire reason Reflection was carved out as puzzle-specific in the first place (Structural Decision 3, above).

---

## Correct-Group Acknowledgments

### Pool 1 — First Correct Group
*Function: quiet reassurance — the player now understands the game.*

| Line | Status |
|---|---|
| "That's it." | **Approved** |
| "Yeah, those go together." | **Approved** |
| "There you go." | **Approved** |
| "That's the one." | **Approved** |
| "You've got it." | Proposed — natural, but more generic than the approved four |
| "Exactly that." | Proposed — understandable, slightly less conversational than the approved four |
| "Good — now you know how this goes." | **Retired — too teacherly/explanatory** |
| "That's the shape of it." | **Retired — sounds written rather than spoken** |

### Pool 2 — Middle Correct Groups (2nd and 3rd)
*Function: brief, freely rotating acknowledgment. No escalation.*

| Line | Status |
|---|---|
| "Nice catch." | **Approved** |
| "There it is." | **Approved** |
| "Good eye." | **Approved** |
| "There we go." | **Approved** |
| "Oh, nice." | **Approved** |
| "Look at that." | Proposed — natural, but could read as performative when repeated |
| "That fits." | **Retired — sounds like software confirming a rule** |
| "You saw it." | **Retired — slightly unnatural in context** |

### Pool 3 — Final Correct Group
*Function: completion, not victory. Never "you won." Never over-celebrates. Never duplicates what Reflection is about to do.*

| Line | Status |
|---|---|
| "That's all of it." | **Approved** |
| "That's everything." | **Approved** |
| "There it all is." | **Approved** |
| "All four, right there." | Proposed — slightly tally-like |
| "And there's the whole scene." | Proposed — still worth testing, but likely reads as internal Agrupa terminology rather than Sofía's spontaneous speech |
| "There's the picture." | **Retired — not quite natural enough on its own** |

---

## Reusable Interaction Pools — Ordinary Incorrect, One Away, Duplicate, Reveal

**Recovered directly from the implemented Restaurant Version 3 source, per Solara — Approved.**

### Ordinary Incorrect Feedback
*Function: selected when an incorrect guess is not a proximity ("One Away") or duplicate case. Rotates; a used line is not repeated within the same session while unused alternatives remain.*

| Line | Status |
|---|---|
| "Not quite." | **Approved** |
| "Not this group." | **Approved** |
| "Try another combination." | **Approved** |
| "Keep looking." | **Approved** |

### Other confirmed, separate interaction copy (not part of the rotating pool above — distinct message types)
- **One Away:** "One Away." — used only when exactly three of four selected Tiles belong together.
- **Duplicate guess:** "You already tried that group."
- **Fourth-incorrect-guess reveal transition:** "Not quite. Let's look at the whole puzzle together."

These three remain fixed, non-rotating messages, distinct from the four-line ordinary-incorrect pool above and from the correct-group acknowledgment pools.

---

## Reflection Copy (puzzle-specific — never templated)

**Governing rules for every Reflection note (confirmed by Solara — this is a standing checklist, not a one-time reminder):**

- Every puzzle ends with an individually authored personal note from Sofía that responds to that specific World or lived experience. **Not a rotating generic pool — see the two-category distinction above.**
- Uses Sofía's conversational register, never functional UI language.
- Must sound like something Sofía herself would actually say.
- Reflects the specific puzzle — never generic praise ("Great job," "You did it," "Learning is a journey").
- May include a brief observation, a small deadpan or humorous beat, and one sincere line when earned — a possible rhythm, not a mandatory template.
- Humor comes from Sofía's own perspective and self-awareness, never from mocking the player.
- Code-switching may appear when it sounds natural, never as mechanical translation.
- Short and restrained — Sofía does not speak merely because the screen has room (see Scarcity and Silence, README Section 4A). **Exception: unlike other conversational moments, a Reflection note itself is never skipped — every puzzle gets one, per README Section 4A's explicit Scarcity-and-Silence exception.**
- Every proposed note is reviewed as actual dialogue, exact wording preserved and approved. An abstract instruction like "Sofía encourages the player" is not sufficient — per the Dialogue Approval Rule.
- A puzzle-specific emoji may appear within the authored note when approved. **This is distinct from Athena's universal paw element** (README Section 4A) — the emoji is puzzle-specific content within the line itself; the paw is a constant, separate visual element near every signature, not part of the written copy.
- The written signature is always exactly: **— Sofía.** Nothing appended.
- **When multiple candidates all satisfy the rules above, the deciding question is "would someone who knows Sofía believe she would actually say this?" — not "which joke is funniest?" (new, confirmed Hair Salon, this revision).** Reflection is authentic dialogue first, humor second. See the Hair Salon entry below for the precedent case.

### Coffee Shop (already shipped, Prototype 0.2)
**Status:** Approved / Live
> "Coffee first. Spanish second." ☕
> — Sofía

### Restaurant (new, this revision — retired candidates, new candidates proposed)

**Character-continuity error, retired candidates (all three):**

| Retired candidate | Reason |
|---|---|
| "I ordered before I could translate the whole menu. Confidence, not fluency." 🍴 | Portrays Sofía as needing to translate a Spanish menu — she is naturally bilingual and a Spanish teacher, not a learner. Conflates the Foundation's player-facing hypothesis ("confidence precedes fluency") with Sofía's own character. |
| "I still don't know what everything on a menu means. I know what I want, though." 🍴 | Same error — implies incomplete Spanish comprehension |
| "Ordené antes de terminar de traducir el menú. Confidence over fluency, always." | Same error, in code-switched form |

**Root cause, recorded for future authoring:** these lines were drafted by borrowing the product's own philosophy about the *player's* learning journey and mistakenly voicing it as Sofía's personal uncertainty. Sofía's humor should come from ordinary bicultural life (choosing, deciding, everyday friction) — never from incomplete Spanish comprehension. This is now a standing check for any future Sofía-voice line, not just this entry.

**New candidates — humor about choosing, not understanding:**

| Candidate | Note |
|---|---|
| "I know exactly what I want… hasta que me dan el menú." 🍴 | **Approved.** First shipped use of natural code-switching in Sofía's conversational voice — natural, specific, no confusion between her identity and the learner's experience. |
| "Todo se ve bien. That's the problem." 🍴 | Proposed — strong second choice; sharper and more deadpan, may read as even more distinctly her, but the approved line is warmer for a first bilingual-rhythm moment |
| "I know exactly what I want… until they hand me the menu." 🍴 | Proposed, lowest priority — fine on its own, but contributes least to character continuity since it skips the code-switching entirely |

**Status:** Primary candidate Approved. Alternates remain Proposed for possible future use elsewhere.

### Hair Salon (Entry 003)

**Status:** Approved

> "Le dije 'un poco más corto' y salí con una nueva personalidad." ✂️
> — Sofía

**Retired candidate and the reasoning behind the choice — first character-level (not structural) precedent for Reflection writing, preserve for future authoring:**

| Retired candidate | Reason |
|---|---|
| "Le dije 'un poco más corto' y ahora parezco recién salida del ejército." | Recognizable and could be funny, but read as punchline-driven rather than something Sofía would actually say — exaggerated rather than gently self-aware. |

The approved version was preferred not because the retired one violated a rule, but because it better matched her established voice: conversational rather than punchline-driven, gently self-aware rather than exaggerated, rooted in an ordinary shared human experience, consistent with her warm bicultural personality.

**New standing authoring guidance, confirmed by Jamie/Solara — applies to all future Reflection candidates, not just this one:** when multiple candidates satisfy the formal rules (register, brevity, no mockery, etc.), the deciding question is **"would someone who knows Sofía believe she would actually say this?"** — not "which joke is funniest?" **Reflection is authentic dialogue first, humor second.** This is a distinct check from the character-continuity error caught on Restaurant's first draft (Sofía-as-learner) — that was a factual/identity error; this is a tonal/voice-fit judgment call between two otherwise-valid options.

---

## Not Yet Drafted

World-completion messages (if distinct from Pool 3), Home Screen onboarding conversational framing (if any — current draft is functional-register only, see README Section 9). To be added in future passes as prioritized.

## Governing Rules (inherited from README Section 4A — not restated in full here)

- Every conversational line must pass the ten-question Conversational Voice Test before status advances to Approved.
- No exclamation marks, per Agrupa's product-wide punctuation restraint, except where authentic spoken Spanish or literal clue content requires them.
- No exaggerated success language, achievement/grading language, generic encouragement, or escalating praise.
- Any line must be reviewed as an actual quotation, not approved as an abstract description of intended effect.

## Implementation Rule (new, this revision)

**Rotating pools must not repeat the same line twice within a single puzzle session.** Randomness alone can accidentally recreate the exact repetition problem the library was built to solve — e.g., "Nice catch." appearing for both the 2nd and 3rd correct group in the same playthrough. Selection logic should exclude any line already shown earlier in that session before rotating.
