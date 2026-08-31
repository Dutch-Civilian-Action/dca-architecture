---
document_type: dca_shared_foundation
status: current
scope: organisation-wide
does_not_define:
  - final_domain_schema
  - final_relationship_schema
  - final_location_model
  - final_operating_model
---

# DCA Shared Object Boundaries

## Purpose

Define the minimum cross-organisational object boundaries that DCA systems, data models, interfaces, and AI must preserve even when operational evidence arrives mixed together.

These boundaries are independent of any specific Airtable base, Slack channel, AI provider, plugin, or domain implementation.

The governing principle remains:

**Reality authorises the model.**

A source may mention several different things in one sentence. Convenience of capture is not permission to collapse them into one object.

## Core boundaries

Keep these meanings distinct whenever the evidence supports the distinction:

- **person** — a human individual;
- **organisation** — an organisation, company, foundation, group, institution, or other organisational entity;
- **location** — a physical place used or mentioned in the work;
- **contact route** — a phone number, WhatsApp number, email address, handle, or other route through which someone can be reached;
- **operational function / step** — what a person, organisation, location, or route is doing in a specific piece of work;
- **relationship** — an evidenced connection between otherwise distinct people, organisations, or DCA;
- **operational fact / state** — a time-bounded fact about the work, goods, activity, decision, or current situation.

Association does not change object type.

Examples:

- a person working for an organisation remains a person;
- an organisation using a handover point remains an organisation, while the handover point remains a location;
- a phone number used by a person remains a route, not the person itself;
- a Logistics role performed in one case does not turn the person or organisation into that role;
- a location used for pickup, unloading, temporary holding, or handover does not become the organisation's general address unless evidence establishes that separately.

## Mixed evidence

One source item may support several objects and several links between them.

For example:

```text
"Harry at Azzurro says the boxes are ready. Handover is at Gate B."
```

may support, without collapsing them:

- Harry — person;
- Azzurro — organisation;
- Gate B — location;
- Harry ↔ Azzurro — contextual association where supported;
- Gate B — handover function for this operational case;
- the boxes / their state — operational fact.

Preserve the shared evidence/provenance connecting those objects rather than representing the sentence as one combined entity.

## Identity and canonical data

A domain capability may preserve a local/staging reference to a person, organisation, or location without owning that entity's canonical identity.

Where DCA has an established canonical identity source:

- use it to reconcile identity when access and evidence allow;
- do not let another domain silently redefine the entity type, identity, partner status, or canonical relationship;
- do not merge a person and organisation merely because both appear in the same operational statement;
- do not treat access to canonical data as permission to mutate it from an unrelated domain workflow.

Identity reconciliation and domain-state capture are separate operations.

## Locations and operational function

A physical place may have different operational meanings, for example:

- warehouse;
- temporary holding location;
- pickup point;
- drop-off point;
- unloading point;
- handover point.

Preserve the function the evidence actually states.

Do not translate one function into another merely because the implementation has a nearby field or select option. In particular, a handover point is not automatically a pickup location, and a temporary holding location is not automatically a warehouse or canonical address.

When a location materially affects where goods are, where a handoff occurs, or what someone must do, it should remain separately recoverable from the operational evidence. This does not require every place mention to become a canonical Location object.

## Schema and implementation boundary

When an implementation cannot represent a supported distinction cleanly:

1. preserve the original evidence;
2. keep the unsupported structure unresolved or descriptive;
3. do not invent precision, entity type, role, relationship, location function, or canonical meaning to satisfy the schema;
4. route the mismatch to the appropriate System & Structure / implementation path.

The implementation must adapt to validated organisational meaning, not the reverse.

## Capability versus access

These shared boundaries are organisational meaning. They are not a credential or capability grant.

A runtime may need to know that person, organisation, location, route, role, and relationship are distinct even when it has no permission to read or write the system that stores canonical relationship data.

Therefore:

```text
shared object boundaries
= organisation-wide meaning

capability behaviour
= how a bounded capability works with those objects

access / credentials
= which systems and actions a runtime is allowed to use
```

Do not solve a missing shared invariant by granting a domain capability or its credentials everywhere.
