---
document_type: dca_shared_drive_readme
drive: DCA Vault
semantic_role: restricted_secrets_and_credentials
status: current
canonical_home_for:
  - restricted_credentials
  - secrets
  - protected_access_material
not_canonical_for:
  - general_technical_documentation
  - operational_documents
  - organisational_knowledge
---
# DCA Vault — Semantic Structure

## Purpose
This Shared Drive is a restricted security boundary for credentials, secrets, and other protected access material.

## What belongs here
- encrypted credential material;
- secrets and access information requiring restricted handling;
- other material whose primary classification is restricted access/security.

## What does not belong here
- general system documentation;
- architecture diagrams;
- operating procedures;
- ordinary organisational or functional records.

General technical documentation belongs in Systems & Data and may reference the existence/location of restricted material without duplicating secret contents.

## Machine routing rule
Route here only when the artifact itself contains protected secret/access material. Do not infer or expose contents merely because a file exists in this drive.
