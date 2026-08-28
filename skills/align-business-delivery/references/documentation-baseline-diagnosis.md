# Documentation Baseline Diagnosis

Use this reference when the user explicitly asks how a project should maintain documentation, when a new or inherited project has no usable documentation baseline, or when stale, duplicated, contradictory, or unreachable documents prevent reliable delivery. This is an adaptive baseline-repair method, not a fixed documentation template or a general wiki generator.

## Trigger And Boundary

Use this diagnosis when at least one condition is true:

- the user asks what documents the project should maintain or asks to create or repair them;
- a new project has no reliable entry, current decisions, or implementation basis;
- an inherited project has documents, but their authority, freshness, consumers, or relationship to current code is unclear;
- several repositories, clients, owners, or modules need shared business or delivery boundaries;
- implementation cannot safely continue because no reachable current baseline can be identified.

Do not trigger it for an ordinary local fix whose current behavior, ownership, and validation path are already clear. Do not create documents merely because a possible category is absent.

This skill may diagnose and recommend the minimum documentation system. Create or reorganize files only when the user requests or authorizes that work and the writable roots are established. Do not silently replace product design, architecture design, project management, or a specialist documentation method.

The user's existing documentation system, naming, maintenance preferences, and proposed topology are first-class constraints. Understand and preserve them before recommending a change. The role list in this reference is a diagnostic vocabulary, not a mandatory architecture. If the user's structure can answer the required delivery questions, use it even when it differs from this reference's examples. When a concrete risk remains, explain the affected consumer and failure mode, then recommend the smallest compatible adjustment; do not rename, move, split, merge, archive, or replace the user's documents without explicit authorization.

## Diagnose Before Recommending

Establish the evidence surface before inventorying documents. A project's current local workspace, committed baseline, and collaborator- or release-visible baseline answer different questions and must not silently substitute for one another:

- when the user asks what is currently maintained locally, include relevant uncommitted and untracked material in the inspection;
- when the user asks what another worker can obtain, inspect the committed or otherwise shared baseline;
- when the user asks about a public or released baseline, inspect the actual published projection, tag, package, or deployment source;
- when these surfaces differ, report the divergence directly, such as "maintained locally but not shared," instead of describing the material as wholly absent or already available to collaborators.

For version-controlled projects, an isolated clean worktree represents its starting commit, not automatically the user's full current workspace. State that limitation or compare it with the active working tree when the question requires current local facts. A local commit or `HEAD` is not automatically collaborator-visible: verify its relationship to the relevant upstream, remote branch, package, or published source before calling it cloneable or shared. If that relationship is not checked, label the conclusion as the local committed baseline and name shared reachability as unverified. For non-Git projects, apply the same distinction to local, shared, and deployed evidence. Do not automatically commit, publish, or copy local-only material merely because the diagnosis found a reachability gap.

Inspect the reachable project facts needed to answer:

```text
Project: purpose, lifecycle, current phase, regulated or operational risk
Consumers: developers, product, operations, external systems, AI agents
Topology: repositories, clients, modules, shared contracts, owners
User preference: existing taxonomy, naming, maintenance habits, intended changes, protected documents
Current evidence: instructions, README, designs, prototypes, schemas, code, history, tests
Document condition: current, candidate, stale, duplicated, contradictory, historical, local-only
Change pressure: which facts change often and which downstream work they invalidate
```

Do not infer that a document is authoritative from its filename, numbering, age, detail, or repeated citation. Check its current consumers and agreement with current decisions and code facts.

## Select The Minimum Useful Topology

Choose document roles by actual consumer and risk. The following roles are options, not required files or names:

| Role | Use when it answers a recurring delivery question |
| --- | --- |
| Project entry or index | People or agents cannot tell what to read, what is current, or what is historical |
| Collaboration instructions | Repository conventions, writable boundaries, verification, and AI collaboration need a durable entry |
| Product or business baseline | Business goals, scope, rules, and exclusions otherwise remain implicit or scattered |
| Concept, ownership, or state model | Shared objects, relationships, identifiers, lifecycle, or state transitions drive several modules |
| Interface or data contract | Repositories, clients, owners, or external systems need a frozen shared boundary |
| Data or migration design | Persistent structures, initialization, migration, compatibility, or rollback require controlled consumption |
| Prototype or interaction basis | Visible entry, page flow, actions, and state expression are acceptance inputs |
| Task dependency ledger | Several owners or modules have prerequisites, parallel boundaries, invalidation, or handoff risk |
| Major-change impact record | A change can invalidate shared contracts, data, state, several modules, or prior acceptance |
| Verification or operations evidence | Completion claims depend on reproducible tests, runtime checks, deployment, or support procedures |
| Current status and decision record | A long-running personal or interruption-prone project must recover current position and rejected choices |

Typical starting shapes:

- **Small, stable project:** repository README, collaboration instructions, and only the current status or decisions that cannot be recovered cheaply from code.
- **Bounded business module:** current business basis, relevant contract or interaction basis, concise change impact, and verification evidence.
- **Stale inherited project:** first create or repair an authority index and status labels; do not rewrite every historical document before identifying consumers.
- **Complex multi-module system:** separate business baseline, shared concepts or states, contracts, data design, interaction basis, dependency ledger, major changes, and verification when each has a real consumer.
- **Long-running personal project:** current status, decisions and reasons, recoverable handoff, and richer history may be useful, while current and historical material remain distinct.

## Recommendation Contract

Return a compact recommendation before creating a large document set:

```text
Existing material:
- path or source | current use | authority/status | keep/repair/merge/archive

Recommended minimum additions:
- role | consumer | question it decides | update trigger | create now or later

Not recommended:
- document or category | why it would duplicate, go stale, or lack a consumer

Authority and maintenance:
- entry/index
- source of truth by dimension
- historical boundary
- change-to-document update mapping
```

Use the user's chosen documentation model and the project's existing naming and directory conventions. A numbered document family is appropriate only when it improves stable navigation and agrees with that basis; do not copy another project's numbering or taxonomy.

## Default Output And Detail Escalation

The diagnosis may require broad inspection, but the default user-facing result is a compact decision summary. Use this order unless the user requests a full audit:

1. overall conclusion;
2. current document roles and only material anomalies;
3. minimum compatible recommendations;
4. documents or categories not recommended;
5. one next action and any unverified boundary.

Do not paste the complete file inventory, command output, every link check, or a file-by-file evidence diary into the default response. Include the evidence path or consumer only for a conclusion that affects the decision. Summarize repeated healthy findings instead of listing them individually. A mature existing system with no material gap should be reported as such rather than receiving a new document plan. Expand into a detailed evidence table only when the user asks for a full audit, evidence details, competition material, or a high-risk authority conflict requires it. Concise output does not reduce the required inspection depth or permit static inspection to be presented as complete validation.

## Creation And Repair

When authorized to implement the recommendation:

1. Preserve existing valid documents and user changes.
2. Establish one reachable entry that names current sources and historical boundaries.
3. Repair links, status labels, ownership, and source-of-truth statements before adding depth.
4. Move or mark historical material only when its replacement is current and consumers are known; do not delete by default.
5. Put each durable fact in one authority by dimension and link to it elsewhere.
6. Record each document's consumer, decision scope, and update trigger in the index or document introduction.
7. Keep temporary plans, AI execution traces, and one-off reviews local unless they have an active cross-person handoff or formal-review consumer.
8. Verify that every required source is reachable from the intended repository or execution environment.

## Change-To-Document Mapping

At a meaningful change, update only the affected authorities:

| Changed dimension | Usually inspect or update |
| --- | --- |
| Business goal, rule, scope, or exclusion | Product or business baseline |
| Core object, ownership, identity, or lifecycle | Concept, identifier, or state model |
| Visible entry, operation, or flow | Prototype or interaction basis |
| Cross-owner request, response, state, or error | Shared interface contract |
| Persistent structure or compatibility | Data design and initialization or migration asset |
| Prerequisite, owner, readiness, or invalidation | Dependency ledger |
| Cross-module effect or invalidated acceptance | Major-change impact record |
| Proven capability or residual risk | Verification or operations evidence |

One change may affect several dimensions, but do not mechanically touch every document. A major-change record is an impact and re-verification entry, not a duplicate commit log or a full implementation diary.

## Completion Test

A documentation baseline is usable when a new authorized worker can determine, without chat history:

- what the project is and what current task or phase is active;
- which source decides each relevant dimension;
- which materials are historical, pending, local-only, or superseded;
- what can be changed now and what is protected or blocked;
- which downstream contracts or evidence must be updated when the current fact changes.

If those answers are already cheap and reliable, stop. More documents would be maintenance cost, not alignment.

## Relationship To Other References

This reference diagnoses and bootstraps the minimum documentation topology. `document-and-artifact-lifecycle.md` governs consumption and lifecycle after artifacts exist. `source-arbitration-and-baseline.md` resolves conflicts among sources. `module-delivery-and-coordination.md` governs task readiness and dependency status. `execution-scope-guard.md` decides whether the authorized task may write the recommended files.
