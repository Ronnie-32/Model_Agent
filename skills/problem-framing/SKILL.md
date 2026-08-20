---
name: problem-framing
description: Use at the start of a mathematical-modeling problem to turn the statement and attachments into a requirement contract, data/rule mechanism, assumption and construct registers, identification analysis, and task DAG before selecting models.
---

# Problem Framing

## Outcome

Create `workspace/00_intake/analysis_contract.md` using the template. Read sections 1–3 of `docs/MODELING_PLAYBOOK.md` only when the relevant choice is nontrivial.

## One-pass inspection

1. Read official rules, statement, addenda, and requested deliverables.
2. Inventory attachments, then inspect schemas/types before bulk content.
3. For each material task translate:

`stakeholder question -> mathematical target -> use-time information -> output -> evidence -> downstream use`

4. Reconstruct the observation/rule mechanism: unit, keys, time, repeated/hierarchical/spatial structure, missingness/censoring, regimes, support, units, selection, leakage.
5. Separate `observed | derived | latent | assumed | decision`; state identification and main failure risk.
6. Define material constructs/metrics before calculating them. Record decision role, observable basis, scale/unit/direction, aggregation/weights/thresholds, uncertainty, and blind spot.
7. Classify material assumptions and record implication, check, sensitivity, and fallback.
8. Build a task DAG and interface list. State only knowledge gaps that could change architecture or evidence.

## Data actions

Do not clean automatically. For each material transformation:

`observation -> interpretation -> action -> modeling consequence`

EDA is warranted only when it reveals structure, diagnoses an assumption, motivates architecture, or supplies later evidence.

## Exit

Framing is complete when every material verb has a target, deliverable, constraint, evidence expectation, and downstream location; model-family names are not required.

If `review_mode=standard`, prepare Problem Understanding in the review log and pause. Do not ask about routine ambiguities that a transparent assumption/scenario can resolve.

## Reject

- copying the whole statement into an artifact;
- brainstorming algorithms before defining the target;
- random splits before understanding time/entities;
- proxy metrics without a construct argument;
- unique latent estimates without identification;
- separate decomposition/data/geometry reports that duplicate the same evidence.
