---
status: working
owner: jamie
last_reviewed: 2026-08-01
depends_on:
supersedes:
related: ./README.md, ./puzzle-production-ledger.md
---

# Agrupa Diagnostic Methodology — Extracted Notes

**Provenance note:** extracted from an operational "Project Synchronization: Diagnostic Protocol Engineering Phase" handoff document (a thread-continuity note, not itself a governance artifact). Per Jamie's explicit instruction — "archive knowledge, not logistics" — the handoff document itself was not preserved in `ledger`; only the durable, not-already-captured engineering insights below were extracted. Team-role descriptions and status claims from that handoff are *not* carried forward here, since `./README.md` (Agrupa Canonical README v2.0) is the more recent document and supersedes them.

**Known discrepancy, flagged rather than silently resolved:** the source handoff claimed Moment Independence had reached 3 validated occurrences (Movie Theater, Gas Station, Coffee Shop) and was "ready for a real governance decision now." `./README.md` (newer) states only 2 occurrences qualify and that Coffee Shop does **not** count as a third. This file defers to the README's count as current; the handoff's claim is stale and is not repeated as fact here.

---

## Loop 1 / Loop 2 Distinction

**Loop 1** — fast, local puzzle revision. No governance implications. An author fixing an individual Tile or Moment based on one piece of evidence.

**Loop 2** — pattern accumulation across puzzles → candidate research finding → human validation → only then a possible governance update (e.g., a new Puzzle Constitution rejection criterion).

**Explicit rule:** the AI must never silently rewrite its own authoring behavior based on accumulated pattern-noticing. Noticing a pattern is Loop 1-scale; treating that pattern as a rule the AI now follows without human validation would cross into ungoverned self-modification. Validated must continue to mean *confirmed through independent human playtesting*, not author-side reasoning however many times repeated — this is a core defense against confident-sounding but thin conclusions.

## Three-Way Localization Output

When diagnosing where a puzzle's ambiguity or weakness lives (Tile / Moment / World / Board level), the resolution is not a single confidence score but one of three explicit outputs:

1. **Diagnosed** — evidence discriminates cleanly between candidate explanations.
2. **Underdetermined — recommend cheapest discriminating test** — evidence doesn't yet discriminate; test the cheaper/more local hypothesis first, re-verify, and let the result earn the diagnosis rather than guessing.
3. **Insufficient evidence** — return to Capture; don't force a diagnosis the evidence doesn't support.

This replaced an earlier, rejected approach ("fewest unsupported assumptions") judged too subjective to apply consistently.

## Status

Both notes above are working methodology, not locked canon — they describe how diagnostic reasoning should proceed when evaluating puzzle ambiguity, but haven't themselves been validated as a formal protocol. If a full Diagnostic Protocol document is ever formally drafted and locked, these notes should be superseded by it rather than maintained in parallel.
