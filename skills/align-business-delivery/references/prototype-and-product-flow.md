# Prototype And Product Flow

Use this reference when a requirement needs page interaction, visible state, page-flow acceptance, or prototype-to-product convergence. It preserves business interaction while incrementally using real pages and components; it is not a backend-rule authority or a general visual-design guide.

## Effective Page Basis

Identify the current effective prototype or real-page basis by a path, version, update time, current decision, or user-confirmed wording. Compare it with the actual page and equivalent existing pages before implementation.

The prototype decides page entry, visible fields, interaction order, user-facing state, and page-flow acceptance. Existing pages and components decide the reusable implementation surface. Preserve the intended business interaction, but reuse current page structure and components first; a local prototype adjustment does not invalidate unseen page regions or justify a page rewrite.

When concrete prototype, page, or interaction material is supplied, consume it before proposing or changing implementation. Internally record the applicable parts of this minimum list:

- Page entry.
- Keep, modify, add, remove, and entry migration.
- Retained regions and explicitly unchanged behavior.
- Changed region and added or removed content.
- Fields, filters, and row actions.
- Dialog, drawer, workspace, or other local interaction surface.
- Open, save, close, confirm, reject, return, and error behavior.
- Data source and API/request/response mapping.

This list is internal for ordinary implementation. Show it only for a requested plan, review, or handoff. If the supplied material already states a concrete interaction, preserve it in the implementation basis rather than claiming its location or behavior is unavailable; ask only for a genuinely missing rule that changes the implementation. Consumption does not grant the prototype authority over backend rules and does not justify rewriting unchanged page regions.

For an implementation handoff, leave consumption proof that identifies the effective prototype basis, the real page/code basis inspected, the applicable checklist items used, conflicts or stale material ignored, and any intentional equivalent implementation. “Referenced the prototype” without this evidence is not consumption.

When a prototype conflicts with a business decision, code fact, or project convention, use `source-arbitration-and-baseline.md` to establish the effective basis.

## Prototype Investment

Choose the smallest artifact that makes the user-facing change unambiguous.

| Level | Use when | Output |
| --- | --- | --- |
| No prototype | Pure backend rule, internal validation, performance work, or a state fix with no page or operation-flow change | Rule, API impact, and acceptance evidence |
| Difference annotation | Copy, one field, one action, local visibility, or small layout change on an unchanged page | Current page basis, before/after difference, retained areas, acceptance checklist |
| Local prototype | New dialog, drawer, local workspace, or complex local interaction | Component interaction, placement, and open/save/close/error behavior |
| Full page prototype | New page, changed core object, information architecture, main entry, or most page areas | Effective full-page basis and page-level acceptance checklist |
| Cross-page flow prototype | Multi-page flow, coordinated clients, operation order, or state-controlled entries | Flow, key pages, entries, returns, visible states, and cross-end data flow |

Escalate from annotation when annotations no longer compose into one clear page, a main entry or operation order changes, a large page body changes, or users must follow a cross-page path. Converge accumulated annotations into one current full prototype, then move old differences to history.

After repeated prototype changes, converge the effective version by path, version, time, current wording, or another project-appropriate identifier. Synchronize the current explanation, change history, and handoff basis; do not require fixed filenames. Historical screenshots or differences cannot override the converged current basis.

## Page-To-Product Closure

For a page-facing change, cover the applicable page entry, filters/defaults, actions, status and summaries, fields and row actions, dialogs or workspaces, read-only/editable boundary, save or submit flow, data flow, API/response mapping, and equivalent existing-system behavior. Every visible input must correspond to a business decision that cannot reliably be inferred; system-derived or internal fields should not become manual inputs by default.

Incremental use of real pages and components must preserve the accepted interaction result. A static prototype decoration is not sufficient reason to bypass existing routes, permissions, component density, or reusable controls.

For a page-facing new capability, first validate entry, interaction, visible state, and data flow against the effective prototype. Once direction is stable, deepen review of backend state, transactions, idempotency, permissions, security, comments, and coupling. This sequencing does not waive an already confirmed backend prerequisite or shared contract.

Before page delivery, prefer runtime page evidence when it is reasonably available. Browser automation is one option, not an Align-owned requirement: the user may perform acceptance when time is limited or they already plan to inspect the page. For a familiar entry and simple change, state what changed, where to view it, and what remains unverified; do not emit a mechanical acceptance checklist. Add only brief test guidance when state combinations, test data, or multi-step interaction make manual verification non-obvious.

Without runtime evidence, do not describe code inspection, lint, build, or static checks as page acceptance. Report the actual evidence level and the unverified runtime boundary.

## Boundary

Do not use a prototype alone to decide backend rules, data ownership, state transitions, or API contracts. Those decisions belong to the applicable business-model, contract, and source-arbitration references. A workflow paradox belongs to the business-model/state responsibility; this reference may only record its page expression, such as a blocked entry, required return path, or visible state.

For a small page change, use no prototype or a difference annotation rather than starting a full page-flow process. Keep non-blocking prototype classification internal unless a plan, review, handoff, or full evidence is requested.
