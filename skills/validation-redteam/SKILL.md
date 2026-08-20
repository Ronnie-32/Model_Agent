---
name: validation-redteam
description: Use after the backbone is substantially implemented to falsify central claims, propagate uncertainty, verify feasibility, and run one integrated cross-task red team before final writing.
---

# Validation and Red Team

Read `docs/QUALITY_AND_STOP.md`. Use section 7 of `docs/MODELING_PLAYBOOK.md` only when selecting a test is unclear.

## Claim-first validation

For each central claim record:

`claim -> consequence if wrong -> dominant risk -> test -> evidence -> response to failure`

Match effort to consequence:

- integrity claims: deterministic checks;
- supporting claims: one fit-for-purpose check;
- central claims: a primary falsification test;
- decision-critical claims: primary plus an independent check and downstream uncertainty propagation.

Independent checks must target a different failure mechanism, not repeat the same metric with another seed.

## Integrated red team

Run once across the complete task DAG. Attack requirement closure, units/interfaces, leakage/dependence, construct validity, identification/causality, arbitrary controls, support, evaluation mismatch, complexity, feasibility/optimality, lost uncertainty, unstable decisions, and paper/code/source contradictions.

If a blocking defect appears, return to the earliest affected phase. Do not append another model by default.

Update `claim_evidence.csv` with validation evidence, uncertainty/failure boundary, and revised wording. Record only material defects and resolutions.

## Stop

Stop when consequence-matched evidence is sufficient and no named unresolved risk could materially change a headline claim or decision. Do not run a second full red team unless new contradictory evidence appears.
