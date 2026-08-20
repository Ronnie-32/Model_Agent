# Skill Router

Load one skill for the current decision. Load a second only when the first exposes a concrete dependency.

| Need | Skill |
|---|---|
| Turn a new statement and attachments into requirements, data mechanism, constructs, assumptions, identification, and a task DAG | `problem-framing` |
| Close a specific domain/method/data/citation gap with verified sources | `research-model-discovery` |
| Generate and select coherent end-to-end solution architectures | `architecture-design` |
| Formulate, code, fit, solve, simulate, and save the selected backbone | `modeling-execution` |
| Falsify central claims, audit uncertainty/feasibility, and run the integrated red team | `validation-redteam` |
| Turn verified evidence into figures, story, paper, abstract, or memo | `paper-construction` |

Typical flow:

`problem-framing -> [research if a gap exists] -> architecture-design -> modeling-execution -> validation-redteam -> paper-construction`

Do not chain-load skills for reassurance. Skills change decisions; they are not stage-completion badges.

Routing preference: Sol owns framing/architecture/synthesis; Luna owns bounded execution artifacts. If runtime routing is unavailable, continue with the current agent and record the fallback rather than pretending delegation occurred.
