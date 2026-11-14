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

Before choosing a mechanism, connect it to a confirmed requirement, applicable agreement, or inspected existing behavior. An assistant's earlier plan or claim of necessity is not evidence of a requirement. When the user rejects a mechanism, inspect what the original path already does and withdraw dependent additions whose only basis was that mechanism; retain independently required behavior and valid later changes. For restoration or a minimal delta against a named base, compare code structure as well as results; leave unrelated code unchanged.

When a consequential claim is called "confirmed," trace its adoption and applicability, not just its latest citation. Several documents repeating or citing an assistant's proposal are not independent confirmation. A demo, rehearsal, or other-environment value stays in that context until adopted for the target; preserve unchanged target identifiers when only another dimension was authorized to change. Inspect the relevant origin or report the precise evidence gap before propagating the claim across artifacts.

## Checkable Facts

When context, documents, code, schema, database records, configuration, prototypes, logs, APIs, or source history can answer a question, inspect them before offering causes or options. Internally retain:

```text
Checked:
Facts:
Conclusion:
Uncertain:
```

Keep this record concise or internal during routine work. If evidence is unavailable, name the missing source instead of replacing inspection with “probably,” “maybe,” or a list of plausible causes. A prototype marker may establish a visible page rule, but it cannot by itself create a backend validation, state, ownership, or data rule.

Match each conclusion to the object, source version, environment, and coverage actually inspected. For a different or broader target, inspect that target or keep the broader claim unverified. An empty search establishes only that the search found no match; check the path or matching method before treating it as absence.

When repairing a migrated or copied feature, inspect the reachable source implementation and the target call path before inventing a new contract. Passing tests for a newly invented path does not prove that it matches the existing source contract.

Before excluding a cause, check whether the evidence exercises the disputed step in the applicable version. A prepared object or downstream-only test cannot establish the correctness of the acquisition, query projection, mapping, or state transition it bypasses. When observed data contradicts the expected flow, inspect that affected boundary before sending the user to broader historical investigation. Keep technical diagnosis with the appropriate specialist; this is an evidence-coverage check, not a mandatory full-system trace.

For an unusual sequence or concurrency concern, trace roles, page and API entries, required states, real callers, and existing guards. Business prohibition, absence of a normal UI path, and an enforced server guard are different evidence. Exclude unsupported product assumptions without creating a new business decision from a technically constructible request. Close the defect concern only when evidence shows no actionable consequence or effective protection contains it. If an actually callable interface has a reproducible authorization or consistency defect, report it even without a normal UI path; keep protection within the authorized invariant and ownership rather than redesigning the product. Ask the user only when resolution needs a genuine business choice; findings outside the current batch follow the review-finding gate in `execution-scope-guard.md`.

## Previously Verified Methods

For a repeated operation, proactively find the relevant project agreement, actual prior artifact, and validation basis; the user need not name them again. Search the task's entry/index, related procedure or module, and relevant history as needed, not all project history. Check whether the goal, environment, structure, and critical preconditions still apply. If so, reuse the method, table or component boundary, operating sequence, artifact destination, and acceptance approach; adapt only target parameters and demonstrated scenario differences. Reuse is not evidence that new target data was checked or that execution is authorized. Revalidate changed preconditions and target facts without making the user re-prove unchanged logic. If the prior basis is inaccessible or materially conflicts, identify that specific gap rather than presenting a replacement as the established method.

Finding another table, an optional safeguard, or a candidate improvement does not itself invalidate the method or authorize adding it. When it is genuinely inapplicable, identify the concrete difference and adjust only that part; preserve valid work. Compare the complete increment with the adopted basis before delivery or after a scope correction, not just the statement that last failed. Keep the operational handoff usable in the receiver's actual working conditions.

Judge simplification by clear business responsibilities and lower operator effort, not statement, method, or file counts. Preserve each operation's own preconditions; share them only when genuinely common. Consistency does not require forcing distinct operations into one statement or abstraction, nor does separation alone prove a safer result.

When replacing a manual operation with a feature, preserve its confirmed observable outcome while adapting authorization, transactions, and failure handling through existing project mechanisms. A reusable business result does not require copying manual SQL literally or inventing a new permission scheme, abstraction, or page.

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
