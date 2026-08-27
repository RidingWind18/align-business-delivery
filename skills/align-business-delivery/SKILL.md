---
name: align-business-delivery
description: Use when existing business-system or complex business work needs a reviewable baseline from vague requirements, or when continuous feedback, complex correction, an interrupted long-running delivery, or commit-batch confusion creates material drift risk among PRDs, prototypes, implementation, business contracts, state models, task boundaries, clients, modules, or repositories.
---

# Align Business Delivery

Use the lightest safe process to turn incomplete business input and current-system facts into a traceable, executable, and verifiable delivery baseline. Keep requirements, product flow, business contracts, implementation, and validation aligned without requiring the user to write a large process prompt.

This skill is for existing business systems and complex business features. It is not a replacement for generic planning, implementation, TDD, debugging, testing, code review, worker scheduling, branch management, or project management.

## Operating Principles

- Check facts that can be checked. Do not replace available inspection with “probably” or “maybe.”
- State the current system before the target change.
- Treat confirmed user decisions, current code facts, AI inferences, recommendations, pending confirmations, and out-of-scope findings as different kinds of information.
- A draft PRD, prototype, generated document, or external capability output is not automatically the current business baseline; it must be consumed, calibrated, or confirmed.
- Analysis depth follows business risk. A deeper review does not expand the authorized implementation scope.
- Read access, deeper inspection, and similarity to another project do not grant write access. Establish the writable roots and protected user changes before editing or delegating execution.
- Preserve project conventions and verified standard modules over generic preference.
- Ask only questions that block the current decision. Continue safe, non-blocking work internally.
- Separate the current execution request from conceptual questions, candidate ideas, pending decisions, later-stage work, and explicit exclusions. Discussion is not implementation authorization.
- Keep the current feedback batch authoritative for active item membership and lifecycle status across turns; arbitrate each item's substance by source dimension. Do not reopen resolved or superseded items without new regression evidence.
- Keep routine output concise: current conclusion, blocking decision, next action, evidence, and residual risk.

## Choose The Lightest Mode

**Fast closure** applies to local copy, style, visibility, validation, mapping, or one-point fixes that do not change business state or shared contracts. Check the full value path that matters, then implement and verify without producing a full PRD or module map. Fast closure removes extra business-alignment artifacts; it does not waive a professional method that the user, host, or that capability's own trigger requires.

**Standard module work** applies to a bounded module enhancement, an existing-page change, or local client/server linkage with clear ownership and contracts.

**Full design** applies to a new system or large module, core object or state changes, workflow refactoring, multi-client or multi-repository contracts, unresolved ownership, or several dependent modules.

Escalate only when discovered facts increase business risk. De-escalate when inspection proves the change is local and existing patterns cover it.

## Entry And Return Routing

This is a fact-based router, not a stage plan or a visible checklist. Do not output every route merely because the skill triggered, and do not require work to pass through them in order. Skip any route already supported by current, consumed evidence.

- **Vague input**: capture the requested start mode. For organize-only, initial business draft, or reviewable PRD-baseline requests, form one complete reviewable business baseline here without requiring specialist exploration. For explicit option exploration, comparison, formal product design, or prototyping, freeze the verified inputs and hand the formal artifact to the appropriate specialist capability; do not create a parallel formal artifact.
- **Existing baseline**: inspect current documents, code, database, prototypes, history, and conventions; arbitrate only the dimensions that conflict.
- **Affected module refinement**: refine only the current module or affected page, data flow, state behavior, and prototype investment.
- **Development-batch freeze**: record the effective scope, contracts, dependencies, ownership, acceptance, and unresolved blockers, then hand planning or implementation to the appropriate specialist capability.
- **Execution drift return**: re-enter only when feedback, interruption, source conflict, ownership conflict, dependency invalidation, or scope discovery changes the frozen package. Return only the affected module to its earliest unresolved route.
- **Delivery convergence**: compare delivered behavior with the effective business goal, evidence, and actual completion level.
- **Fast closure**: for a verified local change, inspect the affected value path, implement, and validate without creating a full baseline, lifecycle, or task ledger.

Lightweight means low-interference routing and concise output, not shallow business analysis.

Before forming a complete draft baseline from incomplete input, organizing raw items under a no-expansion request, handling a mixed-intent message or current feedback batch, or confirming modules/items step by step, read `references/requirement-intake-and-convergence.md`. Keep the document body readable and preserve the requested start mode and pace. Internally preserve confirmed facts, code facts, AI inferences, recommendations, pending decisions, and out-of-scope items. Present them as a compact matter table or list unless the user requests a formal audit, full evidence, or separately expanded categories; combine empty categories into one short note rather than six mechanical headings. Use inline labels only where ambiguity could change later design.

During execution, when an adjacent data, document, contract, or module issue is discovered, read `references/execution-scope-guard.md` and classify it as required adjacent closure, blocking conflict, out-of-scope discovery, or later optimization before changing it. Discovery and deeper analysis do not authorize implementation outside the frozen package.

Before resuming writes after context compression, a material or cross-day interruption, a task or batch switch, unclear active scope or commit membership, or explicit feedback that work is confused, incomplete, or drifting, read `references/requirement-intake-and-convergence.md` and `references/execution-scope-guard.md`. Restore only the minimum internal execution snapshot needed for the active batch. A continuous "continue" with clear scope proceeds directly. If the user says to stop, analyze, or clarify first, perform read-only inspection only; do not modify, stage, commit, push, or resume an older plan until the current batch is confirmed.

When the user supplies a concrete prototype, page description, or interaction material for implementation or review, read `references/prototype-and-product-flow.md` before changing the page. Consume the supplied entry, retained and changed regions, fields and row actions, local workspaces, key operations, data/API mapping, and explicitly unchanged behavior. Do not claim that concrete interaction is missing when the supplied material states it, and do not turn mandatory consumption into a full-page rewrite.

When changing a shared mapper, result mapping, value object, component, hook, query, or base method with multiple consumers, read `references/execution-scope-guard.md` and perform a risk-triggered consumer check. Do not apply this gate to an independent page, private method, or single-consumer query.

## Mandatory Gates

Before any file or asset write, or before delegating an execution unit that may write, read `references/execution-scope-guard.md` and establish the allowed write roots, owned asset classes, read-only references, prohibited repositories or modules, and pre-existing user changes. Pass the same boundary to the receiver and check each write target against it. Multiple projects in one workspace are not one writable scope.

Before producing or applying an irreversible or difficult-to-recover action, read `references/source-arbitration-and-baseline.md` to verify the exact goal, object, environment, mechanism, and destructive details. Then read `references/execution-scope-guard.md` for the pause/continue decision. If authorization is incomplete, do not place the unconfirmed object or action in an executable or optional cleanup artifact; a disabled-by-default switch, comment, preview, guard, or "optional" label does not supply authorization. Pause only the risky part and continue safe current-scope delivery. If authorization is complete and current facts agree, proceed without asking for the same confirmation again.

Before starting a dependent module when task status, code, commits, validation, or acceptance disagree, read `references/module-delivery-and-coordination.md`. Do not choose the most optimistic source, mark the task `DONE`, or create downstream business files while the conflict remains. When authoritative evidence agrees and the gate is formally released, advance and enter the authorized downstream scope without repeated confirmation.

## Reference Routing

Read only the target references required by the current stage and risk:

- `references/requirement-intake-and-convergence.md`: vague requirements, complete draft baseline, organize-only or stepwise intake, mixed intent, current feedback batches, quoted or annotated history, parent-request recovery, or fact/inference/recommendation separation.
- `references/source-arbitration-and-baseline.md`: checkable facts, conflict among user decisions, PRDs, prototypes, code, database, history, conventions, current batch, or irreversible-action authorization.
- `references/prototype-and-product-flow.md`: prototype investment, real-page and component reuse, page interaction, data flow, state expression, or prototype-to-implementation tracking.
- `references/document-and-artifact-lifecycle.md`: document consumption, project-class governance, current versus historical material, consumers, version ownership, or initialization/migration/verification/deployment asset boundaries.
- `references/business-model-state-and-refactor.md`: core objects, relationships, state, time, ownership, workflow paradox, minimal traceability, old/new chains, compatibility, migration, rollback, or semantic preservation.
- `references/module-delivery-and-coordination.md`: module package, readiness, complete business states, topology or dependency ledger, invalidation, cross-owner contract, multi-unit delivery, status conflict, completion level, or downstream release.
- `references/execution-scope-guard.md`: mode escalation, writable-root and delegation boundary, interruption recovery, pause-for-analysis, delivery-batch separation, review findings, lightweight display/validation/submission closure, current change package, discovery classification, adjacent closure, local reopen, unauthorized scope, or risky-action continuation.
- `references/delivery-convergence-and-evidence.md`: midpoint convergence, delivery consistency, actual capability boundary, evidence level, truthful completion, unverified item, or residual risk.

## Capability Handoff

- This skill owns verified business facts, the effective baseline, authorized scope, decisions the receiver must not make, the expected artifact, and the return point.
- This skill may produce a complete reviewable business baseline for organize-only, initial-draft, or PRD-baseline requests. Specialist capabilities own option exploration and comparison, formal product design or prototyping, technical planning, implementation, debugging, testing, review, and their execution methods.
- This skill decides only whether it actively initiates a specialist handoff. Mere installation or availability is not a reason for this skill to initiate one. Organize-only intake, fact classification, source arbitration, feedback convergence, interruption recovery, and fast closure do not by themselves require an Align-initiated handoff.
- When the current authorized request requires a specialist-owned artifact or method, initiate the handoff. When the user names or supplies a specialist, the host requires it, or the specialist has triggered under its own rules, cooperate with that workflow and pass the business context below; do not suppress, replace, or reinterpret that trigger because ordinary engineering or fast closure appears sufficient.
- When handoff is required, do not silently substitute this skill's own design, plan, prototype, implementation method, or review. Hand verified inputs to the specialist once. When its artifact returns, calibrate only conflicts, scope, ownership, evidence, and validity before admitting it to the effective baseline; do not generate a second artifact of the same kind.
- While specialist work remains within the frozen package, stay low-interference. Re-enter only for a changed business basis, scope or ownership conflict, dependency invalidation, interruption recovery, or a completion claim unsupported by evidence.
- If no specialist capability exists, use ordinary engineering practice. Missing specialist capability is not itself a blocker; continue at the abstraction requested from confirmed facts and request detail only when the next concrete action requires it.
- External output does not become the effective business baseline until it is consumed, calibrated, or confirmed.
- Do not require or name a particular model, IDE, plugin, agent system, or skill in the formal workflow.

## Completion

At a delivery claim, commit or push, formal handoff, large-batch end, or requested omission/scope review, read `references/delivery-convergence-and-evidence.md` and compare requested scope, actual changes, excluded work, and evidence. Use a quick internal comparison for simple work and an explicit package comparison only for complex multi-module or cross-repository delivery.
