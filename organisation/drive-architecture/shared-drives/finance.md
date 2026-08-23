---
document_type: dca_shared_drive_readme
drive: DCA Finance
semantic_role: finance_operations_and_financial_truth
status: current
canonical_home_for:
  - validated_financial_records
  - receipts
  - reconciliation
  - finance_reporting
  - declarations_reimbursements
  - finance_administration
not_canonical_for:
  - donor_intent
  - fundraising_outreach
  - technical_integration_design
---
# DCA Finance — Semantic Structure

## Purpose
This Shared Drive holds DCA's finance operations and the evidence used to establish financial truth.

## What belongs here
- validated transactions and bookkeeping outputs;
- reconciliation material;
- receipts and supporting documentation;
- declarations, reimbursements, and finance-administration records;
- contracts where Finance is the operational owner;
- finance reports;
- in-kind financial treatment / valuation material;
- time-based finance records and archives.

## What does not belong here
- donor-facing intent or campaign narrative;
- fundraising outreach history;
- system schemas, integration definitions, automation code, or AI logic;
- general operational evidence merely because it has a cost.

## Hierarchy semantics
Useful semantic zones include:
- finance standards / current procedures;
- transactions / reconciliation;
- receipts / evidence;
- declarations / reimbursements;
- contracts / administration;
- in-kind finance;
- reporting;
- working / validation;
- period-based archive.

Year folders are valid as temporal partitions, but the semantic meaning of the records still comes from finance operations.

## Boundary rules
- fundraising intent → Fundraising;
- finance-validated transaction truth → Finance;
- technical matching between Donorbox, Bunq, Informer, Airtable, or other systems → Systems & Data.

## Machine routing rule
Route here when the artifact establishes, supports, or reports finance-operational truth. Do not route here solely because money is mentioned.
