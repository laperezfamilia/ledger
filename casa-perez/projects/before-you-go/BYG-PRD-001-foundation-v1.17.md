---
status: canon
owner: jamie
last_reviewed: 2026-08-01
depends_on: ./BYG-GOV-001.md, ./BYG-DES-001.md
supersedes:
related: ./BYG-PRD-001.md, ./BYG-PRD-001-amendments.md, ./BYG-UX-001-foundation-v1.6.md, ./BYG-DEC-001-foundation-v1.21.md, ../../governance/GOV-004-product-scope-safety-responsible-use.md
---

# BYG-PRD-001: Before You Go — MVP Product Specification

**Version 1.17 | Status: Foundation v1.1, Approved Build Authority — pending audio validation deliverable (§5)**
Governs against: BYG-GOV-001 (Product Constitution). Voice governed by: BYG-DES-001 (Voice & Design Language). Screen-level UX: BYG-UX-001.

**Lineage note (2026-08-01):** filed under this distinguishing filename, not `BYG-PRD-001.md`, because `BYG-PRD-001.md` and `BYG-PRD-001-amendments.md` already hold earlier content (§7 "Post-Capture Decision Tree & Edit/Refine Allowances," §7a "Conversation Continuity") that **does not match this document** — different §7 topic entirely, no Edit Situation/Refine dual-allowance model, no Context/Preparation continuity data model anywhere here. Per Jamie's explicit instruction, both sources are preserved as-is, unreconciled, until provenance is investigated. See `./BYG-PRD-001.md` and `./BYG-PRD-001-amendments.md` for the earlier material and the matching note there. Tracked in `STATE.md` org debt.

---

## 1. Input Experience
Single input field. One prompt: **"What's coming up?"** Supporting text: "Tell us about the conversation you'd like to feel ready for."

One input experience supports two intentions without a visible mode selector:
- **Immediate:** "I'm meeting my landlord tomorrow."
- **Future practice:** "I want to practice landlord conversations."

The model infers tense, urgency, and emotional framing from phrasing. No separate onboarding branch in V1.

*Flag: revisit if user testing shows learners are confused about which intent they're expressing. Tracked in BYG-DEC-001 parking lot (Owner: Claude).*

**Onboarding addition (§20):** before reaching this input field for the first time, onboarding asks a required dialect question — *"Which Spanish would you like to prepare for?"* — with primary learner-facing options "Mexican Spanish" and "Spanish from Spain" ("Peninsular Spanish" may appear as secondary explanatory text, never as the only label). This sets `default_dialect` and is changeable later in Settings → Learning Preferences, not on this screen.

*Full Home screen layout and hierarchy — greeting, supporting copy, placeholder example, CEFR display, primary button, Recently Prepared, first-time state — is specified in BYG-UX-001 §2.*

## 2. Ready Pack Structure
1. Situation Summary
2. What You Could Say
3. What You Might Hear
4. Key Vocabulary
5. Just In Case
6. Ready Card
7. One Quick Rehearsal
8. Native-speed audio (attached to relevant phrases throughout, especially §3)
9. A Note Before You Go

*Flag: "Just In Case" naming is unresolved pending cold testing — see BYG-DEC-001 parking lot and provisional rationale.*

## 3. Ready Card
Not a summary. Contains only the handful of highest-value phrases a learner could screenshot and carry into the situation. This is the layer that must be reachable within the five-minute target (§8).

## 4. One Quick Rehearsal
Approximately **six to eight total alternating lines/turns**, with each speaker participating several times. Scripted, not adaptive roleplay. Enough to create conversational rhythm, not a simulation.

## 5. Audio
Native-speed audio is a V1 requirement, particularly for "What You Might Hear." Slow-speed audio is deferred (non-goal, BYG-GOV-001 §10).

**Technical validation gate — required before vendor or pipeline selection:**
- Voice naturalness
- Dialect suitability
- Generation latency
- Caching behavior
- Estimated cost per Ready Pack
- Multilingual limitations
- Playback reliability / accessibility

No vendor or economics assumption is final until this gate passes. This is the first critical-path technical item after Foundation approval; it runs in parallel with non-technical screen-flow and visual design work (Track A/B, BYG-DEC-001), not before it.

*Dialect linkage (§20): the Mexican Spanish / Peninsular Spanish coverage already required in this gate (below) is not incidental — voice selection for audio generation must be driven by a pack's `pack_dialect` field, never a single fixed voice regardless of dialect.*

### Audio Validation Deliverable

Owner: Claude, with Jamie and Solara approving final product quality.

Test a small phrase set across at least:
- Mexican Spanish
- Peninsular Spanish

*Scope note: French and Italian were previously listed here as test cases. Per the reaffirmed V1 language scope (§19, BYG-DEC-001), French and Italian are future-expansion possibilities only and are explicitly not to expand V1 validation, onboarding, audio, prompt, or QA scope — removed from the required test matrix accordingly. If a vendor's French/Italian quality happens to be visible during testing, that's incidental information, not a V1 deliverable requirement.*

Evaluate each vendor/pipeline candidate on:
- Naturalness
- Dialect accuracy
- Intelligibility
- Latency
- Estimated cost per Ready Pack
- Caching behavior
- iOS/Android playback reliability
- Licensing and commercial-use terms

**Goal:** identify the simplest vendor that meets the V1 quality bar — not the most feature-rich option.

Completion of this deliverable is the trigger that unblocks vendor selection (BYG-DEC-001 parking lot).

## 6. Repeat Situations / Retrieval
When a new situation resembles a past one:
1. Retrieve the most relevant previous Ready Pack via lightweight similarity matching.
2. Pass the retrieved pack to the model with instructions to preserve load-bearing language, introduce modest useful variation, and avoid verbatim repetition.
3. No comparison is shown to the learner. No curriculum-tracking or phrase-overlap-scoring subsystem is built.

**Recommended V1 mechanism:** lightweight tagging / normalized intent matching (situation type + key entities) rather than full semantic embedding search. This is the simplest approach that supports "similar situation" detection without a vector database or ranking infrastructure.

*Flag: this is a recommendation, not a locked decision. Confirm during architecture review. Semantic similarity search is the fallback if tagging proves too coarse in testing. Owner: Claude; trigger: structured pack schema and saved-history model finalized (BYG-DEC-001 parking lot).*

*CEFR interaction (§18): situation-matching for retrieval must include CEFR level as part of the match key, not just situation type + entities. A same-level revisit (e.g., "Walking Athena" requested again at the learner's existing A1 pack) is a retrieval-with-variation case per this section. A different-level request for the same situation (§18's "Try this at another level") is a distinct, deliberate new generation — not a retrieval-and-vary case — and must not blend register/complexity across levels.*

*Dialect interaction (§20): dialect is also part of the match key, alongside CEFR level. Unlike level, dialect is not something learners are expected to deliberately vary pack-to-pack (§20) — so a retrieval match should ordinarily use the learner's current `default_dialect` rather than surfacing a dialect switcher. Never blend Mexican and Peninsular Spanish within a single retrieved-and-varied pack.*

## 7. Refine My Ready Pack
After generation, the learner may issue one-step clarifications (e.g., "She's nervous around other dogs," "Use more formal language"). The AI updates the existing structured pack rather than regenerating from scratch. This is not open chat.

- **Ceiling:** three focused refinements per Ready Pack.
- After the third: *"This pack has changed quite a bit. Would you like to create a fresh Ready Pack using everything you've clarified?"*
- Refinements operate on structured Ready Pack data (§9) and update only what the clarification materially changes — not the whole pack.

Constitutional grounding: the learner has the final word; the AI interprets, the learner decides; revision never requires starting over.

*Note: the 3-refinement ceiling above is a locked UX decision (BYG-DEC-001 #6) and does not change. Whether a refinement consumes a full, partial, or zero usage/generation credit is a separate, unresolved monetization question — see BYG-DEC-001 Monetization parking lot. Do not hardcode a credit-cost assumption for refinements in the backend; keep it configurable.*

## 8. Five-Minute Promise — Measurable Definition
The promise is: **within five minutes, the learner can reach a usable Ready Card and feel more prepared.** It does not mean the entire Ready Pack must be read, heard, and rehearsed in five minutes.

Design requirement — the Ready Pack is layered:
- Skim the essentials (Ready Card) when time is short.
- Explore audio and vocabulary when time allows.
- Complete One Quick Rehearsal when useful.

**Target:** time to a usable Ready Card under normal conditions is under five minutes. This is the measurable requirement engineering and content generation should be held to.

## 9. Data Model Requirement
Ready Packs must be stored as **structured data** (distinct fields per section: Situation Summary, What You Could Say, What You Might Hear, Key Vocabulary, Just In Case, Ready Card, Rehearsal, Audio references, Note) — not a single generated text blob. This is required to support both Refine My Ready Pack (§7) and Repeat Situations retrieval (§6).

**CEFR extension (§18):** every Ready Pack additionally stores its own `pack_level` field (CEFR level used for that specific generation). This is distinct from and does not overwrite the learner's `default_level` preference (§10, §18) — the data model must not assume a situation exists at only one level.

**Dialect extension (§20):** every Ready Pack additionally stores its own `pack_dialect` field, distinct from and not overwritten by the learner's `default_dialect` preference (§10, §20) — so changing the default later never retroactively alters previously generated packs or their audio.

## 10. Memory Data Model
Practical fields only, per BYG-GOV-001 §8:
- `learning_language` and `support_language` — two distinct fields, not a single "native language" field (§19)
- `default_dialect` — the learner's current onboarding/Learning Preferences dialect choice (V1: Mexican Spanish or Spanish from Spain); distinct from the per-pack `pack_dialect` (§9, §20)
- Learner level (`default_level` — the learner's onboarding/Learning Preferences CEFR setting; distinct from the per-pack `pack_level`, §9, §18)
- Translation preferences (how `support_language` is used — e.g. inline vs. on-demand — not the language choice itself)
- Saved Ready Packs (structured, per §9)
- Recent situation history (for retrieval, §6)

No relationship, character, or narrative-continuity fields.

## 11. Build Stack
FlutterFlow is the primary build environment. FlutterFlow AI generates the majority of screens; Jamie's role is Creative Director rather than UI engineer. Codex provides engineering support rather than initial architecture.

The AI orchestration backend (pack generation, refinement, retrieval, audio pipeline) is a distinct engineering surface from the FlutterFlow screens and needs its own scoping.

*Flag: backend architecture/hosting not yet specified. Owner: Claude; trigger: Foundation v1.0 approved and Ready Pack structured data schema finalized (BYG-DEC-001 parking lot).*

## 12. Competitive Positioning & Differentiation Test
BYG is not valuable because ChatGPT is incapable of generating situational language — a skilled, motivated user can already do this with enough prompting effort (confirmed via real-world examples, e.g. patients prompting ChatGPT to prep for doctor's appointments). BYG is valuable because the learner should not need prompting expertise, repeated iteration, manual organization, or emotional bandwidth to turn a blank chat into usable real-world preparation.

**Feature Differentiation Test** — apply to every proposed feature:
> Could an ordinary user obtain the same usable result from raw ChatGPT with one obvious sentence and no meaningful cleanup?
> - If yes, that feature alone is not meaningful differentiation.
> - If the learner would otherwise need multiple prompts, manual organization, repeated refinement, or prompt-engineering skill, BYG is providing real product value.

**Current differentiation stack:**
- Zero-prompt expertise (single input field encodes what to ask for)
- Guaranteed Ready Pack structure (not a wall of chat text)
- Fast path to a usable Ready Card
- Preparation for both saying and hearing
- Native-speed audio
- One Quick Rehearsal
- Focused refinement rather than open chat
- Practical preparation memory
- Consistent warmth and emotional architecture
- Mobile-first real-world usability
- A personal library of reusable preparation (§13) rather than disposable chat output

**Memory guardrail:** avoid broad claims like "ChatGPT doesn't remember." Say instead: *BYG remembers exactly the practical information needed for conversation preparation, inside a purpose-built workflow.* (ChatGPT's own custom GPTs, for comparison, explicitly do not carry memory or prior conversations between sessions — confirmed via OpenAI's GPT documentation, July 2026.)

**Platform risk (see also BYG-DEC-001):** general AI platforms may eventually reproduce pieces of this workflow. BYG's long-term differentiation is product judgment, learner psychology, interaction design, emotional architecture, preparation workflow, speed of focused iteration, and integration with the larger language-learning portfolio — not a technical capability ChatGPT categorically lacks. No pivot recommended; proceed remains the current decision.

## 13. Saved Ready Packs & My Ready Packs Library
A generated Ready Pack must never disappear or exist only inside a conversational thread. This reframes the product from "an app that generates AI responses" into "a personal library of real-life conversation preparation" — a stronger product identity that also answers part of the "why not ChatGPT" question without ever naming ChatGPT.

**Automatic Saving:** every completed Ready Pack is automatically saved until the learner deletes it. Reopening a saved Ready Pack does **not** count as generating a new one (no generation cost, no usage-credit consumption — ties to §12/Monetization tracking).

**My Ready Packs (V1 core requirement):** a dedicated library where the learner can:
- View saved Ready Packs
- Reopen the complete Ready Pack
- Access the Ready Card directly
- Replay previously generated audio
- Rename
- Favorite
- Delete
- Search

**Data model impact (extends §9):** the structured Ready Pack schema needs additional library metadata fields — title/rename, favorite flag, created/last-opened timestamps, and a soft-delete flag rather than hard deletion, so "delete" is safely reversible during early testing.

*Strategic rationale for why this matters beyond mechanics — including its role as an answer to "why not ChatGPT" — is documented in BYG-DEC-001, Documented Product Reasoning.*

## 14. Collections (V1.x Fast-Follow — Locked Classification)
Grouping related Ready Packs (e.g., a "Spain Trip" collection containing Airport → Hotel, Ordering Coffee, Restaurant Dinner, Asking for Directions; or an "Everyday Practice" collection containing recurring local situations) is a real, validated need — it's the difference between a pile of packs and a "Spain trip folder" a learner thinks in terms of.

**Locked classification (BYG-DEC-001):**
- **My Ready Packs library (§13) is the core V1 requirement** — saved, retrievable, replayable, renameable, favoritable, searchable, deletable.
- **Collections management UI is a V1.x fast-follow, not required for the initial tester-ready release.** The initial release does not require creating collections, moving packs between collections, collection management screens, or collection-specific navigation.
- **Data-model preparation is required in V1**, even though the UI isn't: include an optional `collection_name` field (nullable, freeform) on the Ready Pack schema from the start, so collections can be added later without a migration-heavy rebuild.
- **When added, collections live inside My Ready Packs** — not a fourth primary navigation destination (see §15).

This lets the first build ship without an extra screen while keeping the door open for "Spain Trip"-style grouping to arrive quickly once the library is working reliably and early testers show how they naturally want to group their packs.

## 15. Navigation
Primary V1 navigation: **Prepare | My Ready Packs | Settings.** Locked, including post-Collections (§14) — collections live inside My Ready Packs and do not become a fourth destination.

## 16. Monetization-Flexible Architecture Requirement
Pricing, free-trial-vs-freemium, usage allowances, bundles, and tier structure are all unresolved (BYG-DEC-001 Monetization parking lot) and must not block product design or initial FlutterFlow work. However, the backend must be built so that these can be introduced or changed later **without a major rebuild**:

- Usage/generation counts should be tracked per account from V1, even before any limit is enforced, so real usage data exists when pricing is decided.
- Subscription tier should be a configurable account attribute, not hardcoded logic scattered through the app.
- The system must not promise or market unlimited newly generated Ready Packs (BYG-DEC-001 Decision #10) until real costs and usage patterns are known.
- Refinement credit-cost accounting (§7 note above) must be configurable, not assumed.
- Reopening a saved Ready Pack (§13) must not consume a generation credit.

This is an architectural constraint on how data is modeled now, not a monetization decision.

## 17. Related Ready Pack Suggestions (Understanding Loop)
Part of the Ready Pack completion state. Framed internally as a three-part "understanding" loop: before generation (the app advances the learner's stated situation into a clear preparation plan), inside the pack (content mirrors the real situation, not a flattened version of it), and after the pack (a small number of genuinely related next situations).

**Understanding Checkpoint Rule (locked, replaces earlier "reflects" language per BYG-DES-001):**

- **Simple, clear input** — generate immediately, without unnecessary acknowledgement.
- **Multi-part input** — advance the situation into a concise plan that names the distinct moments the Ready Pack will cover.
  > Example: *"We'll focus on talking with Athena during your walk, and we'll also get you ready in case a neighbor stops to chat."*
- **Material ambiguity** — ask one focused clarification, only when the missing information would materially change the Ready Pack.
  > Example: *"What would you most like help with at the wedding?"*

This preserves the internal purpose — confirming understanding before generating — without giving prompt-writers license to echo the learner's words mechanically. Preserved rules: no "It sounds like…," no "Based on your input…," no AI self-commentary, never merely repeat the learner's words back, and every visible sentence must Prepare, Encourage, Clarify, or Guide (BYG-DES-001 §4). Preferred product-language verb is **advance**; where technical precision is more useful than voice, **"translate the situation into a preparation plan"** is acceptable.

**Completion-state order (locked):**
1. Ready Card
2. A Note Before You Go
3. "You may also want to feel ready for…"
4. Optional action: Create this Ready Pack

Related suggestions must never compete with the Ready Card or delay access to it — they appear only after the learner has already reached the useful part of the experience, preserving the five-minute promise (§8).

**Section language:** "You may also want to feel ready for…"

**Per-suggestion fields:** concise title, a one-line reason it's relevant, and an optional suggested future collection label (ties to §14 — this is just a suggested label on the field, not a commitment to build collection management in V1).

Example:
> **Checking into your hotel**
> Because you mentioned going directly there from the airport.

**V1 boundary (locked):**
- Return **up to three** related Ready Pack ideas as structured metadata in the *original* generation response — no separate AI call.
- **Nothing generates automatically.** A second full Ready Pack is only created when the learner deliberately taps "Create this Ready Pack" — a normal generation, tracked like any other (§16).
- Suggestions must be **dismissible**.
- **No separate recommendation engine and no behavioral tracking.** Suggestions are derived only from the current situation and permitted practical-profile context (§10) — reuses the situation-tagging approach already planned for retrieval (§6), pointed forward instead of backward.
- **Placement constraint:** suggestions must appear clearly after/below the Ready Card in the completion state and never compete with it for attention — they cannot interfere with the five-minute promise (§8).

**Generation prompt quality rule (locked language, use verbatim when drafting the prompt):**
> Suggest only situations that are a natural extension of the learner's stated experience, practical context, or likely next step. Do not recommend generic popular topics, duplicate the current Ready Pack, or generate suggestions merely to increase engagement.

**Governing rule:** recommend the next useful moment, not more content for its own sake.

## 18. CEFR Level Architecture
Grounded in two real use patterns: **just-in-time preparation** (a quick brush-up for something happening soon, e.g. ordering coffee in Spain) and **ongoing real-life practice** (revisiting a familiar situation over time at increasing levels, e.g. walking Athena in A1 language one day, A2 later, B1 after that). Product framing: *"Real life stays the same. Your language grows."*

**Architecture (locked):**
- BYG uses the standard **CEFR framework, full range A1–C2** (reaffirmed — no artificial ceiling): A1 Beginner, A2 Elementary, B1 Intermediate, B2 Upper Intermediate, C1 Advanced, C2 Proficient.
- The learner chooses a **default CEFR level** during onboarding, changeable later in Learning Preferences (Settings, §15). This preselects the level for new Ready Packs.
- The learner can **override the level for an individual Ready Pack** without changing the permanent default.
- **Every Ready Pack stores its own `pack_level`** (§9) — the data model must not assume one situation exists at only one level.
- The completion state includes a simple action: **"Try this at another level."** Selecting a level generates and saves a **new** Ready Pack for the same or closely related situation — a normal tracked generation (§16), not a variant of the existing pack.

**Rationale for the full range, not a B2 ceiling:** V1's language scope is intentionally narrow (Spanish, English support, two dialects — §19, §20), so there's no need to also cap proficiency. BYG is not a systematic CEFR curriculum and does not teach or track progression through levels — it calibrates one situational Ready Pack to the learner's selected proficiency. C1/C2 learners have a different need, not an absent one: preparation for unfamiliar, formal, professional, medical, culturally nuanced, or region-specific conversations.

**Higher-level generation must differ qualitatively, not just get longer.** As level increases, favor:
- More idiomatic language
- More subtle register choices
- Richer, context-specific vocabulary
- More realistic native-speed responses (ties to §5)
- More advanced clarification, softening, negotiation, and recovery language
- Reduced translation support, per the learner's separate translation preference (§10) — not automatically tied to level, but level-appropriate defaults are reasonable

**V1 storage/display:** separate saved Ready Packs, e.g. *Walking Athena — A1*, *Walking Athena — A2*, *Walking Athena — B1*, each independently viewable/searchable/favoritable in My Ready Packs (§13).

**Not required for MVP (V2 concept only):** grouping same-situation, multiple-level packs into a single growth-path view (e.g., *Walking Athena: A1 ✓ · A2 ✓ · B1 ✓ · B2*). **Flagged for future scrutiny, not approved now:** a checkmark-based level-completion view would need careful review against two locked V1 non-goals (BYG-GOV-001 §10) before it's built — "systematic grammar curriculum" and "progress gamification." Supporting all six CEFR levels does not, by itself, imply a progress ladder, mastery tracking, or curriculum — nothing about assigning a CEFR register to a single Ready Pack's language violates those non-goals (it calibrates complexity for one real conversation, it doesn't sequence lessons or track mastery) — but a visible multi-level "path" with completion marks starts to resemble exactly the curriculum/progress-bar pattern the Constitution excludes. That review should happen deliberately when V2 is scoped, not be assumed through by this section.

*Interactions with other sections: retrieval (§6) must treat level as part of the match key; the data model (§9) and Memory Data Model (§10) distinguish `default_level` (preference) from `pack_level` (per-generation); "Try this at another level" consumes a generation credit like any other new pack (§16).*

## 19. Learning Language & Support Language Architecture
Two distinct concepts, not one field and not a boolean:
- **`learning_language`** — the language the learner is preparing to use in the real conversation.
- **`support_language`** — the language used for translations, explanations, guidance, and interface support where applicable.

**Deliberately not modeled as "native language".** Support language is more inclusive and functionally accurate — the product only needs to know what the learner is preparing to use and what language best supports their understanding, not their linguistic origin.

**V1 scope (locked, fixed values):**
- `learning_language` = Spanish
- `support_language` = English

This does not expand V1 into a multilingual interface or a multi-language product — the values are fixed for V1, not learner-selectable.

**Future-compatibility requirement:** the architecture must remain compatible with learners independently choosing from supported learning languages and supported support languages in a later version (e.g. Learning Spanish/Support English, Learning English/Support French, Learning Italian/Support German). Concretely: keep `learning_language` and `support_language` as two separate fields from V1 onward, even while both are fixed — do not hardcode a single combined "Spanish-for-English-speakers" assumption anywhere in the data model, prompts, or content pipeline that would need to be untangled later.

## 20. Dialect Architecture
**V1 supported dialects:** Mexican Spanish, Spanish from Spain (Peninsular Spanish).

**Onboarding (locked):** dialect preference is a required V1 onboarding choice, not optional and not inferred. Learner-facing prompt: *"Which Spanish would you like to prepare for?"* Primary labels: "Mexican Spanish" / "Spanish from Spain" — "Peninsular Spanish" may appear as secondary explanatory text but is never the only label shown to the learner.

**Changeable later:** Settings → Learning Preferences, same location as CEFR default level (§18).

**Data model (locked):**
- `default_dialect` — the learner's current preference, used for future Ready Packs.
- `pack_dialect` — the dialect used for one specific Ready Pack, stored per-pack (§9).
- Changing `default_dialect` must never retroactively alter previously generated packs or their audio — each pack's `pack_dialect` is fixed at generation time.

**Dialect must consistently govern:**
- Vocabulary and regional word choice
- Pronunciation and audio voice selection (§5)
- Likely phrases in "What You Might Hear"
- Grammar and forms where regionally relevant
- Register and natural conversational usage

**Never mix dialects within one Ready Pack**, unless a future feature explicitly and deliberately explains a relevant regional alternative (not silent blending).

**V1 UX (locked, distinct from CEFR):** dialect is selected at onboarding and changed in Settings only — **no per-pack dialect selector on the Prepare screen in V1**, unless user testing demonstrates frequent switching is genuinely necessary. This is a deliberate contrast with CEFR level (§18), which learners may want to vary pack-by-pack for growth: dialect instead ordinarily reflects the real region or community the learner is preparing to communicate with, so it behaves more like a stable preference than a per-situation choice.

## 21. Explicit Teaching Surface (Settings)
Complements the Implicit Teaching pattern governed in BYG-UX-001 §1 (Placeholder Library, screen hierarchy, voice, progressive disclosure). Where implicit teaching works by modeling without the learner feeling taught, explicit teaching serves learners who want a deeper understanding on demand.

**V1 requirement:** Settings includes a **"Using Before You Go"** section containing short, optional coaching cards explaining what the product can help with and how to get the most from it. Opt-in, not a forced onboarding flow — the learner navigates to it, it doesn't interrupt Prepare or the completion flow.

**Not curriculum:** these cards explain product usage (what BYG does, how to describe a situation, how refinements/levels/dialect work), not Spanish grammar or language instruction — this does not conflict with the systematic-grammar-curriculum non-goal (BYG-GOV-001 §10).

## 22. Non-Goals
See BYG-GOV-001 §10 (governing copy — not duplicated here to avoid drift).
