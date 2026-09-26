---
document_type: dca_system_standard
status: current
scope: development_testing_and_production_promotion
provider_independent: true
---

# Development, Testing and Production Promotion

## Purpose

Define how DCA develops and tests system changes before adopting them in operational use. This standard applies to data models, mappings, interfaces, AI behaviour, integrations and automation. It inherits the [Shared System Structural Rules](shared-system-structural-rules.md); it does not grant credentials, change action authority or make a proposed domain model canonical.

Use development/test environments for new structures, unresolved mappings and experiments that could change operational meaning or behaviour. Routine work through an accepted operational workflow continues in its established destination; it does not require a fresh test-base cycle for every record or minor correction.

## Environment roles

| Environment or layer | Purpose | Authority boundary |
|---|---|---|
| Development/test | Build and inspect candidate structures; test behaviour with bounded examples and copied source data | Successful entry or execution does not establish operational truth or production readiness |
| Evidence/reconciliation staging | Preserve genuine submissions, evidence, unresolved reconstruction and validation lineage | Operational evidence remains meaningful even before canonical promotion; this layer is not a disposable schema sandbox |
| Production | Maintain accepted structures and operational records through the applicable workflow | A production destination does not make every proposed schema, imported value or generated result validated |
| Historical/legacy source | Preserve earlier operational material for an authorised reconstruction or migration | Its location in a test workspace does not make its contents synthetic or safe to overwrite |

The current workspace/base identities and Airtable-specific capability context are maintained in the [DCA AI workspace map](https://github.com/Dutch-Civilian-Action/dca-ai/blob/main/context/airtable-workspace-map.md). Resolve the development destination and intended production destination separately.

For Airtable builds, use the current [DCA Airtable Implementation Standard](https://docs.google.com/document/d/17yO7HdChXXvlxekLJjSqiHNgDWmKQm2VstpErtSJ_4c/edit?usp=drivesdk) for implementation conventions after establishing the relevant structural and operational requirements.

## Build and test a bounded change

1. State the question or change being tested, the exact environment and base/system identities, the intended production destination, and the source/version being mapped. Reuse an appropriate designated test environment after checking its contents and purpose. A similarly named or historical base is not automatically a suitable sandbox.
2. Start with the smallest representative sample that can test the real uncertainty. For a workbook migration, use source-linked examples before attempting a full transfer or exhaustive reconstruction. Include incomplete, conflicting, aggregate or individually identified cases when they are relevant and available; do not manufacture precision to make the model pass.
3. Keep copied real examples distinguishable from synthetic fixtures. Preserve source references, original values, identifiers, uncertainty and validation status. A controlled test using real evidence does not make that evidence fictional. Test copies are not a second operational register, and synthetic fixtures must not enter operational matching or reporting.
4. Exercise the candidate structure and relevant behaviour in the designated environment. AI and other enabled development features may be used within the task's existing access and authority. Contain test side effects within the agreed scope; a test label alone does not authorise live messages, external transactions or production writes.
5. Record what was tested against which schema/configuration revision, the observed result and any remaining gap in the existing build record or PR. System & Structure reviews representation and mapping; the relevant operational owners validate meanings, source interpretation and usability. Use existing decision authority rather than inventing a parallel approval role.

Testing should address the change's actual risks and unresolved questions. Do not require an elaborate test programme where a small, inspectable example is sufficient.

## Keep acceptance claims separate

- **Structure accepted:** the model and mapping represent the reviewed examples at their supported granularity.
- **Data validated:** the relevant records, meanings, quantities and gaps have been reviewed at the stated scope. Accepting a sample does not validate the full historical dataset.
- **Behaviour verified:** the specified runtime or workflow actually behaved as expected under the tested conditions. Schema existence, available features and a successful manual action do not prove an automated runtime works.
- **Production adopted:** the accepted change was applied to its intended production destination and read back there.

State only the stages supported by evidence. Preserve remaining uncertainty and workflow-specific gates.

## Promote the accepted change

Apply the accepted schema/configuration and reconcile the required real data into the established production destination. Do not promote by silently relabelling the whole test base, overwriting production with a test copy, or copying synthetic fixtures. Preserve stable organisational identities, provenance, corrections, relationships and known overlap so the same underlying goods or event is not counted twice.

Before enabling a feature in production, check the actual target's feature availability, runtime access and behaviour. Development entitlements do not establish production entitlement or executor capability. Where the target differs, adapt and verify the bounded change rather than assuming a successful test transfers unchanged.

Keep the migration or correction path proportionate to the change, verify the affected production records/configuration by readback, and update the existing repository mapping/build record with the actual outcome. Testing or schema acceptance does not automatically authorise downstream valuation, reporting, automation or other separately gated work.
