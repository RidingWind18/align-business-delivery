# Source Arbitration And Baseline

Use this reference when current decisions, detailed design, prototype, code, configuration, source history, project conventions, similar modules, or the current task batch point in different directions. It establishes the current effective basis; it does not replace technical design or decide execution pause and continuation strategy.

## Dimension-Specific Decisions

Do not make one source answer every question.

| Source | Decides | Does not decide alone |
| --- | --- | --- |
| Latest confirmed user wording or current decision | Business goal, allowed scope, frozen or deferred rules | Existing behavior, project style, or migration cost |
| Detailed design or PRD | Target objects, states, rules, and interface intent | Whether current code already supports the target |
| Prototype or prototype basis | Page entry, visible state, interaction order, and page-flow acceptance | Backend architecture, component internals, or unseen unchanged areas |
| Code, database, configuration, logs, and source history | Existing facts, dependency impact, compatibility cost, and migration risk | A later confirmed product target |
| Project instructions and similar standard modules | Naming, placement, components, layering, comments, and verification conventions | Business-rule or page-flow changes |
| Current task or batch | What confirmed work is allowed now | Overall target completion |

Follow verified project convention ahead of generic preference. State conflicts by dimension, retain non-conflicting work, and request only the decision needed to establish the current effective basis. A confirmed future target does not put every related change into the current batch.

## Checkable Facts

When context, documents, code, schema, database records, configuration, prototypes, logs, APIs, or source history can answer a question, inspect them before offering causes or options. Internally retain:

```text
Checked:
Facts:
Conclusion:
Uncertain:
```

Keep this record concise or internal during routine work. If evidence is unavailable, name the missing source instead of replacing inspection with “probably,” “maybe,” or a list of plausible causes. A prototype marker may establish a visible page rule, but it cannot by itself create a backend validation, state, ownership, or data rule.

## Baseline Record

For standard-module or full-design work, record the applicable parts of:

```text
Current task/batch: goal, allowed changes, explicit exclusions
Effective business basis: latest decision, detailed design, open business questions
Effective UI basis: prototype source, page flow, unchanged areas
Implementation facts: code paths, data/config/runtime facts, source-history baseline
Convention basis: instructions, similar modules, local patterns
Conflict scan: conflict, decision needed, non-blocking assumption
Boundary: keep, modify, add, remove, defer
```

For a narrow change, keep only the relevant facts internally and report the concise conclusion. A calibration, external-capability output, or draft becomes part of this baseline only after it has been consumed, calibrated, or explicitly confirmed.

## Irreversible Authorization Facts

Before producing or applying an irreversible or difficult-to-recover action, establish that authorization covers all five facts:

1. Business goal.
2. Exact affected object or records.
3. Execution environment.
4. Execution mechanism.
5. Each destructive detail not already implied by the first four facts.

Authorization never expands across dimensions. Approval to clean one category does not authorize an object of unknown purpose; a confirmed target structure does not authorize a destructive migration method. When all five facts are confirmed and consistent with current facts, they authorize the specified action without repeatedly asking for the same confirmation.

This reference decides whether the facts authorize the irreversible action. `execution-scope-guard.md` owns whether work pauses, continues safely, narrows, or returns to an earlier stage; `document-and-artifact-lifecycle.md` owns the lifecycle classification of scripts and other artifacts.
