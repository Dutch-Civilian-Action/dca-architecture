---
document_type: dca_shared_structure_method
status: current
scope: organisation-wide
replaces: "Structure Method — fixed Layer / Entry Point / Anchor derivation model"
does_not_define:
  - final_operating_model
  - fixed_essential_functions
  - final_roles
  - final_procedures
  - final_system_objects
  - permanent_platform_schema
---

# DCA Structure Method — Reality to Requirements

## Purpose

This method defines how DCA moves from **relevant current DCA reality** toward justified structural, information, and system responses.

It exists to prevent DCA from designing structure, procedures, roles, data models, or technical objects before the reality they are meant to support is sufficiently understood.

The governing rule is:

**Reality authorises the model.**

This method does not define the final DCA Operating Model. It defines the discipline used to discover what DCA may actually need.

## Relevant current reality

The method may begin from:

- **Operational Reality** — what happens in DCA domain work;
- **Capability Reality** — what an organisational capability actually does, maintains, changes, supports, depends on, and enables;
- both, where the question crosses the boundary.

Capability Reality must be evidence-backed. Intended mandate, role descriptions, artifact presence, implementation activity, or tool ownership do not by themselves establish current capability reality.

See `capability-reality.md` for the evidence and monitoring boundary.

## Core sequence

```text
Relevant DCA evidence
→ Operational Reality and/or Capability Reality
→ Shared Organisational Reality
→ Recurring Workflows / Capability Patterns
→ Organisational Requirements
→ Structure + Information Requirements, where justified
→ System Requirements, where justified
→ System Support
→ Live Operational Use / Maintained Capability
→ New Evidence
→ Updated Reality
```

A bounded domain or capability may move through this sequence when its own evidence and validation are sufficient. DCA does not need to complete the sequence organisation-wide before improving a specific area.

Likewise, an information-preservation or reconciliation workflow does not need to wait for the entire organisational model to be known. Once its relevant requirement is sufficiently established, the required support may move forward while broader reconstruction and validation continue.

## 1. Start from relevant current reality

Begin with the evidence relevant to the question.

For domain work, use evidence of what actually happens: observed and reported work, variation, exceptions, uncertainty, visibility gaps, and current dependencies.

For an organisational capability, use evidence of what the capability actually does and maintains: artifacts and revisions, decisions, repositories, system state, runtime behaviour, dependencies, maintenance work, failures, and downstream use where relevant.

Preserve distinctions between:

- direct operational evidence;
- capability evidence;
- validated shared reality;
- derived interpretation;
- uncertainty or visibility gaps;
- pilot-introduced practice;
- proposed future practice.

Do not silently treat a proposal, pilot, technical implementation, historical document, intended mandate, artifact presence, or activity volume as current organisational reality.

## 2. Reconstruct recurring workflows and capability patterns

Connect validated observations into the work that repeatedly happens.

Ask:

- What starts the work?
- What happens next?
- Who participates?
- What information is needed?
- Where are decisions made?
- Where are handoffs?
- What depends on what happened earlier?
- What varies?
- What is exceptional?
- Where does visibility or context break?
- For a capability: what is maintained, monitored, corrected, or handed over repeatedly?

A reconstructed workflow describes recurring reality. It is not automatically a procedure.

**Workflow ≠ procedure.**

## 3. Identify dependencies and consequences

For each part of the workflow or maintained capability, make visible what it creates for:

1. the person or function doing the work;
2. the next person or function;
3. DCA as an organisation.

Relevant consequences may include continuity, time, rework, handoff quality, reliability, traceability, reporting, shared visibility, person-dependence, learning, and the ability to continue when a usual role holder is unavailable.

## 4. Derive recurring functions where evidence supports them

Recurring workflows or maintained capability reality may reveal recurring organisational capabilities or functions.

A function should not be introduced because it sounds appropriate for an NGO or because an earlier model declared it.

It should be identified when repeated, sufficiently established DCA reality demonstrates that DCA must reliably perform or maintain a capability.

Keep the distinction explicit:

- recurring work can reveal a function;
- a function is not automatically a role;
- a function is not automatically a department, circle, layer, system object, or platform component.

**Function ≠ role.**

No final set of essential DCA functions is fixed by this method.

## 5. Derive organisational requirements

Once a recurring workflow, function, or maintained capability is sufficiently visible, ask what DCA must reliably be able to do, know, preserve, hand over, retrieve, monitor, or continue.

For each requirement, keep explicit where relevant:

- supporting evidence and scope;
- recurrence or bounded-case status;
- operational owner or validator;
- dependencies and handoffs;
- decisions that belong in the work;
- minimum information that must survive;
- uncertainty, variation, and exceptions;
- continuity requirements;
- what can vary safely;
- what cannot safely vary.

Only after the requirement is visible should DCA decide whether a structural response is needed.

## 6. Derive structure only where required

Possible organisational responses include:

- clearer ownership;
- a role boundary;
- a functional interface;
- a rule of engagement;
- a minimum required operation;
- a procedure;
- a standard;
- shared information;
- a decision boundary;
- no additional formal structure.

The response must be proportional to the requirement.

Structure is a response to reality, not the starting assumption.

## 7. Derive information requirements

Ask what must remain knowable and reusable for the workflow or capability to continue without unnecessary reconstruction.

Examples include:

- identity;
- status;
- source/provenance;
- decision or confirmation;
- relationship;
- handoff context;
- uncertainty;
- operational outcome;
- capability state;
- evidence required by downstream work.

The target is **minimum useful preservation**, not maximum capture.

The information requirement should remain meaningful even if the implementation tool changes.

When distributed evidence must be recovered, matched, reconciled, persisted, or exposed for reuse, apply the **DCA Reconstruction & Reconciliation Method** rather than inventing those rules inside a technical implementation.

## 8. Derive system support when the relevant requirement is sufficiently established

**System support follows the relevant requirement once that requirement is sufficiently established.**

DCA does not need to postpone a bounded technical response until every adjacent workflow or the whole organisation has been reconstructed. Equally, a tool or integration must not be introduced merely because it is available.

Possible responses may include Airtable, Google Drive, Slack, forms, APIs, integrations, AI extraction or reconciliation, notifications, labels, automation, reporting infrastructure, monitoring, another tool, or no new system at all.

**Organisational requirement ≠ technical implementation.**

Tool capability does not define the organisational model.

## 9. Test through live use and capability maintenance

A proposed response is not correct merely because it is internally coherent or technically functional.

Test it in real bounded work or through the real maintenance of the capability it supports.

Evaluate whether it:

- reduces repeated asking and reconstruction;
- preserves the information the next person actually needs;
- reduces person-dependence;
- supports handoffs;
- remains usable under real variation and exceptions;
- creates less burden than the reconstruction it replaces;
- preserves uncertainty rather than hiding it;
- improves organisational visibility or continuity where intended;
- remains current and transferable over time.

Success is not that a tool works. Success is that the relevant DCA reality becomes more understandable, transferable, reusable, and maintainable.

## 10. Feed new evidence back into shared reality

Live work and maintained organisational capabilities create new evidence.

That evidence may confirm, qualify, contradict, or invalidate the reconstructed workflow, capability interpretation, derived requirement, structural response, or system support.

```text
Current Reality
→ Workflow / Capability
→ Requirements
→ Response
→ Live Use / Maintained Capability
→ New Evidence
→ Updated Reality
```

No downstream model is protected from correction by new evidence.

## Relationship to Reconstruction & Reconciliation

The two current shared methods have different responsibilities.

```text
STRUCTURE METHOD
What does relevant current reality justify DCA needing?
        ↓
requirements / structure / information / system support

RECONSTRUCTION & RECONCILIATION METHOD
How does distributed organisational and operational evidence become
reliable, reusable shared organisational information?
```

The Reconstruction & Reconciliation Method may supply or maintain the shared information on which structural reasoning depends. The Structure Method may in turn reveal new preservation, reconciliation, retrieval, or monitoring requirements.

They form a feedback relationship rather than a single organisation-wide waterfall.

## Authority and boundaries

This document is the current DCA method for deriving structure and system support from organisational reality.

It supersedes the earlier Structure Method insofar as that document required facts to be assigned through a predetermined sequence of fixed Layers, Entry Points, and Anchors before the current requirement had been established.

It also supersedes **DCA Workflow-Based Structural Alignment Logic** as a separate active method. The useful workflow, dependency, consequence, function, requirement, testing, and feedback logic from that predecessor is incorporated here.

This supersession does **not** mean that every concept, object, pilot, or implementation produced under earlier models is invalid. Existing artifacts remain evidence or implementation history and must be evaluated on their own support and current status.

In particular:

- old system vocabulary must not silently become baseline organisational reality;
- pilot-supported concepts remain pilot-supported unless separately adopted;
- functions are derived where evidenced, not predefined;
- the final DCA Operating Model remains open until sufficient validated organisational evidence supports it;
- technical architecture must not independently redefine organisational truth.

## Relationship to other DCA sources

- **DCA Operational Reality** supplies the current domain-operational evidence base.
- **System & Structure Capability Reality** supplies evidence-backed understanding of what the S&S capability actually does and maintains.
- **DCA Derived Organisational Reality** contains evidence-backed organisational inferences without defining the Operating Model.
- **DCA Reconstruction & Reconciliation Method** governs how distributed organisational and operational evidence and live capture become reliable reusable shared organisational information.
- **Domain plans and pilots** test bounded requirements through live work.
- **DCA architecture specifications** formalise stable meaning once sufficiently justified.
- **DCA Systems & Data** implements technical support where required.
- **DCA AI** may apply these methods but does not authorise organisational reality.

## Short rule

When something in DCA is structurally unclear:

**Do not ask first what object, layer, role, table, automation, or procedure should exist.**

Ask first:

**What does the relevant current reality show, what repeatedly needs to happen or be maintained, and what must DCA therefore be able to preserve or perform?**
