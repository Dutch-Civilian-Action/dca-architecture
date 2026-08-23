---
document_type: dca_shared_drive_readme
drive: DCA Uploads
semantic_role: temporary_intake_and_staging
status: current
canonical_home_for: []
not_canonical_for:
  - organisational_knowledge
  - operational_records
  - technical_authority
---
# DCA Uploads — Semantic Structure

## Purpose
This Shared Drive is temporary intake and staging only.

It is not a knowledge store and should not become the canonical home of any DCA artifact.

## What belongs here
- newly received files awaiting classification;
- temporary migration intake;
- temporary documentation/media staging before routing to the correct Shared Drive.

## What does not belong here
- final or authoritative documents;
- long-lived operational records;
- system schemas;
- permanent media archives;
- files left here simply because their destination is unclear.

## Lifecycle semantics
An item in Uploads should move through:
intake → classification/review → canonical destination or deletion.

Migration staging does not change the authority or connector permissions of a legacy file; it is only a human organisation aid.

## Machine routing rule
Never treat presence in Uploads as a domain or authority signal. Determine the artifact's real domain and lifecycle status, then route it out.
