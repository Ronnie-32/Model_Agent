# Framework Rationale and Evidence Base

This file records why V2 differs from the previous framework. It is for framework maintenance, not routine contest loading.

## 1. Existing-framework disposition

| Area | Decision | Rationale |
|---|---|---|
| Requirement-first framing, epistemic roles, identification | KEEP | High-value protection against answering the wrong mathematical question. |
| Architecture before algorithms; cross-task DAG | KEEP | Directly supports coherent multi-question solutions. |
| BFME innovation | KEEP | Connects complexity to a falsifiable failure instead of novelty theater. |
| Research verification and claim/source separation | KEEP | Strong anti-hallucination and reproducibility discipline. |
| Risk-matched validation and uncertainty propagation | KEEP/MODIFY | Preserved, but verification now scales by claim consequence rather than a fixed count. |
| G0–G10 plus four runtime phases | MERGE | Ten named gates repeated across files and encouraged ceremonial checking; replaced by phase exit criteria and blocking defects. |
| Default three-architecture tournament | MODIFY | Candidates now arise from structural hinges; one is allowed when obvious, 2–3 when ambiguity is real. |
| Problem decomposition, data audit, problem geometry skills | MERGE | They read the same inputs and write the same analysis contract; one framing pass reduces context reload and contradiction. |
| Separate completion and quality documents | MERGE | Both repeated blocking defects, gate criteria, and stop rules. |
| Long design specification and completed implementation plan | DELETE | Historical prose duplicated runtime rules and incorrectly claimed a workspace skeleton that was absent. |
| Numeric 100-point internal rubric | DELETE | Useful dimensions were retained, but precise weights invited rubric gaming without empirical calibration. |
| Assumption and metric/construct design | ADD | Previously implicit despite being central to evaluation, risk, fairness, momentum, and C-problem work. |
| Human Review | ADD | Four configurable major checkpoints, with architecture as the primary decision pause. |
| Sol/Luna routing and effort escalation | ADD | Separates judgment-heavy work from execution while requiring honest fallback when controls are unavailable. |
| Artifact ownership/no-duplicate-agent rule | ADD | Prevents repeated multi-agent reasoning and conflicting edits. |

## 2. Evidence that changed the design

### Official COMAP expectations

COMAP describes Outstanding reports as highest-level work in modeling, solving, and communicating—not merely advanced algorithms. Its current instructions say judges primarily care about thought processes, problem analysis, modeling approaches, and mathematical methods. The Problem C Veena Mendiratta Award specifically values application orientation, usefulness, clarity, creative/effective data use, and an understandable model.

**Design consequence:** keep methodology, decision value, and paper communication co-equal; do not optimize model count.

### Official CUMCM expectations

CUMCM's national judging rules require problem-specific judging points, multiple independent reviews for top submissions, and explicit attention to outstanding innovation. Current format rules require runnable source programs and supporting data/materials that match the paper.

**Design consequence:** architecture and innovation need problem-specific evidence; code/output/paper traceability is a blocking requirement.

The official 2023 newsletter includes the undergraduate High Education Press Cup team's account of the C problem: the bottleneck was constructing meaningful indicators from 870,000 noisy sales records; the team used domain seasonality/periodicity to split effects and connect pricing/replenishment, while trying and revising several methods.

**Design consequence:** construct design and real-world mechanism deserve first-class treatment; algorithm lists are only useful when roles are distinct.

### Representative MCM Outstanding paper

Official 2024 results identify control number 2401298 as an Outstanding Winner for Problem C. The public paper operationalizes “momentum” as residual behavior beyond a memoryless/binomial baseline, connects measurement, testing, prediction, generalization, and a coaching memo, and reports visible prediction failures.

**Design consequence:** preserve baseline-residual constructs, cross-question interfaces, stakeholder translation, and failure analysis.

The same paper also assigns psychological/physiological latent states from indirect game data and makes broad generalization claims. Award status therefore does not make every modeling choice universally safe.

**Design consequence:** high-level papers are evidence for patterns, not templates; identification and claim strength must still be red-teamed.

### Recent modeling-agent research

MM-Agent decomposes open-ended modeling into problem analysis, model formulation, computational solving, and reporting, and reports that baseline agents often omit abstraction, constraints, and assumptions. ModelingAgent reports gains from specialized roles, tool use, shared memory, and critic feedback, but still identifies creativity, data reliability, domain adaptation, and structural coherence as limitations.

The public MM-Agent implementation also uses repeated actor–critic refinement and potentially many code/debug retries.

**Design consequence:** retain staged solving, tools, compact shared artifacts, and targeted critique; reject fixed repeated critique loops and duplicate agent work. Use an expected-information test before another round.

## 3. Verified sources used for V2

- COMAP, current MCM/ICM instructions and judging guidance: https://www.contest.comap.com/undergraduate/contests/mcm/instructions.php
- COMAP, designation definitions: https://www.contest.comap.com/undergraduate/contests/mcm/faq.php/instructions.html
- COMAP, 2024 results and control-number verification: https://www.contest.comap.com/undergraduate/contests/mcm/contests/2024/results/
- COMAP/Mathmodels resource index showing official problems, commentaries, and student papers: https://www.comap.org/?id=67&view=article
- CUMCM national award judging rules (2023 revision): https://www.mcm.edu.cn/html_cn/node/b1f48689659f0660e80a2d6279d7b37d.html
- CUMCM paper/supporting-material format rules (2026 revision): https://www.mcm.edu.cn/html_cn/node/4cd596519c9eb9fbd866398f6df0caa3.html
- CUMCM 2023 newsletter and named-prize team account: https://www.mcm.edu.cn/upload_cn/node/710/sLP3Yqqke0a723489510b62852fe6956188c65cb.pdf
- “农作物的种植策略”赛题评述, DOI 10.19943/j.2095-3070.jmmia.2025.02.04: https://qxyy.cbpt.cnki.net/portal/journal/portal/client/paper/1c39675be244c2c0d22b0be695b89eaf
- Public copy of MCM 2024 C paper 2401298 (designation verified separately above): https://reformship.github.io/pages/3competition/4mcm/MCM%20Outstanding/2024/C/2401298.pdf
- MM-Agent paper and implementation: https://arxiv.org/abs/2505.14148 and https://github.com/usail-hkust/LLM-MM-Agent
- ModelingAgent paper: https://aclanthology.org/2025.findings-emnlp.85/

## 4. Evidence boundary

COMAP's full student-paper/commentary library may require membership, and many public CUMCM paper copies do not independently establish national-award status. V2 therefore does not claim to have exhaustively read every winning paper or to reproduce an official universal scoring rubric. It retains only patterns supported by opened primary/official materials or award papers whose identity was independently verified.

## 5. Light dry-run

Two representative prompts were routed through the V2 decision logic without fitting models or reproducing full papers.

| Problem | Structural hinge found | Candidates generated | Backbone selected | Risk-matched validation | Anti-bloat result |
|---|---|---|---|---|---|
| MCM 2024 C, tennis momentum | Score advantage vs a distinct latent/residual state; match-level dependence; prediction vs explanation | (A) memoryless score baseline plus residual momentum state; (B) direct win-probability predictor without a momentum construct | A only if the residual construct is stable and improves held-out, match-grouped prediction; otherwise B and an explicit “no separable momentum” conclusion | Point/order-preserving null tests, grouped temporal holdout, calibration, ablation of the momentum state, boundary on psychological interpretation | Prevented treating score runs as proof of momentum and prevented adding a latent layer without incremental evidence. |
| CUMCM 2024 C, crop planning | Deterministic plan vs scenario/stochastic or robust decision under yield, price and demand uncertainty | (A) deterministic MILP baseline; (B) scenario stochastic extension; (C) robust extension for poorly estimated ranges | A as the auditable feasibility baseline; promote B or C only if replay/stress tests materially change allocations or downside risk | Constraint audit, benchmark solution, scenario replay, parameter sensitivity and decision-stability map | Produced one optimization spine instead of separate forecast, evaluation and optimization model stacks. |

The dry-run exposed one needed adjustment that is now in the templates: constructs and assumptions require explicit registers before architecture selection, and architecture candidates are optional rather than a fixed three-model tournament.
