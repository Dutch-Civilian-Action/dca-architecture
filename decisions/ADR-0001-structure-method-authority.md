# ADR-0001 — Replace the Fixed Layer / Anchor Structure Method

**Status:** Accepted  
**Date:** 2026-08-23

## Context

The earlier DCA `Structure Method` required organisational facts to be processed through a predetermined architecture:

```text
Fact → Layer → Entry Point → Anchor → Minimal Data → Event → Connection → System Output
```

It treated five Layers, their Entry Points, and their Anchors as stable system requirements and instructed later structure to remain aligned with that model.

Subsequent audited Operational Reality, Derived Organisational Reality, workflow reconstruction, and live domain work established a stricter evidence boundary: DCA should reconstruct recurring work and derive organisational requirements before fixing structure or technical implementation.

The current organisation-wide sequence is:

```text
Operational Reality
→ Shared Organisational Reality
→ Recurring Workflows
→ Organisational Requirements
→ Structure + Information Requirements, where justified
→ System Requirements, where justified
→ System Support
→ Live Operational Use
→ New Operational Reality
```

Keeping both methods as current authority would create a contradiction: the older method predetermines the structural categories through which reality must pass, while the newer method requires structure to remain corrigible until justified by reality.

## Decision

The fixed Layer / Entry Point / Anchor `Structure Method` is no longer current DCA structural authority.

The current organisation-wide derivation method is:

`organisation/shared-foundations/reality-to-requirements-method.md`

The new method is a **method**, not a replacement Operating Model.

It does not fix:

- a final set of DCA functions;
- a final organisational chart;
- final roles;
- final layers or anchors;
- a permanent Airtable schema;
- one universal DCA cycle;
- a final technical architecture.

## Consequences

- Existing pilots, system objects, schemas, and documentation created under the previous model are not automatically invalidated.
- Their current authority must be evaluated from operational evidence, lifecycle status, and actual adoption.
- Fixed layer/anchor vocabulary must not be used as baseline organisational reality unless independently supported.
- AI instructions that require the old fixed model must be audited and updated before they are treated as current.
- The old Google Drive `Structure Method` should be marked superseded and archived; its legacy file currently requires manual handling because the connected app cannot modify that file ID.
- Future Operating Model work must be derived from sufficiently validated organisational evidence rather than created as the immediate replacement for the old model.

## Rationale

This decision preserves the useful discovery made by the old architecture work without allowing its structural assumptions to override newer evidence.

The objective is not to replace one fixed model with another. It is to establish a method by which DCA can progressively discover, test, and revise the structure it actually needs.
