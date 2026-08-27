# Module Delivery And Coordination

Use this reference when several modules, owners, clients, or repositories share a business contract or dependency chain. It controls business readiness and capability handoff, not staffing, schedules, execution-unit dispatch, or general project management.

## Module Package

For each affected module, keep a compact package containing its goal, current basis, implementation nature, page change, prototype investment, confirmed decisions, open design blockers, prerequisites, shared contracts, parallel safety, owner, deliverables, acceptance evidence, and upstream-change risk.

Use the following business states:

- `DRAFT`: the module boundary or main decisions are still being formed.
- `BLOCKED`: a prerequisite, frozen contract, or required decision is missing.
- `READY`: inputs, contract, scope, deliverables, and acceptance criteria are sufficiently settled to begin.
- `IN_PROGRESS`: authorized work is active on the current basis.
- `PAUSED`: started work is intentionally interrupted but retains an owner and resumable state.
- `REVIEW`: the declared delivery is available for required review or acceptance.
- `REWORK`: review found a required correction before acceptance.
- `DONE`: required evidence and acceptance support the whole declared delivery level.
- `OBSOLETE`: the task or basis has been superseded and must not direct new work.

Other local progress labels may exist, but they must not disguise the effective business state. Keep base capability, service-side stage, page or client stage, and whole-module completion distinct.

## Readiness And Minimal Contracts

A module is `READY` only when its business goal, current carrying path, main rules, object ownership, shared boundary, deliverables, and acceptance criteria are clear enough that no open issue can change its main design.

Freeze only the minimum boundary needed across owners: shared business operations, authoritative data, shared states, direction of use, compatibility expectations, and required idempotency or transaction semantics. Do not use a shared contract to prescribe another owner's internal routes, transport shapes, classes, local errors, or implementation details unless those are themselves the cross-owner boundary.

An output from a specialist, tool, or independent worker is input for review, not automatically a current business baseline. It enters the baseline only after it has been consumed and calibrated against the authoritative facts or accepted by the appropriate owner.

## Handoff Source Fidelity

Before handing a package to another module or execution unit, preserve the source status of each consequential rule: user-confirmed decision, verified current-system fact, verified technical derivation, recommendation or candidate, or pending decision. A recommendation must not become an implementation requirement merely because it makes the package easier to execute. When the user has confirmed an observable result and the internal mechanism can be determined from reachable code, samples, history, or data, inspect that evidence and record the verified technical conclusion; until then, keep the mechanism as a candidate rather than asking the user to approve an internal algorithm or presenting it as a business rule.

Include a compact current-baseline identifier and ensure the receiver can actually read the authoritative basis needed for the assigned work. A local-only, untracked, inaccessible, or merely mentioned artifact is not a reachable basis. Provide an authorized readable source or keep the affected decision blocked; do not compensate by flattening uncertain content into a definitive handoff rule.

When an upstream correction replaces a handoff rule, mark the superseded package or affected rule `OBSOLETE`, pause only the dependent work, preserve unrelated valid increments, and require the receiver to consume the reachable replacement baseline before continuing. Do not roll back whole files or discard unaffected work merely because one handoff rule changed.

## Dependency Invalidation

When an upstream business rule, object structure, state machine, shared contract, or accepted boundary changes, find direct and indirect dependents. Mark started work for impact assessment, move affected work to `REVIEW` or rework as appropriate, record the changed source and required re-verification, and prevent continuation on the old basis.

Independent work may proceed only when shared writes and unresolved shared business decisions are absent. This is a dependency rule, not an instruction to create a schedule or dispatch workers.

## Topology, Ledger, And Dependency DAG

For multi-module, multi-repository, multi-client, multi-unit, cross-day, or interruption-prone work, keep a lightweight Dependency DAG or task ledger when it makes ownership and invalidation visible. Record official backend, management, client, and other writable repositories separately from prototype or reference-only repositories. Readable topology does not grant write access.

The ledger records module state, owner, prerequisite, shared contract/baseline version, writable root, deliverable, acceptance evidence, block or pause reason, and downstream invalidation. An interruption becomes `PAUSED` or `BLOCKED`; an upstream change marks affected downstream work for re-verification before continuation.

It is safe to express a pipeline such as design N, implement N-1, and review N-2 only when each stage has a frozen input, disjoint ownership/write scope, and an explicit return path for review findings. This skill does not assign people, schedule work, or dispatch execution units.

## Conflict And Downstream Gate

When a ledger or declared prerequisite says `BLOCKED`, `REVIEW`, or incomplete, but code, a commit, a partial inventory, or a representative check looks complete, treat the discrepancy as an unresolved evidence conflict. This reference owns the readiness gate. If the authoritative sources themselves conflict, use `source-arbitration-and-baseline.md` to establish the current effective basis, then return here to re-evaluate the gate. Resolve readiness using that basis, the current ledger, reachable active baseline, complete deliverable inventory, evidence covering every acceptance object, and required acceptance.

Until it is resolved:

- Do not mark the prerequisite `DONE`.
- Do not start a dependent module or create its business files.
- You may complete explicitly authorized, safe missing work within the current module and add evidence without changing its truthful state.
- If the current task is already `BLOCKED` by an unresolved prerequisite, internal artifact completion does not move it to `REVIEW`; retain `BLOCKED` until that prerequisite gate is released. Use `REVIEW` only when no prerequisite block remains and the task's own declared delivery awaits acceptance.

Release is symmetric: when authoritative evidence and required acceptance agree that the prerequisite is complete, advance the state and permit the authorized dependent module to begin. Do not retain a gate or request a confirmation that the authoritative record has already supplied.
