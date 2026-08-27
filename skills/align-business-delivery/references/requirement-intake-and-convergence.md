# Requirement Intake And Convergence

Use this reference when business input is vague, incomplete, cross-module, or needs to become a reviewable baseline before implementation detail is frozen. It does not prescribe general interviewing, planning, or execution strategy.

## Start Modes

Choose the start mode from the user's request and the available material.

| Mode | Use when | Output |
| --- | --- | --- |
| Reviewable draft baseline | The user needs a complete PRD, product proposal, or prototype baseline from incomplete material | A normally readable, complete draft that makes uncertainty visible without presenting it as frozen fact |
| Linear organize-only | The user asks to organize existing material, avoid expansion, or confirm items in sequence | A faithful, ordered consolidation; record gaps without filling them with new business rules |

Both modes begin with current behavior before target behavior when existing facts are available. In either mode, do not answer a checkable question with a guess: inspect available documents, code, schema, API, prototype, configuration, or runtime evidence first. State what was checked, the resulting fact, and what remains unverified.

## Readable Draft And Matter List

Keep the PRD, product proposal, or prototype body in normal readable structure. Do not force a label onto every sentence. Internally maintain these distinct matter categories:

- Confirmed facts: business decisions or instructions explicitly confirmed by the responsible owner.
- Code facts: verified current behavior, schema, configuration, dependency, or source-history facts.
- AI inference: a logical deduction from existing evidence that has not been confirmed by the business owner.
- Recommendation: a preference recommendation among multiple feasible options; it becomes a confirmed basis only after explicit adoption.
- Pending confirmation: a decision, fact, or boundary that cannot yet be verified or frozen.
- Out of scope: a discovered item that is not authorized for the current baseline or task.

For normal output, express populated categories in one compact matter table or list and combine empty categories into a short note such as "no code facts or out-of-scope items were verified." Expand all six category headings only for a formal baseline audit, full evidence, handoff that needs category-by-category traceability, or an explicit user request. This presentation rule never permits merging one category's meaning into another.

Use an inline label in the body only when an ambiguity is consequential: it could change business meaning, ownership, state, scope, acceptance, or a later design decision. Other uncertainty belongs in the matter list so the main document remains reviewable.

## Convergence

Build the first useful baseline from available evidence without waiting for every detail. A complete draft baseline may describe goals, actors, main modules, primary flows, assumptions, and acceptance direction, provided unconfirmed content remains in its proper matter-list section.

For linear organize-only work, preserve the supplied order and meaning. Separate confirmed material from gaps, but do not turn gaps into inferred rules or recommendations unless the user changes the mode.

As facts are verified or decisions are made, promote only the affected item: a confirmed decision may replace a pending item, inference, or recommendation. Do not silently rewrite earlier material or treat a draft as the current effective implementation basis before source arbitration establishes that basis.

## Interaction Boundary

Keep non-blocking classification and consolidation internal unless the user asks for a plan, review, handoff, or full evidence. Ask only for decisions that block the main baseline; do not repeat facts already available in the supplied material.

### Stepwise Confirmation

When the user asks to confirm items slowly, linearly, module by module, or one by one, process one module or sub-item at a time and only one per round. Ask at most three questions, and only when they block the current item. Record other modules and future ideas without expanding them into the current answer or task. Move to the next item only after the current item is confirmed, explicitly deferred, or blocked.

### Mixed Intent

Internally normalize a mixed message into:

- Current execution request.
- Conceptual question only.
- Candidate idea.
- Pending or unconfirmed item.
- Later-stage work.
- Explicitly excluded from this round.

Execute only the current authorized request. A question, suggestion, or future possibility does not become a deliverable merely because it appears beside an imperative.

### Current Feedback Batch

Treat the user's latest turn, referenced passage, or explicitly named recent turns as the current feedback batch. Prefer the business object identified by the quotation or annotation; do not pull unrelated historical issues into the batch.

First identify what each quotation or annotation is doing: it may name the current business object, define the current problem scope, mark a historical execution cutoff, dispute an old conclusion, supply evidence, or locate the parent request. Do not assume the quoted text is the whole current scope. Ordinary feedback about a current object should be handled directly; it does not require mechanically reopening the entire history.

When the user says "up to here," "at this point," or asks to combine a quoted node with the question it answered, locate the original turn and its parent user request. Use the parent request as the scope and the quoted text as the time cutoff, then reconstruct each in-scope item's state at that cutoff. Do not backdate issues first discovered after the cutoff. When original records and current artifacts are available, inspect them instead of relying only on a compact summary or memory.

Track each relevant item as pending, in progress, fixed, superseded, confirmed regression, or out of scope. Fixed or superseded items do not return to pending without new regression evidence. When a conclusion reverses, record the new basis, the old conclusion it invalidates, and the directly affected downstream items. Older screenshots, prototypes, plans, and feedback remain history unless the current batch promotes them back into the effective basis.

Keep the full feedback ledger internal during routine work. Unless the user requests a plan, review, or handoff, report only the current affected item, any reversal evidence, the next action, and a short note that unaffected or closed items retain their state.

Use `source-arbitration-and-baseline.md` when available sources disagree about the current effective basis. Use `prototype-and-product-flow.md` only when the baseline needs page interaction or visible-flow expression. Use `document-and-artifact-lifecycle.md` when the evidence or artifacts themselves have unclear current status or consumer.
