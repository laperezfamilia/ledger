---
status: working
owner: jamie
last_reviewed: 2026-08-10
depends_on: ../projects/before-you-go/, ./GOV-004-product-scope-safety-responsible-use.md, ../../company/governance/operating-model.md
supersedes:
related: ../projects/before-you-go/find-the-words-implementation-roadmap.md, ../projects/before-you-go/find-the-words-continuity-pivot-discovery-2026-08-06.md, ../projects/before-you-go/BYG-GOV-001.md, ../projects/before-you-go/BYG-DEC-001-foundation-v1.21.md, ../../STATE.md
---

# casa-perez-hq ↔ ledger reconciliation (2026-08-10)

**Evidence-gathering only, per Jamie's explicit instruction.** Nothing was migrated, deleted, reorganized, or declared canonical as part of this pass. This is the first task run under the new Claude/Solara GitHub collaboration protocol — findings below are left as a repo artifact specifically so Solara's independent pass (if she runs one) can be compared against this one rather than relayed through Jamie.

**Scope checked:** every repo currently accessible to this session — `laperezfamilia/ledger` (this repo) and `casa-perez-hq/find-the-words`, the only repo under the `casa-perez-hq` org this session has access to. If other `casa-perez-hq` repos exist that this session can't see, this document doesn't cover them.

## The headline finding

**The reconciliation this task expected to find (duplicated/conflicting canon) isn't the real issue. The real issue is that a full day of real, approved work — spanning both repos — is sitting on matched, never-merged branches in each, invisible to anyone reading either repo's default branch.**

Both `ledger` and `find-the-words` have a branch named `claude/find-the-words-setup-z361it`, evidently from one working session that spanned both repos on 2026-08-06. Neither branch is merged into its repo's default branch. Together they contain:

- **In `ledger`:** a Founder Decision (Sofía is a cross-product identity — `BYG-GOV-001` §9 amended, v1.1 → v1.2, full record at `BYG-DEC-001-foundation-v1.21.md` Decision #32), a Founder Observation on Instructional Continuity, the actual Placeholder Library content (171 entries, resolving org debt open since 2026-08-01), a Discovery-status product-pivot synthesis (`find-the-words-continuity-pivot-discovery-2026-08-06.md` — "Prepare → Go → Return → Build"), and two documentation-drift corrections (a stale FlutterFlow stack reference, a half-triggered retrieval-tagging flag).
- **In `find-the-words`:** a scaffolded Next.js app, a full Ready Pack generation/refinement implementation with tests (`src/lib/ready-packs/`), Sofía's Find the Words voice as structured data (`content/characters/sofia/find-the-words-voice.ts`, per `engineering-principles.md`), a founder showcase batch of 10 hand-authored Ready Packs, an evaluation harness, and an architecture doc. 7 commits.

Right now, `ledger`'s default branch (`claude/casa-perez-kb-init-4hd2r8`) still shows `BYG-GOV-001` as **v1.1**, and `find-the-words`'s default branch (`main`) is still just the initial README + `.gitignore`. Anyone — including Solara, including a fresh Claude session — reading only the default branches gets a materially stale picture of both governance state and implementation progress.

## The six questions

**1. What Casa Pérez material exists in each location?**
`ledger`'s `casa-perez/` folder (default branch) holds the governance/spec/research layer: Agrupa's locked design canon, GOV-004, Before You Go's Foundation v1.1 documents (`BYG-GOV-001`, `BYG-DES-001`, `BYG-PRD-001-foundation-v1.17`, `BYG-UX-001-foundation-v1.6`, `BYG-DEC-001-foundation-v1.21`), brand assets, and the Casa Pérez decision log. `find-the-words`'s default branch holds nothing product-specific yet — a bare scaffold. The real implementation content for both exists only on the orphaned branches described above.

**2. Is anything duplicated?** No meaningful duplication found. The two repos' actual (default-branch) content doesn't overlap — one holds docs, the other is empty. The orphaned branches are complementary halves of one body of work (docs in `ledger`, code in `find-the-words`), not duplicates of each other.

**3. Does anything conflict?** One real conflict, already self-resolved on the orphaned branch but not yet visible anywhere else: `find-the-words`'s implementation needed to know whose voice would write its coaching, which surfaced a direct contradiction between `BYG-GOV-001` §9's original text ("must never... share characters") and work already assuming Sofía voices Find the Words. This was caught and resolved as a Founder Decision (see above) — but that resolution lives only on the unmerged branch, so the contradiction is technically still live in every branch Jamie or Solara would normally read.

**4. Does one location have newer/more authoritative versions?** Yes — the orphaned branches, dated 2026-08-06, are newer than both repos' current default-branch state, and at least one item on them (the Sofía cross-product Founder Decision) is explicitly founder-approved, not tentative. "Newer and more authoritative" and "not merged" are true at the same time here, which is the actual problem.

**5. Do the two locations serve different purposes and should they stay separate?** **Yes — and this doesn't need a new Founder Decision, because it's already one.** `STATE.md`'s 2026-08-03 "Transition point" entry (already on `ledger`'s default branch) states the intended split explicitly: `ledger` is institutional memory (governance, research, the "why"); `find-the-words` is the product repo (code, issues, PRs, the "how"). The orphaned `find-the-words` branch's own `README.md` restates the identical relationship independently ("Governing philosophy, product specs, voice/design language, and engineering principles live in `ledger`... Start there... This repository is the implementation home"). Two independent statements of the same architecture, from two different sessions — that's real confirmation the split is sound, not something this reconciliation needs to relitigate.

**6. What should eventually migrate or get designated canonical?** This is the part that needs Jamie's decision, not mine. My read of the evidence: the most natural resolution is merging each orphaned branch into its own repo's default branch — that's what would make the already-approved Sofía decision, the Placeholder Library, and the real implementation actually visible where people look for them, and it doesn't require deciding anything new (the content already carries its own approved/Discovery status markers, unchanged). But merging is an implementation action, and per the new protocol neither AI turns Discovery into a Founder Decision by committing something — and this isn't Discovery, it's *already-decided-but-unmerged* work, which is a different situation the protocol doesn't explicitly name. Flagging rather than acting:

## What needs Jamie's decision

- **Should `claude/find-the-words-setup-z361it` be merged into `ledger`'s default branch, `find-the-words`'s default branch, both, or neither?** If yes, who does it — Claude (repository steward by default) or explicit joint review with Solara first, given her mutual-review role covers founder-intent/UX preservation and this branch contains a real product-philosophy pivot (§ the Continuity Pivot synthesis) she may want to weigh in on before it becomes visible as "the" state of the repo.
- **Should the Continuity Pivot Discovery synthesis get any response now**, or stay parked exactly as filed (Discovery only, explicitly not ready to build from)? Not this reconciliation's call — noted because merging the branch would make it newly visible to whoever reads `ledger` next, which may itself prompt the question.
- Nothing else found rises to needing a Founder Decision — items 1-5 above either have no conflict or already follow from locked governance.

## What I did not do

Did not merge, rebase, cherry-pick, or otherwise move any content from either orphaned branch. Did not modify `BYG-GOV-001`, `BYG-DEC-001-foundation-v1.21`, or any other canonical document. Did not touch `find-the-words` at all beyond fetching and reading. This document and a short `STATE.md` Org Debt pointer are the only changes made.
