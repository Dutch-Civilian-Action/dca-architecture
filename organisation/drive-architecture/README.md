# Drive Architecture

Semantic architecture for DCA Shared Drives and document routing.

This area defines how people and machines determine the canonical organisational home, lifecycle state, and authority of DCA artifacts. Folder names may evolve; the semantic routing logic should remain stable.

## Canonical specifications

- `routing-logic.md` — global Shared Drive architecture and routing rules
- `shared-drives/` — semantic meaning of each active Shared Drive
- `shared-drives/legacy/` — retired Shared Drives retained only as migration/source context

## Active Shared Drives

- `shared-drives/organisation.md`
- `shared-drives/board.md`
- `shared-drives/warehouse-logistics.md`
- `shared-drives/ukraine-operations.md`
- `shared-drives/fundraising.md`
- `shared-drives/finance.md`
- `shared-drives/marketing-storytelling.md`
- `shared-drives/systems-data.md`
- `shared-drives/uploads.md`
- `shared-drives/vault.md`

## Legacy Shared Drives

- `shared-drives/legacy/dca-core.md`
- `shared-drives/legacy/dca-files.md`

## Relationship to Google Drive

The files in this repository are the canonical, version-controlled semantic specifications.

Each actual DCA Shared Drive may contain a simpler local README for people working in that Drive. Those local READMEs should explain the Drive in user-friendly language and point back to the canonical specification here. They are an interface to the architecture, not a second independently maintained source of truth.
