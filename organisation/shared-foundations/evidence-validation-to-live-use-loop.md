---
document_type: dca_shared_operating_method
status: current
scope: organisation-wide
related_method: organisation/shared-foundations/reality-to-requirements-method.md
does_not_define:
  - final_operating_model
  - final_domain_procedures
  - final_roles
  - permanent_tooling
---

# DCA Evidence → Validation → Live Use Loop

## Purpose

This is the practical working loop DCA uses after real operational evidence is captured or a validation session takes place.

It turns evidence into the correct organisational object without collapsing evidence, terminology, standards, requirements, implementation, and adoption into one thing.

The governing principle remains:

**Reality authorises the model.**

This document complements the broader `reality-to-requirements-method.md` by answering the practical question:

> We learned something from real work. What happens to it now?

---

## The loop — 10 second view

```text
Observe / ingest real work
→ preserve evidence
→ reconstruct what it means
→ validate with the people doing the work
→ classify the validated outputs
→ route each output to its correct home
→ document stable meaning where justified
→ implement only what the validated result requires
→ use it in real work
→ observe what breaks, varies, or changes
→ correct the data / standard / system / model
→ repeat
```

The loop is continuous. A technically working implementation is not the end state. Live use creates new evidence.

---

# 1. Observe / ingest real work

Evidence can come from any current operational source, for example:

- Slack messages, threads, huddles, notes, transcripts, or files;
- Airtable records and operational changes;
- Asana work, comments, status changes, handoffs, and completion evidence;
- Google Workspace documents and files;
- direct reports from the people doing the work;
- physical operational observation;
- AI-supported intake where the original human input and provenance are preserved.

Do not begin by asking what table, role, procedure, automation, or organisational object should exist.

Begin by asking what happened, what is known, what is uncertain, and what the work currently requires.

---

# 2. Preserve before interpreting

Before restructuring or correcting information, preserve the evidence and its provenance.

Keep distinct where relevant:

- original input;
- source and channel;
- person supplying or validating it;
- time;
- direct report versus quoted evidence;
- correction versus new information;
- uncertainty;
- conflicts;
- earlier interpretation that was later corrected.

A correction must not silently erase the evidence or interpretation it corrects.

**Preservation ≠ validation.**

---

# 3. Reconstruct

Connect the evidence into the smallest useful picture of the work.

Typical reconstruction questions:

- What happened?
- What is currently true?
- What changed?
- What starts this work?
- What happens next?
- Who or what is involved?
- What information is needed?
- What decision is being made?
- Where is the handoff?
- What varies?
- What remains unknown?
- What depends on one person remembering or interpreting something?

Do not turn one observed path into a procedure merely because it can be drawn as a flow.

**Observed workflow ≠ required procedure.**

---

# 4. Validate with the people doing the work

Validation is not a database review.

The operational validator should be able to answer in normal working language:

- Is this correct?
- What is wrong?
- What is missing?
- What is uncertain?
- What words would you actually use?
- Is this a normal case, variation, or exception?
- Is this decision always made this way?
- What would another person need to know to continue the work?

The validator does not need to understand the implementation schema.

During validation preserve exact corrections and operational vocabulary.

---

# 5. Extract the validation result

After each validation session produce a short bounded result under four headings:

## Confirmed

What the validator explicitly accepted as correct.

## Changed

What was corrected, renamed, reclassified, or otherwise changed by validation.

## Unresolved

What remains uncertain or needs more evidence.

## New evidence discovered

Operational information revealed during the validation session that was not part of the original reconstruction.

Do not silently treat discussion as confirmation.

---

# 6. Classify and route each output

A validation session usually produces several different kinds of output. They do not all belong in the same document or system.

| Validated output | Primary destination | Purpose |
|---|---|---|
| New or changed operational fact | relevant operational data / staging system | preserve current operational information and provenance |
| Correction to an earlier interpretation | correction path in operational data / evidence record | keep history and corrected meaning traceable |
| Operational terminology | `#struct-oper-standards` → durable standards/terminology document | establish shared organisational language |
| Candidate standard or missing standard | `#struct-oper-standards` | discuss and validate minimum shared rules |
| Validated standard | Shared Drive `00 Standards & Current Procedures` | durable operator-facing current standard |
| Procedure / SOP | Shared Drive standards/procedures area | document a repeatable required way of working once sufficiently validated |
| System, data, interface, or AI requirement | `#struct-system-build` + relevant build/pilot task | implement support justified by operational requirements |
| Operational action | relevant operational Asana project | perform the actual work |
| Build / validation / experiment | Structural Alignment & Pilots | track bounded system or structural validation work |
| Current organisational evidence | DCA Operational Reality maintenance | preserve evidence about how DCA currently works |
| Evidence-backed structural implication | DCA Derived Organisational Reality | preserve derived organisational findings without prematurely fixing the Operating Model |
| Canonical person / organisation / relationship | relationship reconciliation process | promote only after identity and relationship validation |
| Stable cross-organisational method / architecture | `dca-architecture` | version-controlled canonical meaning |
| AI implementation of a stable method | `dca-ai` | provider-independent or provider-specific AI behaviour and tests |

The routing rule is:

**Route by the kind of organisational object produced, not by where the conversation happened.**

A single meeting may therefore update several destinations.

---

# 7. Where discussion, durable documentation, work, data, and architecture live

## Slack — discussion and validation

Slack is the conversational surface where operational evidence is discussed, terminology is tested, standards are proposed, and corrections are surfaced.

For operational standards and terminology:

`#struct-oper-standards`

Expected flow:

```text
operational evidence
→ discuss / define
→ validate with relevant operators
→ document current standard
→ maintain when new evidence appears
```

Slack discussion is evidence of discussion and validation. It is not by itself the durable standard.

## Shared Drive — operator-facing current documentation

Shared Drive is the durable human-readable home for current operational standards, current procedures, manuals, and supporting documents used in normal work.

Current standards/procedures belong under:

`00 Standards & Current Procedures`

A domain may maintain one living standards document with sections for:

- validated terminology;
- current standards;
- standards under validation;
- known exceptions / variations;
- linked procedures or SOPs.

Do not create a separate document for every candidate rule before the rule has stabilised.

## Asana — work to be performed

Asana tracks work, not organisational truth.

Use operational projects for actual operational work.

Use Structural Alignment & Pilots for build, validation, migration, reconciliation, and learning work.

A completed Asana task means the work is recorded as completed. It does not automatically prove adoption, operational effectiveness, or organisational truth.

## Airtable and other operational systems — structured operational state

Operational systems preserve structured current state, evidence-linked staging, reconciliation status, and canonical records where appropriate.

They do not define DCA terminology or organisational policy simply because a field or option exists.

Airtable field names and choices should follow validated organisational meaning, not invent it.

## GitHub — canonical stable method and system meaning

`dca-architecture` holds stable organisational and system specifications that should remain meaningful independently of a specific runtime or interface.

`dca-ai` holds how AI runtimes apply DCA methods, context, workflows, tests, and provider-specific behaviour.

GitHub is not the primary home for day-to-day operational evidence or operator-facing live records.

---

# 8. Standards loop

A missing standard should normally emerge from repeated real decisions, ambiguity, inconsistency, unsafe variation, avoidable reconstruction, or key-person dependence.

Do not ask operators to invent a complete SOP from memory before the real decisions are visible.

Use this sequence:

```text
Observe recurring decision / variation
→ capture examples
→ ask why the decision is made
→ express the smallest candidate rule
→ test it against another real case
→ identify exceptions
→ validate with the people doing the work
→ publish as a current minimum standard
→ test whether another person can use it
→ revise from live evidence
```

A candidate rule should answer a real operational need.

Examples of evidence that a standard may be needed:

- people repeatedly ask the same person what to do;
- work stops when one context holder is absent;
- similar cases are handled differently without a meaningful reason;
- the next person cannot continue because the previous decision is not visible;
- a physical or information constraint repeatedly requires the same judgement;
- repeated reconstruction costs more than preserving a minimum rule.

The target is the **minimum useful shared rule**, not maximum formalisation.

---

# 9. Terminology loop

Operational terminology is organisational meaning. It must not be defined accidentally by Airtable options, AI prompts, or developer vocabulary.

Use this sequence:

```text
term appears in real work
→ capture the context in which people use it
→ compare competing meanings
→ validate with the people closest to the work
→ record agreed definition in operational standards
→ update system fields / AI instructions / Asana wording to conform
→ keep unresolved terms explicitly unresolved
```

The direction of authority is:

```text
validated organisational language
→ implementation vocabulary
```

not:

```text
implementation vocabulary
→ organisational language
```

---

# 10. Standard → system loop

Once a rule or information requirement is validated, ask whether existing systems support it.

Example:

```text
Operational rule:
Goods must be identifiable and locatable by another operator.

Then ask:
- Does the operational data preserve a sufficient location?
- Does the interface expose it?
- Does AI ask for it when missing?
- Does the warehouse need a physical marker?
- Does another operator actually understand and use it?
```

One operational requirement may create several implementation tasks.

The standard remains independent of the chosen implementation.

**Rule ≠ Airtable field ≠ Claude prompt ≠ label ≠ automation.**

These are different implementations of the same underlying requirement and may change independently.

---

# 11. Live use closes the loop

After implementation, test the response in normal work.

Ask:

- Can the next person retrieve what they need?
- Does the operator still have to reconstruct the same context manually?
- Are corrections easy to make without erasing evidence?
- Do variations still fit?
- Does the new structure create unnecessary work?
- Does it reduce dependence on the person who previously held the context?
- Does the standard actually help someone make the intended decision?

If the answer is no, do not protect the model because it was already implemented.

Update the relevant object:

```text
data issue      → correct / reconcile data
terminology     → revalidate term
standard issue  → revise standard
workflow issue  → reconstruct workflow
system issue    → change implementation
assumption issue→ update shared / derived reality
```

Then retest.

---

# 12. Post-validation checklist

After every meaningful validation session:

- [ ] Source notes/transcript/evidence preserved.
- [ ] Confirmed points identified.
- [ ] Corrections identified and preserved as corrections.
- [ ] Unresolved points kept unresolved.
- [ ] New evidence separated from validation of earlier evidence.
- [ ] Operational data updated only where justified.
- [ ] Terminology routed to `#struct-oper-standards`.
- [ ] Candidate standards routed to `#struct-oper-standards`.
- [ ] System/AI/data requirements routed to `#struct-system-build` and appropriate tasks.
- [ ] Actual operational work routed to the operational Asana project.
- [ ] Build/validation work routed to Structural Alignment & Pilots.
- [ ] Relationship changes routed through reconciliation rather than direct assumption.
- [ ] Operational Reality / Derived Organisational Reality assessed separately.
- [ ] Durable operator-facing documentation updated only where meaning is sufficiently validated.
- [ ] Next live test is explicit.

This checklist is a routing check, not a requirement to change every system after every meeting.

---

# 13. Current Logistics example — August 2026

This section is an example of the method applied to current Logistics work. It is not a permanent organisation-wide workflow and should change as Logistics evidence changes.

## Current sequence

```text
Kees validation completed
→ validated terminology + candidate standards to #struct-oper-standards
→ validated Claude/system requirements to #struct-system-build
→ update Claude to the validated semantics
→ Monday live warehouse inventory
→ observe and capture warehouse decisions / judgement
→ derive and validate minimum warehouse rules
→ document validated rules in 00 Standards & Current Procedures
→ retrieval + correction test through Claude
→ attachment test when representative evidence exists
→ reconcile people / organisations / relationships
→ promote only justified findings into Shared Organisational Reality / requirements
→ continue normal Logistics work
→ new evidence enters the loop
```

## Validated terminology from the first Logistics validation

- **Logistics cycle** — operational period from the previous Ukraine transport, through ongoing Logistics work, to the next Ukraine transport.
- **Current goods picture** — currently relevant goods across current operational states.
- **Warehouse inventory** — the subset of goods physically present in warehouse storage.
- **Goods intake** — the recurring process beginning when a concrete message establishes that goods are coming / being offered into the Logistics flow.
- **Logistics information intake** — any other relevant Logistics information, update, correction, partner detail, timing, location, or context arriving at any point.

These definitions belong in operational standards and should then be reflected by system vocabulary.

## Current candidate standards revealed by Logistics work

These are observation targets / candidate standards until separately validated:

- what goods should remain together;
- what can be split;
- how goods are assigned a warehouse/storage position;
- how limited warehouse space should be used;
- how mixed pallets are represented and physically marked;
- when goods are Direct Transit;
- when Direct Transit still requires sorting;
- how temporary holding outside the main warehouse is represented;
- what another volunteer must know to act without reconstructing the decision from Kees.

## Why warehouse storage is a strong first standards case

The storage decision is:

- repeated;
- physically observable;
- immediately testable;
- constrained by real warehouse capacity;
- connected to sorting, inventory, allocation, loading, volunteer work, and retrieval;
- currently dependent on operational judgement that is not yet sufficiently shared.

Therefore the immediate objective is not to write a large warehouse SOP.

It is to observe the decisions made during real inventory/storage work and derive the smallest useful shared rules that another person can actually use.

---

# 14. Anti-patterns

Do not:

- convert every meeting finding into a system field;
- convert every observed workflow into an SOP;
- treat an AI reconstruction as organisational authority;
- overwrite earlier evidence when a correction is supplied;
- make operators validate implementation details they do not need to understand;
- use an Airtable option as proof that organisational terminology has been adopted;
- create canonical relationships directly from a Logistics reference without reconciliation;
- create a new document for every candidate rule;
- treat a GitHub commit as operational adoption;
- treat a completed Asana task as evidence that a standard works;
- allow an implementation to become protected from correction by later reality.

---

# Relationship to the Reality → Requirements method

The broader architecture method is:

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

This document operationalises that method for recurring day-to-day System & Structure work by defining how evidence is validated, classified, routed, documented, implemented, and fed back into live work.

Use `reality-to-requirements-method.md` for the derivation discipline.

Use this document for the practical post-evidence / post-validation working loop.

---

# Short rule

When a validation session ends, do not ask:

> Which document do I update?

Ask:

> What kinds of organisational objects did this evidence produce, and where does each one belong?

Then route them separately, implement only what is justified, test it in real work, and feed the result back into the next evidence cycle.
