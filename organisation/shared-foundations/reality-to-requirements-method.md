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

This method defines how DCA moves from observed organisational reality toward justified structural, information, and system responses.

It exists to prevent DCA from designing structure, procedures, roles, data models, or technical objects before the reality they are meant to support is sufficiently understood.

The governing rule is:

**Reality authorises the model.**

This method does not define the final DCA Operating Model. It defines the discipline used to discover what DCA may actually need.

## Core sequence

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

A bounded domain may move through this sequence when its own evidence and validation are sufficient. DCA does not need to complete the sequence organisation-wide before improving a specific domain.

## 1. Start from operational reality

Begin with what is observed, reported, documented, validated, uncertain, variable, exceptional, or missing in current DCA work.

Preserve distinctions between:

- direct operational evidence;
- validated shared reality;
- derived interpretation;
- uncertainty or visibility gaps;
- pilot-introduced practice;
- proposed future practice.

Do not silently treat a proposal, pilot, technical implementation, or historical document as current organisational reality.

## 2. Reconstruct recurring workflows

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

A reconstructed workflow describes recurring reality. It is not automatically a procedure.

**Workflow ≠ procedure.**

## 3. Identify dependencies and consequences

For each part of the workflow, make visible what it creates for:

1. the person or function doing the work;
2. the next person or function;
3. DCA as an organisation.

Relevant consequences may include continuity, time, rework, handoff quality, reliability, traceability, reporting, shared visibility, person-dependence, learning, and the ability to continue when a usual role holder is unavailable.

## 4. Derive recurring functions where evidence supports them

Recurring workflows may reveal recurring organisational capabilities or functions.

A function should not be introduced because it sounds appropriate for an NGO or because an earlier model declared it.

It should be identified when repeated operational reality demonstrates that DCA must reliably perform a capability.

Keep the distinction explicit:

- recurring work can reveal a function;
- a function is not automatically a role;
- a function is not automatically a department, circle, layer, system object, or platform component.

**Function ≠ role.**

No final set of essential DCA functions is fixed by this method.

## 5. Derive organisational requirements

Once a recurring workflow or function is sufficiently visible, ask what DCA must reliably be able to do, know, preserve, hand over, retrieve, or continue.

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

Ask what must remain knowable and reusable for the workflow to continue without unnecessary reconstruction.

Examples include:

- identity;
- status;
- source/provenance;
- decision or confirmation;
- relationship;
- handoff context;
- uncertainty;
- operational outcome;
- evidence required by downstream work.

The target is **minimum useful preservation**, not maximum capture.

The information requirement should remain meaningful even if the implementation tool changes.

## 8. Derive system requirements only afterward

A technical requirement exists only when organisational or operational reality justifies technical support.

Possible responses may include:

- Airtable;
- Google Drive;
- Slack;
- forms;
- APIs;
- integrations;
- AI extraction or reconciliation;
- notifications;
- labels;
- automation;
- reporting infrastructure;
- another tool;
- no new system at all.

**Organisational requirement ≠ technical implementation.**

Tool capability does not define the organisational model.

## 9. Test through live operational use

A proposed response is not correct merely because it is internally coherent or technically functional.

Test it in real bounded work.

Evaluate whether it:

- reduces repeated asking and reconstruction;
- preserves the information the next person actually needs;
- reduces person-dependence;
- supports handoffs;
- remains usable under real variation and exceptions;
- creates less burden than the reconstruction it replaces;
- preserves uncertainty rather than hiding it;
- improves organisational visibility or continuity where intended.

Success is not that a tool works. Success is that the relevant operational reality becomes more understandable, transferable, and reusable.

## 10. Feed new evidence back into shared reality

Live work creates new evidence.

That evidence may confirm, qualify, contradict, or invalidate the reconstructed workflow, derived requirement, structural response, or system support.

The loop is therefore:

```text
Operational Reality
→ Workflow
→ Requirements
→ Response
→ Live Use
→ New Operational Reality
```

No downstream model is protected from correction by new evidence.

## Authority and boundaries

This document is the current DCA method for deriving structure and system support from organisational reality.

It supersedes the earlier Structure Method insofar as that document required facts to be assigned through a predetermined sequence of fixed Layers, Entry Points, and Anchors before the current operational requirement had been established.

This supersession does **not** mean that every concept, object, pilot, or implementation produced under the earlier model is invalid. Existing artifacts remain evidence or implementation history and must be evaluated on their own operational support and current status.

In particular:

- old system vocabulary must not silently become baseline organisational reality;
- pilot-supported concepts remain pilot-supported unless separately adopted;
- functions are derived where evidenced, not predefined;
- the final DCA Operating Model remains open until sufficient validated organisational evidence supports it;
- technical architecture must not independently redefine organisational truth.

## Relationship to other DCA sources

- **DCA Operational Reality** supplies the evidence base.
- **DCA Derived Organisational Reality** contains evidence-backed organisational inferences without defining the Operating Model.
- **Workflow-based Structural Alignment** applies the method by making recurring work, dependencies, consequences, functions, and requirements visible.
- **Domain plans and pilots** test bounded requirements through live work.
- **DCA architecture specifications** formalise stable meaning once sufficiently justified.
- **DCA Systems & Data** implements technical support where required.
- **DCA AI** may apply this method but does not authorise organisational reality.

## Short rule

When something in DCA is structurally unclear:

**Do not ask first what object, layer, role, table, automation, or procedure should exist.**

Ask first:

**What does the current reality show, what repeatedly needs to happen, and what must DCA therefore be able to preserve or perform?**
