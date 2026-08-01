---
status: active
owner: jamie
last_reviewed: 2026-08-01
depends_on: ./puzzle-production-ledger.md
supersedes:
related: ./README.md
---

# Agrupa Playtest Log

**Status:** Working canonical document. Raw, per-session playtest capture — distinct from two related documents, not a replacement for either:

- **Agrupa Puzzle Production (Ledger):** what was authored, reviewed, approved, built, and deployed, per puzzle. Points here for evidence rather than embedding it.
- **Beta Findings Log (README Section 9):** synthesized product/UX findings and action items *derived from* sessions recorded here — the "so what," not the raw record.

This document is the "what happened," captured as close to verbatim as available — who played, which build, support mode used, completion experience, observed difficulty, enjoyment, usability issues, and notable quotes. Per-session entries here should not be re-interpreted or summarized in place; synthesis belongs in the Beta Findings Log or in a puzzle's Ledger entry, with a pointer back to the specific session(s) here.

## Entry Format

Each session: Tester · Puzzle/Build · Date (if known) · Support mode used · Completion outcome · Notable quotes · Observed issues · Pointer to any Ledger entry or Beta Findings Log item this session informed.

---

## Coffee Shop (Prototype 0.2)

**Session — John**
Puzzle: Coffee Shop (revised board) · Build: Prototype 0.2 · Method: index cards (pre-digital)
- One transient misplacement: "first sip" initially placed with Wait and Receive, self-corrected after one incorrect-response signal.
- Full solve. Correct World inference ("going to a coffee shop and ordering coffee").
- Quote: enjoyed and loved the puzzle; described the learning value as acquiring sixteen words/phrases connected to one experience.
- Informs: Ledger Entry 001, Section E.

**Session — Brandon**
Puzzle: Coffee Shop (revised board) · Build: Prototype 0.2
- 100% correct on first attempt, zero misplacements.
- Quotes: "It was genuinely entertaining." / "It was cool." / "It was challenging in a good way." Also mentioned difficulty sustaining attention generally, but still found the game engaging.
- Informs: Ledger Entry 001, Section E.

**Session — Ava**
Puzzle: Coffee Shop → Restaurant, same session · Build: Prototype 0.2 (Coffee Shop) / Restaurant Version 3
- Coffee Shop: "mostrador" glossed as "counter" was ambiguous (order counter vs. pickup counter).
- See Restaurant section below for her Restaurant session (same tester, later session).
- Informs: Ledger Entry 001 Section E (mostrador finding); Beta Findings Log (gloss-specificity correction, approved).

**Session — Claire**
Puzzle: Coffee Shop · Build: Prototype 0.2
- Found the 🔍 English feature; translated text was too small to notice at first ("oh wait, the English words are small").
- Asked "do I start over with a new game?" after solving — resolved as a first-time-tester check-in, not confusion; she had already seen Reflection and "Play again" correctly.
- Informs: Ledger Entry 001, Section E (legibility finding, distinct from Restaurant's font-size finding below — do not conflate).

**Sessions — Julie and Denham (open gap, added during `ledger` migration)**
Puzzle: Coffee Shop-era, exact board/build unconfirmed · Two separate testers
- Solara recalled (via reconciliation memo) that Jamie discussed feedback from Julie and Denham during the Coffee Shop testing period, and that their feedback contributed to the founder decision to retire the original Coffee Shop board due to recurring ambiguity.
- **No session notes exist yet to reconstruct which exact build they tested, their complete observations, or whether their comments differed from the other testers.** Per Solara's own caution: "I don't want to invent details that aren't supported by the record."
- Jamie has confirmed she remembers the feedback both gave and can provide it — **not yet recorded as of this revision.**
- Informs: Ledger Entry 001, Section E (original-board retirement rationale, partial evidentiary basis) — pending detail.

---

## Restaurant (Version 3)

**Session — John**
Build: Restaurant Version 3
- Overall response: good and fun. Liked clear confirmation on correctly solved groups. Liked the Home Screen install popup.
- On completion: "Got it!" — suggests the completed-puzzle/reveal sequence successfully communicated the overall experience.
- **Accessibility finding, not preference:** asked whether Tile font could be made larger — has poor vision. Current responsive typography keeps text inside Tiles but does not guarantee comfortable readability.
- Informs: Ledger Entry 002, Section E; README Section 5 (Responsive Tile Typography — open accessibility question).

**Session — Ava**
Build: Restaurant Version 3 (played the day after her Coffee Shop session, via text link)
- Reported Restaurant as fun, better, clearer, and easier than Coffee Shop.
- Opening instructions made English-support options clear — had not previously realized during Coffee Shop that support mode was adjustable.
- Switched to "Show all English" mode. Completed in ~2 minutes, zero incorrect guesses, no clue found notably tricky.
- Noticed and liked the varied correct-group encouragement phrases.
- **Confound, explicitly preserved:** faster completion should not be attributed to puzzle difficulty alone — two likely factors: (1) Restaurant's clearer onboarding/support controls, (2) prior familiarity from Coffee Shop the day before. "Show all English" also reduces language burden independent of difficulty. Do not read this session as "Restaurant is too easy."
- Informs: Ledger Entry 002, Section E; identifies need for first-time-user testers (see Open Items below).

**Session — Jamie (founder)**
Build: Restaurant Version 3
- Founder direct play-test, positive. Decision: keep Restaurant active for continued tester rotation; do not overwrite the current build.
- Informs: Ledger Entry 002, Section E (founder observation, not independent playtest).

---

## Hair Salon (Entry 003)

**Session — John**
Build: Hair Salon (post real-device typography/paw/share-title corrections)
- Completed successfully. One incorrect submission, received One Away feedback, immediately corrected and completed.
- No signs of frustration.
- Liked that solved groups remain visible after flipping — naturally reviewed completed Moments while finishing the board.
- Read the entire Reflection screen before exiting. Response: "Okay, good. Yep, I got it." — suggests Reflection is achieving its intended function: not just reward, but a sense of understanding and closure.
- Overall: "The puzzle's good."
- No ambiguity issues identified. No UI concerns surfaced.
- Informs: Ledger Entry 003, Section E.

---

## Farmers Market (Entry 004)

No sessions yet — approved for playtest, not yet built.

## Doctor's Office (Entry 005)

No sessions yet — content fully approved and locked (la receta resolved, Jamie's decision: kept as-is). Cleared to build.

---

## Open Items for Future Sessions

- **Restaurant font-size/accessibility:** needs a larger-text treatment evaluated (Tile dimensions, spacing, clue-length limits, or a dedicated accessibility setting) without introducing clipping or crowding. Preserve current build as tested baseline.
- **Restaurant needs first-time-Agrupa-user testers** — all current Restaurant sessions involved testers with prior Coffee Shop exposure, which confounds difficulty/speed readings. Priority for next test round.
- **Julie and Denham's Coffee Shop-era sessions** — real testers, feedback contributed to the original board's retirement, but no session-level detail recorded yet. Jamie has confirmed she can supply this; add here once received.
