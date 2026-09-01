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

- source system or source type;
- source reference or link;
- source timestamp;
- raw source value where normalisation may remove meaning;
- person or role supplying the evidence;
- source-specific status;
- confidence or validation state.

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

A source review or validation thread may close immediately when the outcome is a verified no-change result such as `already_represented` or `confirmation_only`. A change-bearing thread closes only after the supported change has been persisted and verified. A `conflict_unresolved` or `not_ready` case remains open or is transferred to an explicit validation/reconciliation item.

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

### `DCA Integrations & Reconciliation`

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
