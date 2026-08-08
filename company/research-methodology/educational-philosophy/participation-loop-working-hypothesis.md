---
status: working
owner: jamie
last_reviewed: 2026-08-05
depends_on:
supersedes:
related: ./educational-brief-v1.0-recovered.md, ./conversational-immersion-observation-2026-08-02.md, ../design-research/recognition-vs-evaluation.md, ../design-research/README.md, ../character-architecture/experiments/sofia-teaching-philosophy.md, ../README.md
---

# The Participation Loop — Working Hypothesis (Discovery Only)

**Status: Discovery / working hypothesis. Not canon. Not an implementation directive.** Preserved now, deliberately, ahead of deeper research — Jamie & Solara judged the pattern important enough to record before it gets lost, not because it's settled.

## The core hypothesis

> Language becomes usable through participation, not merely acquisition. Casa Pérez creates a place where learners can participate before they feel ready.

**The working loop:**

> Belonging → Courage → Participation → Evidence → Witness/Recognition → Confidence/Identity → More Participation

More humanly: *Know → Dare → Participate → Be witnessed → Participate again → Become.*

**The formulation Jamie & Solara most want preserved:**

> Stop making speaking the graduation ceremony. Make speaking where learning happens.

**Explicit scope note, preserved as stated:** this doesn't devalue vocabulary, grammar, comprehension, curriculum, explicit teaching, or structured practice. The narrower question: *what prevents acquired language knowledge from becoming usable participation, and can belonging, low-stakes relational interaction, courage, and specific recognition help learners cross that gap?*

## Why this emerged

Converging from several directions independently: learners reporting years or decades of study while still feeling unable to speak; the language communities Jamie has studied being praised specifically for members who actually speak, fear mistakes less, interact with similar-level peers, discuss ordinary life, and participate in supportive community; and the observation that Casa Pérez's own product design already produces this without anyone intending a "practice session" — a learner participates because Beto said something funny or Rosa asked a question, not because they decided to practice Spanish.

**Natural scaling, as described:** 😂 → jajaja → sí → sí, yo también → short phrase → complete response → story → initiating a conversation.

## Where this already intersects existing work

Not a new idea arriving in isolation — it's a mechanism-level connector between several things already established separately:

- **`../design-research/recognition-vs-evaluation.md`** ("the purpose of data is not judgment, the purpose of data is witness") explained *why* witnessing matters. This hypothesis adds *what* should be witnessed specifically (a shift in participation, not general performance) and *why* witnessing that particular thing has causal power — it converts evidence into identity, not just morale.
- **`./educational-brief-v1.0-recovered.md` §1**'s Working Thesis ("the channel should help learners participate more comfortably in ordinary life through Spanish") — this hypothesis is a mechanism-level elaboration of that exact thesis, not a competing one.
- **`./conversational-immersion-observation-2026-08-02.md`** — read retrospectively, that observation (Jamie speaking Spanish unprompted mid-conversation) is arguably a lived instance of this loop already firing: belonging present, courage exercised without anyone requesting it, participation occurring inside a real relationship.
- **`../character-architecture/experiments/sofia-teaching-philosophy.md`** — "mistakes are evidence learning is already happening," "she listens before she corrects" — already describes a character oriented around exactly this loop, without it having been named as a loop.
- **The engagement-ethics work in `../design-research/`** (payoff matches pull, the transparency test, real-world-participation as the third test) — directly relevant to keeping participation-opportunity design honest; see the opportunities-vs-measurement distinction below.

**Is this a renaming of something already established, or genuinely new?** Judged as genuinely new, but not independent: it fills in mechanism-level detail that the existing "Mechanism" layer (a psychologically safe-to-speak environment built through consistent relationships) left abstract. Confidence Transfer names the *outcome*; the Participation Loop proposes the *engine* that produces it. Worth watching whether this becomes a sixth name for the same underlying cluster (Practice Family, Bridge Not Destination, Safe-to-Speak, Confidence Transfer already exist) or whether it earns its place as the mechanism layer specifically — not resolved here.

## Distinguishing participation opportunities from participation measurement

The real risk this hypothesis creates, named directly rather than left implicit: designing generous **opportunities** for participation is squarely aligned with everything already established. Building **measurement** infrastructure to track participation is where this could quietly become the gamification system Jamie & Solara are explicitly trying to avoid.

**Proposed working discipline:** witnessing should be triggered by what a believable, attentive family member could plausibly notice from memory over time — not by a counter, threshold, or dashboard. The test: *if stating the observed shift accurately would require consulting a log rather than genuine memory, it has crossed into surveillance-flavored territory, regardless of whether the underlying data exists.* Sofía's example works ("hace unas semanas me contestabas casi siempre en inglés") because it's the shape of thing a real person remembers — coarse, episodic, meaningful — not the shape of a metrics export.

A second discipline worth naming: witnessing moments should stay **rare and earned**, not frequent or systematic. The moment witnessing becomes predictable or scheduled, it degrades back into evaluation — the exact thing `recognition-vs-evaluation.md` already exists to prevent.

## Relationship as mechanism, not just environment — pressure-tested

Asked directly whether relationship is part of the educational mechanism itself, not merely the emotional scaffolding around it: the Witness step specifically appears to require it. A generic, warm, memory-less chatbot cannot perform Sofía's example line — there is no "hace unas semanas" without continuity of a specific relationship. If the Participation Loop holds, relationship-with-continuity is mechanically necessary for Witness specifically, not just pleasant scaffolding around acquisition elsewhere in the loop. This is falsifiable: if a generic, non-continuous source of equally warm encouragement produced equally strong identity-shift outcomes, that would argue against relationship being constitutive. Directly connects to, and would be real evidence toward, the still-open Character Architecture question of whether character-specific continuity outperforms generic AI.

## Testable through the product vs. needs outside research first

**Testable directly through the product, once something exists:** whether specific participation-inviting design choices increase attempted Spanish use; whether witnessing moments produce any observable behavior change afterward (via the self-report/real-world-missions infrastructure already planned).

**Needs outside research first, before designing around it:** the deeper claim that similar vocabulary/grammar knowledge can coexist with radically different real-world readiness. This maps onto a well-established distinction in applied linguistics — communicative competence versus linguistic competence (Hymes, contra a narrower Chomskyan competence) — worth a literature check before assuming this is a Casa Pérez discovery rather than a known gap with existing research on what closes it.

## Smallest set of high-value research questions before designing around this heavily

Three, not a long list:

1. **Desk research first, cheap:** what does existing SLA literature already say about the competence–performance gap, and does it already identify what closes it? This should happen before anything else — it may sharpen or partially answer the rest.
2. **The genuinely novel, testable claim:** does Witness specifically add anything causally beyond Participation alone — or would repeated low-stakes participation, without any explicit external witnessing, produce the same identity shift on its own? This is the question most worth product-testing once there's something to test.
3. **Can the human-scale-noticing boundary be operationalized reliably**, or does it require case-by-case judgment that resists systematization? Testable cheaply via early mockups and small user tests, before any real build commitment.

## Open questions (Discovery, not resolved)

- Does Witness add causal power beyond Participation alone, or is repeated low-stakes participation sufficient by itself?
- Is "Participation" a genuinely distinct mechanism-layer concept, or will it fold into the existing Confidence Transfer / Mechanism language once pressure-tested?
- Two learners with similar vocabulary and grammar may have radically different real-world readiness if one has repeatedly participated, misunderstood, repaired, initiated, persisted, and been understood. If true, traditional language measures may capture something different from the capability Casa Pérez actually cares about — not yet tested.
