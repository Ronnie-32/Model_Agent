# AGENTS.md — Competition Modeling Agent Framework V2

## Mission

Solve MCM/ICM and CUMCM problems as one evidence-to-decision system:

`Problem -> Structure -> Evidence -> Candidate architectures -> Selection -> Execution -> Validation -> Insight -> Communication`

Optimize modeling quality per token. This repository is a methodology harness, not a model encyclopedia.

## Non-negotiables

1. Treat the statement as a specification: every material verb needs a visible answer and evidence.
2. Reconstruct the observation/rule mechanism before choosing algorithms.
3. Separate `observed | derived | latent | assumed | decision` quantities.
4. State identification before estimation. Report a range, feasible set, or assumption-dependent result when that is all the evidence supports.
5. Define constructs, metrics, objectives, and constraints before selecting estimators or solvers.
6. Select one coherent cross-question backbone. Supporting models must have distinct roles.
7. Prefer the simplest complete architecture that survives credible falsification.
8. Innovation follows `Baseline -> Failure -> Modification -> Evidence` (BFME); complexity alone is not innovation.
9. Prediction, explanation, causality, and decision are different claims and require different evidence.
10. Propagate material upstream uncertainty into downstream recommendations.
11. Save important results structurally; never invent paper numbers while writing.
12. Match claims to evidence. Do not use `causal`, `optimal`, `best`, or `robust` beyond the actual guarantee.

## Runtime

### 0. Start narrowly

- Read the official problem and supplied attachments once; inspect file types before bulk extraction.
- Read `skills/INDEX.md`, then load only the skill needed now.
- Determine competition rules, allowed sources, deliverables, time budget, and `review_mode`.
- Do not preload all docs, historical papers, or skills.

### 1. UNDERSTAND

Use `problem-framing` to create `workspace/00_intake/analysis_contract.md` containing:

- requirement contract;
- data/rule-generating structure and leakage risks;
- epistemic map and identification status;
- assumption and construct registers;
- task DAG and downstream interfaces;
- explicit knowledge gaps.

Exit when the target, evidence obligation, and main failure risk of every material task are clear. In `standard` review mode, issue **Review 1 — Problem Understanding**.

### 2. DESIGN

- Research only stated gaps; use `research-model-discovery` and the research protocol when external facts, data, methods, or citations matter.
- Identify the one or two structural hinges that could change the whole solution.
- Generate one architecture when the structure is obvious; otherwise compare 2–3 genuinely different end-to-end architectures. Four is a hard default ceiling.
- Compare by requirement coverage, structural fit, identification, evidence path, decision value, failure risk, implementation cost, and paper compressibility. Do not use fake weighted scores.
- Select one backbone, define its baseline, BFME modifications, interfaces, validation plan, and stop/return conditions in `workspace/02_design/architecture.md`.

In `standard` or `rapid` review mode, issue **Review 2 — Solution Architecture** and pause. This is the highest-value human checkpoint; do not begin expensive implementation before it is resolved.

### 3. EXECUTE

- Implement the backbone, not the rejected search tree.
- Establish evaluation protocols before fitting or tuning.
- Save code, seeds/configuration, structured outputs, and figure-ready data under the workspace.
- Validate in proportion to the consequence of each claim and its dominant uncertainty.
- Run one integrated red-team pass only after the cross-question chain is substantially complete.
- Return to the earliest broken structural decision, rather than appending another model.

In `standard` review mode, issue **Review 3 — Core Modeling Results** after headline results, uncertainty, feasibility, and failure boundaries are available.

### 4. DELIVER

- Build `workspace/05_results/claim_evidence.csv` before final prose.
- Form the paper story as `question -> structural insight -> model -> evidence -> decision` and map each retained figure/table to one claim.
- In `standard` or `rapid` review mode, issue **Review 4 — Final Analytical / Paper Story** before polishing the final paper.
- Draft from verified artifacts using `paper-construction`; run one final audit in `workspace/07_paper/final_audit.md`.

## Human Review

Set one mode in the analysis contract:

- `standard` (default for a live competition): all four reviews;
- `rapid`: Solution Architecture and Final Story only;
- `autonomous`: no scheduled pause, used only when the user explicitly requests uninterrupted completion.

Use `templates/review_log.md`. Each checkpoint must fit on a compact screen and state: decision needed, recommended choice, evidence, serious alternative, unresolved risk, and consequence of changing course.

Between checkpoints, work autonomously. Ask early only when new evidence would materially change the agreed backbone, a critical assumption, competition compliance, or authorization. Never request approval for routine subtasks.

## Model and Agent Routing

Routing is guidance, not a claim that the runtime exposes controls it does not have.

- Prefer **GPT-5.6 Sol high/xhigh** for problem interpretation, decomposition, architecture, model selection, innovation judgment, difficult mathematics, final interpretation, and paper storyline.
- Prefer **Luna high/xhigh** for data audit/cleaning, EDA, coding, fitting, simulation, numerical experiments, sensitivity, visualization, and routine debugging.
- Escalate dynamically: Sol `medium/high -> xhigh -> max only for a named unresolved difficulty`; Luna `high -> xhigh -> max only when necessary`.
- If model/effort routing is unavailable, the current agent performs the role and records `routing_fallback`; never imply a delegation occurred.
- Delegate only a bounded artifact with a clear owner and acceptance check. Do not ask multiple agents to redo the same reasoning. Architecture and final synthesis retain one Sol owner; execution agents consume the approved contract and write non-overlapping outputs.

## Verification Rule

For every nontrivial verification, write mentally or in the relevant artifact:

`uncertainty/failure risk -> test -> evidence -> claim or decision that could change`

Skip a test when this mapping is empty. Decision-critical claims normally need a primary falsification test plus an independent check; ordinary low-consequence claims may need only integrity checks.

## Knowledge and Context

- `docs/MODELING_PLAYBOOK.md`: load the relevant section for assumptions, metrics, architecture, validation, visualization, or paper narrative.
- `docs/RESEARCH_PROTOCOL.md`: load before external research/citations/data.
- `docs/QUALITY_AND_STOP.md`: load for red-team, readiness, disputed quality, or stop/return decisions.
- `docs/FRAMEWORK_RATIONALE.md`: provenance and framework-maintenance rationale; not routine contest context.

Use native knowledge to generate candidates, verified research to close gaps, and current-problem evidence to select and justify. Search by geometry/mechanism/objective, never by “winning model for the current problem.” Respect live-contest integrity rules.

## Minimal Artifacts

Required for a normal full solution:

1. `workspace/00_intake/analysis_contract.md`
2. `workspace/02_design/architecture.md`
3. actual code plus structured outputs
4. `workspace/05_results/claim_evidence.csv`
5. `workspace/07_paper/final_audit.md`

Add `source_ledger.csv` only when external research/citations are used. Add `review_log.md` when reviews are enabled. Additional artifacts must remove a real coordination, reproducibility, or evidence risk.

## Stop Rule

Stop expanding models, searches, reviews, or plots when all material requirements are closed, the backbone remains defensible against serious alternatives, hard constraints and key interfaces are verified, decision-relevant uncertainty is represented, headline claims survive risk-matched checks, critical numbers/sources are traceable, and another action is unlikely to change the conclusion.

Methodology is strict; execution is light.
