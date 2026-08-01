---
status: active
owner: jamie
last_reviewed: 2026-08-01
depends_on: ./design-constitution.md, ./design-principles-v0.1.md
supersedes:
related: ./README.md, ./playtest-log.md, ./copy-library.md
---

# Agrupa Puzzle Production

**Status:** Working canonical document. Authoritative board inventory and provenance record for puzzles produced under the current AI-authoring and review workflow.

## Purpose

This document answers, per puzzle: *what is the exact current board, how did it get here, what is its status, and where is the supporting evidence?*

It is a **production and provenance record**, not a duplicate of the full research evidence. It links out to the Research Change Log (RCL), Puzzle Batch One evidence (PBO), and the Beta Findings Log rather than re-narrating their contents. It also functions as an accuracy record for the authoring workflow itself — tracking what the AI got right on first pass, what independent review caught, what founder review changed, and what only human testers exposed.

## Scope and Numbering

Numbering begins at **001** with the current, digital, AI-authored workflow (World Naturalness Test → Moments → Parallel Specificity → Tiles → authoring checks → independent review → founder approval → build → test). It intentionally **excludes** the earlier index-card prototype era (Family Road Trip, Grocery Store, Movie Theater, Gas Station, Beach Day, the original Coffee Shop board, etc.). Those remain valuable historical research and stay recorded in PBO/RCL and the README's puzzle-history sections — they are not migrated or reconstructed here. An older World may enter this Ledger later, but only if deliberately revived and re-authored under the current workflow; its prior prototype form does not carry over automatically.

**Puzzle ID convention:** sequential number + World slug (e.g., `001-coffee-shop`). IDs are fixed at creation and never reused, even if a puzzle is later retired.

## Status Values

**Lifecycle status (single source of truth per entry):** Draft → Independent Review → Ready for Build → Testing → Revision Required → Approved → Retired.

**Eligibility flags (Section G, each entry):** boolean, and each is gated on lifecycle status — a puzzle cannot be flagged eligible for anything beyond Draft/Review purposes until it reaches **Approved**. Eligibility flags do not replace or duplicate lifecycle status; they answer a separate, later question (*can this specific approved puzzle be used for X*), not *is it done yet*.

---

## Entry 001 — Coffee Shop (Revised Digital Board)

### A. Identification
- **Puzzle ID:** 001-coffee-shop
- **World:** Coffee Shop
- **Board version:** Revised (replaces retired original board)
- **Current status:** Testing
- **Date created (revised board):** This project's Coffee Shop rework session
- **Date last revised:** Following Ava's mostrador finding (correction pending build)
- **Current build:** Prototype 0.2

### B. Current Board

**Order Your Drink**
| Tile (ES) | Gloss (EN) |
|---|---|
| menú | menu |
| ¿grande o chico? | large or small? |
| ¿aquí o para llevar? | for here or to go? |
| tarjeta o efectivo | card or cash |

**Wait and Receive**
| Tile (ES) | Gloss (EN) |
|---|---|
| mostrador | counter — **correction approved, not yet built: "pickup counter"** |
| esperar | to wait |
| ¡Listo! | ready! |
| buscar tu vaso | look for your cup |

**Customize**
| Tile (ES) | Gloss (EN) |
|---|---|
| palito | stir stick |
| sobres de azúcar | sugar packets |
| tapa | lid |
| servilletas | napkins |

**First Sip**
| Tile (ES) | Gloss (EN) |
|---|---|
| primer sorbo | first sip |
| ¡Ay, quema! | ow, that's hot! |
| soplar | blow on it |
| ahh | satisfied sound |

### C. Authoring Provenance

- **Predecessor:** replaces the retired original Coffee Shop board. Original board's Order Your Drink Moment contained "your name?" and Wait and Receive contained "here you go" — both removed because their real-world referents (identification, gratitude) recur at more than one phase of the experience regardless of wording. Full original-board record and retirement rationale: README Section 7; founder decision documented there.
- **Revision driver:** live authoring session applying the referent-based content-type boundary criterion (first articulated during this rework — see README Section 5/8), the dialogue-over-label technique, and the social-script recurrence caution.
- **Self-audit note:** the authoring pass initially missed two things a second check caught — see README Section 8 for the full account (this is the origin case for the referent-based criterion itself).
- **Naturalness refinements during authoring:** "para llevar" → "¿aquí o para llevar?" (dialogue over label); "quema" → "¡Ay, quema!" (natural spoken reaction).

### D. Review Checklist
| Check | Result |
|---|---|
| World Naturalness Test | Passed (retrospective on original World selection; unaffected by board revision) |
| Parallel Specificity | Passed |
| Moment Independence | Passed — original-board violations resolved, not recurring on revised board |
| Referent-recurrence check | Passed on revision; originating case for this check |
| Social-script recurrence check | Passed on revision; originating case for this check |
| Dialogue-over-label review | Applied ("¿aquí o para llevar?") |
| Mexican Spanish naturalness | Founder-reviewed live during authoring |
| A1–A2 suitability | Passed |
| Bilingual-gloss specificity | **Issue found post-build — see Ava's finding below. Not yet re-verified after correction.** |
| Visual-density / mobile readability | Passed |
| Second independent review | Not formally run as a discrete step (predates the two-reviewer process established for Entry 002) |

### E. Playtesting Evidence

**Full session records now live in the Agrupa Playtest Log ("Coffee Shop (Prototype 0.2)" section) — this is a status summary only, not the raw record.**

Six sessions to date: John (transient self-corrected slip, full solve, positive), Brandon (clean 100% first-attempt solve, positive), Ava (mostrador gloss finding, corrected — see Section C), Claire (English-translation legibility observation, monitoring, no change approved pending recurrence; "start over" question resolved as non-issue), Julie (loved the game, suggested solved-group colors / One Away / duplicate-guess feedback, positive on classroom suitability), Denham (suggested "missed tries" framing, more encouraging in-game feedback, reduced onboarding friction). **Julie and Denham's suggestions plausibly map to several since-built features (solved-group colors, One Away, duplicate-guess protection, onboarding, removal of the confusing mistake counter) — see `./playtest-log.md` for the full detail and the caveat that this provenance link isn't confirmed, just plausible.**

**Related open finding (not Coffee-Shop-specific):** How to Play does not currently explain that Play Again reshuffles the same sixteen Tiles, or that switching English-support mode between attempts allows self-adjusted difficulty. Tracked in Beta Findings Log; not a defect of this board.

### F. Revision History
| Change | Reason | Evidence | Board Version |
|---|---|---|---|
| Removed original naming/gratitude Tiles; full rework | Referent-recurrence across Moment boundaries | Founder direct observation (5 original participants) | Original → Revised |
| "para llevar" → "¿aquí o para llevar?" | Dialogue over label | Founder judgment during authoring | Revised (draft) |
| "quema" → "¡Ay, quema!" | Natural spoken register | Founder judgment during authoring | Revised (draft) |
| "mostrador" gloss: "counter" → "pickup counter" | Bilingual gloss specificity | Ava, Prototype 0.2 playtest | **Approved, not yet built** |

### G. Eligibility and Future Use
- Eligible for beta/test deployment: **Yes** (currently live, Testing status)
- Daily production release: **Pending Approved status** (per Ledger rule: eligibility flags require Approved lifecycle status; current status is Testing pending mostrador gloss correction)
- Recent-access feature: **Not planned for MVP — decided against** (daily-puzzle-only is a resolved founder decision, not a parked option; see README Section 9)
- Eligible for future paid archive: Pending — requires Approved status; currently Testing pending gloss correction
- Eligible for curated pack: Not yet evaluated
- Classroom suitability: Not yet evaluated
- Open issues: mostrador gloss correction not yet built/re-verified

---

## Entry 002 — Restaurant (First AI-Authored Board)

### A. Identification
- **Puzzle ID:** 002-restaurant
- **World:** Restaurant
- **Board version:** 1 (post-independent-review)
- **Current status:** **Testing.** Reported by Solara, this revision: implemented, gone through multiple internal polishing passes, awaiting or undergoing independent player testing. **Not independently verified by Claude beyond Solara's report.** Full lifecycle "Approved" status still requires completed playtest evidence per Section G — implementation alone does not satisfy that gate.
- **Date created:** This project's Restaurant authoring session
- **Date last revised:** Same session (post-review corrections)
- **Current build:** Separate development build (reported by Solara; distinct from Coffee Shop's stable Prototype 0.2 build — see README Section 1)

### B. Current Board

**Getting Seated**
| Tile (ES) | Gloss (EN) |
|---|---|
| ¿tienen reservación? | do you have a reservation? |
| mesa para dos | table for two |
| por aquí | this way |
| esta es su mesa | this is your table |

**Ordering Your Meal**
| Tile (ES) | Gloss (EN) |
|---|---|
| ¿qué recomienda? | what do you recommend? |
| ¿qué va a pedir? | what are you going to order? |
| para mí… | I'll have… |
| ¿algo de tomar? | something to drink? |

**Enjoying the Meal**
| Tile (ES) | Gloss (EN) |
|---|---|
| buen provecho | enjoy your meal |
| está delicioso | it's delicious |
| pásame la sal | pass me the salt |
| más pan, por favor | more bread, please |

**Paying the Check**
| Tile (ES) | Gloss (EN) |
|---|---|
| la cuenta, por favor | the check, please |
| ¿con tarjeta o en efectivo? | card or cash? |
| la propina | the tip |
| quédese con el cambio | keep the change |

### C. Authoring Provenance

**Provenance summary:** Claude — first-draft author and self-audit. Jamie — initial founder review, confirmed the board's core structure and direction. Solara — subsequent independent review; identified "el menú" as the stronger Moment-boundary risk and proposed both naturalness refinements. Jamie — final founder review and approval of the resulting board.

- **World Naturalness Test:** Passed easily — Restaurant decomposes into standardized phases (arriving/seating, ordering, eating, paying) more readily than Coffee Shop did even pre-revision.
- **Moments judged naturally available, parallel in scope:** Getting Seated → Ordering Your Meal → Enjoying the Meal → Paying the Check.
- **First-pass AI author (Claude) self-audit flagged:** "buen provecho" and "más pan, por favor" as possible boundary risks.
- **Founder review by Jamie confirmed the board's core structure and direction** — first-pass self-audit findings (below) were carried forward into this review, not superseded by it.
- **Self-audit (Claude) findings, confirmed acceptable on review:** "buen provecho" and "más pan, por favor" — both flagged by the first-pass author as possible boundary risks; both judged acceptable — "buen provecho" correctly belongs at Enjoying the Meal (said as food arrives/eating begins, not order confirmation); "más pan, por favor" is *less* ambiguous than a bare "pan, por favor" because "más" implies the meal is already underway.
- **A subsequent independent review by Solara identified "el menú" as the stronger Moment-boundary risk:** handed over at seating, used at ordering; referent spans the Moment boundary regardless of wording. Removed, replaced with "¿qué recomienda?" (dialogue, ordering-exclusive, adds guidance-request evidence type not otherwise on the board).
- **Solara's independent review also proposed two additional naturalness refinements:**
  - "¿qué le puedo traer?" → "¿qué va a pedir?" — original phrasing could recur later if a server asks about dessert/refills; revised phrasing anchors specifically to placing the meal order.
  - "¿cómo desea pagar?" → "¿con tarjeta o en efectivo?" — more concrete, more natural in Mexican Spanish, more beginner-accessible.
- **Second audit (post-correction) found:** no remaining referent-recurrence, social-script, bilingual-gloss, or Moment-boundary issue.
- **Jamie reviewed and gave final founder approval to the resulting board.** Status confirmed Ready for Build.
- **Status of this result:** authoring and self-audit result only. **Not yet playtest-validated.**

### D. Review Checklist
| Check | Result |
|---|---|
| World Naturalness Test | Passed |
| Parallel Specificity | Passed |
| Moment Independence | Passed (post-correction) |
| Referent-recurrence check | Failed on first pass (el menú) — corrected, passed on second pass |
| Social-script recurrence check | Passed — no recurring courtesy/naming content anywhere on board |
| Dialogue-over-label review | Applied ("¿qué recomienda?" replacing a label-style Tile) |
| Mexican Spanish naturalness | Jamie's founder review, followed by Solara's secondary independent review; final revisions approved by Jamie |
| A1–A2 suitability | Passed |
| Bilingual-gloss specificity | Passed |
| Visual-density / mobile readability | Passed |
| Second independent review | **Yes — Jamie's initial founder review, followed by Solara's secondary independent review. First formal multi-pass review under this workflow; this entry is the origin case for requiring independent review as a standard step. Final approval by Jamie.** |

### E. Playtesting Evidence

**Full session records now live in the Agrupa Playtest Log ("Restaurant (Version 3)" section) — this is a status summary only, not the raw record.**

Three sessions to date, all positive overall: John (liked correct-group confirmation and the install popup; clean completion; **also raised a genuine accessibility finding — Tile font too small for reduced vision, distinct from Claire's Coffee Shop legibility finding, see Playtest Log**), Ava (fun/clearer/easier than Coffee Shop, ~2 min clean solve — **explicit confound preserved: prior Café familiarity + full-English mode, not attributable to puzzle difficulty alone**), Jamie (founder direct play-test, positive; decision to keep Restaurant active for continued rotation).

**Open next steps, both from Solara:** (1) evaluate a larger-text accessibility treatment without introducing clipping/crowding, preserving the current build as tested baseline; (2) prioritize first-time-Agrupa-user testers for the next round, since all current sessions carry the prior-familiarity confound.

### F. Revision History
| Change | Reason | Evidence | Board Version |
|---|---|---|---|
| "el menú" removed → "¿qué recomienda?" | Referent spans Getting Seated / Ordering boundary | Jamie's founder review, followed by Solara's secondary independent review; final revisions approved by Jamie | Draft → v1 |
| "¿qué le puedo traer?" → "¿qué va a pedir?" | Prevents future recurrence with dessert/refill offers | Jamie's founder review, followed by Solara's secondary independent review; final revisions approved by Jamie | Draft → v1 |
| "¿cómo desea pagar?" → "¿con tarjeta o en efectivo?" | Naturalness, specificity, beginner clarity | Jamie's founder review, followed by Solara's secondary independent review; final revisions approved by Jamie | Draft → v1 |
| Board content finalized; handed to Solara for build | Content review complete, no outstanding issues | Founder approval, this revision | v1 (unchanged content, status advanced) |

### G. Eligibility and Future Use
- Eligible for daily release: Pending successful build, playtest, and Approved status
- Recent-access feature: **Not planned for MVP — decided against** (daily-puzzle-only is a resolved founder decision, not a parked option; see README Section 9)
- Eligible for future paid archive: Pending Approved status
- Eligible for curated pack: Not yet evaluated
- Classroom suitability: Not yet evaluated
- Open issues: none identified in review; awaiting build and first playtest to confirm

---

## Entry 003 — Hair Salon (First-Round-Approved Board)

### A. Identification
- **Puzzle ID:** 003-hair-salon
- **World:** El salón de belleza — Hair Salon
- **Board version:** 1 (post-founder-review)
- **Current status:** **Testing.** Built as a completely separate app/deployment from Restaurant (specifically so Restaurant's live tester link stays untouched), gone through real-device iPhone testing, corrected (typography, paw placement, share title — see Section F), and reported ready for another tester round. **Build authorization confirmed, this revision:** Jamie explicitly approved the proposed separate-app plan with "Let's build." Hair Salon was then implemented as an independent deployment, preserving Restaurant and Coffee Shop unchanged — not an unapproved implementation.
- **Date created:** This project's Hair Salon authoring session
- **Date last revised:** Following real-device testing corrections (typography, paw placement, share title)
- **Current build:** Separate, standalone app/deployment — distinct from both Coffee Shop and Restaurant, does not share or overwrite either live tester link

### B. Current Board

**Checking In**
| Tile (ES) | Gloss (EN) |
|---|---|
| ¿Tiene cita? | Do you have an appointment? |
| ¿A nombre de quién? | What name is it under? |
| ¿Quién sigue? | Who's next? |
| Espere aquí, por favor. | Wait here, please. |

**Getting the Cut**
| Tile (ES) | Gloss (EN) |
|---|---|
| la capa | the salon cape |
| tijeras | scissors |
| un poco más corto | a little shorter |
| el espejo | the mirror |

**Making Conversation**
| Tile (ES) | Gloss (EN) |
|---|---|
| ¿De vacaciones? | Going on vacation? |
| mucho tráfico hoy | lots of traffic today |
| ¿Y la familia? | How's the family? |
| ¿Viste el partido? | Did you see the game? |

**Paying and Leaving**
| Tile (ES) | Gloss (EN) |
|---|---|
| ¿Cuánto es? | How much is it? |
| la propina | the tip |
| ¿Le gustó? | Did you like it? |
| Hasta la próxima. | Until next time. |

**Reflection (Approved, this revision — see Agrupa Copy Library for full authoring precedent and retired-candidate reasoning):**
> "Le dije 'un poco más corto' y salí con una nueva personalidad." ✂️
> — Sofía

### C. Authoring Provenance

**Provenance summary:** Claude — first-draft author and self-audit. Jamie — independent review; caught a near-duplicate farewell pair and a register-consistency issue the first-pass self-audit missed; approved final board.

- **World Naturalness Test:** Passed — arguably more intuitive than Restaurant, given the salon visit's highly standardized single-visit structure.
- **Moments:** Checking In → Getting the Cut → Making Conversation → Paying and Leaving. Deliberately split by content type rather than pure sequence, since conversation runs concurrent with the cut in real life but is a distinct content type.
- **First-pass self-audit (Claude) caught two referent-recurrence risks during drafting, corrected before first review:** a generic "have a seat" phrase originally risked appearing at both Checking In and Getting the Cut (same trap as Restaurant's "el menú"); a hair-color reference originally risked blurring Making Conversation into Getting the Cut's technical content. Both replaced before the board was first shared.
- **Founder review (Jamie) caught what self-audit missed:**
  1. "ya casi" replaced with "¿A nombre de quién?" — more diagnostic check-in interaction; English gloss no longer adds information the Spanish doesn't contain.
  2. "el tráfico de hoy" → "mucho tráfico hoy" — reads as natural conversational fragment rather than a formal label.
  3. "¿Y tu familia?" → "¿Y la familia?" — more idiomatic in casual Mexican conversation; avoids an unmotivated tú/usted register shift against the rest of the board. **Self-audit gap, acknowledged:** this register-consistency check was missed on first pass.
  4. **"nos vemos pronto" and "hasta la próxima" identified as near-duplicate** — both communicate essentially the same farewell sentiment within one Moment, a direct DP-002 violation ("every clue must contribute distinct, meaningful evidence"). **Self-audit gap, acknowledged:** this is exactly the class of error DP-002's Operational Test is designed to catch and it was missed on first pass. Resolved: "nos vemos pronto" removed, replaced with "¿Le gustó?" — distinct interaction content (satisfaction check) rather than a second farewell.
- **Naming-referent check (Claude, before finalizing):** "¿A nombre de quién?" introduces identification-type content, the same category that caused Coffee Shop's original naming problem. Checked explicitly against the rest of this board: no second naming or name-calling moment exists elsewhere in Hair Salon's four Moments, so the referent does not recur here. Passes, but flagged as the board's closest-to-the-edge Tile given this project's established watch pattern on social-script/identification content.
- **Second audit (post-correction) found:** no remaining referent-recurrence, social-script duplication, or Moment-boundary issue.

### D. Review Checklist
| Check | Result |
|---|---|
| World Naturalness Test | Passed |
| Parallel Specificity | Passed |
| Moment Independence | Passed |
| Referent-recurrence check | Caught and corrected twice pre-review (Claude self-audit); one borderline case (naming) explicitly checked and cleared |
| Social-script recurrence check | Passed post-correction — single farewell only, single naming instance only |
| Dialogue-over-label review | Applied — 9 of 16 Tiles are spoken dialogue; Getting the Cut is object-label-heavy by design, consistent with Coffee Shop's validated Customize Moment precedent |
| Distinct-evidence check (DP-002) | **Failed on first pass** (near-duplicate farewell pair) — corrected on founder review |
| Mexican Spanish naturalness / register consistency | **Failed on first pass** (tú/usted inconsistency) — corrected on founder review |
| A1–A2 suitability | Passed |
| Bilingual-gloss specificity | Passed |
| Visual-density / mobile readability | Not yet formally checked against Responsive Tile Typography (Restaurant-only implementation as of this revision) |
| Second independent review | Yes — Jamie |

### E. Playtesting Evidence

**Full session record in the Agrupa Playtest Log ("Hair Salon (Entry 003)" section) — this is a status summary only.**

First session: John. Clean successful completion, one incorrect submission self-corrected via One Away feedback, no frustration. Notably reviewed solved groups after flipping and read the full Reflection screen before exiting ("Okay, good. Yep, I got it."). — positive signal for Reflection's intended closure function. No ambiguity or UI issues surfaced. One tester to date — additional sessions still needed before Approved status.

### F. Revision History
| Change | Reason | Evidence | Board Version |
|---|---|---|---|
| Generic "have a seat" removed pre-review | Referent recurrence risk (Checking In / Getting the Cut) | Claude self-audit | Draft → Draft |
| Hair-color reference removed pre-review | Content-type blur with Getting the Cut | Claude self-audit | Draft → Draft |
| "ya casi" → "¿A nombre de quién?" | More diagnostic; English gloss no longer adds unstated information | Jamie founder review | Draft → v1 |
| "el tráfico de hoy" → "mucho tráfico hoy" | Naturalness — reads as conversational fragment | Jamie founder review | Draft → v1 |
| "¿Y tu familia?" → "¿Y la familia?" | Register consistency (avoids unmotivated tú/usted shift) | Jamie founder review | Draft → v1 |
| "nos vemos pronto" removed → "¿Le gustó?" | Near-duplicate farewell (DP-002 violation) | Jamie founder review | Draft → v1 |
| Reflection copy approved: "Le dije 'un poco más corto' y salí con una nueva personalidad." ✂️ | See Agrupa Copy Library for retired-candidate reasoning and the new Character-Fit Tie-Breaking Rule this decision established | Jamie/Solara approval | v1 (unchanged Tile content) |
| Unsolved Tile typography: 15px/13.5px/12px → 13px/12px/11px (matches Restaurant baseline) | Real-device iPhone testing showed original sizing felt visually heavy, crowded longer clues | Solara, real-device testing | Build-only, no content change |
| Paw placement: centered under "Sofía," smaller, lighter, contained inside Reflection card | Real-device implementation refinement | Solara, real-device testing | **Confirmed compliant, this revision — README Section 4A's governing rule updated to reflect this as the approved treatment; earlier blanket prohibition superseded** |
| Share title corrected: "Agrupa — Hair Salon" → "Agrupa" | Original title revealed the World in text-message link previews, violating the World-secrecy principle (README Section 2) | Solara, real-device testing | Build-only, no content change |

### G. Eligibility and Future Use
- Eligible for daily release: Pending successful playtest and Approved status (build now complete)
- Eligible for beta/test deployment: **Yes** — built, real-device tested, corrected, ready for another tester round
- Recent-access feature: Not planned for MVP — decided against
- Eligible for future paid archive: Pending Approved status
- Eligible for curated pack: Not yet evaluated
- Classroom suitability: Not yet evaluated
- Open issues: none — both previously flagged items (paw placement compliance, build-authorization record) resolved this revision

---

## Entry 004 — Farmers Market (Approved for Playtest)

### A. Identification
- **Puzzle ID:** 004-farmers-market
- **World:** Farmers Market
- **Board version:** 1
- **Current status:** **Approved.** Jamie's explicit founder decision, this revision: skips the normal Testing-before-Approved gate. Reasoning stated by Jamie: core game mechanics are already validated (Restaurant, Hair Salon); this round's purpose is testing authoring-process consistency, not mechanics again. **Not built by Solara — content-approval only, no playtest evidence exists for this specific board.** This is a recorded exception to the standard lifecycle rule, not a claim that Testing happened.
- **Date created:** Developed in parallel with Entry 005, as a deliberate test of methodology generalization (Jamie's Phase 2 request)
- **Current build:** None yet

### B. Current Board

**Browsing the Stalls**
| Tile (ES) | Gloss (EN) |
|---|---|
| qué frescas | how fresh |
| mira esto | look at this |
| huele bien | it smells good |
| de temporada | in season |

**Sampling**
| Tile (ES) | Gloss (EN) |
|---|---|
| pruébalo | try it |
| está dulce | it's sweet |
| un pedacito | a little piece |
| ¿qué tal está? | how is it? |

**Choosing and Buying**
| Tile (ES) | Gloss (EN) |
|---|---|
| ¿cuánto cuesta? | how much is it? |
| un kilo | a kilo |
| efectivo | cash |
| ¿tienes cambio? | do you have change? |

**Carrying It All Home**
| Tile (ES) | Gloss (EN) |
|---|---|
| pesa mucho | it's heavy |
| las manos llenas | hands full |
| al carro | to the car |
| qué buena compra | what a good haul |

**Register:** tú (casual/informal) throughout, deliberate choice for a casual market interaction — distinct from Entry 005's formal register, part of the deliberate structural contrast between the two parallel entries.

### C. Authoring Provenance

**Provenance summary:** Claude — first-draft author, self-audit, naturalness self-check pass. Solara — independent fresh-read naturalness review, no changes requested.

- **World Naturalness Test:** Passed easily.
- **Moments deliberately non-sequential** — a genuine structural contrast with Coffee Shop/Restaurant/Hair Salon's fixed-sequence counter-service structure. Browsing, Sampling, Buying, and Carrying Home don't have one fixed real-world order.
- **Self-audit (Claude) caught and corrected before first review:**
  - "una libra" → "un kilo" — pounds are not the Mexican Spanish default.
  - "¿tiene cambio?" → "¿tienes cambio?" — was accidentally usted, breaking the board's consistent tú register.
- **"al carro" vs. "al coche":** flagged as a genuine regional judgment call, not an error. Jamie's decision: keep "al carro" as-is.
- **Independent review (Solara):** fresh read, explicitly treated as if seeing the board for the first time. Pass on both overall World coherence and every individual Moment. Specifically praised "un pedacito" for giving Sampling its own distinct flavor without overlapping Browsing. No changes requested to any Tile.
- **English gloss review (Solara, separate pass, this revision):** all sixteen glosses reviewed as learner-facing interpretive aids, not dictionary translations — standard applied: immediate recognition, natural everyday English, matching the Spanish's feeling, avoiding over-translation. **Fully approved, zero changes requested.** Specifically praised "hands full" (not "my hands are full") for preserving the remembered-flash quality, and "what a good haul" for "qué buena compra" as a localization stronger than a literal translation ("what a good purchase") — capturing the actual feeling of leaving a market with good finds.

### D. Review Checklist
| Check | Result |
|---|---|
| World Naturalness Test | Passed |
| Parallel Specificity | Passed |
| Moment Independence | Passed |
| Referent-recurrence check | Passed |
| Social-script recurrence check | Passed |
| Dialogue-over-label review | Applied throughout |
| Mexican Spanish naturalness / register consistency | Passed — self-audit caught one register slip, corrected; independent review confirmed clean |
| Distinct-evidence check (DP-002) | Passed |
| A1–A2 suitability | Passed |
| Bilingual-gloss specificity | **Passed — independently reviewed by Solara (this revision), zero changes requested** |
| Visual-density / mobile readability | Not yet checked against Responsive Tile Typography baseline (Section 5) |
| Second independent review | Yes — Solara (both Spanish naturalness and English glosses, separate passes) |

### E. Playtesting Evidence

None yet. Fully approved for playtest — cleared to build. See Agrupa Playtest Log once sessions exist.

### F. Revision History
| Change | Reason | Evidence | Board Version |
|---|---|---|---|
| "una libra" → "un kilo" | Naturalness — Mexican Spanish default | Claude self-audit | Draft → Draft |
| "¿tiene cambio?" → "¿tienes cambio?" | Register consistency (tú throughout) | Claude self-audit | Draft → Draft |
| Independent review, no changes | Naturalness confirmed | Solara | Draft → v1 (Approved for playtest) |
| English gloss independent review, no changes | Learner-facing gloss standard confirmed | Solara | v1 → **Fully approved, cleared to build** |

**Reflection — gap identified and closed, this revision.** No Reflection note existed for this entry despite the locked README Section 4A rule (every puzzle ends with a Sofía note, no exceptions). Root cause and fix: see README Section 5, Structural Completeness Check expansion.
> "Compré para un ejército. Otra vez." 🥬
> — Sofía
**Status: Retired, this revision.** Jamie's assessment: does not consistently capture Sofía's actual voice — a character-fit gap, not a technical error. Claude authored this without access to the full character constitution Solara is developing; awaiting Solara-authored replacement once that reference exists. See correspondence with Solara for full context.

### G. Eligibility and Future Use
- Eligible for daily release: **Approved by founder exception — no playtest evidence exists for this board.** Should be revisited if/when real-player evidence becomes available.
- Eligible for beta/test deployment: Content fully cleared, but **not currently being built by Solara** — this round of work is authoring-process focused, not implementation focused (see Entries 006/007)
- Recent-access feature: Not planned for MVP — decided against
- Eligible for future paid archive: Approved status reached (via founder exception, not standard lifecycle)
- Eligible for curated pack: Not yet evaluated
- Classroom suitability: Not yet evaluated
- Open issues: **Reflection note retired — did not capture Sofía's voice, awaiting Solara-authored replacement (see Section F).** No other content issues. **Status note:** Approved via explicit founder exception to the standard Testing-before-Approved gate — flagged for accuracy, not treated as equivalent to playtest-validated Approved status.

---

## Entry 005 — Doctor's Office (Approved for Playtest, One Founder Decision Pending)

### A. Identification
- **Puzzle ID:** 005-doctors-office
- **World:** Doctor's Office (routine checkup, kept deliberately general per Jamie's instruction)
- **Board version:** 1
- **Current status:** **Approved.** Jamie's explicit founder decision, this revision: skips the normal Testing-before-Approved gate, same reasoning as Entry 004 (mechanics already validated; this round tests authoring consistency, not mechanics). Spanish content, la receta decision, and English glosses all resolved, including one gloss revision: "súbase aquí" → "hop up here." **Not built by Solara — content-approval only, no playtest evidence exists for this specific board.**
- **Date created:** Developed in parallel with Entry 004
- **Current build:** None yet

### B. Current Board

**Checking In**
| Tile (ES) | Gloss (EN) |
|---|---|
| ¿ya se registró? | have you checked in? |
| su seguro, por favor | your insurance, please |
| su identificación | your ID |
| llene esto | fill this out |

**The Waiting Room**
| Tile (ES) | Gloss (EN) |
|---|---|
| cuánto falta | how much longer |
| las revistas viejas | the old magazines |
| por fin | finally |
| el silencio | the silence |

**The Exam**
| Tile (ES) | Gloss (EN) |
|---|---|
| respire hondo | breathe deeply |
| el estetoscopio | the stethoscope |
| súbase aquí | hop up here |
| todo se ve bien | everything looks good |

**Checking Out**
| Tile (ES) | Gloss (EN) |
|---|---|
| su próxima cita | your next appointment |
| la receta | the prescription |
| hasta luego | see you later |
| el estacionamiento | the parking lot |

**Register:** usted (formal) throughout — deliberate, and a genuine contrast with Entry 004's tú register. Medical settings default to formal address in Mexican Spanish regardless of familiarity.

### C. Authoring Provenance

**Provenance summary:** Claude — first-draft author, self-audit, naturalness self-check pass. Solara — independent fresh-read naturalness review; explicitly deferred the la receta content question to Jamie as product policy, not naturalness.

- **World Naturalness Test:** Passed easily.
- **Content-safety scoping, per Jamie's explicit instruction:** kept deliberately general — routine-visit mechanics only, nothing about symptoms, diagnosis, or illness.
- **Self-audit (Claude) caught and corrected before first review:** an original "tome asiento" (have a seat) at Checking In risked the exact same referent-recurrence trap as Hair Salon's original draft, since sitting is also the entire content of the next Moment (Waiting Room). Removed, replaced with "su identificación."
- **La receta — resolved, this revision.** Claude raised it as a content-safety judgment call requiring Jamie's sign-off. Solara's independent review recommended keeping it, with reasoning: linguistically, "la receta" is one of the most common, ordinary end-of-visit Tiles in everyday Mexican Spanish — not inherently medication-heavy in feel, and arguably more representative than an alternative like "las vitaminas" (optional, not universal to every visit). **Jamie's decision: keep "la receta" as-is.** Board fully locked, no further content review needed on this item.
- **Independent review (Solara):** fresh read, pass on overall World coherence and every Moment. Specifically praised The Exam as the strongest Moment on the board, and the Waiting Room for capturing a *feeling* (boredom, anticipation) rather than relying purely on objects.
- **English gloss review (Solara, separate pass, this revision):** same learner-facing standard applied as Entry 004. Fifteen of sixteen glosses approved without change, including two specifically praised localizations: "¿ya se registró?" → "have you checked in?" (closer to the actual American-medical-office social script than the literal "have you registered?"), and "cuánto falta" → "how much longer" (stronger learner gloss than a literal "how much is left?"). **One revision:** "súbase aquí" originally glossed "get up here," which read slightly odd in English; changed to **"hop up here"** — better captures the medical-assistant social script than the literal instruction. Board fully approved following this single change.

### D. Review Checklist
| Check | Result |
|---|---|
| World Naturalness Test | Passed |
| Parallel Specificity | Passed |
| Moment Independence | Passed |
| Referent-recurrence check | Caught and corrected pre-review (Claude self-audit — "have a seat" trap) |
| Social-script recurrence check | Passed |
| Dialogue-over-label review | Applied throughout |
| Mexican Spanish naturalness / register consistency | Passed — usted maintained throughout, confirmed by independent review |
| Distinct-evidence check (DP-002) | Passed |
| A1–A2 suitability | Passed |
| Content safety (health-adjacent World) | **Passed.** La receta resolved — Jamie's decision, kept as-is. |
| Bilingual-gloss specificity | **Passed — independently reviewed by Solara (this revision); one revision applied ("súbase aquí" → "hop up here")** |
| Visual-density / mobile readability | Not yet checked against Responsive Tile Typography baseline (Section 5) |
| Second independent review | Yes — Solara (both Spanish naturalness and English glosses, separate passes) |

### E. Playtesting Evidence

None yet. Board fully approved and locked — cleared to build.

### F. Revision History
| Change | Reason | Evidence | Board Version |
|---|---|---|---|
| "tome asiento" removed → "su identificación" | Referent-recurrence risk (Checking In / Waiting Room) | Claude self-audit | Draft → Draft |
| Independent review, no Tile changes; la receta flagged for Jamie | Naturalness confirmed; content-policy question distinguished from naturalness | Solara | Draft → v1, pending final lock |
| La receta decision: keep as-is | Founder product-policy decision | Jamie | v1 → Fully locked (Spanish content) |
| "súbase aquí" gloss: "get up here" → "hop up here" | English gloss review — localization improvement, medical-assistant register | Solara | **Fully approved, cleared to build** |

**Reflection — gap identified and closed, this revision.** No Reflection note existed for this entry despite the locked README Section 4A rule. See README Section 5, Structural Completeness Check expansion.
> "Leí una revista de 2019. Me enteré de todo." 🗓️
> — Sofía
**Status: Retired, this revision.** Jamie's assessment: does not consistently capture Sofía's actual voice — a character-fit gap, not a technical error. Awaiting Solara-authored replacement. See correspondence with Solara for full context.

### G. Eligibility and Future Use
- Eligible for daily release: **Approved by founder exception — no playtest evidence exists for this board.** Should be revisited if/when real-player evidence becomes available.
- Eligible for beta/test deployment: Content fully cleared, but **not currently being built by Solara** — this round of work is authoring-process focused, not implementation focused (see Entries 006/007)
- Recent-access feature: Not planned for MVP — decided against
- Eligible for future paid archive: Approved status reached (via founder exception, not standard lifecycle)
- Eligible for curated pack: Not yet evaluated
- Classroom suitability: Not yet evaluated — content-safety review specifically relevant here given the health-adjacent World; worth flagging for extra scrutiny before any classroom use is considered
- Open issues: **Reflection note retired — did not capture Sofía's voice, awaiting Solara-authored replacement (see Section F).** No other content issues.

---

## Entry 006 — Laundromat (Approved)

### A. Identification
- **Puzzle ID:** 006-laundromat
- **World:** Laundromat
- **Board version:** 1 (post-correction)
- **Current status:** **Approved.** Full independent review complete (Solara) — Spanish and English glosses both confirmed. Not yet built.
- **Date created:** Developed in parallel with Entry 007, deliberately chosen for structural contrast against all five prior puzzles (solitary, task-based, minimal dialogue — none of the prior five lack a service-worker interaction)
- **Current build:** None yet

### B. Current Board

**Sorting and Starting:** separa los colores (separate the colors) · el detergente (the detergent) · ¿tienes monedas? (do you have coins?) · la máquina 6 (machine 6)

**Waiting:** el zumbido (the humming sound) · una revista vieja (an old magazine) · ya casi (almost done) · mira el reloj (watch the clock)

**Folding:** todavía calientita (still warm) · doblar bien (fold it neatly) · una media perdida (a missing sock) · apilar las toallas (stack the towels)

**Heading Out:** la canasta llena (the full basket) · huele a limpio (it smells clean) · hasta la próxima (until next time) · no olvides nada (don't forget anything)

### C. Authoring Provenance

**Provenance summary:** Claude — first-draft author, self-audit, English Gloss Self-Check. **Incident: initial draft was presented to Jamie with Folding and Heading Out missing Tiles (2/4 and 3/4 respectively) — caught by Jamie, not self-detected. Corrected and re-verified; see README Section 5, Structural Completeness Check, added directly because of this incident.** Solara — full independent review, Spanish and English both, no changes requested.

- **World Naturalness Test:** Passed.
- **Self-audit:** "ya casi" checked specifically against the Hair Salon precedent (where a similar phrase caused a referent-recurrence problem) — confirmed safe here, since Laundromat has no competing check-in Moment for it to bleed into.
- **English Gloss Self-Check catch:** "doblar bien" first-pass gloss was "fold well" — grammatically correct but stiff; revised to "fold it neatly."
- **Independent review (Solara):** approved without changes, both languages.

### D. Review Checklist
| Check | Result |
|---|---|
| World Naturalness Test | Passed |
| Parallel Specificity | Passed |
| Moment Independence | Passed |
| Referent-recurrence check | Passed |
| Social-script recurrence check | Passed |
| Dialogue-over-label review | Applied where natural; some object-label content by design (Sorting, Folding) |
| Mexican Spanish naturalness / register consistency | Passed — confirmed by independent review |
| Distinct-evidence check (DP-002) | Passed |
| A1–A2 suitability | Passed |
| Bilingual-gloss specificity | Passed — independently reviewed |
| **Structural Completeness Check** | **Failed on first draft (Folding, Heading Out incomplete) — caught by Jamie, corrected, re-verified at exactly 16/4-per-Moment** |
| Visual-density / mobile readability | Not yet checked against Responsive Tile Typography baseline (Section 5) |
| Second independent review | Yes — Solara |

### E. Playtesting Evidence

None yet. Not built.

### F. Revision History
| Change | Reason | Evidence | Board Version |
|---|---|---|---|
| Folding and Heading Out completed to 4 Tiles each | Structural completeness failure on first draft | Jamie caught the gap | Draft (incomplete) → Draft (complete) |
| "doblar bien" gloss: "fold well" → "fold it neatly" | English Gloss Self-Check | Claude self-check | Draft → v1 |
| Independent review, no changes | Naturalness confirmed, both languages | Solara | v1 → **Approved** |

**Reflection — gap identified and closed, this revision.** No Reflection note existed for this entry despite the locked README Section 4A rule. See README Section 5, Structural Completeness Check expansion.
> "Encontré un calcetín de hace tres lavadas. Investigación en curso." 🧦
> — Sofía
**Status: Retired, this revision.** Jamie's assessment: does not consistently capture Sofía's actual voice — a character-fit gap, not a technical error. Awaiting Solara-authored replacement. See correspondence with Solara for full context.

### G. Eligibility and Future Use
- Eligible for daily release: Pending build and playtest
- Eligible for beta/test deployment: Content fully cleared, pending build
- Recent-access feature: Not planned for MVP — decided against
- Eligible for future paid archive: Approved status reached
- Eligible for curated pack: Not yet evaluated
- Classroom suitability: Not yet evaluated
- Open issues: **Reflection note retired — did not capture Sofía's voice, awaiting Solara-authored replacement (see Section F).** No other content issues.

---

## Entry 007 — Birthday Party (Approved)

### A. Identification
- **Puzzle ID:** 007-birthday-party
- **World:** Birthday Party (at home)
- **Board version:** 1 (post-correction)
- **Current status:** **Approved.** Full independent review complete (Solara) — Spanish and English glosses both confirmed. Not yet built.
- **Date created:** Developed in parallel with Entry 006, deliberately chosen for structural contrast (no service-worker role at all — purely social/family Moments, unlike all six prior puzzles)
- **Current build:** None yet

### B. Current Board

**Setting Up:** ¿dónde pongo esto? (where do I put this?) · los globos (the balloons) · ¿necesitas ayuda? (need help?) · casi es hora (it's almost time)

**The Cake:** apaga las velitas (blow out the candles) · pide un deseo (make a wish) · huele a chocolate (it smells like chocolate) · ¡feliz cumpleaños! (happy birthday!)

**Opening Presents:** ¿puedo abrirlo? (can I open it?) · ¡me encanta! (I love it!) · no debiste (you shouldn't have) · ¿de quién es este? (whose is this?)

**Saying Goodbye:** gracias por venir (thanks for coming) · maneja con cuidado (drive safely) · nos vemos pronto (see you soon) · qué bonita fiesta (what a lovely party)

### C. Authoring Provenance

**Provenance summary:** Claude — first-draft author, self-audit, English Gloss Self-Check. **Incident: initial draft was presented to Jamie with The Cake missing a Tile (3/4) — caught by Jamie, not self-detected.** Corrected and re-verified. Solara — full independent review, Spanish and English both.

- **World Naturalness Test:** Passed.
- **Self-audit catch, referent-recurrence:** "gracias por venir" was almost duplicated as a generic greeting at Setting Up — same social-script trap as Coffee Shop's original naming/gratitude problem. Removed from Setting Up; gratitude now appears exactly once, at Saying Goodbye.
- **Self-audit catch, grammar:** "las globos" corrected to "los globos" (globo is masculine).
- **English Gloss Self-Check catch:** "no debiste" first-pass gloss was "you didn't have to" — accurate but flat; revised to "you shouldn't have," the actual idiomatic phrase for this social moment.
- **Independent review (Solara) — one gloss discussion, resolved:** Solara initially suggested "Need help?" → "Do you need help?" for closer grammatical fidelity to "¿Necesitas ayuda?" On reflection, reversed this recommendation and kept the original "Need help?" **New working principle established from this discussion (see README Section 5):** Agrupa's English glosses are recognition cues, not textbook translations — a shorter, natural fragment that evokes the same moment as the Spanish is generally preferable to a grammatically fuller sentence. Consistent with other approved glosses ("Hands full," "Cash," "Finally," "What a good haul"). **Explicitly a working pattern to watch, not promoted to canon.**

### D. Review Checklist
| Check | Result |
|---|---|
| World Naturalness Test | Passed |
| Parallel Specificity | Passed |
| Moment Independence | Passed |
| Referent-recurrence check | Caught and corrected pre-review (Claude self-audit — gratitude duplication) |
| Social-script recurrence check | Passed post-correction |
| Dialogue-over-label review | Applied throughout |
| Mexican Spanish naturalness / register consistency | Passed — one grammar correction (los globos), confirmed clean by independent review |
| Distinct-evidence check (DP-002) | Passed |
| A1–A2 suitability | Passed |
| Bilingual-gloss specificity | Passed — independently reviewed; one gloss discussion resolved in favor of original ("Need help?") |
| **Structural Completeness Check** | **Failed on first draft (The Cake incomplete) — caught by Jamie, corrected, re-verified at exactly 16/4-per-Moment** |
| Visual-density / mobile readability | Not yet checked against Responsive Tile Typography baseline (Section 5) |
| Second independent review | Yes — Solara |

### E. Playtesting Evidence

None yet. Not built.

### F. Revision History
| Change | Reason | Evidence | Board Version |
|---|---|---|---|
| The Cake completed to 4 Tiles | Structural completeness failure on first draft | Jamie caught the gap | Draft (incomplete) → Draft (complete) |
| "gracias por venir" removed from Setting Up | Referent-recurrence — social-script duplication risk | Claude self-audit | Draft → Draft |
| "las globos" → "los globos" | Grammar correction (gender agreement) | Claude self-audit | Draft → Draft |
| "no debiste" gloss: "you didn't have to" → "you shouldn't have" | English Gloss Self-Check — idiomatic accuracy | Claude self-check | Draft → v1 |
| "Need help?" retained (not changed to "Do you need help?") | Recognition-over-completeness principle established | Solara, reversing her own initial suggestion | v1 → **Approved** |

**Reflection — gap identified and closed, this revision.** No Reflection note existed for this entry despite the locked README Section 4A rule. See README Section 5, Structural Completeness Check expansion.
> "Pedí un deseo. No se los voy a decir." 🎂
> — Sofía
**Status: Retired, this revision.** Jamie's assessment: does not consistently capture Sofía's actual voice — a character-fit gap, not a technical error. Awaiting Solara-authored replacement. See correspondence with Solara for full context.

### G. Eligibility and Future Use
- Eligible for daily release: Pending build and playtest
- Eligible for beta/test deployment: Content fully cleared, pending build
- Recent-access feature: Not planned for MVP — decided against
- Eligible for future paid archive: Approved status reached
- Eligible for curated pack: Not yet evaluated
- Classroom suitability: Not yet evaluated
- Open issues: **Reflection note retired — did not capture Sofía's voice, awaiting Solara-authored replacement (see Section F).** No other content issues.

---

## Entry 008 onward

Not yet started. World not yet selected. Per process, future entries should be opened at Draft status from the beginning of their authoring session, not added retroactively after completion, so the full provenance chain is preserved without reconstruction.
