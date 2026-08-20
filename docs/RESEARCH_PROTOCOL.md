# Research and Citation Protocol

Load this document when external facts, methods, data, software behavior, contest rules, award identities, or citations matter.

## 1. Start from a decision-relevant gap

Write:

`I need to know ____ because it could change ____.`

Generate a small native candidate set first. Research is a verification/extension layer, not a substitute for problem framing.

Valid modes:

- domain mechanism;
- method assumptions/identification;
- estimator/solver implementation;
- external data/parameter;
- validation design;
- current competition rules;
- citation support.

Do not browse to collect model names or inflate the bibliography.

## 2. Search by structure

Prefer:

`geometry + data structure + mechanism/objective/constraint + validation`

Avoid “best model for C problem,” current-contest solution sharing, or winner-paper copying. During a live contest, check the current rules before searching and exclude prohibited current-problem discussions/repositories.

## 3. Source priority

1. official rules, problem statements, agencies, standards, original papers, official package/data documentation;
2. peer-reviewed reviews, established books, university/research-institute material;
3. blogs, repositories, tutorials, and mirrors for discovery or artifact access only;
4. anonymous reposts, SEO summaries, and generated content: not evidence.

For an award paper found on a mirror or GitHub, verify the control number/designation against the official results before treating it as an award paper. A repository README is a self-claim unless independently verified.

## 4. Verify identity and content separately

Before using a source, verify as applicable:

- exact title, authors/institution, year/date, venue, DOI/stable URL;
- that the opened content supports the precise claim;
- population/context and transferability;
- whether the source is primary or repeating another source.

Search snippets are discovery aids. Never invent metadata or cite from memory. If support is weak, narrow the claim, label an assumption, use a range/scenario, or remove it.

## 5. Research artifact

When research begins, create `workspace/00_intake/source_ledger.csv` from the template. Retain only sources that change modeling or support a paper claim.

For external data/parameters record:

`publisher | retrieval date | variable | definition | unit | population/period | transformation | use | transferability | license/citation`

Keep separate:

- external evidence: `claim -> verified source`;
- project evidence: `result claim -> output -> code -> input data -> validation`.

Literature cannot replace computation the problem requires.

## 6. Research models and modifications

Compare only serious candidates on:

`assumptions | structural fit | identification | failure modes | validation | implementation feasibility | source IDs`

A problem-specific hybrid does not need a fabricated scholarly name or exact literature twin. Its components, assumptions, estimation, and evidence must be explicit.

External features must have semantic/mechanistic relevance, aligned time/entity/geography/units, provenance, and an ablation or other value check.

## 7. Efficient search budget

For one ordinary gap, start with one precise query and one broader query, inspect a handful of credible candidates, and verify the best 2–3. Search deeper only for disagreement, high-stakes uncertainty, or a niche method.

Stop when the gap is resolved enough to decide, credible alternatives are understood, central claims have verified support, conflicts are recorded, and further browsing is unlikely to change the architecture or paper.

## 8. Final citation audit

- every citation exists in the source ledger;
- identity and relevant content are verified for central claims;
- claim wording does not exceed the source;
- URLs/DOIs point to the right work;
- no decorative unused references remain;
- current disclosure and AI-use rules are satisfied.
