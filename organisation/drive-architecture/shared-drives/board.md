---
document_type: dca_shared_drive_readme
drive: DCA Board
semantic_role: formal_board_governance
status: current
canonical_home_for:
  - board_minutes
  - board_decisions
  - board_governance_records
  - board_period_records
not_canonical_for:
  - functional_operations
  - technical_implementation
  - informal_working_material
---
# DCA Board — Semantic Structure

## Purpose
This Shared Drive is the formal governance record space for DCA's board.

## What belongs here
- board meeting records, minutes, resolutions, approvals, and formal governance material;
- documents whose authority comes specifically from board review or decision;
- governance records that must remain attributable to a board period or year.

## What does not belong here
- ordinary functional working documents;
- operational source records;
- technical schemas or implementation material;
- copies of canonical documents from other drives merely because the board discussed them.

## Hierarchy semantics
This drive is naturally time-oriented. Year or governance-period groupings are valid because board records derive meaning from when a decision or governance action occurred.

When the board approves or reviews a canonical artifact owned elsewhere, preserve the board decision here and reference the canonical artifact rather than creating an uncontrolled new source of truth.

## Machine routing rule
Route here only when the artifact is a formal board-governance record or when its authority specifically derives from board action. Otherwise route to the organisational or functional domain that owns the underlying work.
