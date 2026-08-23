---
document_type: dca_reconstruction_reconciliation_method
status: current
scope: organisation-wide
purpose: turn distributed operational evidence and live capture into reliable reusable shared organisational information
---

# DCA Reconstruction & Reconciliation Method

## Purpose

This method defines how DCA turns distributed operational evidence and live capture into reliable, reusable shared organisational information while preserving provenance, uncertainty, source authority, and validation boundaries.

It exists because important DCA reality is often distributed across people, conversations, documents, spreadsheets, operational platforms, email, historical records, and technical systems. Reuse requires more than collecting those sources: the underlying facts, identities, relationships, consequences, uncertainty, and provenance must be reconstructed and reconciled without silently inventing certainty.

## Boundary with the Structure Method

The two methods answer different questions.

### DCA Structure Method — Reality to Requirements

**What does current reality justify DCA needing?**

It derives organisational, information, structural, and system requirements from operational reality.

### DCA Reconstruction & Reconciliation Method

**How does DCA turn distributed operational evidence into reliable shared organisational information?**

It governs reconstruction, matching, conflict handling, provenance, validation, persistence, consolidation, and reuse.

Neither method replaces the other.

A bounded information-preservation or reconciliation workflow may move forward as soon as its relevant requirement is sufficiently established. DCA does not need to reconstruct the whole organisation first.

**System support follows the relevant requirement once that requirement is sufficiently established.**

## Core information loop

```text
                     DCA OPERATIONAL REALITY
                            │
              ┌─────────────┴─────────────┐
              │                           │
              ▼                           ▼
       RECONSTRUCTION                 LIVE CAPTURE
       recover existing              record new facts
       distributed reality           as work happens
              │                           │
              └──────────┬────────────────┘
                         ▼
                  RECONCILIATION
              identity / matching
              conflict / uncertainty
              provenance / validation
                         │
                         ▼
               SHARED OPERATIONAL RECORD
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
        OPERATIONAL USE       SHARED REALITY
        views / workflows     reconstruction
              │                     │
              └─────────┬───────────┘
                        ▼
                 RECHECK + LEARN
                        │
                        ▼
               NEW OPERATIONAL REALITY
```

A shared operational record is not necessarily one database. It is the reliable organisation-held information that survives source fragmentation and can be retrieved and reused by the work that depends on it.

## 1. Start with a bounded preservation need

Do not begin by importing everything because a source exists or an API is available.

Ask:

- What operational fact, relationship, event, decision, or consequence needs to remain usable?
- Who needs it later and for what work?
- What is lost today when it is not preserved?
- What minimum evidence is needed to support it?
- What uncertainty or variation must remain visible?

The target is **minimum useful preservation**, not maximum collection.

## 2. Identify and preserve source evidence

Treat messages, documents, spreadsheets, platform records, exports, forms, photos, system records, and human reports as sources or representations of reality.

Do not confuse the source with the fact it may support.

Where useful, preserve:

- source system or source type;
- source reference or link;
- source timestamp;
- raw source value where normalisation may remove meaning;
- person or role supplying the evidence;
- source-specific status;
- confidence or validation state.

A platform field is not automatically the organisational truth of the same name.

## 3. Reconstruct what the evidence says

Reconstruction recovers the operational meaning that is distributed across sources.

This may include:

- identifying the person, organisation, partner, donation, activity, shipment, or other subject involved;
- connecting related records or events;
- recovering chronology;
- preserving the consequence of a communication or decision;
- identifying what is still unknown;
- separating source-specific state from shared organisational meaning.

Reconstruction must not silently fill missing information.

## 4. Reconcile identity and meaning

Reconciliation determines when different pieces of evidence refer to the same underlying subject or organisational fact.

Possible work includes:

- identity matching;
- duplicate detection;
- organisation/contact matching;
- relationship matching;
- event matching;
- source-to-canonical mapping;
- normalisation needed for comparison;
- conflict detection;
- distinguishing changed reality from inconsistent evidence.

A candidate match is not a confirmed identity merely because it looks plausible.

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
- direct fact versus derived interpretation.

Absence of evidence is not evidence of absence.

Normalisation should make comparison possible without erasing meaningful source differences.

## 6. Validate only at the required boundary

Not every field requires manual confirmation, and not every AI-assisted match requires the same validation.

Define what may be:

- accepted directly from an authoritative source;
- accepted when corroborated;
- inferred provisionally;
- queued for review;
- confirmed only by the role closest to the work;
- left unresolved because the available evidence is insufficient.

Validation should be proportional to the consequence of being wrong.

## 7. Persist the reconciled result with provenance

Once sufficiently supported, persist the reusable shared result in the appropriate organisation-held record or system.

Preserve enough provenance that DCA can later understand:

- where the information came from;
- what was changed or normalised;
- what remains uncertain;
- who or what validated it;
- when it was last checked;
- which source-specific values should still be retained.

Persistence does not mean deleting historical evidence or flattening all sources into one record.

## 8. Consolidate operational consequences

A new activity, message, platform event, or corrected identity may affect other organisation-held records.

Where justified, consolidation applies those consequences so that connected work remains coherent.

Examples may include:

- updating an outreach cycle after a real interaction;
- linking a donation to the correct contact or organisation;
- applying a durable do-not-contact consequence;
- connecting a partner fact to the organisation that operational work retrieves later;
- creating a review item when a consequence cannot be applied safely.

Consolidation must remain auditable and must not invent downstream consequences that the evidence does not support.

## 9. Expose the shared information for operational use

Shared information is valuable when the people and workflows that need it can actually retrieve and use it.

Possible retrieval surfaces include:

- Airtable interfaces or views;
- operational dashboards;
- reports;
- AI-assisted retrieval;
- Slack-linked views;
- workflow inputs;
- communication and reporting inputs.

The retrieval surface is replaceable. The underlying organisational meaning and provenance should remain intelligible independently of the tool.

## 10. Recheck and learn

New evidence may confirm, correct, split, merge, or invalidate an earlier reconciliation.

Reconciliation is therefore not a one-time cleanup exercise.

```text
Capture / Reconstruction
→ Reconciliation
→ Shared Record
→ Operational Use
→ New Evidence
→ Recheck
```

Where a repeated reconciliation problem reveals a missing organisational or information requirement, feed that finding into the DCA Structure Method.

## Critical distinctions

Keep these distinctions explicit:

- source record ≠ operational fact;
- duplicate candidate ≠ confirmed same entity;
- platform status ≠ organisational relationship status;
- reconstruction ≠ invention;
- reconciliation ≠ forced certainty;
- reconciled ≠ manually validated in every case;
- clean data ≠ complete operational reality;
- shared operational record ≠ final Operating Model;
- technical canonical record ≠ authority over upstream reality;
- AI-supported match ≠ organisational fact unless its validation boundary is satisfied.

## Current implementation mapping

The method is implementation-independent. Current DCA systems already contain working examples of parts of it.

### `2 | DCA Relationships & Workflows`

Current examples include organisation/contact identity, relationship records, outreach activities and cycles, contact intake, review queues, source references, validation state, cleanup logs, and consolidation markers.

Its role is not defined by Airtable itself. It currently implements parts of the shared relationship, activity, review, and operational-use layer.

### `DCA Integrations & Reconciliation`

Current examples include platform-source staging, sync-run tracking, Donorbox source records, Mailchimp source records, and integration review queues.

It currently implements parts of platform ingestion, staging, matching, reconciliation, and review.

### Other DCA sources

Google Workspace, Gmail, Slack, WhatsApp, spreadsheets, platform exports, operational documents, and human input may all provide evidence or live capture.

They do not become canonical organisational truth merely because they are the source.

### DCA AI

AI may support extraction, comparison, matching, classification, review preparation, consolidation checks, and retrieval.

AI must preserve source authority and uncertainty and must not silently resolve identity, conflict, or organisational meaning beyond the permitted validation boundary.

## What this method does not do

This method does not:

- define the final DCA Operating Model;
- define a universal central database;
- require all sources to be copied into one platform;
- redesign existing Airtable bases merely because this method exists;
- require organisation-wide reconstruction before bounded reconciliation can proceed;
- make every source field a shared organisational field;
- make every repeated data-cleanup step a permanent procedure.

## Short rule

When DCA information is distributed or inconsistent:

**Preserve the evidence, reconstruct the underlying reality, reconcile only what the evidence supports, keep uncertainty visible, persist the reusable result with provenance, and recheck it when new reality appears.**
