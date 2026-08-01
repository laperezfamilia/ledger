---
status: working
owner: jamie
last_reviewed: 2026-08-01
depends_on: ../../characters/character-voice-methodology.md
supersedes:
related: ./copy-library.md, ./README.md
---

# Sofía's Little Observations — Agrupa Application

**Provenance note:** this document was originally titled "Agrupa Reflection Voice Bank," then renamed "Sofía's Little Observations" once Solara recognized it collects something broader than Agrupa Reflection copy — hundreds of tiny things Sofía notices about ordinary life, extending to Shorts, Casa Pérez conversations, the AI chat, and Etsy products. The general character-architecture insight behind that discovery (the Three Lenses, the Human Recognition Diagnostic) now lives at `../../characters/character-voice-methodology.md`. This file keeps the practical observation bank and its Agrupa-specific application, split per Jamie's instruction: "split the knowledge, but preserve the source."

**Status:** Working. Batch 1 (below) is partially re-sorted against the confirmed diagnostic; Batches 2 and 3 (Jamie's and Solara's contributions) are still awaited. What's used in Agrupa Reflections is a subset of this bank, not the whole purpose of the document — see `./copy-library.md` for lines that have actually shipped.

**Agrupa's working rule:** everything collected and used for Reflection should come from Lens 2 (see `../../characters/character-voice-methodology.md`'s Three Lenses) — noticing the world, not narrating herself.

---

## Calibration Rule 2 — Specificity Over Genericness

A generic version and an Athena-specific version can express the same idea with very different results:
- *"The dog treats itself to whatever falls on the floor"* — good, but could be any dog.
- *"Athena has never once believed something falling on the floor was an accident"* — same idea, but now it's specifically **her** world, not a generic observation. Better.

**Working implication:** where a real, established detail from Sofía's actual life (Athena, specific people, specific habits) can replace a generic stand-in without forcing it, that's usually the stronger version.

## Calibration Rule 3 — Vary the Cadence

Avoid repetitive openers ("There's always..." / "Somebody always...") across many lines in sequence — after ~10 examples the pattern becomes noticeable as a *device* rather than reading as natural noticing. Examples of varied rhythm, same voice:
- "The corner piece disappears until someone says they don't care which piece they get."
- "Every waiting room has that one magazine nobody admits they're reading."
- "I still think warm towels deserve more credit."

---

## Batch 1 — Claude's original 30, re-sorted against the confirmed rules

**✅ Yep, that's her**
16. The last slice sits there for twenty minutes out of politeness.
18. The dog treats itself to whatever falls on the floor. *(Solara's Athena-specific rewrite is stronger — see Rule 2.)*
22. Every group photo has one person still getting ready.
27. The candles never blow out on the first try.
30. Nobody's ever actually "just looking."
11. Somebody always says "just a light trim" and means something else entirely. *(people self-delusion — fits the Human Recognition Diagnostic cleanly)*
15. Somebody's going to save you a seat they don't have room for. *(people behavior)*
17. Everyone has a coffee order they pretend is simple. *(people self-delusion)*
21. Somebody's definitely going back for seconds and calling it "just a little more." *(people self-delusion)*
26. Somebody's going to ask "is this seat taken" about an empty room. *(social ritual, people behavior)*

**🌊 Confirmed drift — "universe is unfair" cluster (Bucket C)**
5. The good parking spot appears right when you give up looking.
8. The line moves fastest right after you switch lines.
12. The ice always melts before you're ready for it to.
14. The umbrella works perfectly until you actually need it.
20. The good radio station only comes in for two minutes.
25. The bag always rips on the way to the car, never before.
29. The last box always weighs more than the first ten.

**🎀/📚 Other flagged drift**
1. There's always a slowest walker directly in front of you. *(too cynical, not warm — Solara)*
2. Someone's phone is always at 1%. *(generic internet joke — Solara)*

**Borderline cases, resolved this revision:**
- 7. Somebody's going to ask if the WiFi password is case-sensitive. — **Bucket A ✅.** Predictable social behavior; someone really does ask this. Passes more strongly than first assessed.
- 19. There's always a receipt nobody asked for. — **Bucket C ❌.** No person revealed — a system default, not a human dynamic.
- 10. The waiting room clock runs slower than every other clock. — **Bucket C ❌ as worded.** Objective claim about the clock, not a human belief; possibly rescuable with reframing (see the framing observation in the methodology doc) — e.g., "Everyone swears the waiting room clock is broken."
- 23. The last piece of the puzzle is never where you left it. — **Bucket C ❌ as worded.** Same issue as #10; possibly rescuable the same way.

**Not yet re-evaluated (remaining original lines):** 3, 4, 6, 9, 13, 24, 28. *(28, the missing-sock line, should likely be excluded from the general bank regardless of quality — too close to the retired Laundromat-specific Reflection candidate in `./copy-library.md`.)*

---

## Batch 2 — Jamie's contribution

*(awaiting)*

## Batch 3 — Solara's contribution

*(awaiting)*

---

## Calibration Notes (the actual point of this document)

- **"Too teacher"** tends to happen when an observation explains *why* it's true instead of just stating it.
- **"Too stand-up"** tends to happen when a line has a setup/punchline shape rather than a single flat observation.
- **The Human Recognition Diagnostic is the core check**, not just "avoid irony." Ask whether a person's psychology/behavior/social dynamic *causes* the pattern, or whether a person merely *notices* an independently-existing mechanical fact. "Situational Mechanics" (Bucket C — receipts, clocks, puzzle pieces, umbrellas, parking, radio signal) is now a named, confirmed failure category, not a one-off preference — seven+ examples from one batch alone.
- **Framing can rescue a Bucket C rejection (untested hypothesis)** — the same phenomenon may cross from Bucket C to Bucket A if reframed as a human belief/admission ("everyone swears the clock is broken") rather than an objective claim about the object ("the clock runs slower"). Worth testing deliberately on more Bucket C rejects before treating this as confirmed.
- **Specificity (Rule 2)** — a generic version is a fine draft, but check whether a real established detail from her actual life would make it stronger before finalizing.
