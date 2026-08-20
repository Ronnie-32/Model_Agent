---
name: modeling-execution
description: Use after architecture approval to formulate and implement the selected backbone, generate reproducible structured outputs, and connect upstream estimates and uncertainty to downstream decisions.
---

# Modeling Execution

## Model contract

For each central component maintain compactly:

`requirement -> geometry -> baseline -> failure -> modification -> assumptions -> identification -> formulation -> estimation/solver -> output -> validation -> uncertainty -> downstream`

## Order of work

1. Fix the evaluation protocol and use-time information set before fitting/tuning.
2. Implement the simplest credible baseline when feasible.
3. Diagnose the specific failure that justifies a modification.
4. Define targets/estimands or decision variables, objectives, hard constraints, and risk before choosing the solver.
5. Implement the approved backbone with current-problem code; avoid generic infrastructure unless repeated use proves necessary.
6. Save central outputs as CSV/JSON/tables/figure data, plus seed/configuration where stochastic.
7. Pass intervals, samples, feasible sets, or scenarios through interfaces when uncertainty affects downstream decisions.
8. Reject or narrow a component when its failure condition is met.

## Ownership and routing

Luna high/xhigh is preferred for bounded data/code/simulation/visualization artifacts. Give each delegated artifact one owner, inputs, output path, and acceptance check. Do not duplicate architecture reasoning or let execution agents silently change constructs/assumptions.

If execution reveals a structural conflict, stop that branch and return the evidence to the Sol architecture owner. Record routing fallback when controls are unavailable.

## Handoff

When the integrated backbone and headline outputs are ready, use `validation-redteam`. In standard mode, Core Results review occurs only after primary uncertainty, feasibility, and failure boundaries are visible.

## Reject

- hyperparameter search before valid evaluation;
- console-only headline results;
- manual paper numbers;
- model stacking without unique roles;
- treating a successful solver exit as feasibility proof;
- keeping failed branches merely to show effort.
