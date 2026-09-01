---
document_type: dca_authority_map
status: current
scope: organisation-wide
purpose: distinguish current authority, working sources, archived implementation, and superseded structure
---

# DCA Authority Map

## Purpose

DCA contains current reality, working interpretation, architecture, historical models, pilots, implementation records, and archived technical material. These must not be treated as one authority level.

This map exists so people and AI can determine what a document or evidence source may legitimately authorise.

The governing rule is:

**A document's detail, confidence, age, or title does not establish authority. Authority depends on its current status, scope, evidence boundary, and relationship to validated organisational reality.**

## Current shared foundations and methods

### DCA Capability Reality

Canonical architecture specification:

`organisation/shared-foundations/capability-reality.md`

Status: **CURRENT**

Role: distinguishes Operational Reality from Capability Reality and defines the evidence and monitoring boundary for organisational capabilities.

Authority boundary: artifact creation, implementation activity, tool presence, or intended mandate do not by themselves establish capability reality or organisational adoption.

### DCA Structure Method — Reality to Requirements

Canonical architecture specification:

`organisation/shared-foundations/reality-to-requirements-method.md`

Status: **CURRENT**

Role: defines how DCA moves from relevant current reality — Operational Reality, Capability Reality, or both — toward justified organisational, information, structural, and system responses.

It does not define a final Operating Model or a fixed set of functions, layers, anchors, roles, procedures, or system objects.

### DCA Reconstruction & Reconciliation Method

Canonical architecture specification:

`organisation/shared-foundations/reconstruction-reconciliation-method.md`

Status: **CURRENT**

Role: defines how DCA turns distributed organisational and operational evidence, plus live capture, into reliable reusable shared organisational information while preserving provenance, uncertainty, conflicts, and validation boundaries.

Authority boundary: it does not define the Operating Model, a universal central database, or a permanent platform schema. It governs the information-reliability process, not the final organisational structure.

Provider-independent execution contract for established findings:

`Dutch-Civilian-Action/dca-ai/workflows/reconcile-established-findings-into-maintained-reality.md`

Status: **CURRENT**

Role: after source-first reconstruction, self-evaluation, and required validation, compare each established current candidate with its authoritative maintained target; classify the reconciliation outcome; route, persist, and verify any justified change; and preserve the downstream result in the reconstruction lineage.

This workflow implements the shared method. It does not outrank the maintained target or create write authority by itself.

The current questions are different:

- Capability Reality: **What does this organisational capability actually do and maintain, based on evidence?**
- Structure Method: **What does relevant current reality justify DCA needing?**
- Reconstruction & Reconciliation Method: **How does distributed evidence become reliable shared organisational information?**

## Current organisational reality sources

### DCA Operational Reality — 2nd Pass

Status: **CURRENT VALIDATION SOURCE**

Role: current organisation-wide reconstruction and validation of domain operational reality.

Authority boundary: operational claims remain subject to their explicit evidence/validation/uncertainty status. The document does not itself define future structure.

### System & Structure Capability Reality

Status: **ACTIVE WORKING EVIDENTIAL REALITY**

Role: maintained evidence-backed view of what System & Structure actually does, maintains, changes, supports, depends on, and enables.

Relevant observable evidence may include:

- Google Drive artifacts, revisions, routing, and maintained shared assets;
- GitHub commits, ADRs, architecture/specification changes, and repository state;
- Slack alignment, validation, correction, dependency, publication, and use evidence;
- Airtable/system state, reconciliation, integrations, automations, monitoring, and failures;
- downstream evidence that DCA work retrieves, uses, depends on, corrects, or ignores S&S outputs.

Authority boundary:

- capability evidence does not automatically define role or mandate;
- artifact creation does not prove adoption;
- GitHub commits and technical implementation do not independently become organisational authority;
- Slack discussion does not automatically become validated fact;
- activity does not prove successful outcome;
- unresolved interpretation remains working evidence until the relevant validation boundary is satisfied.

### DCA Derived Organisational Reality

Status: **CURRENT WORKING EVIDENTIAL SOURCE**

Role: evidence-backed organisational inference derived from current reality.

Authority boundary: explicitly not the Operating Model. It does not define essential functions, layers, roles, procedures, system objects, or future structure.

## Current working organisational material

### DCA System & Structure — Organisation-Wide Plan

Status: **WORKING**

Role: navigation and execution plan for maintaining Operational Reality and S&S Capability Reality, workflow visibility, information preservation and reconciliation, requirements, architecture, system support, live use, monitoring, and learning.

Authority boundary: not the Operating Model and not final technical architecture.

### DCA Organisational Concepts & Relationships

Status: **WORKING / CONCEPT MODEL**

Role: develops shared concepts and critical distinctions including Operational Reality ≠ Capability Reality, Organisation ≠ Structure, Structure ≠ System, Workflow ≠ Procedure, Function ≠ Role, artifact ≠ adoption, and source record ≠ organisational fact.

Authority boundary: useful source material, but not yet a canonical ontology or final organisational model. It should define concepts and relationships, not compete with the current methods.

## Superseded predecessor material

### DCA Workflow-Based Structural Alignment Logic

Status: **SUPERSEDED AS ACTIVE METHOD / PREDECESSOR SOURCE**

Role: predecessor working method that made recurring workflows, dependencies, consequences, candidate functions, requirements, testing, and feedback visible.

Its useful logic is incorporated into the current DCA Structure Method — Reality to Requirements. It must not be treated as a competing current method.

Its older wording **“System Support Comes Later”** is superseded by:

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

These remain historical evidence of prior architecture and may contain reusable distinctions or implementation history. They must not be used to require fixed layers, entry points, anchors, or system objects in current structural derivation.

## Archived technical implementation

Technical documents derived from earlier models may remain useful as implementation history, but archive location does not make them current technical authority.

Examples include System Logic — Overview and DCA System — Airtable Schema.

Status: **ARCHIVED / REQUIRES REVALIDATION BEFORE REUSE**

A table, field, identifier, system object, or technical relationship from these documents may be reused only when the current requirement and current architecture still justify it.

## Current implementation examples

Current Airtable and integration structures may implement parts of the current methods without themselves becoming organisation-wide architecture.

Examples include:

- `2 | DCA Relationships & Workflows` — current relationship, activity, intake, review, cleanup, and operational-use structures;
- `DCA Integrations & Reconciliation` — current platform staging, sync, reconciliation, and integration-review structures.

Their technical schemas remain implementation. Their organisational meaning must stay grounded in current requirements and evidence.

## Legacy AI material

Historical pre-reality-first DCA AI skills are preserved under `dca-ai/skills/legacy/` in the `dca-ai` repository. They are **LEGACY** and must not be loaded or treated as current DCA AI capability definitions.

DCA System Builder v2 — Gem Instructions is a **LEGACY / SUPERSEDED AI INSTRUCTION SOURCE** where it requires the old Operating Model and fixed layers/anchors to remain highest authority.

## Authority resolution rules

When sources disagree, apply these rules:

1. **Operational evidence does not become structure automatically.**
2. **Capability evidence does not become mandate, adoption, or outcome automatically.**
3. **Artifact creation ≠ organisational adoption.**
4. **GitHub commit ≠ organisational decision unless current authority supports that interpretation.**
5. **Slack discussion ≠ validated organisational fact automatically.**
6. **Technical implementation ≠ organisational structure.**
7. **Activity ≠ successful outcome.**
8. **Working interpretation does not become current authority automatically.**
9. **Pilot practice does not become baseline practice automatically.**
10. **Archived or superseded documents cannot override current reality or current architecture.**
11. **AI output is derived output unless its claims are grounded in relevant current sources.**
12. **Uncertainty must remain uncertainty until relevant evidence resolves it.**
13. **Current architecture may constrain interpretation, but it cannot manufacture operational or capability facts.**
14. **A discovered pattern does not become a structural decision merely because it is coherent.**
15. **System support follows the relevant requirement once that requirement is sufficiently established.**
16. **Validation does not equal maintained-state change; compare, classify, persist, and verify the outcome.**
17. **A completed task, generated draft, or publication is not evidence that a maintained target was updated.**
18. **Reality authorises the model.**

## Short current authority chain

```text
Operational evidence + Capability evidence + live capture
→ Operational Reality and/or Capability Reality
→ reconstruction / reconciliation / validation where needed
→ Shared Organisational Reality
→ evidence-backed organisational inference
→ current shared methods / architecture
→ justified organisational and information requirements
→ technical requirements / implementation
→ live operational use / maintained capability
→ new evidence
```

This is not a rigid organisation-wide waterfall. Bounded work may advance when its own evidence, requirement, and validation boundary are sufficiently clear.

No downstream layer may retroactively overwrite upstream reality merely to preserve an earlier model or implementation.
