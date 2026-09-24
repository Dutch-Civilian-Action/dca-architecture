---
document_type: working_assessment
status: proposal_for_review
date: 2026-09-24
scope: dca_architecture_and_dca_ai_repository_boundaries
does_not_define:
  - new_organisational_function
  - inbox_ownership
  - claude_project_scope
  - new_repository
  - runtime_authorisation
---

# DCA AI and architecture — repository boundary assessment

## Decision requested

Keep DCA organisational meaning and cross-functional responsibility grounded in current DCA reality and, when sufficiently established, in `dca-architecture`. Keep AI-supported work contracts, packaging, adapters, access configuration, and tests in `dca-ai`. Before expanding Bas's Claude project to cover three shared inboxes, establish what kinds of work enter those inboxes, which DCA function owns each kind, what follow-through must survive, and what is only a handoff. Then adapt the Claude configuration. Do not split `dca-ai` merely because it has grown.

This is a working assessment, **not** an accepted organisational decision, a live project instruction, or evidence that the proposed workflow is deployed.

## Scope and evidence

Repository snapshot on 24 September 2026: `dca-ai` main tree `717167e` (209 files, about 2.61 MB); `dca-architecture` main tree `a1d8c70` (33 files, about 0.22 MB). About 1.39 MB and 76 files of the AI repository are the [Claude design asset bundle](https://github.com/Dutch-Civilian-Action/dca-ai/tree/main/providers/claude/skills/dca-design), including fonts, images, components and UI kits. The remaining 133 files total about 1.22 MB. Repository byte size therefore overstates instruction growth.

The [recent merged PR history](https://github.com/Dutch-Civilian-Action/dca-ai/pulls?q=is%3Apr+is%3Amerged) shows 20 `dca-ai` PRs merged from 17 through 24 September; [architecture history](https://github.com/Dutch-Civilian-Action/dca-architecture/pulls?q=is%3Apr+is%3Amerged) shows one in the same interval. This is a measure of change activity, not proof that the architecture is deficient or that any specific AI rule is unnecessary. This review inspects repository content and recorded runtime evidence; it does not independently inspect the live Claude project configuration or run Claude acceptance cases.

## Current division of responsibility

| Source | Current role | Boundary |
| --- | --- | --- |
| [DCA authority map](../organisation/shared-foundations/authority-map.md), [shared object boundaries](../organisation/shared-foundations/shared-object-boundaries.md), and [structural rules](shared-system-structural-rules.md) | Cross-domain meaning and method | Do not infer current inbox ownership or a final operating model from an AI project. |
| [Current Operational Reality](https://docs.google.com/document/d/11_JG166GB_OUydQdzHU7dMUYOCJUpxj_yFLkJgOOOLU/edit) and relevant functional evidence | What people currently do, decide, hand over, and leave unresolved, with its validation status | The repository pointer is not a substitute for reading the maintained source. |
| [DCA Fundraising](../organisation/drive-architecture/shared-drives/fundraising.md), [Organisation](../organisation/drive-architecture/shared-drives/organisation.md), and [Marketing & Storytelling](../organisation/drive-architecture/shared-drives/marketing-storytelling.md) semantic routes | Established functional/document homes | Fundraising outreach, organisation-wide governance, and communication production have different responsibilities. |
| [`dca-ai` workflows](https://github.com/Dutch-Civilian-Action/dca-ai/tree/main/workflows), [governance](https://github.com/Dutch-Civilian-Action/dca-ai/tree/main/governance), [skills](https://github.com/Dutch-Civilian-Action/dca-ai/tree/main/plugins), [providers](https://github.com/Dutch-Civilian-Action/dca-ai/tree/main/providers), and [tests](https://github.com/Dutch-Civilian-Action/dca-ai/tree/main/tests) | AI execution contracts, packaging, runtime configuration, and verification | AI instructions apply established meaning; their presence in Git is not organisational adoption or proof of runtime loading. |

The repositories already *state* this boundary. The issue is whether each new rule is placed and loaded at the correct layer, remains proportionate to the work, and has evidence of effect.

## Findings and risks

1. **A real implementation capability exists, but its scope is narrower than the proposed inbox project.** [Fundraising outreach](https://github.com/Dutch-Civilian-Action/dca-ai/blob/main/workflows/prepare-fundraising-outreach.md) is an experimental preparation workflow for churches, Rotary, donors, funders and partners; [the Claude project guide](https://github.com/Dutch-Civilian-Action/dca-ai/blob/main/providers/claude/projects/fundraising-outreach.md) records intended configuration and explicitly does not establish live deployment. A message received at `community@`, `info@` or `volunteer@` may concern Fundraising, volunteer onboarding, Logistics, Finance, or general coordination. The address is a route, not proof that all such work belongs in one Fundraising capability. Renaming the project to “External Relationships & Correspondence” before classifying the real requests could quietly broaden authority. The name suggested in conversation is therefore a **candidate**, not an approved scope.

2. **The repository, installed skill, project instructions, and runtime result are separate states.** The [Winter Needs test record](https://github.com/Dutch-Civilian-Action/dca-ai/blob/main/tests/workflows/review-dca-needs.md) reports an initial cold-trigger failure, and a later first-turn run with skill-read activity but failures of one-Need-at-a-time behavior and operational language. It also records a later operator-reported successful handoff without enough evidence to mark the full acceptance set passed. The exact loaded revision was not established. These observations do not isolate document length or instruction count as the cause. They do establish that a Git correction is insufficient as a runtime verification. [PR #60](https://github.com/Dutch-Civilian-Action/dca-ai/pull/60) proposes correcting the overly broad Winter handover; it was open at this snapshot and is not the live project configuration.

3. **Repeated mandatory rules may widen their practical effect.** The [AI authority rules](https://github.com/Dutch-Civilian-Action/dca-ai/blob/main/governance/authority-rules.md#dataset-prerequisite-for-operational-automation) require a shared dataset before downstream operational automation. A version is repeated in [Claude provider guidance](https://github.com/Dutch-Civilian-Action/dca-ai/blob/main/providers/claude/README.md#dataset-prerequisite-across-claude-surfaces), the [Fundraising project guide](https://github.com/Dutch-Civilian-Action/dca-ai/blob/main/providers/claude/projects/fundraising-outreach.md), and Winter instructions. The rule has an intentional narrow scope; the [architecture development standard](development-testing-and-promotion.md) permits bounded design and testing before production adoption. A runtime that applies the repeated stop condition to ordinary drafting, source inspection, or Dev/Test work would exceed that scope. The Fundraising guide explicitly carves ordinary work out, which indicates this requires a focused behavior check. No contradiction or actual misapplication is established by document comparison alone.

4. **Some general work contracts are AI-specific and legitimately belong in `dca-ai`; some underlying meanings may need DCA-level decisions first.** The [meeting-action workflow](https://github.com/Dutch-Civilian-Action/dca-ai/blob/main/workflows/meeting-actions-to-asana.md) and [Need review workflow](https://github.com/Dutch-Civilian-Action/dca-ai/blob/main/workflows/review-dca-needs.md) can define how AI assists existing work. They cannot independently decide who owns cross-domain messages, who may confirm a commitment, or whether a newly observed practice has become a DCA standard. [Draft PR #57](https://github.com/Dutch-Civilian-Action/dca-ai/pull/57) is already separating a meeting-action contract from executor identity; review it as part of this boundary audit rather than treating the branch as main.

5. **Document weight is not equivalent to the active context delivered to Claude.** The full repository is not necessarily loaded in every Claude session. The critical audit unit is a real task's active path: project instruction → triggered skill → reachable workflow/authority source → tool access → observed result. Large archived tests or design assets may have no effect on an inbox reply. Conversely, a short but overbroad standing instruction may affect every reply.

## Proposed sequence

1. **Resolve the DCA-level question with a bounded sample of real inbound work.** Use current Operational Reality and representative threads from the three shared inboxes. For each thread identify the request, person/organisation and route where established, relevant function, current owner/decision right, handoff, next action, record of the outcome, and unresolved ownership. Distinguish Fundraising replies from volunteer onboarding, operational requests, Finance matters and general organisational coordination. Do not add a generic “External Relationships” function or new system object solely to fit a Claude project.

2. **Record only the established cross-domain boundary in the appropriate DCA home.** Function-specific procedures remain with their functions; organisation-wide responsibility or handoff rules belong in the Organisation working structure and, when validated, its canonical route. Amend `dca-architecture` only for stable, cross-domain meaning or requirements. Reuse the existing identity/relationship and provenance rules.

3. **Run a thin `dca-ai` inventory before extending capability.** For every active AI workflow and Claude project, record the organisational requirement/source, owner, status, actual user task, entry point, loaded skill and workflow, permitted tools/actions, live deployment evidence, acceptance result, and overlapping instructions. Mark proposed, tested, configured, and adopted states separately. Prioritise the Winter and Fundraising paths and the three open PRs [#60](https://github.com/Dutch-Civilian-Action/dca-ai/pull/60), [#57](https://github.com/Dutch-Civilian-Action/dca-ai/pull/57), [#52](https://github.com/Dutch-Civilian-Action/dca-ai/pull/52). Continue targeted fixes; defer broad new standing rules until their source, scope and runtime effect are clear.

4. **Then adapt Bas's Claude surface.** Preserve the existing bounded Fundraising preparation capability. Add inbox triage/routing only for the DCA-level cases established above; keep each function's decision and maintained record in its existing home. Test with real representative asks from Bas's account, including a Fundraising reply, a volunteer enquiry, and an `info@` message that belongs elsewhere. Verify skill loading, source access, concise response, handoff, and whether a message is merely drafted or actually sent. A project name should describe the proven operational scope.

5. **Decide on a repository split only if it solves an observed boundary.** Plausible triggers are different maintainers or review authority, release cadence, credential exposure, or runtime packaging that cannot be kept clean within directories. The design asset bundle already explains much of the byte count; splitting the AI workflow and provider folders now would introduce cross-repository version coordination without resolving instruction loading or organisational authority. Reassess after the active-path inventory.

## Review outcome sought

Agree the investigation order and ownership of the DCA-level inbox classification. This PR accepts no new Claude authority, changes no live instructions, and does not require all DCA architecture to be finished before a bounded useful workflow can advance.
