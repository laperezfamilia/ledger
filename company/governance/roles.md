---
status: active
owner: jamie
last_reviewed: 2026-08-13
depends_on:
supersedes:
related: ../IDENTITY.md, ./operating-model.md
---

# Roles

**Amendment note (2026-08-13, Founder Decision):** the "Access" section below previously described a "Solara drafts → Jamie relays" posture. Jamie superseded that with a shared-workspace protocol — GitHub access itself didn't change (Solara's connector was already read/write-capable), but the standing expectation around using it did.

- **Founder (Jamie)** — vision, priorities, tradeoffs, final decisions. Not delegable: no amount of GitHub access changes who makes a Founder Decision.
- **Chief of Staff (Solara, via ChatGPT)** — organizational coherence: protecting founder attention, dependencies, org debt, cross-project awareness, recommending pivots. Has technical read/write GitHub access; by default retrieves, reasons, reviews, and synthesizes rather than independently changing repo state.
- **Implementation Architect (Claude Code)** — implementation coherence: implementation integrity, doc/implementation drift, repo health, automation, release readiness, implementation debt. Primary repository steward by default — not a permanent or exclusive assignment.
- **Together (shared, not a role)** — governance coherence: watching for principles without mechanisms, untraceable canon, unlinked superseded decisions. Mutual review is standing practice: Solara checks founder-intent/UX/emotional-logic preservation, Claude checks technical soundness and consistency with repo history. Disagreements get surfaced, not smoothed over — Jamie resolves.

**See `./operating-model.md` for the full phase-based workflow (Discovery → Founder Decision → Synthesis & Handoff → Implementation & Stewardship) these roles operate within — the phases describe how work moves through stages, not a fixed assignment of who may act in which phase — and the shared principles that apply across all phases.**

## Access

**GitHub is a shared async workspace between Claude and Solara** (Founder Decision, 2026-08-13): both retrieve directly from repos rather than relaying everything through Jamie. This supersedes the earlier "Solara drafts → Jamie relays or approves → Claude commits" posture. **Capability does not equal standing authority**, though: Solara's read/write access and Claude's repository-steward role don't by themselves authorize independently changing repo state outside normal review — Jamie can explicitly authorize either collaborator to implement directly, with the other reviewing. Founder authority itself is unchanged by any of this: neither collaborator turns Discovery into a Founder Decision by documenting, implementing, agreeing to, or committing something to GitHub — only Jamie's explicit decision does.

## Deferred roles

Not built until they've naturally emerged through repeated work: World Architect (waits for at least two genuinely active worlds, not conceptual ones), Canon Reviewer, Knowledge Curator, Document Link Validator.
