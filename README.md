# Competition Modeling Agent Framework V2

A compact, methodology-first Codex framework for COMAP MCM/ICM and CUMCM, with special attention to data, prediction, evaluation, optimization, mechanism, and decision-oriented C problems.

It is designed to improve decisions about **what to model and why**. It intentionally does not ship a model encyclopedia, a mandatory algorithm toolkit, or a long historical-paper archive.

## Start a project

1. Put the official statement in `problem/` and supplied files in `problem/attachments/`.
2. Start Codex at this repository root.
3. State the competition, deliverables, time constraints, and desired review mode.

Example:

> Solve the supplied problem under this repository's AGENTS.md. Use standard human review, so pause only at Problem Understanding, Solution Architecture, Core Results, and Final Story. Between checkpoints work autonomously.

For uninterrupted execution, explicitly request `review_mode=autonomous`.

## Runtime shape

`UNDERSTAND -> DESIGN -> EXECUTE -> DELIVER`

- UNDERSTAND: requirement closure, data/rule mechanism, constructs, assumptions, identification, task DAG.
- DESIGN: targeted research, structurally distinct candidate architectures, backbone selection, BFME plan.
- EXECUTE: reproducible code/results, risk-matched validation, uncertainty propagation, integrated red team.
- DELIVER: claim-evidence map, analytical story, figures/tables, paper, final audit.

## Directory map

```text
AGENTS.md                         always-on control plane
docs/
  MODELING_PLAYBOOK.md            conditional methodology
  RESEARCH_PROTOCOL.md            external evidence rules
  QUALITY_AND_STOP.md             readiness and stopping
  FRAMEWORK_RATIONALE.md          audit and evidence provenance
skills/INDEX.md                   skill router
skills/*/SKILL.md                 six stage capabilities
templates/                        compact reusable artifacts
problem/                          official statement and attachments
workspace/                        current-problem work products
```

## Design principle

`maximum modeling quality per token`

The framework preserves decisions, interfaces, evidence, and unresolved risks—not duplicated reasoning transcripts.
