---
document_type: dca_shared_drive_architecture
version: 2026-08-21
status: current
scope: all_shared_drives
routing_order:
  - organisational_domain
  - artifact_function
  - lifecycle_status
  - authority_status
canonical_rule: "Domain first; status second; authority explicit."
---

# DCA Shared Drive Architecture & Routing Logic

## Purpose

This document defines how DCA's Shared Drives are interpreted and how material is routed between them. It is intended for both people and machines.

The structure is semantic first. Folder names may change over time; the meaning of the organisational domains and lifecycle states should remain stable.

The core rule is:

**Classify by what an artifact is and which organisational reality it belongs to, not by who created it, which tool was used, or which team happened to touch it.**

A second rule follows from this:

**Moving an artifact to the correct domain must never silently promote its authority.**

A draft remains a draft. A pilot remains a pilot. Historical evidence remains historical evidence. A migration file does not become a current schema merely because it has been moved into a systems drive.

## 1. The organisational separation

DCA's Drive architecture separates four different questions.

### Shared organisational reality

**Question:** What is true, known, reported, validated, uncertain, or historically evidenced about DCA?

**Canonical home:** DCA Organisation.

This includes organisation-wide operational reality, derived organisational reality, validation evidence, and preserved cross-domain knowledge.

### Organisational structure and governance

**Question:** How is DCA organised, governed, bounded, and held together?

**Canonical home:** DCA Organisation, with formal board governance records in DCA Board.

This includes functions, roles, responsibilities, boundaries, decision rights, policies, operating-model material, organisational definitions, handovers, and organisation-wide decisions.

### Functional operations

**Question:** How does DCA actually perform work in a functional domain?

**Canonical homes:** the relevant functional Shared Drives.

- DCA Warehouse & Logistics
- DCA Ukraine Operations
- DCA Fundraising
- DCA Finance
- DCA Marketing & Storytelling

Operational artifacts should live with the function that performs or owns the work.

### Systems and data

**Question:** How do technology, data structures, platforms, integrations, automations, AI, and technical infrastructure support DCA's work?

**Canonical home:** DCA Systems & Data.

System & Structure work may touch every organisational domain. That does not make every artifact a system artifact.

## 2. Routing algorithm

When deciding where a file belongs, evaluate it in this order.

### Step 1 — Identify the organisational domain

Ask what reality the artifact primarily describes or supports.

Examples:

- a warehouse SOP → Warehouse & Logistics
- a Rotary outreach email → Fundraising
- a finance reconciliation report → Finance
- a website content draft → Marketing & Storytelling
- an organisation-wide operational reality reconstruction → Organisation
- an Airtable schema → Systems & Data

### Step 2 — Identify the artifact function

Distinguish between the activity itself and the technical implementation of that activity.

Examples:

- outreach execution and call history → Fundraising
- CRM data reconciliation logic → Systems & Data / relationship data
- Airtable interface instructions used temporarily to reconcile CRM history → Systems & Data / relationship-data migration
- logistics packing procedure → Warehouse & Logistics
- Airtable fields that implement logistics tracking → Systems & Data

A tool does not determine the domain. Using Airtable does not automatically make an artifact an Airtable artifact.

### Step 3 — Identify lifecycle state

After the domain is known, classify status.

Common semantic states are:

- **Current / authoritative** — approved or actively relied upon as the present source or procedure.
- **Working / planning** — being developed; not authoritative yet.
- **Input / validation** — evidence or proposed interpretation awaiting confirmation.
- **Pilot / test** — bounded experiment; not baseline organisational practice unless separately adopted.
- **Migration / build** — transitional technical or data-reconstruction material.
- **Archive / historical** — superseded, completed, obsolete, or preserved for evidence/history.

These lifecycle states should not be confused with organisational domains.

### Step 4 — Make authority explicit

Location alone does not establish authority.

Authority must be visible from the lifecycle state and the document itself. In particular:

- archived material is not current authority;
- pilot material is not baseline practice;
- source evidence is not automatically canonical truth;
- a technical implementation is not organisational reality;
- a proposal is not an adopted procedure;
- absence of evidence is not evidence of absence.

### Step 5 — Choose one canonical home

Prefer one canonical file in one primary domain.

When another function needs the same artifact, use a shortcut, link, reference, or generated output rather than creating uncontrolled copies.

## 3. Common hierarchy semantics

Not every Shared Drive needs identical folders. The following semantic zones can be used where they fit the domain.

### Authoritative / current

Material that defines or records the currently accepted state: standards, procedures, canonical schemas, current organisational reality, approved guidance, or validated records.

### Working / planning

Material actively being designed, planned, edited, or prepared. It can inform work but must not be treated as current authority until promoted deliberately.

### Inputs / validation

Raw input, evidence, stakeholder validation, unresolved questions, reconciliation sources, or proposed interpretations awaiting confirmation.

### Pilots / tests

Bounded experiments designed to validate a workflow, procedure, data model, interface, or operating assumption. Pilot evidence may later support adoption, but the pilot itself does not become baseline merely because it worked.

### Migration / build

Temporary artifacts required to build or reconcile a system: imports, mapping files, legacy exports, transformation sheets, reconstruction evidence, review queues, and implementation iterations.

### Archive / historical

Superseded or historical material retained for reference, evidence, auditability, or reconstruction. Archive is a preservation state, not a dumping ground for unresolved material.

## 4. Cross-domain rules

### Operational artifact vs technical artifact

Store the operational work with the function; store the technical mechanism that supports it in Systems & Data.

Example:

- church outreach list and sent-email history → Fundraising
- CRM schema and migration mapping → Systems & Data

### Shared truth vs function-specific evidence

Function-specific evidence stays with the function. When it is reconciled into organisation-wide truth, the consolidated result belongs in DCA Organisation.

Example:

- mission verification photos → Ukraine Operations
- organisation-wide conclusion derived from repeated mission evidence → DCA Organisation

### Verification media vs storytelling media

Evidence collected to prove delivery, handover, or operational occurrence belongs with the operational function. Media selected or produced for communication belongs with Marketing & Storytelling. Reference across drives rather than duplicating uncontrolled copies.

### Financial truth vs fundraising intent

Donor intent, campaign context, and fundraising interaction belong in Fundraising. Validated financial transactions, receipts, reconciliation, and bookkeeping truth belong in Finance. Technical matching/integration logic belongs in Systems & Data.

### Structure vs systems

Roles, organisational functions, boundaries, governance, and decision rights belong in Organisation even when they are represented in Airtable or another platform. The technical schema representing them belongs in Systems & Data.

## 5. Semantic map of the DCA Shared Drives

```text
DCA
├── GOVERNANCE
│   └── DCA Board
│       └── formal board records organised primarily by governance period / year
│
├── SHARED ORGANISATIONAL REALITY + STRUCTURE
│   └── DCA Organisation
│       ├── shared organisational reality
│       │   ├── current canonical reality
│       │   ├── validation / evidence awaiting consolidation
│       │   └── historical reality and reconstruction archive
│       ├── organisational structure & governance
│       │   ├── current structure / governance
│       │   ├── working structure / governance
│       │   └── superseded structure / governance archive
│       └── organisation-wide knowledge domains
│           ├── policies / official material
│           ├── people / onboarding
│           ├── meetings / decisions
│           └── handovers / organisational knowledge
│
├── FUNCTIONAL OPERATIONS
│   ├── DCA Warehouse & Logistics
│   │   ├── authoritative standards / current procedures
│   │   ├── operational planning / working material
│   │   ├── inputs / validation
│   │   ├── pilots / tests
│   │   ├── operational records / materials where needed
│   │   └── archive
│   │
│   ├── DCA Ukraine Operations
│   │   ├── mission planning
│   │   ├── mission / execution records
│   │   ├── partner coordination
│   │   ├── verification / delivery evidence
│   │   ├── receipts / reports
│   │   ├── field notes
│   │   ├── story intake
│   │   └── archive where required
│   │
│   ├── DCA Fundraising
│   │   ├── fundraising standards / operating guidance
│   │   ├── campaigns
│   │   ├── donor stewardship / post-donation
│   │   ├── grants
│   │   ├── events
│   │   ├── outreach operations
│   │   ├── working / planning / fundraising data
│   │   ├── validation inputs
│   │   └── archive
│   │
│   ├── DCA Finance
│   │   ├── finance standards / operating guidance
│   │   ├── transactions / reconciliation
│   │   ├── receipts / supporting documentation
│   │   ├── declarations / reimbursements
│   │   ├── contracts / finance administration
│   │   ├── in-kind financial treatment
│   │   ├── reporting
│   │   ├── working / validation
│   │   └── time-based archive where appropriate
│   │
│   └── DCA Marketing & Storytelling
│       ├── brand authority
│       ├── communication / marketing strategy
│       ├── source media and content production
│       ├── published content
│       ├── newsletter
│       ├── website content
│       ├── print / events
│       ├── working / validation
│       └── archive
│
├── SYSTEMS + DATA
│   └── DCA Systems & Data
│       ├── technical architecture / standards
│       ├── platform implementations
│       │   ├── current
│       │   ├── working
│       │   ├── migration / imports / build
│       │   └── archive
│       ├── CRM / relationship-data infrastructure
│       │   ├── current
│       │   ├── working
│       │   ├── reconciliation / migration / build
│       │   └── archive
│       ├── integrations / automation
│       ├── AI / agents
│       ├── data warehouse / reporting infrastructure
│       ├── technical documentation
│       ├── tests
│       └── technical archive
│
├── RESTRICTED
│   └── DCA Vault
│       └── secrets / credentials / restricted access material only
│
├── TEMPORARY INTAKE
│   └── DCA Uploads
│       └── unclassified or temporarily staged material awaiting routing
│
└── LEGACY / RETIREMENT
    ├── DCA Core
    │   └── migration source only; no new canonical material
    └── DCA files
        └── migration source only; no new canonical material
```

## 6. Current implementation state

As of 21 August 2026:

- **DCA Organisation**, **DCA Systems & Data**, and **DCA Warehouse & Logistics** already have the new semantic skeleton actively being populated.
- **DCA Ukraine Operations** and **DCA Marketing & Storytelling** are already comparatively well bounded by function, even though their folder naming is not identical to the common lifecycle pattern.
- **DCA Fundraising** and **DCA Finance** are valid functional homes but still contain older mixed structures that can be normalised gradually.
- **DCA Board** remains a dedicated governance record space and is appropriately time-oriented.
- **DCA Vault** remains separate and restricted.
- **DCA Uploads** is temporary intake, never a canonical knowledge store.
- **DCA Core** and **DCA files** are legacy spaces to migrate and retire rather than extend.

This distinction matters: the semantic architecture is the governing model even while physical migration is still incomplete.

## 7. Machine-routing summary

A machine routing a DCA artifact should apply these questions in order:

1. What organisational domain does the artifact primarily concern?
2. Is it the work itself, evidence about the work, organisation-wide truth derived from the work, or a technical mechanism supporting the work?
3. What is its lifecycle state: current, working, validation, pilot, migration/build, or archive?
4. What authority does it actually have?
5. Is there already a canonical artifact that should be referenced instead of copied?

If domain or authority cannot be determined confidently, route to a review/validation state rather than silently promoting it.

## 8. Short rule set

1. **Domain first.**
2. **Artifact function second.**
3. **Lifecycle/status third.**
4. **Authority must be explicit.**
5. **One canonical home; reference elsewhere.**
6. **Tools do not define organisational domains.**
7. **Pilots do not silently become baseline practice.**
8. **Historical evidence does not silently become current truth.**
9. **Moving a file must not promote it.**
10. **When uncertain, preserve and review rather than invent.**
