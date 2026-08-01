---
status: active
owner: jamie
last_reviewed: 2026-08-01
depends_on: ./design-constitution.md, ./design-principles-v0.1.md, ./authoring-prompt-v0.3a.md
supersedes:
related: ./puzzle-production-ledger.md, ./copy-library.md, ./playtest-log.md, ./master-reference-v1.4.md, ../../characters/character-voice-methodology.md, ./sofia-observations-bank.md
---

# ¡Agrupa! — Canonical README v2.0

**Status of this document:** Orientation and index only. This README summarizes canon and research state; it does not replace the governing documents. Where this README and a governing document disagree, the governing document controls (see Section 11).

**Supersedes:** AGRUPA_README_CANONICAL_v1.0.md (not held in `ledger` — v1.0's unique content, if any, is not confirmed recoverable; flagged as an open item). **This revision (v2.0, synchronization-corrected) replaces an earlier draft of v2.0 that was already stale at the moment of writing** — it described the revised Coffee Shop board and Version 0.2/beta build as future work when both had already happened. Corrected per Solara's synchronization message: current live-build status, completed Coffee Shop rework and its test results, Ava's mostrador finding, the Beta Findings Log, and current (non-phased) team-role language.

**Honesty note, carried forward from v1.0 and still true:** This document reflects one project's conversation history. Its author (Claude) holds full context reliably within a single thread but not automatically across separate future ones — this document exists specifically so the project's state survives independent of that. Where evidence is thin, incomplete, or contested, this README says so rather than resolving it silently.

---

## 1. Project Overview

¡Agrupa! (originally "The No-Name Game") is a small, experimental, web-based daily puzzle for beginner learners of Spanish. Players reconstruct four recognizable pieces of everyday human experience ("Moments") from sixteen Spanish word/phrase fragments ("Tiles"), then discover the larger everyday context ("World") that unites all four.

**Current development stage:** Three builds now run separately — **Coffee Shop remains the stable, primary tester build (Prototype 0.2)**, protected from disruption; **Restaurant is a separate development build**, the current reference/baseline for shared standards (typography, onboarding); **Hair Salon is now also a completely separate app/deployment**, built this way specifically so Restaurant's live tester link stays untouched. **None of these three should be reconnected, merged, or have their live deployment reused/overwritten in a way that changes an existing tester link — standing rule, this revision.** **This entire build architecture is reported by Solara — not independently verified by Claude beyond what's stated here.** Which refinements validated in Restaurant or Hair Salon get backported into Coffee Shop / a shared foundation remains an open decision (Section 14).

**Immediate objectives, in order (updated, this revision):** (1) preserve Coffee Shop as the stable beta-testing build; (2) finish visual QA and founder review of Restaurant; (3) test Restaurant with independent players, with contemporaneous evidence capture; (4) decide which Restaurant refinements should be backported into the shared prototype foundation; (5) continue puzzle production and test enough Worlds before treating any one prototype as the gold standard; (6) bring Moment Independence to Jamie as a formal governance decision once a qualifying third occurrence exists.

---

## 2. Core Product Identity

**LOCKED — Design Constitution, Foundation, Puzzle Constitution.** Unchanged since v1.0 and unaffected by anything in this document. Design Constitution and Design Principles now live as their own canonical files — see `./design-constitution.md` and `./design-principles-v0.1.md`.

```
16 Tiles → 4 Moments (4 Tiles each) → 1 World
```

Players reconstruct a recognizable lived experience through evidence — not sorting vocabulary into semantic categories. This is Design Constitution Principle 1 ("Recognition Over Categorization") and Design Principle DP-001, and it remains the single most load-bearing idea in the project. See Section 8 for why this matters concretely, not just philosophically, in the Coffee Shop finding.

**Share-metadata secrecy rule (new, this revision — standing rule, not puzzle-specific).** No deployment title, browser title, text-message preview, social preview, metadata, filename, or tester-facing label may reveal the World before a player completes the puzzle. This directly protects the mechanic above — the World reveal is the intended climax of recognition (Section 3), and a link preview stating the World in advance defeats it before play begins. **Default share title: "Agrupa"** — never the World name (e.g., a Hair Salon deployment reading "Agrupa — Hair Salon" in a text-message preview was an early violation of this rule, corrected this revision).

---

## 3. Current Gameplay Rules

Updated to reflect Prototype 0.2 (Coffee Shop, the stable tester build) and Restaurant (separate development build — see Section 1). Items below are shared unless marked otherwise.

- **Board:** Sixteen Tiles, shuffled. On replay, the same sixteen Tiles reshuffle to new positions. **Built and confirmed working.**
- **Solving:** Player selects four Tiles, submits.
- **Feedback:** Immediate correct/incorrect confirmation on every submission. **Built.** John confirmed this was helpful in testing.
- **Mistake indicator:** The confusing "0/4, 1/4..." submit-button counter was removed. **Built.** Bilingual submit-button copy now reads: *Selecciona cuatro tarjetas · Select four cards.*
- **Onboarding:** Hamburger-menu "How to Play" access added. **Built.** John confirmed directions worked and the puzzle was easy to understand in this round.
- **Proximity feedback:** One Away implemented. **Built.** Two Away remains deliberately held back (DP-003 tension — see Section 8).
- **Duplicate-guess protection:** **Built.**
- **Reveal behavior:** Neutral, non-punitive language required at all times (Constitution Principle 5; DP-009) — governs the built reveal-state copy.
- **English support:** Discoverability improved. **Built.**
- **Solved-group colors:** Complementary colors per completed Moment. **Built.** Testers liked this.
- **Completed-board pause before Reflection:** **Built.**
- **Reflection screen:** Confirmed through direct testing as one of the strongest elements of the experience. **Now guaranteed on every puzzle, no exceptions (Section 4A, Scarcity and Silence exception, this revision).** Content has been updated and is working well; the Coffee Shop and Restaurant Reflection lines are formally Approved in the Agrupa Copy Library (Section 6).
- **Home Screen install onboarding — Restaurant only, reported not yet backported to Coffee Shop.** Per Solara: implemented — one-time post-completion prompt, persists after dismissal, permanent instructions in the hamburger menu, device-specific iPhone/Android wording, using the approved shortened message ("...so tomorrow's puzzle is one tap away"). Draft copy was written in this thread; formal Approved status in the Copy Library not yet recorded there — see Section 6.
- **Responsive Tile Typography — Restaurant and Hair Salon, reported not yet backported to Coffee Shop.** Per Solara: the three-tier system is implemented, not merely conceptual. **Exact pixel thresholds now adopted as the Agrupa baseline (this revision) — see Section 5.**
- **Solved-group presentation — Restaurant only, newly reported this revision, not independently verified beyond Solara's report:** solved groups retain their four visible Tiles rather than collapsing to only the Moment title; newly solved groups receive a gentle entrance animation.
- **Feedback rotation — Restaurant only.** Correct-group feedback rotates by solve position (per the Copy Library's approved position-aware pools, Section 6); no line repeats within a session. **Ordinary incorrect feedback rotates through a four-line Approved pool** ("Not quite." / "Not this group." / "Try another combination." / "Keep looking.") — recovered directly from the Restaurant implementation source, per Solara. **One Away, duplicate-guess, and the fourth-incorrect reveal transition remain separate, fixed, non-rotating messages**, distinct from the ordinary-incorrect pool and from each other. Full detail: Agrupa Copy Library.

---

## 4. Language Standards

**WORKING (Puzzle Constitution) — unchanged since v1.0.** Mexican Spanish default, A1–A2 target, B1+ permitted only under stated conditions, short mobile-readable Tiles, on-demand English gloss per Tile. Full Puzzle Constitution text: `./master-reference-v1.4.md`, Section 5.

---

## 4A. Sofía's Voice in Agrupa

**Status and Source:** This section is the product-specific application of the fuller Sofía Pérez — Voice Brief for Agrupa game copy/dialogue and its Family Context & Character Balance Addendum. Those documents remain the governing source for Sofía's history, personality, family context, established speech patterns, and long-term arc. If this section ever conflicts with the fuller approved character brief, the fuller character brief governs. (See Section 6 for the source document's index status. **Note, added during `ledger` migration:** no standalone Voice Brief document has been located — per Solara's reconciliation, this is embedded knowledge distributed across character development conversations, not a frozen missing artifact. See `../../characters/character-voice-methodology.md` for the related, more general character-methodology material extracted from Sofía's Little Observations.)

**Connective note, added during integration:** this section's "no exaggerated success, no shaming mistakes" guidance under Encouragement and Feedback is the tone-level implementation of already-locked **DP-009** ("revealed answers are part of learning, not evidence of failure") — the two should be read together, not as separate rules that happen to agree. Similarly, the exclamation-mark restraint below is a direct generalization of Jamie's decision to remove the exclamation mark from the product's own name — one founder decision, extended into a documented style principle.

### Purpose

Agrupa does not have a separate, manufactured "app voice." Agrupa is Sofía's product — she created it, authored it, and continues to refine it. The words players encounter throughout the game should naturally reflect the person who made it. Agrupa does not borrow, adopt, or imitate Sofía's voice; it speaks the way it does because Sofía wrote it. The goal is not to make educational software sound friendly — it is to preserve the authenticity of Agrupa's creator.

### Core Principle: One Voice, Two Registers

Every piece of copy should pass this test: *if Sofía built this herself, would she have written these words here?* The answer looks different depending on what the copy is doing. Agrupa uses one voice expressed through two natural registers — **functional** and **conversational**. These are not two versions of Sofía; they are two ways the same capable person naturally communicates in different contexts.

### Character Foundation

Sofía is 27, recently laid off, and building a Spanish YouTube channel and her first educational app during a genuine transitional period. She is intelligent, educated, capable, driven, emotionally grounded, self-aware, warm, modern, naturally bilingual, and quietly confident. Her current circumstances are a setback and a pivot, not her permanent identity. She comes from a loving, supportive, financially stable family and has a soft place to land — her humor about the current chaos comes from confidence and perspective, not desperation or incompetence. **She is not a "hot mess" character.** She is a capable person navigating a rough patch with grace, humor, and determination. Her long-term trajectory is toward successful entrepreneurship; Agrupa belongs to the beginning of that arc.

### Established Voice Characteristics

Self-deprecating with sincerity underneath; conversational rather than classroom-formal; talks to the audience as though they are already friends; confident enough to own chaos without apologizing for it; casual and slightly deadpan when things go wrong; naturally code-switched rather than mechanically translated; funny because she is perceptive and self-possessed; respectful and thoughtful; never sarcastic at the player's expense; capable of dropping the joke for one brief, sincere moment when it matters.

### Register 1 — Functional

Used for buttons, navigation, menus, settings, mode names, control labels, and other interface elements whose primary job is usability (e.g., Play Again, Menu, English, Settings — illustrative only, not locked UI strings; see the future Copy Library noted in Section 6). Clarity wins here: functional copy should be conventional, brief, accessible, restrained, consistent, easy to scan. A button does not need to sound like a spoken joke to belong to Sofía — a capable designer would not force personality into every tool label. **This does not exempt functional copy from character or quality.** "It is only a label" must not become a loophole for careless or generic writing. Even plain words can still feel like Sofía through restraint, bilingual choices, typography, spacing, and the absence of unnecessary friction. Plainness is not the same as genericness.

### Register 2 — Conversational

Used whenever Sofía is communicating directly with the player: the loading/opening greeting, feedback after a guess, encouragement, One Away feedback, duplicate-guess feedback, waiting/transition moments, the Reflection card, and closing/return invitations. This is where her full established character voice belongs — natural rhythm, gentle humor, short self-aware remarks, code-switching, warmth, deadpan acknowledgment, occasional vulnerability, and one sincere beat when earned. This register must never collapse into generic "friendly teacher" language.

### Emotional Relationship With the Player

Sofía talks *to* the player, not *at* them. She is not a classroom teacher grading performance, a game-show host, a motivational speaker, a cheerful mascot, an achievement announcer, a chatbot, or a narrator constantly explaining the interface. She is sharing something she made and staying present while the player explores it. The underlying emotional relationship: *we're figuring this out together.*

### Humor

Sofía's humor comes from her perspective, timing, intelligence, and self-awareness — brief, dry, lightly chaotic, gently deflective, confident, code-switched, self-directed. It is never loud for the sake of loudness, forced into every interaction, based on mocking a player's mistake, edgy at another person's expense, cruel toward her family, desperate, incompetent, artificially "relatable," or written like a brand imitating a young person. The joke should reveal character, not decorate the interface.

### The Joke-to-Sincere-Beat Pattern

One of Sofía's most distinctive established rhythms: she meets difficulty or uncertainty with a joke or light deadpan deflection; when the moment genuinely matters, she drops the joke and gives one short, direct, sincere line, without over-explaining the feeling afterward. Approved character examples from the fuller brief: *"Nadie contestó. Está bien. Está bien."* / *"Voy a lograrlo. De verdad."* / *"Gracias por estar aquí desde el episodio uno."* This rhythm should not be used mechanically on every screen — its value comes from scarcity. It is especially relevant for Reflection (below).

### Code-Switching

Natural, not translation-first — one bicultural person speaking naturally, not "Spanish sentence, English bolted underneath." The product may still display explicit bilingual labels or translations where required for usability (a functional design need, not a representation of Sofía's conversational cadence). When Sofía herself speaks conversationally, naturalness governs the blend, not a fixed formatting template.

### Encouragement and Feedback

Sofía should make the player feel noticed, not scored. Feedback may confirm a correct group, acknowledge proximity, gently redirect after an incorrect attempt, flag a repeated guess, and make room for another attempt. It should not exaggerate every success, announce "winning," sound like a reward system, grade ability, shame mistakes, or over-celebrate routine progress. *(See connective note above — this is DP-009's tone-level expression.)*

### Reflection

Reflection uses the conversational register and is one of the strongest opportunities for Sofía's full voice, since it occurs after the player has space to look back. It should not feel like a report card, performance summary, score announcement, generic congratulatory screen, language lecture, or motivational speech — it should feel like Sofía briefly looking back at the experience with the player. A strong Reflection moment may follow (not as a required template, but as a rhythm to consider): a short character-specific observation → an optional light/deadpan beat → one direct sincere line → a simple functional return action. Reflection copy must be authored as an actual line of Sofía's, not paraphrased into generic sentiments like "you did great" or "learning is a journey" — those describe an intended effect, not her words.

**Signature and paw print — resolved and superseded, this revision.** Every Reflection note is signed plainly: **— Sofía**. One small, low-opacity paw appears nearby as a separate visual element. In the approved Hair Salon treatment, the paw is centered beneath the word "Sofía," rather than beneath the full signature line including the dash. It must remain visually distinct from the signature and must not read as a logo, stamp, appended character, or formal two-line signature block.

**Resolution history, preserved for context:** the earlier rule stated the paw was "not a stacked icon under her name" and explicitly rejected anything "directly underneath, like a signature block." That blanket prohibition on any placement beneath the name conflicted with the approved live Hair Salon treatment (centered beneath the word "Sofía") and **is now superseded by the more precise rule above.** The distinction that survives from the original decision: what's actually prohibited is a *logo/stamp/signature-block* read (paw + full "— Sofía" line treated as one graphic unit) — not placement beneath the name itself, which the original wording overstated. The paw represents Athena (Sofía's dog, Future Story Seed canon in Casa Pérez) resting nearby while she writes — it should read as something the player *notices*, not something *presented* to them, consistent with the Scarcity and Silence principle below.

**Distinct from each puzzle's own themed emoji** (e.g., Coffee Shop's ☕, Restaurant's 🍴, both already Approved in the Copy Library) — the paw is a constant, universal element appearing on every Reflection screen; the emoji is puzzle-specific content within each authored line. These should not be conflated in implementation.

**Still open, pending live UI review (visual/build, not content):** exact paw size, opacity, spacing from the signature, final placement in the Reflection layout.

**Explicit scope boundary, preserved as stated:** this decision does not authorize or begin work on Sofía's broader character architecture, biography, or personality — that work has not started. Within Agrupa specifically, Athena exists only as this one background environmental detail, nothing further.

### Scarcity and Silence

Sofía should not speak simply because the interface has space. A line should be added only when it improves clarity, reassurance, emotional connection, character continuity, player momentum, or the meaning of Reflection. If removing a line improves the experience, remove it. Agrupa does not use Sofía to fill empty space.

**Exception, explicit (this revision — Jamie's decision, discussed with Solara):** this discretion does not apply to Reflection. **Every puzzle ends with a Sofía note, with no exceptions.** Testing without one felt cold, less personal, and less likely to bring a player back — Reflection is exactly the moment this document already identifies as the strongest opportunity for her voice, and it should never be silently skipped. All other Scarcity and Silence discipline (loading greeting, in-line feedback, etc.) is unchanged — this exception is scoped to Reflection only.

### Punctuation and Exclamation Marks

Agrupa itself is written without exclamation marks (see connective note above). Interface copy uses punctuation with restraint. Exclamation marks may appear when they are a natural part of authentic Spanish speech or the literal content of a clue — e.g., **¡Ay, quema!** and **¡Listo!** from the revised Coffee Shop board (Section 7/8) — but should not be used automatically to manufacture enthusiasm. Avoid generic copy like "Amazing!" or "Great job!" unless a future line is explicitly approved as genuinely in-character and contextually earned.

### Authoring Process

**Question Zero, before writing or approving any line:** is this a functional/navigational label, or a moment of communication with the player?

*If functional* — evaluate for clarity, brevity, consistency, accessibility, scanability, usefulness, then confirm restraint and bilingual presentation remain compatible with Sofía's authorship.

*If conversational* — apply the full Conversational Voice Test: (1) Would Sofía actually say this? (2) Does it follow her established rhythm rather than generic friendly-teacher language? (3) Does it sound like a real person speaking to people she already treats as friends? (4) If humor is present, is it grounded in her perspective rather than added decoration? (5) Does her confidence read as capability rather than chaos? (6) Is the line respectful to the player and to everyone else? (7) Is any sincere beat earned, brief, and free of over-explanation? (8) Does code-switching, if present, feel natural? (9) Is the line shorter than it could be? (10) Does this moment genuinely need Sofía to speak? If the answer to any question is no, revise or remove the line.

**Dialogue Approval Rule:** any proposed line of Sofía's must be presented as an actual quotation and reviewed as dialogue — not as an abstract design intention like "Sofía encourages the player." Her exact wording, timing, and tonal movement are what determine whether the character is preserved.

**Character-Fit Tie-Breaking Rule (new, this revision — confirmed via the Hair Salon Reflection precedent, Agrupa Copy Library):** when multiple candidate lines all satisfy the formal rules above, the deciding question is **"would someone who knows Sofía believe she would actually say this?"** — not "which option is funniest?" Reflection, and Sofía's dialogue generally, is authentic character first, humor second. This is distinct from the character-*continuity* check (never portraying her as needing to translate Spanish, etc.) — that catches factual/identity errors; this catches tonal ones between two otherwise-valid options.

### Character Continuity Standard

A player should be able to play Agrupa, watch Sofía's YouTube channel, and return to Agrupa, experiencing one continuous person. The app and the channel may use different registers because they perform different functions, but neither should feel like a different Sofía. Consistency requires integrity of worldview, intelligence, warmth, confidence, humor, bilingual rhythm, vulnerability, and restraint — not identical sentence structures everywhere.

### Closing Principle

Agrupa does not use Sofía to give the app personality. Agrupa has personality because it is something Sofía chose to build. This voice system exists to preserve that truth.

---

## 5. Visual & Instructional Design Principles

### Locked (Design Constitution + Design Principles v0.1, DP-001–DP-009)

Unchanged since v1.0 — see `./design-constitution.md` and `./design-principles-v0.1.md` for full text. Core commitments: recognition over categorization; every clue contributes distinct evidence; support preserves discovery; mistakes and reveals are part of learning, never framed as failure; coherence must be genuine, not retrofitted; recognition is the tie-breaker among otherwise-acceptable choices; shared humanity over spectacle.

### Working / Research-Stage (status updated this revision — see Section 8 for full evidentiary detail)

- **Moment Independence** — each Moment must own a sufficiently independent recognizable experience, or two Moments compete for the same underlying activity. **Status: Corroborated** (two qualifying occurrences — Movie Theater, Gas Station). Not yet Recurring Pattern. Candidate for a future Puzzle Constitution rejection criterion, pending Jamie's governance review.
- **Content-type boundary criterion (new, this revision)** — refines Moment Independence's mechanism. Two adjacent Moments fail independence not simply because a World is sequential, but specifically when a Tile's **real-world referent** inherently recurs at more than one phase of the lived experience — **regardless of how the Tile is worded.** Rewording does not fix a referent that genuinely happens twice in real life (e.g., a customer's name, said at both ordering and pickup). This is a **revision** of an earlier working idea (self-contained-sub-activity vs. continuous-sequence), not a separate hypothesis — the earlier framing did not survive a retroactive check against the repaired Movie Theater puzzle, which is sequential but works. **Status: one retroactive analytical pass, live authoring evidence from the Coffee Shop rework, and one encouraging initial test round of the revised board. The criterion remains a strong working direction, not yet validated.** See Sections 7 and 8.
- **Visual density ratio, the "ritual" authoring lens** — unchanged from v1.0, still informal working techniques, not research-established.
- **Tile-level shared recognition** ("does this land for someone other than its author") — unchanged from v1.0, one clear occurrence, still watched.
- **English Gloss Naturalness Self-Check (new, this revision) — new formal authoring step, added following the discovery that Spanish naturalness review and English gloss review are genuinely separate checks (Ledger Entries 004/005).** After Spanish content is finalized, before presenting a board for independent review, run a separate pass over every English gloss asking: (1) would a natural English speaker actually say this, or does it read as translated? (2) does it capture the *feeling*/register of the Spanish, not just the dictionary meaning? (3) is it over-translated (too literal, stiff) or under-translated (loses meaning)? (4) would a learner tapping this Tile immediately think "oh, that's what that means here"? **Explicit limitation, stated for the record:** this is a self-check performed by the same model and does not substitute for independent review (currently Solara) — it's a pre-filter, not a replacement. **Note for future code automation:** the architecturally sound version of a "second view" is a genuinely separate model call reviewing finished content without the generation reasoning — ideally a different underlying model entirely — not the same model role-playing a second persona.

  **This is a research protocol, not a promise of value — status: experimental, evaluated on evidence.** Beginning with Ledger Entry 006, this becomes a distinct, documented step in the production workflow before any board is submitted for independent review. For each puzzle, the Ledger will record: whether this pass identified any issues; what those issues were; whether they would likely have been caught later during independent review. The purpose is not simply to add another checklist item, but to evaluate whether this step measurably improves first-pass quality over time. After several additional puzzles, the evidence should answer: does this step consistently catch issues before independent review? What kinds of issues does it catch? Does it reduce the revision required after Solara's review? Does it improve authoring consistency across different Worlds? **If the evidence shows meaningful value, it can be considered for promotion from a working technique into the canonical authoring workflow. If it doesn't demonstrate measurable benefit, it will be revised or removed — not preserved because it sounds useful.**

- **Structural Completeness Check (mandatory, not experimental) — added following an incident during Entries 006/007 authoring where Laundromat and Birthday Party were both presented to Jamie with missing Tiles** (Laundromat: Folding had 2 of 4, Heading Out had 3 of 4; Birthday Party: The Cake had 3 of 4). **This is not a new rule — it's a mechanical verification of already-locked canon** (Foundation Core Vocabulary; Puzzle Constitution Core Structure: 16 Tiles, 4 Moments of 4). The gap was a verification failure, not a governance gap: content-quality checks (naturalness, referent-recurrence) were being actively applied while the most basic structural count was not, because it was assumed rather than mechanically confirmed. **Required as the final step, after every other check, before any board is presented:** count each Moment (must equal exactly 4 Tiles); count the total (must equal exactly 16); confirm every Tile has both a Spanish line and an English gloss present; **confirm a Reflection note exists and is at least Proposed (see expansion below).** **Presentation format note:** boards should be presented as plain per-Moment lists, not markdown tables, when being shared for review — a dropped row in a table is not visually obvious the way a numbered list stopping short is; the incident occurred during table-based mid-edit restructuring. This check is mandatory going forward, not subject to the same evaluate-and-possibly-remove framing as the English Gloss Self-Check above, since it verifies existing locked structure rather than testing a new technique.

  **Scope expanded, this revision, following a second incident: Entries 004–007 all reached "Approved" Ledger status with no Reflection note at all**, despite the locked Section 4A rule that every puzzle ends with one, no exceptions. Root cause: the check above verified Tile completeness but never explicitly included Reflection presence as a gate condition, so a real requirement had no mechanical enforcement. **A puzzle may not be marked Approved in the Ledger without an at-least-Proposed Reflection note on file.** This is now an explicit, checked precondition for Approved status, not an assumed one.

- **English glosses optimize for recognition, not grammatical completeness (new working principle, this revision — Solara, confirmed on Entry 007's "Need help?" gloss) — explicitly a working pattern to watch, not yet canon.** A shorter, natural English fragment that evokes the same mental moment as the Spanish is generally preferable to a grammatically fuller sentence on a Tile — e.g., "Need help?" over "Do you need help?" even though the latter more completely mirrors "¿Necesitas ayuda?" Consistent with other approved glosses following this pattern: "Hands full," "Cash," "Finally," "What a good haul." The reasoning: Agrupa's glosses are recognition cues, not textbook translations — their job is triggering the same remembered moment while staying quick to scan on a mobile Tile, not maximizing grammatical fidelity to the Spanish. **Status: working principle to watch across the next several boards before considering promotion to the formal English Gloss Naturalness Self-Check criteria above.**
- **Responsive Tile Typography (this revision) — resolves the Puzzle Constitution's original open item ("exact maximum character or word count... established through prototype testing").** The resolution is not a number — a fixed character-count limit was considered and explicitly rejected as the wrong kind of answer: character count is a poor proxy for fit, since long phrases of short words wrap differently than single wide words, Spanish accents/punctuation affect rendering, and a hard limit would pressure authors toward weaker label-style Tiles over stronger dialogue-style ones (directly undermining the finding above). Instead: a permanent three-tier responsive system — **Standard**, **Compact**, **Extra Compact** — where the renderer measures actual rendered text, not character count, and steps down a tier only when needed. If a Tile still doesn't fit cleanly at Extra Compact, it does not shrink further — it returns to authoring review.

  **Adopted pixel baseline (confirmed via real-device testing, this revision):**
  - Unsolved Tiles: 13px / 12px / 11px (Standard / Compact / Extra Compact)
  - Solved Tiles: 10px / 9px / 8px
  - Responsive auto-fit behavior stays active throughout.

  **Provenance:** Hair Salon was initially built larger (15px/13.5px/12px) but real-device iPhone testing showed this felt visually heavy and crowded longer clues. Hair Salon was corrected to match Restaurant's existing sizing exactly — the design rationale isn't simply "smaller is better," it's that this specific sizing creates more visual breathing room and better supports pattern recognition; clues read as calmer and less intimidating.

  **Status: Working — adopted as the Agrupa baseline for unsolved and solved Tile typography across future puzzles, unless later testing gives a specific reason to change it.** Not marked fully Locked — this is a strong working default validated by real testing, not yet the kind of multi-cycle-validated decision this project reserves full Locked status for.
- **Moment Identity Statement Check (new, this revision) — added following the Neighborhood Park "los columpios" catch (Entry 008).** A genuinely new category, distinct from referent-recurrence and DP-002 duplication: a Tile can be technically valid (no cross-Moment conflict, no in-Moment redundancy) while still sitting in a *worse-fit* Moment than another available one. Mechanical checks (does this referent repeat? is this a duplicate?) don't catch best-fit placement, because there's no conflict to detect — only a better option elsewhere. **Required step, before Tiles are drafted:** write a one-sentence Moment Identity Statement for each of the four Moments — the specific *kind* of thing that Moment is about, not just its label (e.g., not "Arriving," but "first sensory impressions on entering"). **Required step, before a board is presented:** hold every Tile up against its own Moment's identity statement specifically, not only against the other three Tiles already assigned to it. **Explicit limitation, stated for the record — do not oversell this check:** unlike Structural Completeness (binary, mechanical), this is a judgment call. It should reduce how often a Tile ends up in a not-quite-right Moment, but it is not expected to eliminate the need for independent review to catch the remainder — closer in kind to the Content-Type Boundary Criterion and Dialogue-over-Label techniques above than to the purely mechanical checks.
- **Visual QA step (new, this revision) — new permanent step in the production workflow**, distinct from authoring review. Runs after build, before release, per puzzle: every Tile fits cleanly; no awkward line breaks; Spanish remains readable; English remains readable; no clipping or overflow; visual balance preserved across the board. This is a build-quality check on what the player actually sees, not an authoring-time rule — keep it out of the Authoring Prompt and Puzzle Constitution; it belongs in the Agrupa Puzzle Production ledger's per-entry review process (Section D) once formalized there.

---

## 6. Canonical Document Index

| Document | Version | Status |
|---|---|---|
| Master Reference Document | v1.4 (as of last formal integration) | 🟢 Canonical continuity record — see `./master-reference-v1.4.md` |
| Design Constitution | Locked | 🟢 LOCKED CANON — see `./design-constitution.md` |
| Design Principles | v0.1 (DP-001–DP-009) | 🟢 LOCKED CANON — see `./design-principles-v0.1.md` |
| Authoring Prompt | v0.3a | 🟢 Locked baseline — see `./authoring-prompt-v0.3a.md` |
| Foundation | v0.1 | 🟡 Working — see `./master-reference-v1.4.md` Section 4 |
| Puzzle Constitution | v0.1 | 🟡 Working — see `./master-reference-v1.4.md` Section 5 |
| Evidence Base | Working | 🟡 Working, citation recovery pending — see `./master-reference-v1.4.md` Section 9 |
| Research Change Log (RCL) | RCL-003–RCL-H01 | 🟡 Working — governs Authoring Prompt experiments specifically — see `./master-reference-v1.4.md` Section 8 |
| Puzzle Batch One Evidence Log (PBO) | Ongoing | 🟡 Working — content playtests, distinct from RCL. **No standalone document located; per Solara, embedded knowledge, not a missing artifact.** |
| Beta Findings Log (Prototype 0.2) | Ongoing | 🟡 Working — see Section 9; product/UX findings from Jamie/John/Ava testing of Prototype 0.2, distinct from PBO's puzzle-content-only scope |
| **Agrupa Puzzle Production** (Ledger) | Entries 001–003 | 🟢 **Canonical, authoritative for current-workflow puzzles** — see Section 7; board content, authoring provenance, review status, and eligibility for every puzzle produced under the current AI-authoring workflow. Excludes the index-card era by design. Playtesting evidence is summarized here as status only — full session records live in the Playtest Log (below). See `./puzzle-production-ledger.md`. |
| **Agrupa Playtest Log** (new, this revision) | Active | 🟢 **Raw per-session capture**, distinct from both the Ledger and the Beta Findings Log — who played, which build, support mode, completion experience, quotes, observed issues. The Ledger points here for evidence rather than duplicating it; the Beta Findings Log holds synthesized findings/action items *derived from* sessions recorded here. Three-way split: Playtest Log = what happened; Beta Findings Log = so what; Ledger = current status. See `./playtest-log.md`. |
| **Diagnostic Protocol** | v0.2 | 🟡 **Working — architecture frozen pending validation; two provisional items noted in Section 8.** No standalone document located; per Solara, embedded knowledge. Durable extracted insights: `./diagnostic-methodology-notes.md`. |
| **Recognition Model v0.1** | Draft | ⚪ **Effectively superseded** — its four-level hierarchy was formalized and absorbed into the Diagnostic Protocol's Localization Levels (Tile / Moment Evidence Set / Moment-boundary / World / Board) during terminology reconciliation. Kept for historical reference only. No standalone document located. |
| Sofía Pérez Voice Brief + Addendum | v1 | 🟡 Working creative reference — governs Section 4A (this README); **not canon dialogue itself**; addendum corrects an early mischaracterization (she is capable and stable, not an underdog/"hot mess" character). No standalone document located; see `../../characters/character-voice-methodology.md` for related, more general material. |
| Agrupa Copy Library | Active — largely Approved | 🟢 **Both structural questions resolved:** (1) position-aware rotation — First / Middle (2nd+3rd, shared) / Final correct-group pools; (2) reusable pools stay World-agnostic, puzzle-specific voice lives only in each puzzle's authored Reflection line. **Approved and live:** correct-group acknowledgment pools (12 lines across 3 pools); ordinary-incorrect feedback pool (4 lines, recovered from Restaurant Version 3 source); One Away, duplicate-guess, and reveal-transition messages (fixed, non-rotating); the Coffee Shop and Restaurant Reflection lines; an anti-repeat rule. **Critical distinction, confirmed by Solara:** reusable interaction pools (correct/incorrect/One Away/duplicate/reveal) and puzzle-specific authored Reflection notes are two fundamentally different categories — Reflection is never a rotating pool, is authored individually per puzzle, and is guaranteed on every puzzle with no exceptions (README Section 4A). Home Screen onboarding copy was drafted in this thread but not yet formally marked Approved despite being reported as shipped in Restaurant. See `./copy-library.md`. |
| Jamie's Instructional Philosophy | Discovery Draft v0.1 | 🟡 Working, cross-product — see `./master-reference-v1.4.md` Section 3 |
| Governance Log | Master Reference Section 13 | 🟢 Present — see `./master-reference-v1.4.md` Section 13 |
| Version 0.2 Early Access Findings (Jamie's brain dump) | Raw, this session | 🟡 Working — see Section 9 for sorted content. No standalone document located; per Solara, embedded knowledge. |

---

## 7. Puzzle Inventory

**Current production puzzles (Coffee Shop, Restaurant, and all future AI-authored boards) now live in the Agrupa Puzzle Production ledger — the authoritative source for board content, provenance, review status, and eligibility.** This README no longer duplicates that detail; see `./puzzle-production-ledger.md` for the full record of Entry 001 (Coffee Shop) and Entry 002 (Restaurant).

**Historical index-card era (research record only — not migrated into the Ledger; see Ledger front matter for the scope decision):**

| World | Status | Notes |
|---|---|---|
| Family Road Trip | Corrected 4-Moment structure exists (Packing the Car / Gas Station Stop / Choosing the Music / Missing the Exit). Not confirmed playtested. | |
| Grocery Store | Playtested (John, screenshot format) — testing-method confound identified. | |
| Movie Theater | Initial version failed (Moment-boundary overlap: seat-selection evidence split across two Moments). Repaired version retested successfully. | Qualifying Moment Independence occurrence #1. |
| Gas Station | Moment-boundary issue identified (Brandon: "gas cap"/"pump 6"). **Repair not finalized as of last record.** | Qualifying Moment Independence occurrence #2. |
| Beach Day | Pre-playtest authoring revision only. | |
| Public Swimming Pool / Busy Morning at Home | Status unknown — evaluated in the original six-World naturalness round, not confirmed authored. | |

**Original Coffee Shop board:** retired (founder decision). Full evidence record preserved in the Ledger's Entry 001, Section C (Authoring Provenance), rather than here.

**Same caveat as v1.0, still true for the historical table above:** not confirmed to be a complete record of all index-card–era puzzles authored. This does not apply to current production puzzles, which are tracked authoritatively in the Ledger going forward.

---

## 8. Research Status

### Validated
- The core recognition architecture (evidence-based Moments, not vocabulary sorting) produces a working, enjoyable player experience — RCL-003, reinforced by Brandon's clean Coffee Shop solve and the Prototype 0.1 Early Access round overall (voluntary replay with zero external incentive).
- Narrow semantic clustering / insufficient contrast degrades the experience — RCL-005, independently reproduced during Puzzle Batch One's World→one-Moment execution drift.

### Corroborated (two qualifying occurrences — real, but short of Recurring Pattern)
- **Moment Independence** — Movie Theater and Gas Station qualify under the Diagnostic Protocol's Route A (Documented-or-better, independent human playtests). Coffee Shop does **not** currently qualify as a third occurrence — see Section 7.

### Active Hypotheses (genuinely open, ranked by maturity)
1. **Content-type boundary criterion — now tested once, results encouraging but not yet conclusive.** See Section 5. The revised Coffee Shop board (Section 7) is the first real test: John's feedback was broadly positive (clues clearer, no reported Moment-boundary confusion); Ava's one finding (mostrador/counter, above) was a gloss-specificity issue, not a repeat of the original naming/gratitude referent problem the criterion was designed to fix. **This is one test, two testers — encouraging, not yet sufficient to call the criterion validated.** More testing needed before treating it as more than a strong working direction.

   **New candidate watch item, explicitly unvalidated** (two occurrences — naming, gratitude — caught in a single puzzle-authoring session, zero independent playtests yet): social-script content (greetings, thanks, names, small courtesies) appears structurally high-risk for Moment-boundary violations, since these scripts repeat at every human-contact touchpoint in an interaction rather than staying tied to one physical/temporal phase. Physical, object, and sensory content does not share this risk. Not a rule — does not meet Route A's recurrence bar — a caution for authors to watch for a third occurrence elsewhere.

   **Process note:** the AI author applying this criterion missed both instances on first pass despite direct application of the rule — reinforces why the Puzzle Constitution's native/fluent human review requirement catches more than surface naturalness; it catches real-world-knowledge gaps a structural check alone can miss.
2. **Moment Evidence Set vs. Moment-boundary localization** — a provisional isolation test exists ("evaluate the four Tiles as though no other Moment existed") but has not yet been exercised against real, ambiguous data — Coffee Shop's original run resolved to Insufficient Evidence before this distinction became relevant.
3. **Group-level ambiguity** (do four individually-clear Tiles still fail to resolve collectively) — untested as an independent question.

4. **Authoring methodology generalization across social settings (new, this revision — growing confidence, not a conclusion).** Farmers Market and Doctor's Office (Ledger Entries 004/005) were developed deliberately as a structural contrast test against the existing service-counter Worlds (Coffee Shop, Restaurant, Hair Salon) — different Moment sequencing (non-sequential vs. sequential), different register (tú vs. usted), different underlying setting type (retail/browsing vs. healthcare/logistics). Both passed independent naturalness review cleanly. Per Solara's own explicit framing, preserved here: this is "encouraging evidence that the methodology is becoming more robust," but should be "treated as growing confidence rather than a final conclusion until more playtests are complete." **Status: zero playtests yet on either board — this is authoring-and-review-stage evidence only, not validated methodology generalization.**
4. **RCL-H01** (hidden authoring channels) — two independent occurrences observed across the project's history. Explicitly not validated and not permitted to shape locked content, even as illustrative example, until independently confirmed.
5. **New (this revision) — bilingual gloss specificity.** Ava's testing of the revised Coffee Shop board found "mostrador" (glossed as "counter") ambiguous — it could refer to either the ordering counter or the pickup counter. This is a **Documented, specific, attributed finding** from real testing of the *revised* board — the first real evidence the revised board has produced. Candidate general check, explicitly held as a working hypothesis, not yet promoted: **a Tile must remain Moment-specific in both its Spanish text and its English gloss** — a Tile can pass the content-type/referent test in Spanish while its English gloss reintroduces ambiguity the Spanish didn't have. One occurrence; needs recurrence before consideration for canon. Recommended immediate content fix (not a governance change): gloss "mostrador" as "pickup counter" specifically.

**Strengthened finding, this revision:** the ambiguity signal on the original Coffee Shop board is stronger than the earlier record reflected. Per Jamie's direct observation, every tester who played the original board, unprompted, proposed restructuring it toward categorical grouping. This is two separate claims, and they carry different evidentiary weight:
- *"The puzzle was ambiguous enough that multiple independent testers wanted to fix it"* — a real, repeated, convergent signal. This raises the priority and confidence of the underlying ambiguity finding beyond what the two individually-captured playtests (John, Brandon) show on their own.
- *"Categorical grouping is the correct fix"* — a separate claim, not established by the same evidence. Testers proposing a familiar genre convention (grouping-puzzle-style categories) as their fix is useful data about default player intuition, but it is not a diagnosis that categorization is architecturally correct — it directly conflicts with locked Constitution Principle 1 and DP-001, and adopting it would require real governance review, not adoption-by-popularity.

**Explicit test order, decided this revision:** the content-type boundary criterion is tested first, on its own, before any consideration of categorical grouping. **Categorical grouping is recorded as an explicit fallback candidate — to be considered only if the content-type approach fails to resolve the ambiguity across repeated, properly captured tests — not as a parallel option under simultaneous consideration.** See Section 14 for the sequenced plan.

### Open Questions
- Difficulty progression across Moments — unaddressed, variables not yet separated.
- Whether players expect chronological order within a Moment — one player observation (Brandon), not treated as a design requirement.
- Formal inter-tester repeatability — most evidence to date reflects a design-test-diagnose-repair cycle with individual testers, not yet validated across multiple independent testers on the same puzzle.
- Whether the Diagnostic Protocol's Localization Levels need an explicit interaction rule when a diagnosis spans more than one level simultaneously.

---

## 9. Beta Findings Log (Prototype 0.2 — Jamie, John, Ava)

This is Documented, founder-observed material from testing Prototype 0.2, sorted per the project's established three-bucket discipline (content / product experience / product strengths). **This section now reports on a built and tested product, not a pre-build backlog — see Section 3 for what's shipped.**

**Protect (confirmed working well — do not change without reason):**
- Onboarding (How to Play access).
- Visual palette — testers explicit: do not change existing colors, only add complementary solve-state colors.
- Solved-group colors.
- Immediate correct/incorrect feedback.
- One Away feedback.
- English support.
- Reflection screen and content.
- Encouragement tone.
- Replay flow (reshuffle on Play Again).

**Fix or review (specific, targeted, not architectural):**
- **mostrador → "counter"** gloss is insufficiently Moment-specific — see Section 8. Recommended fix: "pickup counter."
- **Step 1 instruction wording:** current "Find four Spanish clues…" should drop the redundant word "Spanish" — revised: "Find four clues that belong to one everyday moment."
- Every English gloss should be checked for Moment specificity, per the new candidate check in Section 8 — not yet a systematic audit, just a flagged direction.
- ~~Bilingual inactive submit-button copy~~ — **already corrected:** *Selecciona cuatro tarjetas · Select four cards.*

**Later / explicitly deferred:** Buy Me a Coffee, Sofía's YouTube/social links, accounts, progress tracking, teacher features, **a "recent puzzles" access feature (decided against — see below)**.

**Approved for future build, not yet implemented:**
- **Home Screen install onboarding — Implemented in Restaurant (per Solara, this revision); not yet backported to Coffee Shop.** One-time post-completion prompt, persists after dismissal, permanent instructions in the hamburger menu, device-specific iPhone/Android wording, using the shortened message drafted in this thread ("...so tomorrow's puzzle is one tap away"). **Formal Approved status in the Copy Library not yet recorded — treat as implemented-but-not-formally-audited until confirmed.**

**Puzzle-archive product decision (resolved, this revision):** the "Recent Puzzles" access feature (previously discussed as "last 3 puzzles") has been decided against, not merely parked. **Founder decision:** Agrupa ships daily-puzzle-only for the MVP — no player-facing access to prior puzzles at all — to keep the experience simple and protect the daily ritual. A future paid, one-time-unlock archive remains a genuine long-term direction, to be considered once a substantial library of high-quality puzzles exists — a future product discussion, not current build work. This decision is independent of the Agrupa Puzzle Production ledger, which continues recording every puzzle from creation regardless of whether or when any player-facing archive ever ships.

**One item flagged for governance, not UX — status unchanged from prior revision:** Jamie's Early Access notes recorded that every tester who played the *original* Coffee Shop board proposed restructuring its Moments into categorical groupings (e.g., "Seating: tables, booth, bar stools, cozy chairs"). This remains a genuinely repeated, multi-tester suggestion, and it materially strengthened the case for reworking the original board — which has now happened, via the content-type boundary criterion (Section 7/8), not via categorization. As a category-based (not lived-experience-based) grouping, the categorization proposal still runs directly against locked Constitution Principle 1 and DP-001. **Status, updated this revision: the primary path (content-type criterion) has now had one encouraging test. Categorical grouping remains an explicit fallback, not adopted and not pursued in parallel, per the original decision.**

---

## 10. Current Build Objective

Two parallel objectives, per the Coffee Shop / Restaurant split (Section 1): **(a)** keep Coffee Shop stable and continue its beta round with contemporaneous evidence capture (per the Diagnostic Protocol's Capture stage), including the still-pending mostrador gloss and Step 1 wording corrections; **(b)** finish visual QA and founder review of Restaurant, then test it with independent players. Once Restaurant's testing produces real evidence, decide which of its refinements (Home Screen onboarding, responsive typography, solved-group presentation, rotating feedback) get backported into Coffee Shop / the shared prototype foundation, rather than assuming all of them transfer automatically.

---

## 11. Source-of-Truth Hierarchy

Unchanged from v1.0, with the Diagnostic Protocol's place made explicit:

1. Design Constitution
2. Design Principles v0.1
3. Approved Puzzle Records (status unconfirmed — see Section 7)
4. Research Change Log (Authoring Prompt experiments specifically)
5. Diagnostic Protocol v0.2 (methodology governing how PBO evidence is captured, classified, and diagnosed — sits alongside PBO, beneath the documents above)
6. README (this document) — summarizes canon and research state; does not replace either.

**Same flagged clarification as v1.0, still unresolved:** whether the Master Reference is a peer document below the Constitution, or the container document that holds the Constitution and Design Principles as internal sections. Not resolved by this revision either — still recommend Jamie/Solara confirm explicitly.

---

## 12. Document Status Legend

Unchanged from v1.0: 🟢 LOCKED / 🟢 APPROVED / 🟡 WORKING / 🟡 EXPERIMENTAL / ⚪ SUPERSEDED / ⚠️ OPEN.

---

## 13. Team Roles & Process (current work, not fixed phases)

- **Jamie** — Founder, Product Owner, retains final decision authority for canon and product decisions (Master Reference Section 0A).
- **Solara** — Currently implementing and testing the live prototype build.
- **Claude** — Consolidating and checking the written record; currently leading documentation synchronization at Jamie's direction.

Responsibilities overlap and shift with the work rather than switching on and off by phase — nobody is "paused" while someone else is "active"; the team works in parallel and this section describes current focus, not exclusive lanes. Major milestones should still conclude with a synchronization document (like this one) so the written record doesn't lag behind what's actually happened.

---

## 14. Recommended Next Steps, in Order

1. ~~Resolve the version-number question~~ — **Resolved:** Coffee Shop is Prototype 0.2 (Jamie's decision).
2. **Make the two still-outstanding Coffee Shop content corrections**: gloss "mostrador" as "pickup counter"; simplify Step 1's instruction wording.
3. ~~Hand Restaurant to Solara for implementation~~ — **Reported complete, this revision.** Restaurant has been implemented, polished internally, and awaits or is undergoing independent player testing (per Solara; Ledger status updated accordingly, Section 6).
4. **Finish visual QA and founder review of Restaurant**, then proceed to independent player testing with contemporaneous evidence capture.
5. ~~Recover the exact ordinary-incorrect feedback pool text~~ — **Recovered, this revision, per Solara.** Four-line Approved pool now in the Copy Library.
6. **Formally mark the Home Screen onboarding copy Approved in the Copy Library** — it's reported as shipped in Restaurant, but the Library hasn't recorded that status yet.
7. ~~Resolve open visual specs for the Reflection screen's paw print element~~ — **Resolved, this revision.** Governing rule updated (Section 4A) to reflect the approved Hair Salon treatment; earlier blanket prohibition superseded.
7a. ~~Set exact Responsive Tile Typography thresholds~~ — **Resolved, this revision.** 13/12/11px unsolved, 10/9/8px solved, adopted as the Agrupa baseline via real-device testing (Section 5).
8. **Decide which Restaurant/Hair Salon refinements get backported into Coffee Shop / a shared foundation** — Home Screen onboarding, responsive typography, solved-group presentation, rotating feedback — once testing produces real evidence, not automatically.
9. **Finalize the two still-provisional Diagnostic Protocol items**: the Moment Evidence Set vs. Moment-boundary isolation test, and any needed multi-level interaction rule.
10. **Bring Moment Independence to Jamie as a discrete governance decision** once a third qualifying occurrence exists.
11. **Continue puzzle production and test enough Worlds before treating any one prototype as the gold standard.**
12. **Design the Agrupa tester-link share-preview card** (new, this revision) — branded preview image, neutral World-agnostic description, consistent across all puzzle builds, proper Open Graph/social metadata rather than a raw onboarding-screen screenshot. **Explicitly not to be designed or implemented without Jamie's approval — do not begin this without direct authorization.**
13. ~~Jamie's decision needed: "la receta" in Doctor's Office~~ — **Resolved, this revision.** Keep as-is.
13a. ~~English gloss independent check needed for both Entries 004 and 005~~ — **Resolved, this revision.** Solara completed a separate learner-facing gloss review for both boards. Farmers Market: zero changes. Doctor's Office: one revision ("súbase aquí" → "hop up here").
14. **Build and playtest Farmers Market (Entry 004)** — fully approved, cleared to build.
15. **Build and playtest Doctor's Office (Entry 005)** — fully approved, cleared to build.
16. **Parked idea, not yet actionable (Solara, this revision): a future "Failure Modes" taxonomy section** — recurring authoring-error categories (structural omission, referent recurrence, English gloss ambiguity, Moment-boundary overlap, weak recognition evidence, visual density issue, translation drift) are beginning to look like named classes rather than isolated incidents. **Explicitly not enough data yet — revisit around Entry 012,** once several more Ledger entries exist to confirm which categories actually recur versus which were one-off.

---

## 15. How to Onboard a New Collaborator (Human or AI)

Unchanged in spirit from v1.0: read this README first, then the Design Constitution, then the Master Reference in full (including Design Principles and the Governance Log), then the current active thread. Confirm understanding — distinguish an established rule from a rediscovery, a rediscovery from a genuine new finding, and a finding from an actual governance proposal — before suggesting changes. If in doubt about status or authority, ask and flag explicitly rather than resolving unilaterally. That habit is the throughline of this project's entire governance discipline, demonstrated repeatedly and concretely throughout the Coffee Shop validation process described above.
