# DCA Shared System — Structural Rules

## Purpose

These rules define how DCA represents organisational and operational reality in shared systems.

They are independent of software platform, database technology, AI provider or model, automation runtime, user interface, and programming language.

Implementations may differ, but they must preserve the structural rules below.

These rules are authoritative over implementation-specific conventions. Platform-specific standards, schemas, agents, extensions, and automations must inherit from them rather than redefine them.

## 1. Reality before structure

System structure must represent real organisational or operational facts.

Before creating or changing a system object, property, relationship, state, workflow, or automation:

- identify the real-world fact being represented;
- identify where that fact belongs;
- distinguish current reality from intended future practice;
- preserve uncertainty, variation, and unresolved interpretation;
- avoid introducing structure only because a particular tool makes it convenient.

Structure must be derived from operational reality rather than used to overwrite it.

## 2. Stable objects and workflow state are different

Stable, reusable organisational objects must remain distinguishable from temporary workflow machinery.

Stable objects may include contacts, organisations, relationships, needs, projects, executions, logistics units, shipments, donations, validated transactions, allocations, deliveries, and impact records.

Workflow structures may contain incomplete information, temporary states, attempts, activities, provisional interpretation, review states, and process-specific data.

Workflow state must not silently become canonical organisational truth.

## 3. Promotion requires resolution appropriate to the target object

Provisional or workflow-held information may become shared canonical information only when it is sufficiently resolved for the object being created or updated.

Promotion must:

- reuse an existing object when it represents the same real-world thing;
- preserve source and provenance;
- preserve uncertainty, conflicts, and unresolved differences;
- avoid duplicate canonical objects;
- avoid classifications not supported by evidence;
- avoid treating successful data entry as equivalent to validation.

Canonical status depends on resolution against the relevant evidence and system boundary, not merely on the fact that information exists in a structured form.

## 4. Stable objects require stable identity

Stable system objects must have a persistent identity independent of their current name, display label, presentation, or platform-specific record identifier.

Human-readable labels may change. Structural identity should not.

Where visible organisational identifiers are used, they should be:

- stable;
- unique within the relevant object type;
- suitable for durable human and system reference;
- independent of a specific software provider.

A platform-native record identifier may support implementation, but it must not be the only identity where DCA requires cross-system continuity.

## 5. Naming expresses meaning

Names must describe the actual object, fact, relationship, state, or function represented.

Do not name structures around:

- software platforms;
- individual people;
- teams merely because they currently operate them;
- temporary implementation mechanisms;
- vague helper concepts.

Prefer explicit names describing real-world facts, system objects, meaningful relationships, source, certainty, and state.

DCA naming convention:

- collections / object sets: `Title_Case`;
- properties / fields: `snake_case`.

Platform implementations may map these conventions to platform-specific constructs, but the naming meaning remains shared.

## 6. Relationships must retain their meaning

Use a direct relationship when the connection itself carries no additional meaning.

Represent the relationship as its own system object when it has properties of its own, such as:

- role;
- quantity;
- amount;
- state;
- timing;
- certainty;
- source;
- evidence;
- responsibility;
- confirmation.

For example:

Donation → Allocation → Execution

is structurally different from attaching an execution reference directly to a donation, because allocation carries its own meaning and governance context.

## 7. Facts and their provenance must remain connected

The system must preserve not only what is known, but how it is known.

Where relevant, structured information should retain:

- source;
- source reference;
- original or raw value;
- confidence;
- validation state;
- confirmation state;
- traceability certainty.

Provenance and certainty are not substitutes for the fact itself. They describe the evidential basis and confidence under which that fact is represented.

A reconstructed, manually reported, partner-confirmed, finance-validated, and directly observed statement may concern the same subject while carrying different evidential status.

## 8. Raw evidence and resolved structure must remain distinguishable

Do not destroy original information while resolving it into structured system objects.

Where interpretation, matching, classification, or resolution occurs, retain both where needed:

- the original evidence or source value;
- the resolved structured meaning.

This prevents cleanup, AI processing, automation, or later reconstruction from turning an interpretation into unsupported certainty.

## 9. Different state dimensions must not be collapsed

Do not use one generic state to represent different dimensions.

Keep distinct where relevant:

- lifecycle state;
- validation state;
- confirmation state;
- certainty;
- integration or sync state;
- publication or readiness state.

For example, `completed` does not mean `validated`, and neither means `safe_to_publish`.

## 10. Operational truth and outputs are different

Communication, reporting, dashboards, documents, AI responses, and other outputs may represent system truth. They do not create that truth merely by stating it.

The following distinctions must remain explicit where relevant:

- campaign ≠ operational execution;
- communication output ≠ confirmed impact;
- media evidence ≠ confirmed delivery;
- donation ≠ allocation;
- donation ≠ validated transaction;
- relationship context ≠ operational fact.

Outputs must remain traceable to the underlying facts, relationships, evidence, and certainty they represent.

## 11. Do not create fake precision

If DCA knows something only approximately, partially, at aggregate level, through reconstruction, or with unresolved uncertainty, the system must represent that limitation.

Do not create:

- inferred records merely to satisfy a schema;
- artificial object-level detail from aggregate information;
- unsupported relationship classifications;
- exact allocation where only broad use is known;
- confirmed states from weak or indirect evidence.

`unknown` is a valid state when the system does not yet know enough.

## 12. Reuse before creation

Before creating a new stable object:

- search for an existing equivalent;
- resolve identity using available evidence;
- update or connect the existing object when justified;
- create a new object only when it represents something genuinely distinct.

Name similarity alone is insufficient evidence of identity.

Where identity remains unresolved, preserve that uncertainty rather than forcing a merge or duplicate creation.

## 13. Structure around meaningful boundaries

When deciding where information belongs, identify:

- the real-world fact;
- the relevant organisational layer;
- the relevant anchor or stable object;
- whether the information is canonical or workflow-specific;
- whether it represents source, state, certainty, relationship, operation, governance, or output.

A new structure should exist because a meaningful boundary or object exists in DCA reality, not because a platform offers a convenient table, field, tag, folder, or automation primitive.

## 14. Automation follows stable structure

Automation and AI may:

- detect;
- extract;
- compare;
- reconcile;
- validate against rules;
- propose changes;
- perform explicitly safe transformations.

They must not compensate for unresolved structural ambiguity by silently inventing structure, certainty, identity, or organisational truth.

Potentially consequential changes require handling appropriate to their risk. Safe mechanical transformations may be automated where rules are explicit and conflicts are checked. Structural changes that can alter meaning, relationships, data interpretation, or downstream behaviour require review or controlled migration.

When an automated system creates, edits, resolves, or proposes shared-system structure, it must follow these structural rules before applying implementation-specific behaviour.

## 15. Implementation must remain replaceable

No architectural rule may depend on one specific database, SaaS product, AI model, automation engine, messaging platform, or programming language.

Platform implementations translate these rules into platform capabilities.

The architecture remains authoritative when an implementation changes.

Implementation-specific standards may define details such as data types, formulas, primary fields, linked-record behaviour, API mappings, runtime permissions, or extension behaviour, but they must remain subordinate to these structural rules.

## Implementation relationship

This document is the platform-independent structural authority for shared-system representation.

Implementation documents should be separated by concern:

- **Airtable Implementation Standard** — maps these rules into Airtable-specific table, field, type, formula, link, primary-field, interface, extension, and automation behaviour.
- **AI / Agent System Rules** — defines how automated agents and AI systems apply these structural rules when reading, resolving, proposing, or modifying DCA system structure.
- **Other platform adapters** — map the same structural rules into future systems without changing the architecture itself.

The DCA Schema Guard is one enforcement implementation of these rules. It is not the source of the rules.