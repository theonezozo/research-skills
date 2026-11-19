# Platform playbooks

## Contents

- [Capability boundary](#capability-boundary)
- [Live interviews](#live-interviews)
- [Outset](#outset)
- [Marvin](#marvin)
- [Qualtrics](#qualtrics)
- [Preflight and data governance](#preflight-and-data-governance)

Use this as a **2026-09-15 public-documentation snapshot**. Resolve source IDs in
[Sources](sources.md). Verify current account access before committing a design.
Labels mean **documented** by a read first-party page, **proposal** assembled from
documented components, or **unverified** in the reviewed evidence. Unverified
does not mean impossible.

## Capability boundary

| Channel | Documented contribution | Quantitative pricing boundary |
|---|---|---|
| Live research with Marvin | Capture Zoom/Meet/Teams, transcribe, observe and analyze [P4] | Researcher must maintain standardized tasks; conversation is not randomization |
| Outset AI interviews | Guides, probes, stimuli, branching/skips, Likert/matrix/ranking, exports [P1-P2] | Verbatim questions, validated currency fields, arm assignment and exact routing logs unverified |
| Marvin AI interviews | New participant interviews, guides, conditional instructions, recordings and analysis [P3] | Explicitly non-verbatim questioning; deterministic numeric experiment controls unverified |
| Qualtrics surveys | Survey-flow randomizer, embedded data, conditional presentation, respondent exports [P8-P10] | Custom monadic/ladders are implementation proposals requiring programming QA |
| Qualtrics pricing solutions | Native PSM and GG; separately purchased conjoint [P7, M3, P11] | Entitlements, native algorithm/export limitations and compatibility apply |
| Marvin repository/Qualtrics import | Import and analyze survey responses alongside interviews [P5-P6] | Import is not survey launch or a substitute for quantitative source data |

Do not describe static unmoderated questionnaires and conversational AI interviews
as interchangeable. Participants in either must be real sampled humans for
customer evidence; synthetic answers are for explicitly labeled QA only.

## Live interviews

Use a human moderator for unfamiliar charging models, enterprise procurement,
ambiguous authority or complex objections. Use a fixed offer card; ask the buyer
to explain the billing basis before interpreting any price answer.

Separate discovery from measurement: conduct standardized tasks before explanatory
probes that could change later answers, or separate the stages into sessions.
Do not coach answers, negotiate, or add features to overcome a price objection.
Record deviations and mode. Use qualitative thresholds as exploratory findings
unless sample and administration support stronger inference.

Marvin documents live capture, notes, meeting-platform integration and observation.
Disclose observers even when the product hides them from the meeting interface.
Do not infer participant recruitment from recording or panel-management features.
[P4]

## Outset

Use documented AI guide creation, adaptive probes, stimuli, screen sharing and
quantitative-style question types for value discovery, pricing comprehension,
package reactions and explanatory follow-up. Its FAQ documents branching/skips
and transcript, report, CSV and media exports. [P1-P2]

For numeric pricing measurement, first demonstrate:

1. Invariant offer and price wording, without changed terms.
2. Validated numeric capture or a verified structured response field.
3. Assigned conditions and exact price sequence preserved in exports.
4. Deterministic routing and stop rules matching the approved specification.

These controls are **not established by the reviewed pages**. A CSV export or
claim of consistency is not proof. If unavailable, place the quantitative task
in a controlled survey and use Outset for explanations. Treat any cross-tool
linkage as a separately approved implementation, not a documented integration.
Do not claim a native PSM, GG or conjoint engine.

## Marvin

Use AI Interviewer to create new studies, specify goals/questions and conditional
instructions, distribute participant links when authorized, and analyze sessions.
Real-time conversation and push-to-record responses are both documented AI
interview modes, not proof of a fixed-question survey. [P3]

**Do not promise verbatim execution:** the help page explicitly says the AI does
not repeat questions word for word. Fixed-price instructions are useful guardrails
but cannot establish quantitative equivalence by themselves. Audit actual output;
move invariant numeric tasks to another channel when needed.

Treat quotas and temporary all-plan offers as account checks, not stable facts.
Check prototype requirements before proposing tests: the documented workflow has
public/no-login, iframe, screen-sharing and device constraints. Do not make
confidential material public or weaken authentication to meet them. [P3]

Use the documented Qualtrics connector for **approved import and analysis**.
It requires appropriate Marvin plan/seat and Qualtrics API access; map only needed
columns and avoid unnecessary names/emails. Do not infer that Marvin launches or
programs Qualtrics surveys. Reconcile refreshes, duplicates and unmatched records.
[P5]

Use recording/transcript/note exports for qualitative traceability. A note CSV
is not automatically an experimental respondent-by-price dataset. Preserve the
original survey export as the quantitative record; verify AI themes against
responses rather than using summaries as statistical calculations. [P6]

## Qualtrics

### Native versus custom

| Method | Documented native route | Custom route or gate |
|---|---|---|
| Van Westendorp | Marketplace pricing-sensitivity template with logic/reporting [P7] | Four numeric questions with independently specified PSM analysis; verify convention |
| Gabor-Granger | Native pricing study and demand/revenue reporting [M3] | Finite prespecified ladder if exact exposure/routing control is required |
| Conjoint | Choice-based conjoint projects [P11] | Verify separate purchase and permissions; do not equate ordinary survey access with conjoint |
| Monadic | General survey components [P8-P10] | Proposal: randomized single-price blocks with embedded assignment |
| Bracketing/price ladder | General survey components [P8-P10] | Proposal: explicit branches and price/response fields, not an assumed native wizard |

### Native Gabor-Granger restrictions

Verify that these documented constraints fit the study before selecting it:

- Initial prices are randomized within the middle third of the configured range.
- Subsequent prices and intervals follow the solution's algorithm; intervals
  cannot be customized, and shown prices can exceed the configured maximum.
- Only one pricing block is supported per survey; separate studies cannot simply
  be combined into the native final report.
- The documented solution is incompatible with the New Survey Taking Experience;
  custom changes to the basic design fall outside stated support.
- The exact prices shown throughout a respondent's survey are **not available**;
  derived pricing fields and reporting buckets are not a complete exposure log.

Accept those limits explicitly or choose a custom implementation. Do not promise
an arbitrary fixed grid or audit-ready exposure history from the native solution.
Treat native "demand/revenue" labels as stated-response outputs unless calibrated
to actual purchasing. [M3]

### Custom monadic proposal

Screen first, then randomize eligible participants to one grouped condition.
Inside each condition set embedded `arm_id`, `assigned_price` and `offer_version`
and show the matching fixed stimulus. Ask identical outcomes after the assignment.
Define behavior for back navigation/re-entry so exposure cannot silently change.

Use the randomizer's even-presentation option only as presentation balancing,
not a guarantee of equal eligible completed cells. Store assignment as data and
test that exports retain it; do not reconstruct it from question order alone.
Use a controlled account-level assignment strategy if accounts, rather than
individuals, are the experimental units. [P8-P10]

### Custom finite-ladder proposal

Build explicit price questions/blocks and branches from the approved finite
decision tree. Store each shown price and response in distinct fields/rows,
including start, sequence, missingness and terminal reason. Never overwrite the
only price field and lose earlier exposure history.

For binary acceptance, branches must terminate on adjacent accepted/rejected
bounds or at a tested endpoint. Treat unknown/refusal according to the declared
rule, not as rejection. Test every possible route, back-navigation, all-yes,
all-no and contradictory paths. Do not infer this behavior from native GG.

### Conjoint

Check the separate purchase and documented Choice Based Conjoint and Allow
Javascript permissions. Verify current capacity limits and export access for the
planned study. Follow the design/estimation gates in
[Method selection](method-selection.md); do not replace designed tasks with
improvised AI package comparisons. [P11, M4]

## Preflight and data governance

Before fieldwork, verify consent, quotas, collection/export permissions, language,
mobile/accessibility, currency validation, branch behavior and end-to-end data
retention. Test real rendered participant flows, not only editor previews.

Disclose AI/human moderation, recordings, transcription, observers, recipients,
retention and withdrawal. A required legal checkbox is not sufficient evidence
that consent language is adequate. Minimize recordings and identifiers. Do not
put sensitive participant fields in survey URLs. [P3, P9]

Approve source and destination access, residency, processing and retention before
connecting platforms or uploading data. A documented connector is not consent.
Preserve pseudonymous linking keys separately from published outputs.

Reconcile invitations, starts, assignments, completions, exclusions and imports.
Marvin allows multiple submissions and in-progress sessions can exceed a cap;
a response cap is not deduplication. Audit condition and prompt drift before
pooling channels. Pause numeric inference when price exposure cannot be verified.
[P3]
