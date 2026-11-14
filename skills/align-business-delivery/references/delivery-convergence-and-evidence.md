# Delivery Convergence And Evidence

Use this reference before declaring a business delivery complete, and at a midpoint when several increments make drift likely. It controls convergence and truthful evidence claims; it does not duplicate general build, test, review, or release procedures.

## Midpoint Convergence

Run a midpoint review when multiple increments have accumulated, current documents and implementation may have diverged, workflow or page weight has materially grown, completion statements conflict, a major next stage is approaching, or the user requests a state review. It is not a routine status report.

Review:

- Whether current basis, historical trace material, implementation notes, and handoff entry are distinguishable.
- Whether documents claim complete work that implementation or evidence does not support, or the reverse.
- Whether the stated capability is larger than the actual supported boundary.
- Whether temporary compatibility layers, legacy fields or protocols, and deferred gaps have an owner or removal decision.
- Whether the next stage covers the known gaps and residual risks.

## Business Consistency Review

Trigger completion-scope comparison when preparing to claim a fix or feature complete, commit or push, formally hand off delivery, finish a substantial implementation batch, or answer a request to review omissions, expansion, or mixed-in work. Ordinary progress updates, one-file edits, and intermediate test results do not trigger a full convergence review.

For simple work, compare internally: what the user requested, what actually changed, whether anything was omitted or added, and what the evidence covers. For complex, multi-module, or cross-repository work, explicitly compare the frozen package, task ledger, prototype, or shared contract as applicable. Reconcile the changed behavior with its accepted business goal, relevant state or contract boundary, current scope, and declared delivery level. Include adjacent unaffected behavior only when the package's acceptance condition requires it. A locally working artifact is not grounds to claim a broader module, client, integration, or operational capability.

State the actual capability boundary:

- Supported now.
- Not yet verified.
- Not supported or intentionally deferred.
- Residual risk and its owner, decision, or next-stage coverage.

## Requested Review Coverage

For an explicitly requested whole-package review, pass the current change set, applicable project or reference standards, and accepted corrections to the reviewer. Recover the set from the active task and current diff or artifacts; the user's named example is a starting point, not a smaller replacement scope. Inspection methods remain with the specialist.

Compare the returned review's actual coverage and findings with that set, including applicable peers when a finding reveals a repeated issue. The result states supported findings and remaining coverage gaps; a selected object's compliance does not establish the whole package's compliance. Keep unreviewed parts unfinished instead of waiting for the user to name each one. This is not a new report format, whole-repository audit, per-turn check, or authorization to fix findings. An explicitly local review retains its local boundary.

## Evidence Levels

For each material delivery conclusion, state what was verified, by which method, against which artifact or version and environment, and what remains unverified. Evidence may come from static code or document inspection, automated unit or integration checks, generated-artifact inspection, local browser or client execution, local service integration, simulated-environment checks, or real target-environment acceptance. These cover different claims; the strongest available result does not establish the whole delivery.

A unit test or static inspection does not establish page runtime acceptance; local or simulated checks do not establish target-environment acceptance. Report the checks performed, results, coverage gaps, and residual risk. Scale evidence to the declared delivery risk, without forcing every method, a fixed table, or a full-stack checklist for each task. Do not claim success without fresh evidence for that conclusion's boundary.

Check what the evidence actually covers, not just how many checks passed. Apply `source-arbitration-and-baseline.md` when a test bypasses the disputed business step, and `document-and-artifact-lifecycle.md` when a handoff's operational usability is in question.

Bind the claim to the artifact actually delivered: its final contents, entry or invocation, applicable environment, and destination. A temporary copy, earlier revision, or different branch establishes only that version's result; reconcile differences before claiming the delivered version passed. After changing a previously checked artifact, repeat the affected check or disclose the unverified delta. Verification methods remain with the specialist; this does not require a checksum, new report, or user-run checklist for every change.

## Truthful Completion

A delivery conclusion states what changed, the affected modules or assets, the business behavior delivered, the evidence level, unresolved items, and residual risk. Distinguish a completed technical batch, a delivered stage, and a completed whole capability. When evidence is partial, say exactly what is complete and retain the remaining boundary as incomplete rather than using a broad completion label.

Describe changes against the relevant pre-change baseline: distinguish added behavior, a corrected pre-existing defect, and reversal of a defect introduced in this batch. Do not present unchanged behavior or an unverified historical incident as a delivered fix. Keep release and deployment status separate from the code change.

For interrupted or mixed batches, keep implementation state, business blocking priority, and current delivery membership separate. "Coded," "automated checks passed," "runtime verified," "accepted by the user," and "eligible for this commit" are not interchangeable completion claims.
