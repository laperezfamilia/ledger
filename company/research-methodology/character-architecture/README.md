---
status: working
owner: jamie
last_reviewed: 2026-08-01
depends_on:
supersedes:
related: ../README.md, ../../../casa-perez/characters/character-voice-methodology.md, ../../../casa-perez/research/family-architecture-integrity-dignity.md
---

**Part of the company-wide research map:** see `../README.md` — this is Research Program 1 of that index.

# Character Architecture Research Program

**To:** Claude Code
**From:** Jamie & Solara
**Re:** Discovery infrastructure only — not a methodology write-up, not canon.

This research investigates whether psychologically generative fictional characters can be developed through a repeatable discovery process rather than traditional top-down character design.

## Current status

- exploratory
- research only
- no validated methodology
- evidence collection in progress

Avoid language implying we have already established a discipline anywhere in this program.

## Current Research Position

Our current hypothesis is **not**: *"We have invented a new discipline."*

Our current hypothesis is: *"We may be discovering the foundations of a repeatable discipline of Character Architecture."*

Those are intentionally different statements. This program exists to preserve that distinction — optimized for preserving observations, experiments, evidence, uncertainty, and future replication, not for producing conclusions.

## Proposed Working Thesis (2026-08-01)

**Status: Working Thesis — a research direction to test, refine, challenge, or disprove, not a validated conclusion. Not established methodology, governance, or canon.**

> Character Architecture is the discipline of discovering and preserving human identity with enough fidelity that an AI can participate in long-term relationships while remaining recognizably faithful to the identity it embodies.

**Context:** emerged from the Discovery/Preservation working observation (`./research-log.md`, 2026-08-01) — Discovery ("how do we recognize a person?") and Preservation ("how do we preserve that discovered person with enough fidelity that future collaborators, implementations, and AI interactions continue to recognize the same identity over time?"). The four-part documentation convention above is understood as one practical answer to the Preservation half.

**Why this matters:** the objective is not merely AI characters that remain "in character." The aspiration is identity preserved with enough fidelity that people experience continuity over time and naturally feel *"that still feels like Sofía."* This shifts the emphasis from consistency of output to faithfulness of identity.

**Test case:** Experiment 2 (Beto) is the first substantial test of whether this thesis holds beyond Sofía. Future experiments should actively attempt to strengthen, refine, challenge, or disprove it — not simply confirm it. See `./open-questions.md`.

*(`ledger` note: this thesis's "AI participating in long-term relationships" framing overlaps with `../README.md`'s Research Program 3 — Relational Design ("How do we design AI relationships that strengthen people's relationships with themselves and with other people?"). Noted as a cross-program connection worth watching, not merged — Program 1 is about identity fidelity specifically; Program 3 is broader.)*

## Structure

```
character-architecture/
  README.md              ← this file
  research-log.md         ← chronological journal of discoveries, as observations, not doctrine
  evidence-index.md        ← per-discovery: observation, supporting evidence, counter-evidence, confidence, replication requirements
  open-questions.md         ← unresolved research questions, treated as assets, not gaps
  experiments/
    sofia.md                 ← Experiment 1: Sofía Pérez
    (beto.md, when Beto's independent discovery process begins — Experiment 2)
```

## Documentation Convention (Founder Decision — revised 2026-08-01)

**Revision note:** this convention was first approved earlier the same day as a three-part format (Principle / Canonical Example(s) / Interpretation). Founder discussion refined it further, same day, into the four-part format below — recorded here as the current version, with the prior version's reasoning preserved in the "Why this is the standard" section, since the refinement built on it rather than replacing it.

**Working standard for future Character Architecture architectural handoffs.** Every significant architectural principle recorded in this program should have four parts:

1. **Principle** — the architectural conclusion.
2. **Foundational Scene** — the specific scene that caused the principle to be recognized in the first place. This is the primary evidence that changed understanding of the character, not merely a supporting illustration.
3. **Supporting Scene(s)** — additional scenes that consistently reinforce the principle. These strengthen calibration without introducing new conclusions.
4. **Interpretation** — a disciplined explanation of why the evidence supports the principle and how it should guide future implementation. **Interpretation explains the evidence — it must never introduce new architectural claims.** This preserves "resist premature synthesis" (below) at the sentence level, not just the document level.

All examples stay embedded directly with their principle, never separated into another document — a principle read without its anchor drifts back into being just an adjective.

**Evidentiary weight distinction (working methodological refinement, not yet a research conclusion):** not all examples carry equal weight. Distinguish:
- **Foundational Evidence** — the scene that led to the discovery.
- **Supporting Evidence** — scenes that reinforce an already-established discovery.
- **Illustrative Examples** — scenes that fit the principle but did not materially contribute to discovering it.

Character Architecture documents should primarily preserve Foundational and Supporting Evidence. Illustrative examples may remain available for future writing but should not be confused with the evidence that actually established the principle.

**Relationship to the Discovery/Preservation working observation:** per `./research-log.md`'s 2026-08-01 entry, Character Architecture may consist of two distinct disciplines — Discovery ("how do we recognize a person?") and Preservation ("how do we preserve a discovered person with enough fidelity that future collaborators recognize them years later?"). This documentation convention is understood as a possible answer to the *Preservation* question specifically, not to Discovery. That framing is itself a working observation, not validated methodology — noted here only as a cross-reference, not as a reason to change this convention further.

**Why this is the standard, not just a preference:** this same underlying instinct — concrete example over abstract description — had already emerged independently in three places before being named as a convention: this program's own "behaviors reveal character more reliably than adjectives" (`./research-log.md`), Agrupa's Dialogue Approval Rule ("any proposed line must be presented as an actual quotation... not approved as an abstract description of intended effect" — `casa-perez/projects/agrupa/copy-library.md`), and the discovery that architectural principles become significantly more durable when anchored to lived scenes (Sofía synthesis, `./experiments/sofia-2026-08-01-architectural-synthesis.md`). Those three independent emergences are **not** being elevated into methodology yet — but they were strong enough evidence to justify changing the documentation convention itself.

**A principle worth the anchor, as illustration of why this matters:** "Sofía is emotionally warm and socially confident" will drift over time — different writers imagine those adjectives differently. Anchored to a Foundational Scene ("Wait… you were saying?"), it becomes stable, because future writing can be calibrated by resemblance rather than personal interpretation.

**Character voice is calibrated by resemblance, not pass/fail.** A canonical example functions as a reference anchor to compare new writing against ("does this feel closer to the example, or does it drift?"), not a test with a binary pass/fail outcome the way `casa-perez/projects/agrupa/design-principles-v0.1.md`'s Operational Tests work for puzzle design. Same three-part shape (Principle → Rationale/Interpretation → Test/Example), adapted correctly for character work.

## Guiding Research Principles

Same evidence standards as the broader collaboration (see `../../governance/operating-model.md` Shared Principles):

- Recover before recreate.
- Preserve uncertainty honestly.
- Record observations before interpretations.
- Separate evidence from hypotheses.
- Separate hypotheses from founder decisions.
- Replicate before promoting.
- Resist premature synthesis.
- Preserve provenance.

## Validation

Additional experiments should eventually include characters outside Casa Pérez, to determine whether discoveries generalize or are family-specific. The next major validation point is **Beto's independent discovery process** — if patterns already observed in Sofía's discovery (see `casa-perez/research/family-architecture-integrity-dignity.md`) emerge naturally there, without steering, that strengthens confidence the pattern is real rather than inferred from a single character.

## Long-Term Vision (Explicitly Aspirational)

If the research continues to hold through replication, it may eventually support products such as software, books, workbooks, educational material, AI-assisted discovery tools, courses, creator tools, or writer's-room tools.

**These are possible future applications only. They should not influence the research itself.** The evidence should determine what ultimately becomes teachable.

## A Guiding Research Hypothesis

> We are not trying to teach people how to invent characters. We are trying to discover whether people can learn to discover them.

If future evidence supports that statement, wonderful. If it does not, we should be equally willing to revise or abandon it.

The objective is simple: build the best research record possible and let the evidence lead wherever it leads.
