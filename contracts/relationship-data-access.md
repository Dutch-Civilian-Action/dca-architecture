# Relationship Data Access Contract

## Purpose

Define the stable, provider-independent interface for reading, reconciling, and maintaining DCA relationship data.

This contract does not define an AI agent, Airtable prompt, Slack interface, or provider runtime. It defines the shared interpretation that any interface or automation must preserve when interacting with DCA relationship data.

## Scope

This contract applies to interfaces that read or write canonical relationship information involving:

- Contacts
- Organizations
- Contact–Organization relationships
- Partners and other evidence-supported DCA relationship roles
- intake/provenance records
- unresolved review states

The exact physical table and field implementation may evolve. Canonical meaning must remain consistent with the DCA architecture and current validated relationship model.

## Canonical entity boundaries

### Contact

A Contact represents a person or a generic organizational contact route.

A Contact does not inherit DCA relationship roles from an Organization merely because the Contact is linked to that Organization.

### Organization

An Organization represents the organization itself.

Organization classifications and DCA relationship roles must be evidence-supported.

### Contact–Organization relationship

The relationship between a Contact and an Organization must be represented explicitly when the relationship itself carries meaning, such as:

- the Contact acts for the Organization;
- the Contact has a role inside the Organization;
- the Contact has a DCA-facing function for that Organization;
- primary-contact status is known.

The external role inside the Organization, the DCA contact function, and the DCA relationship role are distinct facts.

### Partner

Partner status is a DCA relationship fact and must be evidence-supported.

Operational context alone does not establish partner status. In particular, appearing in Logistics work does not automatically make an Organization or Contact a partner.

## Provenance and intake

New relationship information must preserve its source or equivalent provenance before it changes canonical relationship data.

Where the active implementation uses an intake/staging object, the original submitted information should remain recoverable and linked to the resulting canonical resolution where practical.

Unknown information remains unknown. Interfaces must not complete missing fields by guessing.

## Search before create

Interfaces must search canonical relationship data before creating new Contacts or Organizations.

Creation is allowed only when no sufficiently supported existing identity is found and the submitted identity is clear enough to represent safely.

Interfaces must not create duplicates merely because of differences in:

- capitalization;
- punctuation;
- common abbreviations;
- spacing;
- spelling variation where other evidence indicates the same Organization.

## Identity resolution

Identity resolution must be evidence-based.

For Contacts, strong evidence may include:

1. exact email;
2. exact or normalized phone number;
3. full name together with Organization;
4. name plus other strong contextual evidence.

Name similarity alone is not sufficient evidence for merge or overwrite.

For Organizations, evidence may include:

1. exact or normalized Organization name;
2. known alias;
3. website or domain;
4. location combined with Organization identity/context.

If more than one plausible identity remains, the interface must not resolve the ambiguity by guessing.

## Update behaviour

When one clear canonical match exists:

- add or update only facts supported by the new evidence;
- do not erase existing information because the new source omits it;
- do not silently overwrite conflicting information;
- preserve conflict and source context when the new evidence cannot safely supersede existing data.

When no canonical match exists and identity is sufficiently clear:

- create only the minimum canonical object(s) required by the evidenced reality;
- create the explicit Contact–Organization relationship when that relationship is evidenced;
- avoid assigning unsupported DCA roles, classifications, or partner states.

## Uncertainty and conflict

Ambiguity is valid system state.

If evidence conflicts, identity remains uncertain, or more than one plausible match exists:

- canonical records must remain unchanged unless one source clearly supersedes another;
- the unresolved information must remain visible through the existing review or clarification mechanism;
- the unresolved question should be stated precisely;
- the interface may request additional evidence.

## Privacy and access

Relationship data may contain restricted operational information.

Any interface must preserve the access boundary of the authoritative system.

It must not:

- widen visibility merely because a field can technically be retrieved;
- reproduce restricted personal phone numbers, personal email addresses, or comparable contact details into broad or public communication surfaces;
- bypass the requesting user's permissions.

## Confirmation boundary

This contract does not require one universal confirmation pattern for every implementation.

Implementations must distinguish between low-risk deterministic changes and consequential changes.

Identity-changing, relationship-changing, destructive, ambiguous, or otherwise consequential writes require confirmation or review according to the active implementation policy.

Early pilots may require confirmation before every canonical write.

## Interface neutrality

This contract is independent of:

- Airtable Omni
- Claude
- Slack
- any future AI provider
- any future user interface

Provider-specific instructions belong in the relevant implementation repository. They must implement this contract rather than redefine it.
