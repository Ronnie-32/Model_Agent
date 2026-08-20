---
name: architecture-design
description: Use after framing to generate and select one coherent end-to-end modeling architecture, especially when structural assumptions, task coupling, uncertainty, or decision design admit serious alternatives.
---

# Architecture Design

Read sections 4–6 of `docs/MODELING_PLAYBOOK.md` when needed.

## Generate from hinges

Identify the one or two structural choices most capable of changing the conclusion. Candidate architectures must differ at those hinges, not merely by estimator name.

- Use one candidate when the structure is clear.
- Use 2–3 when serious ambiguity exists.
- Four is a default ceiling.

For each candidate capture:

`task DAG | constructs | estimands/decisions | interfaces | assumptions | identification | uncertainty carrier | validation path | main failure | decision value | cost | paper thesis`

## Select

Compare coverage, structural fit, identification, evidence path, decision value, risk, compute/time, and paper compressibility. Use dominance/reasons, not a fabricated weighted score.

Choose one backbone. Keep at most one challenger only when it supplies independent evidence or could reverse a decision.

Create `workspace/02_design/architecture.md` with:

- selected backbone and one-sentence thesis;
- reasons alternatives lost;
- baseline and BFME modifications;
- interface contracts including uncertainty;
- validation and feasibility plan;
- expansion/return/stop conditions;
- artifact owners and routing fallback if relevant.

## Architecture review

In standard or rapid mode, prepare Solution Architecture in `review_log.md` and pause before expensive implementation. Surface the recommended choice, serious alternative, decisive assumptions, expected evidence, resource cost, and what a route change would invalidate.

## Reject

- one independent model per subquestion with no justified interface;
- solver selection before variables/objectives/constraints;
- full implementation of rejected candidates;
- “advanced” as a selection reason;
- architecture review packets that bury the decision in long prose.
