---
name: align-business-delivery
description: Use when an existing or complex business-system task needs a reviewable requirement or documentation baseline, or conflicting feedback, prototypes, code, contracts, or handoffs cause scope drift.
---

# Align Business Delivery

Align incomplete business input with current-system facts into a traceable, executable, verifiable baseline. Carry requirements, product flow, contracts, and accepted ways of working through implementation and corrections without making the user repeatedly explain them.

This skill is for existing business systems and complex business features. It is not a replacement for generic planning, implementation, TDD, debugging, testing, code review, worker scheduling, branch management, or project management.

The user's explicit task and latest corrections take precedence over this skill's default workflow. Apply only relevant guidance; do not add work or require renewed approval solely to satisfy that workflow.

## Operating Principles

- Check facts that can be checked. Do not replace available inspection with “probably” or “maybe.”
- State the current system before the target change.
- Treat confirmed user decisions, current code facts, AI inferences, recommendations, pending confirmations, and out-of-scope findings as different kinds of information.
- A draft PRD, prototype, generated document, or external capability output is not automatically the current business baseline; it must be consumed, calibrated, or confirmed.
- Analysis depth follows business risk. A deeper review does not expand the authorized implementation scope.
- Read access, deeper inspection, and similarity to another project do not grant write access. Establish the writable roots and protected user changes before editing or delegating execution.
- Proactively find applicable project agreements, accepted artifacts, and verified procedures. Apply them as execution constraints, preserving unchanged parts rather than silently substituting a preferred method.
- Ask only for missing decisions that block the current work. A specialist's required understanding or design confirmation is not a redundant question; use known facts instead of re-interviewing the user.
- In review, check the supported actor and entry, necessary state, and existing protection before escalating an unusual scenario. A technically constructible request alone is not a new business decision.
- Keep routine output concise: current conclusion, blocking decision, next action, evidence, and residual risk.

## Active Task To Next Action

Anchor the next action in the requested result, effective basis, and latest applicable correction. Identify what the latest message changes, retain unaffected confirmed decisions, accepted behavior, exclusions, and valid later additions, then take the next authorized unfinished action. Resolve its effect within the active parent task rather than treating each supplement as a new assignment.

Separate execution requests from conceptual questions, candidate ideas, pending decisions, later work, and exclusions. Discussion alone is not implementation authorization; questions neither authorize new work nor cancel existing authorization. Respect explicit pauses, task switches, real blockers, and specialist gates; keep closed items closed without new evidence. If blocked, identify the precise missing decision or evidence and continue independent authorized work.

Keep this anchor internal, reuse the established task record, and recover only missing or changed facts. It is not a sequence of approval stages, a new document, or a per-turn checklist for the user.

If the user corrects the same task interpretation twice, stop generating another plan or speculative cause list. Re-read the parent request, the two corrections, and the checkable current artifact or source; resolve the exact mismatch before further execution. Keep this recovery internal unless the remaining choice truly belongs to the user.

## Scale Business Alignment

These levels size business-alignment work, not a competing design or approval workflow. A selected specialist owns its process, approval gates, and escalation; do not classify or downgrade that process again here. Choose alignment depth from unresolved business decisions, actual impact, and verified risk.

**Fast closure** applies to a verified local fix with a settled business boundary, including a small state or API-linked correction. Check the affected value path and evidence without a full PRD or module map.

**Standard module work** applies to a bounded enhancement or client/server linkage with sufficiently clear rules, contracts, and ownership.

**Full design** applies when unresolved consequential decisions or demonstrated impact require forming or changing the business boundary. Clarify only the affected objects, rules, flows, or ownership; settled parts need not restart design.

Increase alignment work only for verified unresolved decisions; stop adding alignment artifacts when existing rules cover the change. Lightweight means low interference, not shallow analysis, skipped approvals, or weaker acceptance.

## Mandatory Gates

At the start of a write-capable task package or delegation, read [Required Write Boundary](references/execution-scope-guard.md#required-write-boundary) and its conditional reading index. Read further sections only for matching conditions; the write-boundary gate does not require loading the whole reference. Reuse an established unchanged boundary and revisit affected facts when scope or ownership changes.

Before producing or applying an irreversible or difficult-to-recover action, read [Irreversible Authorization Facts](references/source-arbitration-and-baseline.md#irreversible-authorization-facts) and [Risky-Action Pause](references/execution-scope-guard.md#risky-action-pause). Incomplete authorization cannot be bypassed with an optional executable artifact. Pause only the risky part; proceed without renewed approval when recorded authorization and current facts agree.

Before an execution handoff across independent workspaces, repositories, or external prototype baselines, read `references/module-delivery-and-coordination.md` and verify that the receiver can consume the key authoritative inputs.

Before starting a dependent module when task status, code, commits, validation, or acceptance disagree, read `references/module-delivery-and-coordination.md`. Do not choose the most optimistic source, mark the task `DONE`, or create downstream business files while the conflict remains. When authoritative evidence agrees and the gate is formally released, advance and enter the authorized downstream scope without repeated confirmation.

## Reference Routing

Use this single router as needed, not as sequential stages or a visible checklist. Skip resolved routes; return only affected work to its earliest unresolved decision. Locate the relevant heading and read its section with necessary context, rather than an arbitrary file prefix. Keep long project extracts separate from guidance; recover relevant omitted text when output is truncated. Reuse consumed, unchanged evidence and guidance rather than mechanically reading it again.

- `references/requirement-intake-and-convergence.md`: vague requirements, complete draft baseline, organize-only or stepwise intake, mixed intent, current feedback batches, quoted or annotated history, parent-request recovery, interruption recovery, or fact/inference/recommendation separation.
- `references/source-arbitration-and-baseline.md`: checkable facts, reuse of a previously verified method, source conflicts, current batch, or irreversible-action authorization.
- `references/prototype-and-product-flow.md`: prototype investment, real-page and component reuse, page interaction, data flow, state expression, or prototype-to-implementation tracking.
- `references/document-and-artifact-lifecycle.md`: document consumption, project-class governance, current versus historical material, consumers, version ownership, or initialization/migration/verification/deployment asset boundaries.
- `references/documentation-baseline-diagnosis.md`: missing, stale, duplicated, contradictory, or unclear project documentation; documentation-system recommendation; authority index; minimum useful document topology; or authorized baseline creation and repair.
- `references/business-model-state-and-refactor.md`: core objects, relationships, state, time, ownership, workflow paradox, minimal traceability, old/new chains, compatibility, migration, rollback, or semantic preservation.
- `references/module-delivery-and-coordination.md`: module package, readiness, complete business states, topology or dependency ledger, invalidation, cross-owner contract, multi-unit delivery, status conflict, completion level, or downstream release.
- `references/execution-scope-guard.md`: mode escalation, writable-root and delegation boundary, interruption recovery, pause-for-analysis, delivery-batch separation, review findings, shared-consumer risk, lightweight display/validation/submission closure, current change package, discovery classification, adjacent closure, local reopen, unauthorized scope, or risky-action continuation.
- `references/delivery-convergence-and-evidence.md`: midpoint convergence, delivery consistency, actual capability boundary, evidence level, truthful completion, unverified item, or residual risk.

## Capability Handoff

- This skill owns verified business facts, the effective baseline, authorized scope, decisions the receiver must not make, the expected artifact, and the return point.
- For organize-only, use [Organize-Only Output](references/requirement-intake-and-convergence.md#organize-only-output). When the user requests an initial business draft or complete reviewable PRD baseline, produce that full draft, distinguishing confirmed facts from assumptions and pending decisions. Specialist capabilities own option exploration and comparison, formal product design or prototyping, technical planning, implementation, debugging, testing, review, and their methods.
- This skill decides only whether it actively initiates a specialist handoff. Mere installation or availability is not a reason for this skill to initiate one. Organize-only intake, fact classification, source arbitration, feedback convergence, interruption recovery, and fast closure do not by themselves require an Align-initiated handoff.
- When the current authorized request requires a specialist-owned artifact or method, initiate the handoff. When the user names or supplies a specialist, the host requires it, or the specialist has triggered under its own rules, cooperate and pass the verified business context; do not suppress, replace, or reinterpret that trigger because ordinary engineering or fast closure appears sufficient.
- Hand verified inputs, ownership/dependencies, non-decisions, the expected artifact, and return point to the specialist once. Approval of the goal does not approve a later scope-changing design. Follow existing patterns for internal technical choices; surface a consequential departure and its evidence, not a menu of internal classes for the user to design. On return, calibrate conflicts, scope, ownership, dependencies, evidence, and validity before admitting the artifact to the effective baseline; do not substitute or generate a second artifact of the same kind.
- While specialist work remains within the frozen package, stay low-interference. Re-enter only for a changed business basis, scope or ownership conflict, dependency invalidation, interruption recovery, or a completion claim unsupported by evidence.
- If no specialist capability exists, use ordinary engineering practice. Missing specialist capability is not itself a blocker; continue at the abstraction requested from confirmed facts and request detail only when the next concrete action requires it.
- Do not require or name a particular model, IDE, plugin, agent system, or skill in the formal workflow.

## Completion

At a formal handoff, large-batch end, complex or cross-repository delivery claim, evidence conflict, or requested omission/scope review, read the relevant section of `references/delivery-convergence-and-evidence.md`. For an explicitly requested whole-package review, use [Requested Review Coverage](references/delivery-convergence-and-evidence.md#requested-review-coverage). For a simple fast-closure claim, directly compare the request, actual change, exclusions, and evidence; load that reference only if the comparison exposes uncertainty or broader risk.
