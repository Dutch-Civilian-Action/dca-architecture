---
document_type: dca_reconstruction_reconciliation_method
status: current
scope: organisation-wide
purpose: turn distributed organisational and operational evidence plus live capture into reliable reusable shared organisational information
---

# DCA Reconstruction & Reconciliation Method

## Purpose

This method defines how DCA turns **distributed organisational and operational evidence**, plus live capture of new facts, into reliable, reusable shared organisational information while preserving provenance, uncertainty, source authority, and validation boundaries.

It exists because important DCA reality is often distributed across people, conversations, documents, repositories, spreadsheets, operational platforms, email, historical records, technical systems, runtime traces, and evidence of downstream use. Reuse requires more than collecting those sources: the underlying facts, identities, relationships, consequences, capability state, uncertainty, and provenance must be reconstructed and reconciled without silently inventing certainty.

The method applies to both:

- **Operational Reality** — what happens in DCA domain work;
- **Capability Reality** — what an organisational capability actually does, maintains, changes, supports, depends on, and enables.

See `capability-reality.md` for the capability evidence and monitoring boundary.

## Boundary with the Structure Method

The two methods answer different questions.

### DCA Structure Method — Reality to Requirements

**What does relevant current reality justify DCA needing?**

It derives organisational, information, structural, and system requirements from sufficiently established DCA reality.

### DCA Reconstruction & Reconciliation Method

**How does DCA turn distributed organisational and operational evidence into reliable shared organisational information?**

It governs reconstruction, matching, conflict handling, provenance, validation, persistence, consolidation, monitoring, and reuse.

Neither method replaces the other.

A bounded information-preservation, capability-monitoring, or reconciliation workflow may move forward as soon as its relevant requirement is sufficiently established. DCA does not need to reconstruct the whole organisation first.

**System support follows the relevant requirement once that requirement is sufficiently established.**

## Core information loop

```text
EXISTING / DISTRIBUTED EVIDENCE       NEW WORK / CHANGE
operational + capability sources      operational + capability activity
              │                                  │
              ▼                                  ▼
       RECONSTRUCTION                       LIVE CAPTURE
              │                                  │
              └──────────────┬───────────────────┘
                             ▼
                       RECONCILIATION
                    identity / matching
                  conflict / uncertainty
                  provenance / validation
                             │
                             ▼
              MAINTAINED-REALITY RECONCILIATION
               compare / classify / route / verify
                             │
                             ▼
                SHARED ORGANISATIONAL INFORMATION
                             │
                 ┌───────────┴───────────┐
                 ▼                       ▼
          OPERATIONAL USE          CAPABILITY / SHARED
          views / workflows        REALITY MAINTENANCE
                 │                       │
                 └───────────┬───────────┘
                             ▼
                       RECHECK + LEARN
                             │
                             ▼
                         NEW EVIDENCE
```

Shared organisational information is not necessarily one database. It is reliable organisation-held information that survives source fragmentation and can be retrieved and reused by the work or capability that depends on it.

## Audience and standalone-artifact contract

Artifacts produced during reconstruction and reconciliation have different audiences and must not be written as though those audiences share the same process context.

Before drafting or assigning an artifact, identify one primary audience:

| Audience | Artifact purpose | Required language boundary |
|---|---|---|
| Process maintainer / System & Structure | Preserve technical lineage, object state, routing, reconciliation, persistence, and implementation detail. | Technical method language is allowed. |
| General DCA reader | Understand an established or bounded account of organisational reality. | The artifact must stand on its own without unpublished reconstruction history. |
| Operational validator | Confirm, correct, qualify, or decline to confirm statements about work they know. | Ask only operational questions in normal working language; keep method and system mechanics in a separate maintainer artifact or task. |

Every general-reader synthesis and operational-validation artifact must open with enough visible context for independent use:

- what the artifact is and why it exists;
- its status and authority boundary;
- its intended audience and requested action, if any;
- the scope and relevant date or coverage period;
- how to read or respond to it;
- the material limitations, uncertainty, and validation state.

Do not assume the reader saw earlier drafts, process notes, correction packets, or private conversations. Relative or backward-looking wording such as “former”, “earlier”, “new”, “updated”, “remaining”, “now closed”, or “this run” is usable only when the artifact itself names the antecedent, date/period, and relevant source or publication. Otherwise state the fact directly in reader-visible terms.

Every shareable synthesis or validation artifact must include a human-usable source guide. For each material source or source group, provide as available:

- a human-readable source name or title;
- the account, mailbox, channel, Drive, repository, platform, or other container;
- the relevant date, date range, or coverage period;
- what the source supports;
- material limitations or known gaps;
- a stable reader-usable reference or link where access permits.

An internal evidence identifier may be included as a secondary trace key. It is not a sufficient source reference for an ordinary reader by itself.

An artifact that fails this contract remains a process draft. It is not ready for independent sharing, publication, or assignment to an operational validator.

## 1. Start with a bounded preservation or monitoring need

Do not begin by importing or instrumenting everything because a source exists or an API is available.

Ask:

- What fact, relationship, event, decision, consequence, capability state, dependency, or failure needs to remain usable?
- Who or what needs it later and for what work?
- What is lost today when it is not preserved or monitored?
- What minimum evidence is needed to support it?
- What uncertainty or variation must remain visible?

The target is **minimum useful preservation and monitoring**, not maximum collection.

## 2. Identify and preserve source evidence

Treat messages, documents, spreadsheets, platform records, exports, forms, photos, GitHub history, system/runtime traces, downstream-use evidence, and human reports as sources or representations of reality.

Do not confuse the source with the fact or capability state it may support.

Where useful, preserve:

- human-readable source name or title;
- source system or source type;
- source account, container, or organisational location;
- stable source reference or link where access permits;
- source timestamp, date range, or coverage period;
- what the source supports;
- known limitations or coverage gaps;
- raw source value where normalisation may remove meaning;
- person or role supplying the evidence;
- source-specific status;
- confidence or validation state.

Keep internal evidence identifiers as secondary trace keys. When a synthesis or validation artifact will be read outside the reconstruction process, render these fields as the human-usable source guide required by the audience contract.

A platform field, document, commit, or system trace is not automatically the organisational truth of the same name.

## 3. Reconstruct what the evidence says

Reconstruction recovers organisational or operational meaning that is distributed across sources.

This may include:

- identifying the person, organisation, partner, donation, activity, shipment, capability, or other subject involved;
- connecting related records, events, artifacts, decisions, or changes;
- recovering chronology;
- preserving the consequence of a communication, decision, implementation, or failure;
- identifying what is still unknown;
- separating source-specific state from shared organisational meaning;
- reconstructing what a capability actually does and maintains from observable evidence.

Reconstruction must not silently fill missing information.

## 4. Reconcile identity and meaning

Reconciliation determines when different pieces of evidence refer to the same underlying subject, organisational fact, capability state, or change.

Possible work includes:

- identity matching;
- duplicate detection;
- organisation/contact matching;
- relationship matching;
- event matching;
- source-to-canonical mapping;
- normalisation needed for comparison;
- conflict detection;
- distinguishing changed reality from inconsistent evidence;
- connecting a system or architecture change to the maintained capability it actually affects.

A candidate match or interpretation is not confirmed merely because it looks plausible.

## 5. Preserve conflict, uncertainty, and source differences

When evidence conflicts, do not choose silently.

Keep visible where relevant:

- conflicting source values;
- confidence level;
- unresolved identity;
- unknown relationship;
- missing evidence;
- platform-specific status;
- historical versus current value;
- direct fact versus derived interpretation;
- intended capability versus evidenced capability;
- implementation activity versus demonstrated use or outcome.

Absence of evidence is not evidence of absence.

Normalisation should make comparison possible without erasing meaningful source differences.

## 6. Validate only at the required boundary

Not every field, capability claim, or AI-assisted match requires the same validation.

Define what may be:

- accepted directly from an authoritative source;
- accepted when corroborated;
- inferred provisionally;
- queued for review;
- confirmed only by the role closest to the work;
- left unresolved because the available evidence is insufficient.

Validation should be proportional to the consequence of being wrong.

When the validator is an operational person, ask only about the work they can know directly: what they did, saw, decided, received, handed over, expected, or recorded; what varies; what is missing; what currently happens; and where a concrete record or example exists. Always allow the response **“Not mine to confirm.”**

Do not ask an operational validator to interpret reconstruction objects, evidence-link types, schemas, routing, promotion, architecture, reconciliation mechanics, or implementation fields. System & Structure retains responsibility for those technical translations in its own artifact or task.

If the validator corrects or qualifies wording, restate the changed operational wording and return it for confirmation before treating that exact wording as validated. A response equivalent to “correct” or “no change” is a complete validation result when its scope is clear; do not manufacture a correction or extra work.

## 7. Reconcile sufficiently established current findings with maintained reality

Validation establishes what the evidence supports. It does not by itself establish whether the result is new, already represented, contradictory, historical only, proposed future state, or owned by another organisational destination.

For every sufficiently established finding that may affect current shared reality:

1. resolve the current authoritative target and its revision;
2. compare the finding atomically with what that target already represents;
3. classify the reconciliation outcome;
4. route the finding to the correct organisational home;
5. make only the smallest supported change;
6. persist and re-read or otherwise verify the target;
7. record the outcome, target, revision, actor, time, provenance, and remaining uncertainty.

Use this controlled outcome vocabulary:

- `already_represented` — the maintained target already contains the same material meaning;
- `confirmation_only` — new evidence strengthens an existing maintained claim without requiring a text change;
- `addition` — established current meaning is absent and must be added;
- `correction` — established evidence changes maintained meaning;
- `qualification` — maintained meaning remains valid only with a boundary, variation, or exception;
- `conflict_unresolved` — sources still conflict and no supported write may pretend the conflict is settled;
- `historical_only` — the finding belongs in historical lineage, not current maintained reality;
- `proposed_future` — the finding describes intention, proposal, or expected future state rather than current reality;
- `alternate_destination` — the finding is established but belongs somewhere other than the candidate maintained target;
- `not_ready` — evidence, validation, authority, or target rules are insufficient.

A routing recommendation is not write authority. The target's own identity, validation, naming, and write rules continue to apply.

A source review or validation thread may close when the outcome is a verified no-change result such as `already_represented` or `confirmation_only` and any target-required evidence/status write has also been persisted and verified. A change-bearing thread closes only after the supported change has been persisted and verified. A `conflict_unresolved` or `not_ready` case remains open or is transferred to an explicit validation/reconciliation item.

A reviewer response equivalent to “correct” is recorded as validation evidence. The later maintained-target comparison independently determines whether the supported finding is already represented, confirms existing meaning, or requires an addition, correction, or qualification. Do not manufacture a change merely to produce visible activity, and do not suppress a real maintained-target change merely because the validated wording was correct.

The provider-independent implementation contract is:

`Dutch-Civilian-Action/dca-ai/workflows/reconcile-established-findings-into-maintained-reality.md`

Both full historical reconstruction and incremental reality maintenance must use that same handoff. Historical reconstruction performs it only after source-first reconstruction, self-evaluation, and required human validation; it must not read current maintained reality early in a way that biases reconstruction.

## 8. Persist the reconciled result with provenance

Once sufficiently supported, persist the reusable shared result in the appropriate organisation-held record, document, architecture source, or system.

Preserve enough provenance that DCA can later understand:

- where the information came from;
- what was changed or normalised;
- what remains uncertain;
- who or what validated it;
- when it was last checked;
- which source-specific values should still be retained.

Persistence does not mean deleting historical evidence or flattening all sources into one record.

## 9. Consolidate justified consequences

New activity, evidence, corrected identity, capability change, system event, or architecture change may affect connected organisation-held information.

Where justified, consolidation applies those consequences so connected work remains coherent.

Examples may include:

- updating an outreach cycle after a real interaction;
- linking a donation to the correct contact or organisation;
- applying a durable contactability consequence;
- connecting a partner fact to the organisation that operational work retrieves later;
- updating current S&S capability reality after a verified architecture or system change;
- creating a review item when a consequence cannot be applied safely.

Consolidation must remain auditable and must not invent downstream consequences that the evidence does not support.

## 10. Expose shared information for use

Shared information is valuable when the people and workflows that need it can actually retrieve and use it.

Possible retrieval surfaces include:

- Airtable interfaces or views;
- operational dashboards;
- reports;
- AI-assisted retrieval;
- Slack-linked views;
- workflow inputs;
- communication and reporting inputs;
- capability-health or handover views.

The retrieval surface is replaceable. The underlying organisational meaning and provenance should remain intelligible independently of the tool.

## 11. Monitor material capability change where needed

Where a capability needs to remain reconstructable over time, repeated reconstruction should evolve into proportionate monitoring.

For System & Structure, monitoring may compare:

- current Google Drive artifacts/routing against current authority;
- GitHub architecture and AI specifications against organisation-facing guidance;
- Slack validation/alignment evidence against maintained reality;
- Airtable/system state against documented requirements;
- automation/integration outcomes against intended behaviour;
- downstream use against claims that a capability is functioning.

Monitor **material change**, not every action.

Surface a finding when evidence suggests a new or changed capability, authority drift, stale documentation, system/document mismatch, unresolved dependency, automation failure, key-person continuity risk, repeated reconstruction, or an output that is produced but not actually used.

## 12. Recheck and learn

New evidence may confirm, correct, split, merge, or invalidate an earlier reconciliation or capability interpretation.

Reconciliation is therefore not a one-time cleanup exercise.

```text
Capture / Reconstruction
→ Reconciliation
→ Maintained-Reality Reconciliation
→ Shared Information
→ Operational / Capability Use
→ New Evidence
→ Recheck
```

Where a repeated reconciliation or monitoring problem reveals a missing organisational or information requirement, feed that finding into the DCA Structure Method.

## Critical distinctions

Keep these distinctions explicit:

- source record ≠ operational fact;
- artifact created ≠ organisational adoption;
- GitHub commit ≠ organisational decision unless current authority supports it;
- Slack discussion ≠ validated organisational fact automatically;
- technical implementation ≠ organisational structure;
- tool presence ≠ demonstrated capability;
- activity ≠ successful outcome;
- intended mandate ≠ current capability reality;
- duplicate candidate ≠ confirmed same entity;
- platform status ≠ organisational relationship status;
- reconstruction ≠ invention;
- reconciliation ≠ forced certainty;
- reconciled ≠ manually validated in every case;
- clean data ≠ complete organisational reality;
- shared operational record ≠ final Operating Model;
- technical canonical record ≠ authority over upstream reality;
- AI-supported match ≠ organisational fact unless its validation boundary is satisfied.

## Current implementation mapping

The method is implementation-independent. Current DCA systems already contain working examples of parts of it.

### `2 | DCA Relationships & Workflows`

Current examples include organisation/contact identity, relationship records, outreach activities and cycles, contact intake, review queues, source references, validation state, cleanup logs, and consolidation markers.

### `DCA Evidence & Reconciliation`

Former display name: `DCA Integrations & Reconciliation`. Resolve the same base through `dca-ai/context/airtable-workspace-map.md`; this name correction does not change its authority or promote staging evidence.

Current examples include platform-source staging, sync-run tracking, Donorbox source records, Mailchimp source records, integration review queues, historical Reconstruction Objects, human-validation state, destination routing, maintained-reality comparison outcomes, target references/revisions, and persistence verification.

The reconstruction staging layer records what was established and what happened downstream; it does not become a second canonical truth source.

### System & Structure Capability Reality

Relevant observable evidence may include Google Drive artifacts/revisions, GitHub commits/ADRs/specifications, Slack alignment/validation/correction evidence, Airtable/system state, automation/runtime evidence, and downstream use of S&S outputs.

These are evidence surfaces, not automatic organisational authority.

### Other DCA sources

Google Workspace, Gmail, Slack, WhatsApp, GitHub, spreadsheets, platform exports, operational documents, system/runtime traces, downstream-use evidence, and human input may all provide evidence or live capture.

They do not become canonical organisational truth merely because they are the source.

### DCA AI

AI may support extraction, comparison, matching, classification, review preparation, consolidation checks, retrieval, and capability monitoring.

AI must preserve source authority and uncertainty and must not silently resolve identity, conflict, adoption, outcome, or organisational meaning beyond the permitted validation boundary.

AI may execute the provider-independent maintained-reality reconciliation handoff, but completion requires a recorded comparison outcome and verified persistence where a target write is required. Detection, a generated draft, a task status, or a Slack post is not persistence evidence.

## What this method does not do

This method does not:

- define the final DCA Operating Model;
- define a universal central database;
- require all sources to be copied into one platform;
- redesign existing Airtable bases merely because this method exists;
- require organisation-wide reconstruction before bounded reconciliation can proceed;
- make every source field a shared organisational field;
- make every repeated data-cleanup or monitoring step a permanent procedure;
- treat all observable activity as meaningful capability evidence.

## Short rule

When DCA information or capability reality is distributed or inconsistent:

**Preserve the evidence and what kind of evidence it is, reconstruct the underlying organisational or operational reality, reconcile only what the evidence supports, keep uncertainty visible, persist the reusable result with provenance, and recheck it when new reality appears.**
