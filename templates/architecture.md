# Solution Architecture

## 1. Modeling thesis

State in one paragraph how the observations arise, what must be inferred or decided, and how the sub-questions form one chain.

## 2. Structural hinges

List only choices that materially change the solution, such as:

- deterministic vs stochastic;
- aggregate vs hierarchical;
- direct prediction vs latent-state estimation;
- one regime vs segmented regimes;
- static plan vs state-dependent policy;
- point estimate vs feasible set / posterior / scenario set.

## 3. Candidate architectures

Generate one default candidate. Add a second or third only for a genuine structural hinge.

| Candidate | Backbone and coupling | Strength | Dominant failure risk | Decisive test | Decision value | Verdict |
|---|---|---|---|---|---|---|
| A |  |  |  |  |  |  |

## 4. Selected backbone

- Selected architecture and reason:
- What is intentionally excluded:
- Identification statement:
- Simplest adequate baseline:

## 5. BFME modification record

| Requirement | Baseline | Named failure | Modification | Evidence that could justify it | Revert condition |
|---|---|---|---|---|---|
|  |  |  |  |  |  |

## 6. Cross-task interface contracts

| Stage | Input | Output | Unit / schema | Uncertainty | Consumer | Acceptance check |
|---|---|---|---|---|---|---|
|  |  |  |  |  |  |  |

## 7. Formulation and execution map

For each central component record:

`requirement -> assumptions -> variables -> formulation -> estimation / solver -> output -> validation -> downstream`

| Component | Variables / objective / constraints | Estimator / solver | Owner and suggested route | Artifact |
|---|---|---|---|---|
|  |  |  |  |  |

## 8. Risk-matched validation plan

| Claim / decision | Consequence | Dominant uncertainty | Verification | What result would change the architecture? |
|---|---|---|---|---|
|  |  |  |  |  |

## 9. Architecture review packet

- Recommended backbone:
- Why it is simpler and more complete than the serious alternative:
- Key assumptions and constraints:
- Expected innovation and its BFME rationale:
- Main unresolved risk:
- Explicit decision requested (standard / rapid mode):

## 10. Expansion and return rules

- Add a model only if it closes a requirement, repairs observed failure, resolves identification, improves a decision materially, or provides independent evidence.
- Return to framing only if new evidence changes the generating structure, identification or requirement map.
- Stop candidate generation once one backbone is adequate and the serious alternative has no plausible decision advantage.
