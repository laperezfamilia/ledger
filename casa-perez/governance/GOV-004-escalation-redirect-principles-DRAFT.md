---
status: working
owner: jamie
last_reviewed: 2026-08-03
depends_on: ./GOV-004-product-scope-safety-responsible-use.md
supersedes:
related: ./GOV-004-product-scope-safety-responsible-use.md, ../projects/before-you-go/BYG-GOV-001.md
---

# GOV-004 §7 — Escalation & Redirect Principles (DRAFT PROPOSAL, not founder-approved)

**Status: Draft proposal only.** Not yet reviewed or approved by Jamie. Not canon. Written to fill GOV-004's own "7–11: not yet drafted" gap, specifically the Escalation & Redirect Principles item — proposed now because Find the Words is entering implementation with live conversational AI (Sofía) in the MVP, and this needed to exist before real users, not after.

**This document requires real clinical and legal review before it governs anything.** What follows is a careful first draft, not expert judgment. Treat it as the starting point for that review, not a substitute for it.

## This is not the same question as GOV-004 §6

Worth stating precisely, because it would be easy to conflate the two. §6 (also deferred) is about **harmful communicative content** the learner might request help producing or directing — slurs, harassment, threats, coercion. This document is about a different situation entirely: **a learner disclosing that they themselves are at risk**, in the course of otherwise ordinary use — a sign of self-harm risk, abuse, or acute crisis surfacing mid-conversation. §6 is about what the product will help *say*. This is about what the product does when it learns something *true and serious* about the person it's talking to. Different triggers, different responsible responses. Keeping them separate matters so neither gets solved by accident while solving the other.

## What does NOT trigger this

Worth being explicit here, because overcorrecting would violate everything else already established about emotional safety and warmth. Practicing a difficult conversation with a mother-in-law, discouragement about a job interview, grief someone is preparing to talk about with a doctor, ordinary frustration with the product — none of this is escalation-triggering. Emotionally difficult topics are squarely Supported Use under GOV-004 §4 already. This section governs a narrower, more serious case: genuine indicators that the learner themselves may be at risk, not that the conversation they're preparing for is hard.

## Core principle

When indicators of real risk appear, the product's job changes, immediately and completely, from conversational preparation to something else: **acknowledge with genuine warmth, then point clearly toward real human help — and stop there.**

Two failure modes to avoid, both real risks in different directions:

- **Cold deflection.** A generic, clinical redirect ("I can't help with that, please contact a professional") delivered in a tone inconsistent with everything else the product has been — Sofía doesn't switch voices to deliver this. It should still sound like her, still sound like someone who cares, while being unambiguous that this is beyond what she can actually help with.
- **Overreach.** The product must never attempt to counsel, diagnose, talk someone down, or resolve the situation itself. It is not a crisis line, not a therapist, and pretending otherwise — even with good intentions — is worse than an honest redirect. This connects directly to "practice family, not replacement family" (`company/research-methodology/design-research/adopted-family-design-filter.md`): the principle that the relationship is a bridge to real support, not a substitute for it, applies with the most weight precisely at the moment it would be most tempting to overstep it.

## What the redirect should do

- Acknowledge what was actually said, briefly and warmly — not clinically, not by ignoring it and returning to the task.
- Be honest and clear that this isn't something the product can actually help with — not vague, not softened into ambiguity.
- Point toward real, specific help: a crisis line, a trusted person, a professional — appropriate to what was disclosed.
- Not require the learner to keep explaining themselves to get the redirect. One clear, warm response, not an interrogation.
- Leave the door open to return to ordinary use afterward, without penalty, without the product treating the disclosure as something to remember and reference later inside what's supposed to be a bounded utility tool.

## A real design requirement, not a detail

**Crisis resources are locale-specific, and this product's whole premise is cultural authenticity.** A single US hotline number surfaced to every learner regardless of where they are would be a real failure, not a minor gap — worth flagging clearly as an actual build requirement (resource lookup by learner locale), not something to hard-code once and forget.

## Open, unresolved, and explicitly not decided here

- Exact resource lists per locale — needs real research, not AI-generated guesses at hotline numbers or services.
- Whether any disclosure should be logged for safety-review purposes, and if so, how that's handled consistently with the warmth/surveillance boundary already flagged elsewhere in this repo (`company/research-methodology/design-research/recognition-vs-evaluation.md`).
- Exact detection approach — this document assumes the model itself is expected to recognize genuine risk indicators in context; it does not specify implementation (prompt-level instruction, a separate classifier, or something else), which is an implementation-architecture decision, not a governance one.

**Status: pending founder review, pending clinical/legal review. Not binding until both have happened.**
