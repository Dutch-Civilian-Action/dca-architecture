# DCA Architecture

Canonical, version-controlled specifications for Dutch Civilian Action.

This repository describes **what DCA means and how DCA is structured** across organisational reality, operations, systems, interfaces, and reusable specifications.

It is not the place where day-to-day DCA work is executed.

## Top-level structure

- `organisation/` — shared organisational reality, structure, governance, boundaries, and organisational interfaces
- `operations/` — stable operational specifications and cross-domain workflow definitions
- `systems/` — system and data architecture supporting DCA work
- `contracts/` — explicit interfaces, data contracts, and cross-system agreements
- `templates/` — reusable specification and documentation templates
- `decisions/` — architecture and structural decision records

## Core boundary

DCA architecture is independent of any single AI provider, application, or implementation tool.

AI configuration belongs in `dca-ai`.
Website implementation belongs in `dca-website`.
Operational records remain in their authoritative operational systems and Shared Drives.
