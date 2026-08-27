# Document And Artifact Lifecycle

Use this reference when current business evidence must be consumed, a document may be stale, or an artifact's consumer, execution context, release state, cleanup, or old/new-version effect is unclear. It is a delivery-baseline and artifact-lifecycle guard, not generic document management.

## Consumption Proof

Before a new module or baseline-dependent implementation, consume the relevant current material rather than relying on chat memory. Identify:

```text
Read:
- current decisions, relevant design or prototype basis, current-module material, code facts, and recent affected changes

Directly used conclusions:
- ...

Background only:
- ...

Conflicts or stale material:
- ...
```

Keep this proof internal for ordinary work. State it when the user asks for a plan, review, handoff, or full evidence. Historical material is traceability, not an implementation basis, unless it is promoted back into the current effective basis.

At completion, record alignment with the consumed basis and any deliberate departure, reason, and required update. When a correction changes an authoritative statement, update the affected current decision, index, handoff, prototype basis, or verification record rather than correcting only the immediate response.

## Current And Historical Status

Keep a current source-of-truth index distinct from archived material. Current decisions contain active constraints; handoff material contains current goal and next action; changelogs explain change history; test feedback contains reproducible evidence and residual risk. A stale document should identify its status, current effective basis, reason, use rule, and last-check date. Do not delete old material while a replacement is still being confirmed.

Before implementation or a new module, consume project instruction files, the current module's actual code, and an equivalent standard module when available. Do not enter a module from chat memory alone.

Classify project governance:

- Company business system: keep current decisions, concise change history, handoff basis, and verification evidence; avoid committing routine chat transcripts and temporary plans.
- Personal or fully managed project: richer history, current status, handoff, and reproducible test feedback may live in the repository for long-term continuity, while still separating current from historical material.

Across both classes, distinguish current, historical, process, shared, temporary handoff, and verification materials. Every durable artifact needs a consumer and a current-use rule.

## Asset Classes

Classify an asset by consumer, use, required preconditions, version-control destination, release/consumption status, old-version consumers, and end state. Keep these classes distinct:

| Asset class | Purpose and lifecycle question |
| --- | --- |
| Initialization baseline | Creates a new baseline; determine when it may be corrected in place and who consumes it first |
| Migration asset | Changes an existing baseline; retain ordered preconditions, compatibility effect, and execution history |
| Cleanup asset | Removes data or assets; retain only when its authorized consumer, exact scope, and verification remain meaningful |
| Local-validation asset | Supports one local check; keep local or discard unless it protects durable behavior |
| Deployment asset | Is consumed in a controlled target environment; record environment, permissions, prior state, execution order, and release status |
| Shared-baseline asset | Is relied on by multiple people or future work; version, maintain, and supersede it explicitly |
| Long-term regression asset | Protects current effective behavior; retain according to regression value rather than temporary location or origin |

Do not merge these classes merely to reduce file count. An unreleased, unconsumed structure may be corrected in place; a released or already-consumed structure normally needs a new change asset and instructions for both new and existing consumers. Do not promote an artifact to a shared baseline until its consumer, tool, permissions, pre-state, and lifecycle are clear.

## Boundary

This reference proves consumption and classifies lifecycle. `source-arbitration-and-baseline.md` decides source conflicts and authorization facts; it does not classify asset lifecycle. Execution scope determines whether a discovery changes the current task. Do not trigger a full lifecycle review for an ordinary update whose consumer and lifecycle are already clear.
