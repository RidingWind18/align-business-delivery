# Document And Artifact Lifecycle

Use this reference when current business evidence must be consumed, a document may be stale, or an artifact's consumer, execution context, release state, cleanup, or old/new-version effect is unclear. It is a delivery-baseline and artifact-lifecycle guard, not generic document management. When the project lacks a usable documentation system or the user asks what documents should exist, use `documentation-baseline-diagnosis.md` first.

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

Keep this proof internal for ordinary work. State it when the user asks for a plan, review, handoff, or full evidence. Consumption means the artifact or next action follows the applicable conclusions, not merely that a file was opened or cited. Historical material is not automatically the implementation basis; an inspected, previously verified method may be adopted after the applicability check in `source-arbitration-and-baseline.md`, without reopening unrelated history.

At completion, record alignment with the consumed basis and any deliberate departure, reason, and required update. When a correction changes an authoritative statement, update the affected current decision, index, handoff, prototype basis, or verification record rather than correcting only the immediate response.

For a meaningful change to behavior, contracts, or persistent structure, use [Change-To-Document Mapping](documentation-baseline-diagnosis.md#change-to-document-mapping) to identify the affected authorities. Use that mapping alone, not a full documentation diagnosis; it does not authorize extra writes or updates to unaffected documents.

## Current And Historical Status

Keep a current source-of-truth index distinct from archived material. Current decisions contain active constraints; handoff material contains current goal and next action; changelogs explain change history; test feedback contains reproducible evidence and residual risk. A stale document should identify its status, current effective basis, reason, use rule, and last-check date. Do not delete old material while a replacement is still being confirmed.

When a checkpoint conflicts with a later applicable closure or verified artifact, reconcile the affected item before asking the user to repeat completed work. Update the existing current-status entry when document maintenance is authorized; otherwise report the precise stale statement. Use the project's current-state location, not another parallel ledger. This is targeted recovery, not a new documentation audit.

Before implementation or a new module, consume project instruction files, the current module's actual code, and an equivalent standard module when available. Do not enter a module from chat memory alone.

Classify project governance:

- Company business system: keep current decisions, concise change history, handoff basis, and verification evidence; avoid committing routine chat transcripts and temporary plans.
- Personal or fully managed project: richer history, current status, handoff, and reproducible test feedback may live in the repository for long-term continuity, while still separating current from historical material.

Across both classes, distinguish current, historical, process, shared, temporary handoff, and verification materials. Every durable artifact needs a consumer and a current-use rule.

## Operational Handoff Usability

For an instruction or handoff document, establish how it will actually be used: the reader, action owner, and eventual communication recipient may differ. A user's private talking points are not automatically a document sent intact to an external party. Derive responsibilities from confirmed context; keep consequential unknown ownership pending rather than assigning it to a convenient role. Walk the affected steps as that user: can they obtain inputs, identify the actual setting or file, act within their responsibility, and pass the result to the next owner in dependency order? Distinguish platform labels, code parameters, file names, and explanatory terms where ambiguity affects execution. Leave unknown values with their actual supplier; do not invent them, make collection depend on already having them, or block independent preparation.

Include the explanation needed to complete the task, not a general tutorial. Preserve the user's document structure when workable. This check does not require a new template, status table, or live platform login; formatting checks alone do not establish usability, and a walkthrough is not actual target-environment acceptance.

Organize by the consumer's actual task and reuse boundary. General guidance carries reusable operations; project-specific roles, identifiers and values belong in its application, not both places. A conceptual grouping or request for fewer steps does not itself require a physical archive, dispatcher, role selector, extra directories, or another installation path. Reuse the existing delivery mechanism when it meets the goal; propose a different one only for a demonstrated need, preserving necessary checks and cross-owner handoffs. A recipient-specific document omits unrelated internal work, not the inputs or responses that recipient needs from another owner.

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

This reference proves consumption and classifies lifecycle after relevant artifacts exist. `documentation-baseline-diagnosis.md` recommends or repairs the minimum documentation topology. `source-arbitration-and-baseline.md` decides source conflicts and authorization facts; it does not classify asset lifecycle. Execution scope determines whether a discovery changes the current task. Do not trigger a full lifecycle review or documentation diagnosis for an ordinary update whose consumer and lifecycle are already clear.
