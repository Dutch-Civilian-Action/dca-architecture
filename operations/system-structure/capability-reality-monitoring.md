---
document_type: dca_system_structure_capability_monitoring
status: current
scope: system-and-structure
---

# System & Structure Capability Reality Monitoring

## Purpose

Maintain a current evidence-backed view of what System & Structure actually does and whether the capability remains usable, aligned, and transferable.

This is not an activity diary, role description, backlog, or performance score.

## Evidence sources

Use relevant observable evidence from:

- Google Drive artifacts, revisions, routing, and maintained shared assets;
- GitHub commits, ADRs, architecture/specification changes, repository state, and implementation history;
- Slack alignment, validation, correction, dependency, publication, and use evidence;
- Airtable/system state, schema changes, reconciliation, integrations, automations, monitoring, and failures;
- downstream use showing whether people or workflows retrieve, depend on, correct, or ignore S&S outputs.

## Maintained views

### Capability reality

What S&S actually does and maintains now.

### Dependency reality

What DCA work depends on S&S and what S&S itself depends on.

### Capability health

Whether the capability is current, aligned, monitored, usable, transferable, and able to continue under its real dependencies.

### Change reality

What materially changed and which shared reality, architecture, documentation, AI, or system surfaces need reconciliation as a result.

## Evidence boundaries

- artifact creation ≠ organisational adoption;
- GitHub commit ≠ organisational decision unless current authority supports it;
- Slack discussion ≠ validated organisational fact automatically;
- technical implementation ≠ organisational structure;
- tool presence ≠ demonstrated capability;
- activity ≠ successful outcome;
- intended mandate ≠ current capability reality.

## Monitoring questions

- What recurring S&S work is actually happening?
- What outputs and shared assets are being maintained?
- What materially changed since the previous view?
- Which DCA work depends on those outputs?
- Where do Drive, GitHub, Slack, Airtable/system state, and current guidance disagree?
- Which automations or integrations are working, failing, or unobserved?
- Which knowledge or maintenance still depends on one person?
- Which outputs would be difficult for another person to understand or continue?
- What capability has become organisation-held rather than person-held?

## Finding triggers

Surface a finding when evidence suggests:

- a new recurring capability;
- a capability changed or stopped;
- authority or documentation drift;
- conflicting current representations;
- system/document mismatch;
- unresolved dependency;
- automation or integration failure;
- key-person continuity risk;
- repeated reconstruction that should become organisation-held;
- output produced but not actually used;
- outcome/use evidence contradicting the intended benefit.

## Monitoring rule

**Monitor material change, not every action.**

No material change means no unnecessary report.

## Relationship to current methods

- `organisation/shared-foundations/capability-reality.md` defines Capability Reality and its evidence boundary.
- `organisation/shared-foundations/reconstruction-reconciliation-method.md` governs how distributed evidence becomes reliable shared information.
- `organisation/shared-foundations/reality-to-requirements-method.md` governs how sufficiently established reality becomes justified requirements and support.

## Output

A capability-reality update should contain only what materially changed:

- changed reality;
- new or removed capability;
- new dependency or continuity risk;
- conflict or uncertainty;
- capability-health issue;
- required reconciliation or update.
