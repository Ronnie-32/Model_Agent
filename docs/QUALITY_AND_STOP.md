# Quality, Red-Team, and Stop Standard

Use this document when judging readiness, deciding whether to continue, or running the integrated red team. It intentionally avoids a 100-point score: precise weights invite rubric gaming and obscure blocking defects.

## 1. Blocking defects

Any unresolved item blocks competition-ready status:

1. a material requirement has no direct answer;
2. a central number, citation, dataset, or award claim is fabricated or untraceable;
3. target, time, entity, or preprocessing leakage invalidates evaluation;
4. the observation unit or dependence structure is materially wrong;
5. a latent/nonidentified quantity is reported as uniquely known;
6. correlation, feature importance, or prediction is presented as causal without identification;
7. a recommendation violates a hard constraint or is not operationally defined;
8. optimization lacks objective/constraint consistency and feasibility checks;
9. `optimal`, `best`, or `robust` is stronger than solver/benchmark/stress evidence;
10. weights, thresholds, quantiles, or scenarios that control the decision are arbitrary and untested;
11. support is violated (negative counts, invalid probabilities, compositions not summing correctly, impossible states);
12. headline outputs cannot be reproduced from current code and data;
13. paper, code, figures, and structured outputs disagree;
14. competition format, disclosure, anonymity, or supporting-material rules are violated.

Fix the earliest broken structural decision. Do not hide a defect by adding a later model.

## 2. Phase exit criteria

### UNDERSTAND is complete when

- every material verb maps to a target, output, evidence, and downstream use;
- data/rule mechanism and use-time information are understood;
- observed, derived, latent, assumed, and decision quantities are separated;
- construct definitions and material assumptions are explicit;
- identification and dominant failure risk are known;
- the task DAG is coherent.

### DESIGN is complete when

- structural hinges are explicit;
- serious end-to-end alternatives were considered without algorithm-list padding;
- one backbone is preferred over a simpler serious alternative for stated reasons;
- baseline, BFME modifications, interfaces, uncertainty carrier, and validation path exist;
- the architecture can produce every required decision/output with available evidence and compute.

### EXECUTE is complete when

- current code regenerates headline results;
- evaluation precedes tuning and respects time/entities;
- hard constraints and units are verified;
- material uncertainty flows through interfaces;
- central claims survive risk-matched falsification or are narrowed;
- the final recommendation is feasible and its stability/failure region is known;
- one integrated red team has no unresolved blocking defect.

### DELIVER is complete when

- `claim_evidence.csv` covers every headline result and recommendation;
- every retained visual has one evidence role;
- the paper tells one coherent architecture and directly answers all tasks;
- no new quantitative result was invented during drafting;
- citations come only from verified ledger entries;
- the final audit passes current competition rules.

## 3. Proportional verification

Classify claims by consequence, not by model prestige:

- **Integrity**: file parsing, units, keys, arithmetic, constraints. Verify deterministically.
- **Supporting**: descriptive pattern that does not control a decision. One fit-for-purpose check is usually enough.
- **Central**: inference/prediction that supports a headline conclusion. Use a primary falsification test matched to the dominant risk.
- **Decision-critical**: a claim whose failure changes policy, allocation, ranking, safety, or feasibility. Add an independent check and propagate uncertainty to the decision.

Extra tests require a named unresolved risk and a plausible change to a claim or decision.

## 4. Integrated red team

Run once after the full task chain is substantially complete. Attack:

- omitted requirement or hidden deliverable;
- wrong granularity, time order, hierarchy, or information set;
- false identification or causal overreach;
- construct that does not measure what the paper claims;
- arbitrary weights/thresholds/scenarios;
- evaluation protocol mismatch;
- small-sample complexity and unstable selection;
- impossible predictions or synthetic support;
- optimization feasibility, benchmark, and solver guarantee;
- uncertainty lost at a task interface;
- forecast metric used as proof of policy quality;
- cross-question definitions/units/results that conflict;
- final decision that is not actionable;
- paper/code/source contradiction.

Record only material failures and their resolution. Do not generate a long critique transcript.

## 5. Continue, return, or stop

**Continue** when a missing action could materially close a requirement, resolve identification, falsify a central claim, establish feasibility, change a decision, or repair traceability.

**Return** to the earliest affected phase when new evidence breaks the observation mechanism, construct, assumption, architecture, or decision interface.

**Stop expansion** at evidence saturation when:

- all requirements are closed;
- the backbone survives serious structural alternatives;
- hard constraints and critical interfaces are verified;
- headline claims have consequence-matched evidence;
- material uncertainty is represented downstream;
- decision boundaries/failure cases are characterized;
- numbers and sources are traceable;
- another model, search, review, or plot has negligible chance of changing the result.

Compression, formatting, and compliance checks may continue after model expansion stops.

## 6. Anti-loop rules

Do not automatically:

- reread the full problem after the analysis contract is stable;
- generate exactly three architectures when only one or two are serious;
- run fixed actor-critic rounds on already accepted work;
- ask several agents for the same solution;
- rerun unchanged code or equivalent plots;
- tune after the decision is stable;
- perform a second full red team without new contradiction;
- rewrite prose before evidence changes;
- browse for additional references after the knowledge gap is closed.

The controlling question is:

> What new information will this action produce, and which material claim or decision could it change?
