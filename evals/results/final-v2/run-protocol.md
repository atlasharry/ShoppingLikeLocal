# Final-v2 run protocol

Eight fresh-context solver agents were run, one case per agent, with at most two solvers active at once. They received only the skill path, a single extracted case with shared synthetic-data notice and offline environment, output location, and this execution instruction. No rubric, expected answer, or design history was sent to the solvers.

```text
Use the skill at <repository-root>/SKILL.md to answer the one realistic user request and supplied materials in <isolated-inputs>/<case-id>.json. This is a strictly offline simulation: no web/network, no browser/UI, no account actions, no contacting anyone, no purchasing. Read the skill and only the relevant references it points to; do not inspect other cases, evaluations, expected answers, grading files, prior outputs, or design history. The input includes the full permitted raw materials. Write your exact Chinese user-facing answer to <isolated-answers>/<case-id>.md. Complete that answer using the supplied evidence and acknowledge uncertainties where needed. Do not edit skill files. Return only a brief completion message with the output path.
```

The placeholders replace local absolute filesystem paths only; the instruction wording is otherwise the one dispatched. Input extraction preserves each source case and adds the source file's shared `data_notice` and `default_environment`. Source hashes and canonicalization are in `manifest.json`. Answers were copied byte-for-byte after completion. Skill and reference hashes were checked before and after the runs.

The coordinator prepared the private rubric and separate numerical recomputations, then graded each answer only after that answer had been saved. No grading feedback was returned to solvers. Grading is version-aware, not blind. Exact model settings are unavailable. See `grading.json`, `run-metadata.json`, and `run-events.json` for constraints and observations.
