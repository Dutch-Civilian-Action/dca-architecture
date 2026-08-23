---
document_type: dca_authority_map
status: current
scope: organisation-wide
purpose: distinguish current authority, working sources, archived implementation, and superseded structure
---

# DCA Authority Map

## Purpose

DCA contains current reality, working interpretation, architecture, historical models, pilots, implementation records, and archived technical material. These must not be treated as one authority level.

This map exists so people and AI can determine what a document may legitimately authorise.

The governing rule is:

**A document's detail, confidence, age, or title does not establish authority. Authority depends on its current status, scope, and relationship to validated organisational reality.**

## Current shared methods

### DCA Structure Method — Reality to Requirements

Canonical architecture specification:

`organisation/shared-foundations/reality-to-requirements-method.md`

Status: **CURRENT**

Role: defines how DCA moves from operational reality toward justified organisational, information, structural, and system responses.

It does not define a final Operating Model or a fixed set of functions, layers, anchors, roles, procedures, or system objects.

### DCA Reconstruction & Reconciliation Method

Canonical architecture specification:

`organisation/shared-foundations/reconstruction-reconciliation-method.md`

Status: **CURRENT**

Role: defines how DCA turns distributed operational evidence and live capture into reliable reusable shared organisational information while preserving provenance, uncertainty, conflicts, and validation boundaries.

Authority boundary: it does not define the Operating Model, a universal central database, or a permanent platform schema. It governs the information-reliability process, not the final organisational structure.

The methods have different questions:

- Structure Method: **What does reality justify DCA needing?**
- Reconstruction & Reconciliation Method: **How does distributed evidence become reliable shared organisational information?**

## Current organisational reality sources

### DCA Operational Reality — 2nd Pass

Status: **CURRENT VALIDATION SOURCE**

Role: current organisation-wide reconstruction and validation of operational reality.

Authority boundary: operational claims remain subject to their explicit evidence/validation/uncertainty status. The document does not itself define future structure.

### DCA Derived Organisational Reality

Status: **CURRENT WORKING EVIDENTIAL SOURCE**

Role: evidence-backed organisational inference derived from operational reality.

Authority boundary: explicitly not the Operating Model. It does not define essential functions, layers, roles, procedures, system objects, or future structure.

## Current working organisational material

### DCA System & Structure — Organisation-Wide Plan

Status: **WORKING**

Role: navigation and execution plan for moving from shared reality through workflow visibility, information preservation and reconciliation, requirements, architecture, system support, live use, and learning.

Authority boundary: not the Operating Model and not final technical architecture.

### DCA Organisational Concepts & Relationships

Status: **WORKING / CONCEPT MODEL**

Role: develops shared concepts and critical distinctions such as Organisation ≠ Structure, Structure ≠ System, Workflow ≠ Procedure, Function ≠ Role, and source record ≠ organisational fact.

Authority boundary: useful source material, but not yet a canonical ontology or final organisational model. It should define concepts and relationships, not compete with the two current methods.

## Superseded predecessor material

### DCA Workflow-Based Structural Alignment Logic

Status: **SUPERSEDED AS ACTIVE METHOD / PREDECESSOR SOURCE**

Role: predecessor working method that made recurring workflows, dependencies, consequences, candidate functions, requirements, testing, and feedback visible.

Its useful logic is incorporated into the current DCA Structure Method — Reality to Requirements. It must not be treated as a competing current method.

In particular, its older wording **“System Support Comes Later”** is superseded by:

**System support follows the relevant requirement once that requirement is sufficiently established.**

## Superseded structural model

The following documents belong to the pre-reality-first model and are **SUPERSEDED AS CURRENT STRUCTURAL AUTHORITY**:

- DCA Operating Model — From Circles to System Layers
- Definitions — Core
- Definitions — Extended
- Structure Method — fixed Layer / Entry Point / Anchor method
- Structure Template
- Layer Template
- Pilot Template

These are preserved together under the Drive area:

`Superseded System & Structure Model (pre-reality-first)`

They remain historical evidence of prior architecture and may contain reusable distinctions or implementation history. They must not be used to require fixed layers, entry points, anchors, or system objects in current structural derivation.

## Archived technical implementation

Technical documents derived from the earlier model may remain useful as implementation history, but archive location does not make them current technical authority.

Examples include:

- System Logic — Overview
- DCA System — Airtable Schema

Current location: Systems & Data archive areas.

Status: **ARCHIVED / REQUIRES REVALIDATION BEFORE REUSE**

A table, field, identifier, system object, or technical relationship from these documents may be reused only when the current operational requirement and current architecture still justify it.

## Current implementation examples

Current Airtable and integration structures may implement parts of the current methods without themselves becoming organisation-wide architecture.

Examples include:

- `2 | DCA Relationships & Workflows` — current relationship, activity, intake, review, cleanup, and operational-use structures;
- `DCA Integrations & Reconciliation` — current platform staging, sync, reconciliation, and integration-review structures.

Their technical schemas remain implementation. Their organisational meaning must stay grounded in current requirements and evidence.

## Legacy AI material

### Nested June 2026 `dca-ai/dca-ai/` skills

Status: **LEGACY / PENDING AUDIT**

These skills encode the earlier fixed layer/anchor model and are not current organisational authority.

### DCA System Builder v2 — Gem Instructions

Status: **LEGACY / SUPERSEDED AI INSTRUCTION SOURCE**

The document explicitly instructs AI to treat the old Operating Model as highest authority and never reinterpret fixed layers, entry points, or anchors. That instruction conflicts with the current Reality-to-Requirements method and must not govern current DCA AI behaviour.

It may be preserved as historical AI configuration evidence.

## Authority resolution rules

When sources disagree, apply these rules:

1. **Operational evidence does not become structure automatically.**
2. **Working interpretation does not become current authority automatically.**
3. **Pilot practice does not become baseline practice automatically.**
4. **Archived or superseded documents cannot override current reality or current architecture.**
5. **Technical implementation cannot independently redefine organisational truth.**
6. **AI output is derived output unless its claims are grounded in relevant current sources.**
7. **Uncertainty must remain uncertainty until the relevant human or operational evidence resolves it.**
8. **Current architecture may constrain interpretation, but it cannot manufacture operational facts.**
9. **A discovered pattern does not become a structural decision merely because it is coherent.**
10. **A source record is not automatically the organisational fact it represents.**
11. **System support follows the relevant requirement once that requirement is sufficiently established.**
12. **Reality authorises the model.**

## Short current authority chain

```text
Operational evidence / live capture
→ current Operational Reality + explicit validation status
→ reconstruction / reconciliation where shared information must survive
→ evidence-backed organisational inference
→ current shared methods / architecture
→ justified organisational and information requirements
→ technical requirements / implementation
→ live operational use
→ new operational evidence
```

This is not a rigid organisation-wide waterfall. Bounded work may advance when its own evidence, requirement, and validation boundary are sufficiently clear.

No downstream layer may retroactively overwrite upstream reality merely to preserve an earlier model or implementation.
