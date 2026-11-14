# Execution Scope Guard

Use this reference to keep an execution package within its authorized business boundary, especially for lightweight changes, newly discovered adjacent work, and high-risk actions. It is tool-neutral and does not replace debugging, testing, code review, or generic delivery workflows.

## Required Write Boundary

At the start of a write-capable package or delegation, use [Active Task To Next Action](../SKILL.md#active-task-to-next-action) to establish the authorized goal, allowed behavior, exclusions, writable roots, owned files or asset classes, read-only reference roots, prohibited repositories or modules, pre-existing user changes, acceptance condition, and proportionate verification. Reuse an unchanged boundary; revisit affected facts when scope or ownership changes.

Treat each repository or project root as a separate ownership boundary. A workspace containing several roots is not wholly writable: only roots explicitly owned by the current task may change, while reference projects are read-only by default. Similar code, deeper analysis, and permission to inspect a project do not authorize edits, formatting, builds, generation, migration, or other write-capable commands there.

Before every write-capable tool call, resolve its target and working directory and confirm they remain inside an allowed write root and owned asset class. A command authorized in one project is not authorized in a sibling project. When two or more roots are explicitly owned, work in each confirmed root and use each root's allowed verification without mechanically restricting the task to one directory or asking again for recorded ownership.

## Conditional Reading

Use matching sections, not the whole file or a sequence of stages. Reuse already consumed, unchanged guidance.

| Condition | Read |
| --- | --- |
| Alignment depth or package basis is unclear | [Business Alignment Depth](#business-alignment-depth), [Current Change Package](#current-change-package) |
| Context, active item, or delivery batch needs recovery | [Interruption Recovery And Delivery State](#interruption-recovery-and-delivery-state) |
| User pauses for analysis | [Pause-For-Analysis Gate](#pause-for-analysis-gate) |
| Delegating execution or investigating a boundary breach | [Write And Delegation Boundary](#write-and-delegation-boundary) |
| Discovering possible additional work during implementation or review | [Review-Finding Gate](#review-finding-gate), [Discovery Classification And Adjacent Closure](#discovery-classification-and-adjacent-closure) |
| A fix remains ineffective or verified facts invalidate the package | [Local Reopen](#local-reopen) |
| Changing a multi-consumer asset | [Shared Consumer Check](#shared-consumer-check) |
| Changing a field's display, validation, or submitted value | [Lightweight Value Path](#lightweight-value-path) |
| Irreversible or other high-risk action | [Risky-Action Pause](#risky-action-pause) and source-arbitration authorization facts |

## Business Alignment Depth

Use the alignment levels in `../SKILL.md`, not a second process classifier. Touching a state, permission, shared contract, or several clients does not by itself require broader business design. Retain settled scope and continue safe independent work while an affected decision is clarified. For a local fix, verify the affected condition and one relevant unchanged condition. Deeper analysis does not authorize additional implementation or override a specialist's process.

## Current Change Package

Use the active-task anchor and established write boundary. Add applicable project agreements and prior accepted methods, current implementation facts, acceptance conditions, and the smallest meaningful verification. Check facts that code, configuration, records, interfaces, or documents can answer; when the evidence is unavailable, state the uncertainty and do not treat it as permission. Carry this basis into the next action and specialist handoff; do not regenerate it or a visible checklist for every turn. Reinspect only affected or uncertain parts.

For a lightweight field or form change, determine whether it is display, validation, or submitted-value behavior. Include hidden retained values, saved old values, edit behavior, and the relevant persistence path only when they belong to that same condition.

## Interruption Recovery And Delivery State

Restore a minimum execution snapshot before new writes when context was compressed, work materially or overnight paused, the task or delivery batch changed, the active item or commit boundary is unclear, or the user reports fragmented, omitted, or drifting work. Read the original task record and current artifacts when available; do not reconstruct the batch from a local summary alone. A continuous conversation with a clear active item and boundary does not trigger recovery merely because the user says "continue."

The minimum snapshot records the parent task, current active item, what this round must finish, explicit exclusions, allowed write scope, current blockers, and latest effective correction. Add item history, workspace changes, or three-dimensional status only when they are needed to resolve the interruption or split a delivery. Keep the snapshot internal by default, do not write short-lived execution state into shared documents, and show a concise table only when the user asks to restore state, reconcile omissions, or split delivery.

Judge each item on three independent dimensions:

- Implementation: not started, in progress, coded but untested, automated checks passed, runtime verified, awaiting user acceptance, or complete.
- Business priority: current-flow blocker, non-blocking functional gap, experience or style optimization, later specialist work, or out of scope.
- Current delivery: must ship in this batch, conditionally included, record only, continue after push, or excluded from the current task.

A valid problem is not automatically current implementation work. Compilation, representative tests, runtime verification, user page acceptance, and readiness for the current commit are different facts. Derive blocking priority from the user's current goal and acceptance conditions rather than an assistant-defined ideal of completeness.

### Review-Finding Gate

Review findings use the single classification and admission check in Discovery Classification And Adjacent Closure below. A direct current-acceptance blocker is a candidate for that check, not automatic permission to implement. Analysis depth, a failing test, or an easy fix does not authorize adding work. Keep acceptance priority separate from current-batch membership and ownership.

### Pause-For-Analysis Gate

When the user says to stop, analyze, or clarify first, stop new modifications, staging, commit preparation, commits, pushes, and scope expansion. Read-only inspection and an execution snapshot are allowed. A later "continue" resumes only the latest confirmed batch, not an older plan superseded by correction.

In a workspace with many existing changes, do not begin staging or commit splitting before restoring the snapshot. Separate current blockers and their inseparable dependencies from completed later-batch work, local configuration and generated output, pre-existing user changes, and unverified or red-test code.

## Write And Delegation Boundary

For delegated execution, pass the exact writable roots, read-only roots, prohibited locations, owned assets, allowed verification commands, and existing user changes. The receiver must not enlarge that boundary because an adjacent repository has a more complete implementation. Its safe options are to read the reference, adapt the idea into an owned root, or report a blocking dependency.

If a write or write-capable command crosses the boundary:

1. Stop further writes and commands.
2. Record the actual paths, commands, and observed changes.
3. Remove only increments precisely attributable to the current execution; do not restore whole files or overwrite pre-existing user work.
4. Recheck the affected worktrees and preserve unrelated changes.
5. Retain the boundary breach as failed execution evidence even when recovery succeeds, then rerun in a fresh authorized scope.

## Discovery Classification And Adjacent Closure

Classify each newly discovered item once, whether found during implementation or review:

- Required adjacent closure: directly blocks current acceptance and passes all five admission conditions below.
- Blocking conflict: a needed business decision, authoritative basis, or prerequisite remains unresolved.
- Out-of-scope discovery: belongs to another module, owner, or delivery batch.
- Later optimization: related but non-blocking work not already authorized for this batch.

Only a proposed addition to the current package needs this admission check. Check all five conditions before admitting a directly blocking discovery; use the resulting classification rather than creating another review category or ledger:

1. It is necessary for the current acceptance condition.
2. It belongs to the same operation, interface contract, or data-submission chain.
3. It adds no business rule, state, table, shared contract, or migration strategy.
4. It does not invade another task's or owner's boundary.
5. It can receive the current package's minimal verification.

If any condition fails, do not add it opportunistically. Record it under the applicable classification and continue only the authorized work. Passing the five adjacent-closure conditions does not override the writable-root or ownership boundary.

## Local Reopen

Reopen the smallest affected package when verified facts invalidate its assumed display rule, validation, submission behavior, local contract, or acceptance condition. Reassess the changed boundary and its direct dependent condition; do not turn a local correction into a broad audit without an escalation trigger.

If the same user-visible acceptance symptom remains after two repair attempts or completion claims, stop adding local patches. Downgrade the earlier completion conclusion to unverified, restore the reproducible path, runtime and version facts, prior attempts, and available evidence, then hand root-cause analysis to an applicable specialist debugging capability. If none is available, use ordinary systematic diagnosis. This gate controls re-entry and evidence status; it does not prescribe debugging steps, replace that capability, or expand the authorized scope.

## Shared Consumer Check

Trigger this check only when changing a mapper, result mapping, value object, shared component, hook, query, or base method with multiple consumers. Internally identify the target consumer and the most likely affected non-target consumers, keep the change inside the target query or behavior where possible, validate the target entry, and check one existing entry most likely to regress but expected to remain unchanged. Do not default to a visible consumer inventory or a project-wide scan.

An independent page, independent query, local private method, or verified single-consumer asset does not trigger this check. Apply its normal focused validation instead.

## Lightweight Value Path

For a local field or one-point page change, distinguish display rules, validation rules, and submitted-parameter rules. Inspect the existing component/form state, validator, request payload, backend validation, and persistence behavior only along the affected value path.

When visibility depends on a type or condition, check hidden old values, type switching, create versus historical edit behavior, whether the hidden value remains in form state, whether it is still submitted, and what the backend does when the field is absent or empty. Do not assume that hiding a field means clearing it: choose form-state retention, payload omission, explicit clearing, or another behavior from the confirmed submission and persistence rule, and preserve reversible user input when that rule allows. Verify the affected condition and one unaffected condition. Do not create a full PRD, prototype, module map, or project-wide audit unless verified risk requires escalation.

## Risky-Action Pause

Treat destructive, irreversible, environment-affecting, data-migrating, or unauthorized compatibility-breaking cross-owner actions as high risk. Use `source-arbitration-and-baseline.md` to establish whether the exact action is authorized; do not recreate or weaken that authorization decision here.

When that decision is incomplete or conflicts with current facts, pause only the risky action. Do not place unconfirmed actions or objects in an executable or optional cleanup artifact. A disabled-by-default switch, commented statement, preview, guard, or "optional" label does not make an unauthorized destructive action deliverable; read-only preview may describe affected objects but must not ship the destructive statement. Continue safe current-package delivery such as non-destructive target structure, read-only preflight, clearly labeled non-executable analysis, and a concise pending-decision list. Once the authorization decision is complete and consistent, proceed without re-asking for the same decision.
