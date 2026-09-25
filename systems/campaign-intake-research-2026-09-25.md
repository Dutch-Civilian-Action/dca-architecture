# Campaign intake and Airtable routing — working assessment (25 September 2026)

**Status:** research and proposal for review. This is not an approved data model, a production build instruction, or a decision to move existing Campaigns.

## Question and recommendation

Bas needs one place to supply fundraising campaign facts and open questions without answering across Slack threads. Anja needs those inputs for campaign briefs and Donorbox setup. A reusable intake may help, but an input request, an operational Campaign, a public donation page, a donor designation, an outreach activity, and an allocation have different meanings and review paths.

**Proposed next step:** keep the current Bas working document for the immediate H24 work. Prototype a short request form and provisional `Campaign_Requests` table in the designated Dev/Test Airtable environment. Test it against real cases and the existing Campaigns form. Decide whether a separate intake is warranted or whether the live Campaigns draft path can be safely extended before any production adoption. Do not route unreviewed form submissions into production Campaigns in the meantime.

## Sources checked

- [Current Airtable workspace map](https://github.com/Dutch-Civilian-Action/dca-ai/blob/main/context/airtable-workspace-map.md): production `DCA Relationships & Workflows` is `appMdqKYTMnPmVoVu`; the Shared Structure base has a bounded Projects/Needs build, not a completed Campaigns migration; new schema experiments belong in Dev/Test.
- [Shared Structure build record](https://github.com/Dutch-Civilian-Action/dca-ai/blob/main/context/shared-structure-build.md): Campaigns remain in the current operational location during the controlled transition.
- [Shared System Structural Rules](./shared-system-structural-rules.md) and [Development, Testing and Production Promotion](./development-testing-and-promotion.md): separate the object from its workflow state, source, validation and public claims; test new structures before production adoption.
- [DCA Airtable Implementation Standard](https://docs.google.com/document/d/17yO7HdChXXvlxekLJjSqiHNgDWmKQm2VstpErtSJ_4c/edit): field/table naming, stable IDs, descriptions, lifecycle and validation distinctions, dependency checks, and base guide.
- [DCA Operational Reality — 2nd Pass](https://docs.google.com/document/d/11_JG166GB_OUydQdzHU7dMUYOCJUpxj_yFLkJgOOOLU/edit), especially OR2-178–182, 189–201, 288 and 365. These are reported/observed operating descriptions and unresolved gaps, not an approval for new claims or financial rules.
- [Bas's working donation options](https://docs.google.com/document/d/1lLsitXIZABMQ8qAjS891CcqRrPEG-nz4sy6UYyrOYaA/edit): purpose, frequency and route are different choices; proposed birthday-page allocation language still needs review.
- [Bas input document for H24](https://docs.google.com/document/d/1PLAsEyvONz9JywJQIrXbTUrwJQVe2ovzB6EfWaVGSoA/edit): immediate response surface, with the associated H24 Asana tasks as work tracking.

## Live Airtable observations on 25 September

| Surface | Observed behaviour | Consequence |
| --- | --- | --- |
| [Relationships & Workflows / Campaigns](https://airtable.com/appMdqKYTMnPmVoVu/tblbam3UlEdLGiTRT) (`tblbam3UlEdLGiTRT`) | 12 records. Fields include `campaign_id`, `campaign_name`, `campaign_type`, `owner`, `status`, dates, notes, donations, outreach batches/cycles, and Donorbox events. Types include outreach, fundraising, communication, mission, community and other. Status includes draft. | This is the current operational table, but a draft record is still a Campaign object; it is not automatically an unreviewed intake request. |
| `Create Campaign` Airtable form (`pagPnabIhLEHmR511`) | Creates a Campaign record directly. Requires name, type, owner and status; offers dates and notes. | It does not capture factual sources, uncertainty, page purpose, approval, designation or claim review. Its direct production write is unsuitable as an unreviewed Bas response form. |
| Sample Campaign records | Church and Rotary Outreach 2026, Winter Project — Track A volume goods, Urgent Needs, Monthly Support, an evacuation appeal, a `test` Donorbox entry, and participant fundraiser pages appear in one table. Some have `external_campaign_id` from Donorbox. | The current table spans several operating uses. Record labels and Donorbox identifiers alone do not establish a one-to-one relation between a fundraising purpose, page, outreach activity and campaign. |
| Shared Structure base `appPBY1g1rYKRHbDC` | Current bounded build covers Projects and Needs. | Do not assume Campaigns or intake has already moved there. |

## Boundaries to preserve

1. **Request versus Campaign.** A submitted brief is a proposed input with an author, date, sources, unknowns and review state. A Campaign expresses a chosen purpose and public donor expectation. A request may be returned, combined, split, or linked to an existing Campaign; that relationship is not yet agreed.
2. **Campaign versus page and donation route.** One purpose may appear across a website appeal, Donorbox page, recurring option or participant page. The number of pages is an implementation question, not a required campaign count. Donorbox external IDs and tests belong to the page/route integration.
3. **Facts, media and publication.** For campaign-related outputs in his remit, Bas supplies the purpose, factual points, stories and possible media for each intended publication; other factual owners contribute where the subject requires. Communications develops and reviews wording and visuals. Unsupported numbers, media permissions and proposed donation rules remain open until the relevant operational, rights/privacy and Finance checks and publication approval.
4. **Donation versus allocation.** Campaign totals, transaction records, donor designation, and later allocation/reconciliation must remain distinguishable. A donation option does not by itself decide allocation.
5. **Outreach versus fundraising appeal.** Church/Rotary outreach and a public fundraising appeal may be related without being the same object. Do not force historical records into a new definition to make a form work.

## Candidate Dev/Test intake, for evaluation only

Try a `Campaign_Requests` table with a short form. It should carry provisional inputs, not publish them or create Donorbox pages. Follow the Airtable Implementation Standard for a stable request ID, formula primary display (`ID — name`), snake_case fields, descriptions on fields and controlled options, separate review state and factual validation state, source links, created/updated metadata, and a user-facing guide. These are candidate concepts, not final field names or an accepted schema:

| Form section | Minimum question to Bas/requester | Notes |
| --- | --- | --- |
| Purpose | What is the proposed appeal or brief for, and what work or need would it support? | Link an existing Need/Project/Campaign if known; allow “unknown”. |
| Audience and ask | Who is it for, and what action or donation is being requested? | A church email, Rotary presentation and donation page may need distinct outputs. |
| Facts and evidence | What facts, numbers, examples and source links may be used? Who can verify them? | Record uncertainty and validation separately from the proposed wording. |
| Media candidates | Are there possible photos, video or stories for the website and other outputs? Link or attach them; say what each shows, who made it, and whether permission for this use is confirmed or unknown. | Candidate media is not publication approval; check context, rights, privacy and safe use per output. |
| Donation route | Is a new or existing Donorbox page thought necessary? What donation purpose or designation is proposed? | No forced page count; capture open Finance/Donorbox questions. |
| Timing and handoff | When is the content needed, who owns factual review, who reviews wording, and what remains undecided? | Distinguish an approximate target from an agreed deadline. |

Keep the form short enough for one sitting; link longer working documents where needed. Submission should start a review, with an explicit decision and source-linked mapping into existing Campaigns and any page/communication work. Do not create Campaigns, publish copy, set donation rules, or mark claims validated as an automatic effect of form submission.

## Tests and decision gate

Use a few source-linked cases in Dev/Test: the four H24 briefs, a church/Rotary outreach case, an existing monthly/urgent Donorbox option, a participant/birthday page, and an appeal supporting more than one purpose. Compare each with the current Campaigns draft/form route. Check whether one request can safely map to an existing Campaign, multiple outputs, or no Campaign; whether Bas can complete the form without inventing page counts or approval; whether Anja can see what is still blocked; and whether historical Donorbox/outreach records remain intelligible.

Before adopting a production intake, System & Structure with fundraising, Communications and Finance should decide:

- What makes one Campaign distinct from a Donorbox page and from an outreach grouping? Is the existing `campaign_type` sufficient for those uses?
- Can a draft Campaign safely hold unverified requests, or is a separately governed request object necessary? Who accepts/rejects and links a request?
- Which facts and claims require whose validation, and what permits Donorbox setup/test versus public publication?
- How are donor designation and multiple supported purposes represented without implying an approved allocation rule?
- Which existing Campaign records need data cleanup or cross-links before a new form is exposed?

**Promotion sequence:** document the boundary decision; build and inspect in Dev/Test; test cases and operator experience; check naming, descriptions, ID/display formula, links, permissions and automation effects; obtain structure and data acceptance; plan controlled production adoption and readback. Only then update the operational Airtable map, add any provider-independent intake workflow in `dca-ai`, and bind actual form/adapter automation. These are separate gates, not one launch.


## Bounded Dev/Test build on 25 September

A candidate base was created in the designated **DCA Dev/Test workspace**: `[DEV] DCA Campaign Intake — R01` (`app3iDXtg7mN2tfxz`). Its `Campaign_Requests` table (`tblHRVRABGAvUdE31`) holds provisional request purpose, work/Need, audience and ask, facts/sources, validation questions, intended publications, candidate media attachments/references with context and rights questions, page/route, designation questions, timing, source document, submitter, reviewer, disposition and optional operational Campaign URL. It has separate `request_status` and `validation_status` choices, `created_at`/`last_modified` timestamps, an auto number and formula `request_id`. `Base_Guide` (`tbl1eWlhScjFkSmJa`) also explains scope, handoff and the production gate. The select field descriptions now define each option in Airtable itself, as the implementation standard requires. A **synthetic** `draft`/`not_reviewed` record confirmed the formula resolves to `CRQ-0001`; no H24 or other real request was copied in.

A naming audit against the linked Airtable Implementation Standard found that `Campaign_Requests`, `Base_Guide` and the fields follow Title_Case/snake_case, `request_id` is separate from the primary display, and `last_modified_at` was corrected to `last_modified`. `factual_validation` was renamed `validation_status`; both select field descriptions now define every option. The prototype still lacks the required formula primary display and an Airtable **Base guide** description; the `Base_Guide` table is not a substitute. Authoritative machine-readable rules for the controlled options and representative tests are also outstanding.

This is a schema experiment, **not yet a usable intake form or a standard-compliant build**. The connected Airtable tool cannot create a form or convert the default primary `request_display` from plain text to the required `ID — name` formula. Browser access to Airtable was blocked by a saved preference in this session. There is no form link, linked production Campaign, automation, reviewer permission test or representative case replay. Complete those items and compare with the existing Campaigns draft route before any user intake or production adoption. The prototype base should not be presented to Bas as his current response destination.

## Correction from the initial experiment

An earlier `Campaign Intake` table was created in `DCA - Fundraising & Impact` (`appfrCo2WDS2owEe2`), which is not the current operational destination in the workspace map. It contained one draft record. The table and record were removed on 25 September. Its old `Campaigns` table (`tbld7KLPz97ehZF7F`) still shows an empty reciprocal field `fldQyLqWgSehqnow7`, now plain text after table deletion. This inert field needs a reviewed cleanup with a dependency check; it is not part of the proposed intake. The Bas working document and H24 task links remain usable.
