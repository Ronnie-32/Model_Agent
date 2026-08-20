# Modeling Playbook

Load only the section needed for the current decision. This is a reasoning guide, not a catalog of algorithms.

## 1. Frame the real task

Translate each requirement into:

`stakeholder question -> mathematical target -> information available at use time -> output -> evidence -> downstream use`

Then determine the geometry: description, estimation, prediction, classification, ranking, latent/inverse inference, first-passage, mechanism analysis, optimization, policy, or counterfactual. One natural-language question may contain more than one geometry.

Reconstruct how observations arose:

- unit and key;
- time order and decision time;
- repeated/nested/spatial/network structure;
- measurement process, censoring, missingness, and selection;
- regime or rule changes;
- algebraic support and hard constraints.

This generating structure determines admissible splits, likelihoods, features, and claims.

## 2. Design assumptions deliberately

Use the fewest assumptions needed to make the target answerable. Classify material assumptions:

| Type | Question |
|---|---|
| Definitional | What exactly does the target or construct mean? |
| Structural | What dependence, mechanism, or invariance is imposed? |
| Measurement | How do observations relate to the underlying quantity? |
| Behavioral/domain | What actions or rules are presumed? |
| Computational | What approximation is introduced to make solving feasible? |

For each material assumption record:

`reason -> implication -> observable consequence/test -> decision sensitivity -> fallback if false`

Do not use “for simplicity” as a complete justification. A convenience assumption that changes the answer needs a scenario or sensitivity check.

## 3. Construct variables and metrics

Vague concepts such as risk, momentum, fairness, resilience, attractiveness, difficulty, or sustainability are modeling decisions. Before calculating them, create a compact construct card:

`construct | decision role | observable basis | unit/scale/direction | mechanism | aggregation | weights/thresholds | uncertainty | known blind spot`

Prefer a domain/mechanism baseline and model the deviation when the construct is inherently relative. Keep distinct meanings separate; do not compress outcome, exposure, and vulnerability into one score unless the decision truly requires it.

Check:

- scale and units are meaningful;
- transformations preserve support;
- weights and thresholds have domain, statistical, or decision justification;
- aggregation does not hide decisive subgroup/regime behavior;
- the metric changes when the intended construct changes and stays stable under irrelevant changes;
- uncertainty in inputs can reach the final decision.

For composite evaluation, report component results and trade-offs before a single ranking. Sensitivity to normalization and weights is mandatory when rankings drive recommendations.

## 4. Generate candidate solutions by structural hinges

Do not create candidates by swapping algorithms. First locate the structural hinges that could reverse the conclusion, for example:

- global process vs regime/subgroup process;
- point prediction vs distribution/scenario set;
- direct prediction vs latent/state or first-passage representation;
- unconstrained forecast-then-decide vs joint or robust decision model;
- unique estimate vs feasible-set/partial identification;
- static policy vs state-dependent policy.

Create one architecture if no serious hinge remains. Otherwise create 2–3 end-to-end alternatives that make different choices at these hinges.

Each architecture must specify:

`task DAG | constructs | estimands/decisions | interfaces | assumptions | identification | uncertainty carrier | validation path | main failure | decision value | cost | paper thesis`

Reject a candidate if it cannot be tested with available evidence, violates the use-time information set, or is dominated by a simpler architecture.

## 5. Select and innovate

Select architecture before model details. Compare qualitatively; weighted scoring often adds arbitrary precision.

Use BFME for every retained modification:

1. **Baseline** — simplest credible/domain-native solution.
2. **Failure** — observed or strongly expected problem-specific defect.
3. **Modification** — smallest structural change that targets the defect.
4. **Evidence** — ablation, calibration, recovery, feasibility, or decision improvement that could reject the modification.

Innovation may come from representation, construct definition, constraints, objective, model coupling, uncertainty, scenarios, validation, or explanation. A fashionable estimator without a diagnosed failure is not an innovation.

## 6. Build an integrated C-problem spine

Common C-problem chains are useful as motifs, not templates:

- `data mechanism -> construct/estimate -> forecast/distribution -> risk -> constrained decision`;
- `state construction -> dynamics -> event/turning point -> intervention policy`;
- `latent/feasible-set inference -> rule replay -> evaluation metrics -> mechanism redesign`;
- `demand/cost estimation -> uncertainty scenarios -> inventory/pricing/allocation optimization`;
- `classification probability + asymmetric error cost -> threshold policy -> operational recommendation`.

Every arrow is an interface contract. Record the quantity, unit, indexing, uncertainty representation, and consumer. Do not silently replace a distribution with a point estimate or an estimated association with a causal effect.

If later tasks do not actually need an earlier result, do not force artificial coupling. Coherence means justified flow, not reuse for its own sake.

## 7. Validate what could change the conclusion

Start from the claim, not a checklist:

`claim -> consequence if wrong -> dominant uncertainty/failure -> falsification test -> response to failure`

Examples:

| Geometry | Primary concern | Credible evidence |
|---|---|---|
| Forecast | future leakage/nonstationarity | naive baseline + walk-forward or blocked backtest |
| Repeated data | entity dependence/leakage | group-aware split or hierarchical residual check |
| Inference | misspecification/unstable estimand | residual diagnostics + specification/interval analysis |
| Latent/inverse | nonidentification | feasible set, recovery simulation, or assumption bounds |
| Classification | asymmetric error/calibration | class-cost metrics, calibration, threshold sensitivity |
| Optimization | infeasibility/weak benchmark | explicit constraint audit + bound/exact-small-case/baseline policy |
| Policy/counterfactual | unsupported intervention effect | replay, paired simulation, placebo/negative control when valid |
| Uncertain decision | unstable recommendation | propagate samples/scenarios and map the stability region |

Use independent checks for decision-critical claims when feasible. Independent means a different failure mechanism, not the same metric under another seed.

When a test fails, weaken the claim, change the model, or expose an operating boundary. Do not relabel failure as “robustness analysis.”

## 8. Interpret and visualize

Interpret outputs in four layers:

1. numerical result and uncertainty;
2. mechanism or pattern supported by evidence;
3. decision implication and trade-off;
4. boundary where the implication may fail.

Before making a figure/table, write a one-line brief:

`reader question -> evidence shown -> comparison/uncertainty encoded -> intended takeaway`

Retain a visual only if it serves structure, diagnosis, comparison, uncertainty, or decision. Prefer direct labels, shared scales, visible units, uncertainty bands/scenarios, and decision thresholds. Do not use a heatmap, network, 3D chart, or dashboard merely to look sophisticated.

## 9. Build the paper story from evidence

The final paper exposes the winning architecture, not the whole search tree.

Write a one-sentence thesis that connects all questions. Then use:

`question -> structural insight -> model choice -> quantitative result -> falsification/uncertainty -> direct answer -> link forward`

Allocate page space by claim importance and risk. Put routine derivations, diagnostics, and large tables in appendices/supporting files when rules permit. The abstract/summary must state the problem, unified method, headline quantitative results, validation, and final decision—not a list of model names.

## 10. Failure patterns

- keyword-to-model routing;
- disconnected mini-papers for each question;
- arbitrary composite weights or decision thresholds;
- causal claims from correlation, SHAP, or feature importance;
- random splits for temporal/entity-dependent data;
- solver names used instead of variables/objectives/constraints;
- feasible-looking solver output without constraint verification;
- latent variables named but not identified or measured;
- synthetic data that violate support or leak into evaluation;
- uncertainty confined to a decorative final section;
- repeated actor-critic/review loops without a named unresolved risk;
- paper prose containing numbers that do not exist in structured outputs.
