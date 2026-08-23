---
document_type: dca_shared_drive_readme
drive: DCA Systems & Data
semantic_role: technology_data_infrastructure
status: current
canonical_home_for:
  - technical_architecture
  - platform_schemas
  - data_models
  - crm_data_infrastructure
  - integrations
  - automation
  - ai_agents
  - reporting_infrastructure
  - technical_tests
not_canonical_for:
  - functional_operations
  - organisational_truth
  - organisational_structure_as_such
---
# DCA Systems & Data — Semantic Structure

## Purpose
This Shared Drive holds the technology and data infrastructure that supports DCA's organisational and functional work.

## What belongs here
- technical architecture and standards;
- Airtable schemas, field specifications, naming rules, imports, migrations, and technical working material;
- CRM and relationship-data infrastructure, reconciliation, migration/build artifacts, and technical data models;
- integrations and automations;
- AI and agent definitions;
- data warehouse and reporting infrastructure;
- technical documentation;
- tests;
- superseded technical implementations in archive.

## What does not belong here
- warehouse procedures merely because Airtable supports them;
- outreach emails/call execution merely because CRM records them;
- fundraising or finance operations themselves;
- organisation-wide reality, roles, functions, governance, or structure merely because they may later be represented in a system.

## Hierarchy semantics
Technical domains can each use lifecycle states such as:
- current;
- working;
- migration / imports / build;
- tests;
- archive.

## Core classification rule
**Classify by what the artifact is, not merely what domain it talks about.**

Examples:
- CRM Airtable schema → Systems & Data;
- relationship-data reconciliation mapping → Systems & Data;
- Rotary outreach mail → Fundraising;
- logistics SOP → Warehouse & Logistics;
- Airtable fields implementing logistics tracking → Systems & Data.

## Machine routing rule
Route here only when the artifact is a technical/data mechanism, model, integration, implementation, migration, automation, AI component, or technical test. The work being supported remains in its functional drive.
