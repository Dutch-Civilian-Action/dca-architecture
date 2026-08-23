---
document_type: dca_shared_drive_readme
drive: DCA Fundraising
semantic_role: fundraising_operations
status: current
canonical_home_for:
  - campaigns
  - fundraising_outreach
  - donor_stewardship
  - grants
  - fundraising_events
  - fundraising_reporting
not_canonical_for:
  - validated_finance_transactions
  - crm_technical_schema
  - marketing_publication_production
---
# DCA Fundraising — Semantic Structure

## Purpose
This Shared Drive holds the operational work by which DCA raises, stewards, and follows up funding and supporter relationships.

## What belongs here
- fundraising operating guidance and planning;
- campaigns and campaign working material;
- donor stewardship and post-donation activity;
- grants;
- fundraising events;
- outreach operations, outreach batches, emails, call history, and follow-up material;
- fundraising presentations and fundraising-specific assets;
- fundraising reporting and relevant working data;
- historical fundraising operations in archive.

## What does not belong here
- canonical CRM schema, field definitions, migrations, or integrations;
- validated bookkeeping/transaction truth;
- technical Donorbox/Bunq/Airtable integration logic;
- final marketing publication production that belongs to Marketing & Storytelling.

## Hierarchy semantics
The drive may contain semantic domains such as campaigns, donors/stewardship, grants, events, outreach, planning/working, validation inputs, fundraising data/reporting, and archive.

The current physical folders may still be normalised over time; route by these meanings rather than by old folder names.

## Boundary rules
- donor intent and fundraising context → Fundraising;
- validated financial transaction → Finance;
- CRM/relationship-data infrastructure → Systems & Data;
- published communication → Marketing & Storytelling.

## Machine routing rule
Route here when the artifact is part of fundraising work itself. Route its technical/data implementation to Systems & Data and its validated financial result to Finance.
