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

## Evidence Levels

Report the highest level supported by fresh evidence:

1. Static code or document check.
2. Automated unit or integration check.
3. Generated-artifact check.
4. Local browser or client check.
5. Local service integration.
6. Simulated-environment verification.
7. Real target-environment acceptance.

Lower-level evidence must never be described as higher-level acceptance. Report the checks performed, their results, missing higher-level evidence, and residual risk. Scale the evidence to the delivery risk, but do not claim success without fresh evidence for the declared boundary.

## Truthful Completion

A delivery conclusion states what changed, the affected modules or assets, the business behavior delivered, the evidence level, unresolved items, and residual risk. Distinguish a completed technical batch, a delivered stage, and a completed whole capability. When evidence is partial, say exactly what is complete and retain the remaining boundary as incomplete rather than using a broad completion label.

For interrupted or mixed batches, keep implementation state, business blocking priority, and current delivery membership separate. "Coded," "automated checks passed," "runtime verified," "accepted by the user," and "eligible for this commit" are not interchangeable completion claims.
