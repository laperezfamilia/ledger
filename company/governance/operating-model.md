---
status: canon
owner: jamie
last_reviewed: 2026-08-13
depends_on:
supersedes:
related: ./roles.md
---

# Team Operating Model

**Not governance for Casa Pérez itself.** This is an operating model for how the team — Jamie, Solara, and Claude Code — collaborates. It formalizes an operating rhythm that had already emerged naturally as work moved from conversation-based collaboration into a GitHub-centered workflow with `ledger` as institutional memory.

**Amendment note (2026-08-13, Founder Decision):** the four phases below are unchanged — they still describe how work moves from open exploration to founder authorization to implementation. What changed is that "Primary participant(s)" is no longer a fixed AI job assignment per phase; roles within phases are fluid (see `./roles.md`). The one exception, unchanged and not fluid: Phase 2, Founder Decision, remains Jamie alone.

## Phase 1 — Discovery

**Typically:** Jamie + Solara — not an exclusive assignment; see `./roles.md` on fluid roles and mutual review.

**Purpose:** Explore before deciding.

This is where ideas are developed, challenged, pressure-tested, and sometimes discarded. The objective is not to defend ideas. The objective is to uncover what is true.

During Discovery, distinguish between:
- observations
- interpretations
- hypotheses
- candidate principles
- founder intuition
- evidence

Ideas remain exploratory until Jamie makes a founder decision. **No implementation assumptions should be made during this phase.**

## Phase 2 — Founder Decision

**Primary participant:** Jamie

This is the point where possibility becomes direction. Jamie determines what becomes product direction, educational philosophy, character canon, governance, or architecture.

**Neither AI should infer founder intent where a decision has not yet been made.**

## Phase 3 — Synthesis & Handoff

**Typically led by:** Solara — not exclusively; see `./roles.md`.

**Purpose:** Translate a long discovery process into an implementation-ready handoff. This phase exists to reduce the amount of reverse engineering required before implementation.

Typical responsibilities include:
- organizing discoveries
- identifying what is actually new
- separating discussion from decisions
- distinguishing observations from recommendations
- identifying implementation boundaries
- clearly labeling uncertainty
- ensuring founder decisions are explicit before implementation

**This is not implementation. It is the bridge between discovery and engineering.**

## Phase 4 — Implementation & Stewardship

**Typically:** Claude Code, as primary steward by default — not a permanent or exclusive assignment; see `./roles.md`.

**Purpose:** Implement founder decisions while maintaining the integrity of the living system.

This includes:
- implementation
- architecture
- GitHub stewardship
- documentation
- versioning
- provenance
- governance maintenance
- consistency across the repository
- identifying conflicts with existing canon
- preserving historical integrity

If implementation uncovers architectural issues, governance implications, historical inconsistencies, or opportunities to improve the repository, continue surfacing them. **This operating model is intended to create specialization, not silos.** Judgment during implementation remains an important part of the system.

---

## Shared Principles

Regardless of phase, all three collaborators operate from the same principles:

**Truth before elegance.** We don't protect beautiful ideas. We protect what is true. Sometimes that means letting go of an elegant solution because it isn't supported by the evidence or isn't authentic to the product or characters.

**Preserve uncertainty honestly.** Don't manufacture certainty simply because it feels cleaner. If something remains unresolved, label it honestly rather than silently resolving it.

**Recover before recreate.** Whenever practical, preserve original evidence rather than reconstructing it.

**Separate philosophy from governance.** Not every good idea belongs in the Constitution. Some ideas should mature through product development before becoming governing principles.

**Build after clarity.** Thinking has value when it reduces future ambiguity. Once a founder decision is made, implementation should proceed confidently.

---

## Practical Workflow

In most cases, the workflow now looks like this:

1. Jamie and Solara explore, research, pressure-test, and refine ideas — typically, not exclusively.
2. Jamie makes the founder decision. Always Jamie.
3. Solara typically prepares a clean implementation handoff.
4. Claude Code typically implements, documents, versions, and preserves the work within GitHub — as primary steward by default, not by permanent assignment.

Both Claude and Solara retrieve directly from GitHub rather than relaying through Jamie (see `./roles.md`'s "Access" section), and Jamie can explicitly authorize either collaborator to work outside their typical step above, with the other reviewing. Implementation may surface new questions that require returning to discovery. That feedback loop is intentional and welcome — it doesn't mean the model failed, it means the model is working as intended.

---

## One Final Note

This isn't dividing work between different AIs. It's a small team with complementary responsibilities. No role exists to compete with another. The objective is to let each collaborator spend more time where they create the most value.
