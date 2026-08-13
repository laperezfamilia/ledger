---
status: working
owner: jamie
last_reviewed: 2026-08-06
depends_on: ./find-the-words-implementation-roadmap.md, ./BYG-GOV-001.md, ./BYG-PRD-001-foundation-v1.17.md, ./BYG-UX-001-foundation-v1.6.md, ./BYG-DEC-001.md
supersedes:
related: ./BYG-DEC-001-foundation-v1.21.md, ./placeholder-library-v0.1.md, ../../characters/character-voice-methodology.md, ../../../company/research-methodology/design-research/emotional-role-architecture.md, ../../../company/research-methodology/design-research/recognition-vs-evaluation.md, ../../../company/research-methodology/character-architecture/experiments/sofia-2026-08-01-architectural-synthesis.md, ../../../STATE.md
---

# Find the Words — Continuity Pivot (Discovery Synthesis)

**To:** future sessions, Jamie, Solara, Claude
**From:** Jamie & Solara, synthesized with Claude
**Session type:** Discovery (per `company/governance/operating-model.md` Phase 1) — explicitly **not** a Founder Decision, governance amendment, PRD change, or implementation handoff. Filed in the same spirit and at the same status as `sofia-2026-08-01-architectural-synthesis.md`: a working record of how the thinking evolved, not a conclusion to build from yet.

**How to read this document:** discoveries and open questions are preserved side by side, deliberately. Per Jamie's explicit instruction, the open questions matter as much as the discoveries — they're recorded here so future sessions understand they were left open on purpose, not forgotten. Nothing below should be treated as decided.

---

## 1. The question that started it

*"Why would someone choose Find the Words instead of simply opening ChatGPT?"* Pursued honestly, this question dissolved the working assumption that Find the Words is a "Ready Pack generator." That framing no longer felt like the right product — not because the Ready Pack is wrong, but because it stopped feeling like the center of gravity.

## 2. The shift: from Ready Pack generator to real-life conversation system

**Working thesis, not yet a Founder Decision:** Find the Words' job is not simply to generate preparation for one conversation. It's to help learners gradually bring more of their real life into another language — by preparing for, having, returning to, and building upon recurring real-world conversations. The product rhythm: **Prepare → Go → Return → Build.**

**This is a third independent convergence on the same shape, not a new idea** — worth being precise about the lineage, since that precision is the actual evidence:
1. The original 2026-08-01 "Retention & Product Evolution Proposal," reframing the product from "Describe → Generate → Leave" to "Prepare → Use → Return → Continue" (`BYG-DEC-001.md` Decision #18, `BYG-PRD-001-amendments.md` §7a).
2. This same working relationship's recovery of that material earlier in this conversation, after Jamie asked for a broad search rather than accepting a fresh redesign.
3. Tonight's independent re-derivation, arrived at without deliberately consulting either of the above.

Three independent arrivals at one shape is real signal. It also means this should build on the already-recovered Context/Preparation data model (soft-match Contexts, the trust rules — "the learner names their life," "recognition must be invited" — `BYG-DEC-001.md` Decision #18) rather than be re-derived a fourth time.

## 3. The emotional center

**Founder framing, preserved as stated.** One sentence changed the conversation. Jamie said:

> *"It has my life in it."*

The excitement wasn't about AI capability. It was about recurring parts of a life accumulating instead of disappearing into old chat threads — Walking Athena, John's Family, Spain Trip, Coffee Shop, Pharmacy, Work. Not exercises being collected. A Spanish version of an actual life, gradually built.

## 4. Differentiation reframed

**Working thesis.** Not "better AI." Not "more personality." The differentiation is continuity and organization around the learner's real, recurring life — something ChatGPT structurally resists optimizing for, not merely hasn't built yet.

> *"The value isn't remembering the learner emotionally. The value is helping them avoid starting over every time. Every real conversation becomes material for the next one."*

**Claude's addition to this reasoning, tagged as such:** the mechanism isn't "ChatGPT doesn't have memory" (a feature gap platforms can close). It's that a general-purpose assistant optimized for breadth would make its product worse for most users by imposing a rigid, domain-specific life-organization model on everyone. Specializing this hard is exactly what a purpose-built product should do and a general one structurally resists. This is offered as a sharper, more durable version of the differentiation argument already present in `BYG-PRD-001-foundation-v1.17.md` §12 — not a contradiction of it.

## 5. Sofía's role, clarified

Sofía became smaller and more important at the same time — a quiet instructional guide whose personality shapes the preparation experience, not the product's attraction or emotional center. The learner isn't "using Sofía." They're preparing for their own life. Candidate idea: an "About Your Guide" page, discoverable rather than front-and-center, for learners who want to meet her once they've already come to appreciate the experience.

**Consistency note, not a new finding:** this converges with an existing Founder Decision recovered earlier this same evening — the 2026-08-01 Sofía architectural synthesis's "Audience Relationship" section, where Jamie decided her audience "is intentionally not Sofía's emotional center... not asked to replace it." Tonight's instinct is independently consistent with standing canon, not new territory.

## 6. Recognition, not evaluation — "My Life in Spanish"

**Working concept, name intentionally not locked** (see §8). Not a dashboard, not XP, not streaks, not gamification — explicitly ruled out. A surface that quietly witnesses accumulated real-life experience rather than measuring performance:

> Walking Athena — 23 conversations over 8 months
> John's Family — 12 conversations
> Spain Trip — Planning

The intended feeling: *"Look how much of your life you're living in Spanish now,"* not *"look how much you've studied."* Explicitly aligned with `recognition-vs-evaluation.md`'s existing thesis — *"the purpose of data is not judgment, the purpose of data is witness."*

## 7. Reframing the loop's second half (Solara)

Claude's working description of this loop — "designing what happens after the app closes" — was pressure-tested and refined. Solara's reframing, preserved as offered, two candidate phrasings not yet chosen between:

> *"We stopped treating preparation as the destination. We started treating it as the beginning of a real-world cycle."*
>
> *"We're designing for the learner's return, not just their departure."*

**Why this isn't just rewording:** the product cannot actually design what happens after it closes — the real conversation is outside its visibility entirely. What it can design is the invitation to hear about it when the learner returns. This sharpens, rather than resolves, the Return-mechanism open question in §9 — the whole loop's later stages depend on a voluntary self-report step with no forcing function yet identified.

## 8. Deliberately undecided

Left open on purpose, so the product philosophy can mature before the architecture locks around it:
- The primary object's name (conversation, thread, chat, context, situation, or something else).
- Exact navigation.
- Implementation.
- Constitutional amendments.
- Data model changes.

## 9. Open questions, preserved alongside the discoveries

Per Jamie's explicit instruction: recorded so future sessions know these were left open intentionally, not forgotten.

- **Cold start.** The differentiator is strongest after months of accumulated history and weakest on day one — exactly when "why not ChatGPT" is being asked loudest. What carries the product before there's anything to witness?
- **The Return mechanism.** No forcing function currently exists, and gamification/streaks/notifications are constitutionally off the table (`BYG-GOV-001` §10). One candidate direction, not yet decided: Return doesn't need its own destination if it rides on the motivation the learner already has the next time they come back to Prepare, rather than requiring a separate voluntary trip back.
- **What counts as a "conversation" for witnessing purposes.** Every Ready Pack generated for a recurring situation, or only ones the learner confirms actually happened? This is the difference between a witness and a usage metric wearing a witness's clothing — directly relevant to staying inside the Recognition-vs-Evaluation thesis rather than drifting out of it.
- **One-off situations alongside recurring ones.** Not everything recurs. How does "My Life in Spanish" stay coherent when many situations (return a sweater, one hotel check-in) never become part of a recurring thread?
- **Relationship to existing Foundation documents**, specifically:
  - `BYG-GOV-001` §12 currently centers the *Ready Pack* as the reusable unit of value — if the primary object becomes a recurring thread, the Ready Pack's standing as the top-level product identity shifts, even if nothing it says is directly contradicted.
  - `BYG-GOV-001` §3's Product Promise ("Five minutes. More confidence. Better conversations.") — the five-minute clause was already reclassified from guarantee to positioning principle (old Decision #17); this pivot may mean the promise itself needs to say something about accumulated value, not just soften its speed claim further.
  - `BYG-UX-001-foundation-v1.6.md` §2.5's Placeholder Library is locked as *"not user-personalized in V1"* — in direct tension with a product whose central idea is showing the learner their own recurring life back to them. Not necessarily a contradiction (the anonymous library could remain for first-time input while a returning learner sees their own history as a different surface) but not yet reconciled either.
- **The "bad day" design problem.** What a stale, unvisited recurring context feels like when real-life circumstances change — a relationship ending, a pet passing, a job changing. A surface built to witness growth has a quiet inverse it needs to handle with real care, consistent with `BYG-GOV-001` §5's Emotional Position (the learner should leave calmer than they arrived) — not yet designed.
- **Terminology for the primary object** — intentionally deferred, see §8.

## 10. Working hypotheses for the open questions (Discovery only)

**Added same day, after Jamie flagged that preserving the questions without the current thinking behind them would lose exactly the kind of reasoning this document exists to protect.** None of these are Founder Decisions or implementation guidance — they're the current leaning, offered so a future session inherits the *why*, not just the *what*. Numbered to match §9's questions where they correspond directly; three are new observations §9 didn't already name.

1. **Cold start.** Don't fake continuity or manufacture history. "My Life in Spanish" begins empty on purpose — the learner's first real conversation is the first meaningful brick, not a gap to paper over.
2. **The Return mechanism.** Return shouldn't become its own destination — it should fold into the next Prepare cycle: *"Before we prepare today's Walking Athena conversation, how did last time go?"* Reflection becomes part of preparing again, not a separate trip back into the app. Consistent with, and now more concrete than, the candidate direction already noted in §9 — this is the same idea with a worked example attached.
3. **The primary object's name.** Still intentionally unresolved (see §8) — architecture, learner-facing vocabulary, and emotional identity may end up using different terms entirely rather than one noun forced to do all three jobs.
4. **One-off situations.** Some situations stay single moments; others grow into recurring parts of life. The product shouldn't force every preparation into a long-term structure it doesn't want.
5. **The magic moment** *(new observation, not previously captured in this document)*. The delight isn't the AI generation — it's recognition. The moment someone revisits part of their life and thinks *"I forgot I practiced that"* or *"Look how much this has grown."* Proposed as more emotionally durable than any single AI interaction — a direct extension of §6's Recognition-not-Evaluation thesis.
6. **What the product removes** *(new framing, not previously captured)*. Not primarily grammar difficulty. **The feeling of having to start over.** Every real conversation has the potential to make the next one easier because the learner doesn't lose what mattered. A sharper, more specific version of §4's differentiation argument.
7. **Bad-day design.** Don't hide those parts of a life. Don't celebrate them either. Preserve them quietly and respectfully — *"much like old photographs."*
8. **Annual reflection** *(new concept, not previously captured)*. A yearly "My Year in Spanish" was discussed — explicitly not a productivity report or achievement dashboard, but a quiet witness to how a learner's life has gradually become more bilingual over a year. Recognition, never evaluation — the same discipline as §6, applied at a longer time scale.

**On the loop reframing:** this addition closed with the same reframing already preserved in §7 (*"we're designing for the learner's return, not just their departure"*) — recorded there as reconfirmation, not duplicated here.

## 11. Meta-observation: why this preservation matters

Recovering the old Context/Preparation Continuity Architecture earlier in this same working relationship changed this entire conversation. Without it, tonight would have read as invention rather than recognition — a second, from-scratch design of something already worked through once. This document is preserved in that same spirit: not because the thinking is finished, but so a future session inherits how it evolved, not just where it landed.

---

**Status: Discovery only.** No Founder Decision, no governance amendment, no PRD change, no data model change, and no implementation handoff has occurred. Per `company/governance/operating-model.md`'s four-phase model, the next phase — if and when Jamie chooses to enter it — is a Founder Decision on whether to proceed, not automatically triggered by this document existing.
