# [Study/version] — pilot and launch runbook

Default: manual preparation only. A readiness GO is not launch authorization.
Fill evidence and status; an unchecked critical item is not a pass.

## Freeze the reviewed packet

- Workspace/study identifier and intended mode:
- Guide, screener, AI instructions and branch versions:
- Stimulus versions/order/exposure rules:
- Consent, recording, privacy, retention and access settings:
- Recruiting channel, segment quotas/coverage, initial wave and incentive budget:
- Participant duration estimate and permitted burden:
- Reviewer, decision date and snapshot/hash/reference:

## Pilot coverage and results

Use approved synthetic/internal testing first. Obtain separate approval before
external pilot recruitment, data collection, uploads or spending.

| Check | Cases and actual evidence | Pass / revise / blocked |
|---|---|---|
| Entry and consent | Invitation; eligible/ineligible; decline; withdrawal route; no substantive collection without consent | |
| Participant setup | Required devices/browsers, permissions, bandwidth, access technology, language, text/voice fallback if supported | |
| Capture and privacy | Actual recording scope matches disclosure; private tabs/notifications excluded by safe setup; safe stimuli/test data only | |
| Routing and stimuli | Every branch including no experience, unsure, refusal and technical failure; correct assets, labels, order and readability | |
| AI behavior | Short, complete, contradictory, off-topic, "do not know", refusal and already-answered cases; neutral probes and early stop | |
| Sensitive/adversarial input | Synthetic secret/identifier and instruction to ignore guide; no solicitation, repetition or disclosure; tested safe exit | |
| Timing and burden | Actual distribution/range across paths, probe variability, repetition/interruptions and participant comprehension | |
| Completion | Thank-you, completion signal, incentive handoff/terms; no accidental enrollment or payment from a test | |
| Data and analysis | Usable transcripts/task capture, safe IDs, provenance, consent association, human review of summary/quote accuracy | |

Inspect the real participant flow and resulting transcripts/recordings, not only
editor text. Repeat critical paths to test variable AI behavior. Keep pilot data
separate unless comparability and pooling are explicitly justified.

## Go/no-go

- Critical failures: consent mismatch, sensitive-data exposure, inaccessible required
  path, wrong stimulus/routing, unsafe AI follow-up, unusable evidence.
- Project-specific quality/timing thresholds and rationale, defined before pilot:
- Findings, fixes and retest evidence:
- Unverified critical behavior:
- Decision: GO for [exact version] / REVISE / NO-GO.
- Scope of GO: methodological readiness only; no permission to mutate Outset.

## Explicit action authorization

Before each consequential action, obtain and record explicit approval for the exact
current snapshot, action, target, audience, timing and budget. Separate approval
for external pilot, real-study creation, publishing, recruitment/contact, spending,
confidential upload, live-setting changes and wave expansion. Do not bundle
unrequested authority into a generic "looks good".

- Requested action(s), boundaries and approver:
- Exact approved packet/settings version and current state:
- Recruitment count/coverage, incentive ceiling and time window:
- Approved upload materials and permitted data handling:
- Pause/incident authority, active-session response and resume/expansion authority:
- Approval evidence and expiry/conditions:
- Live-state comparison immediately before action:
- Result: APPROVAL ABSENT / STALE / VALID FOR LISTED ACTION ONLY.

If absent or stale, stop at this manual runbook. Do not create/publish, contact,
spend, upload confidential content or change live settings. Never invent access
credentials or an automation API. After an authorized action, verify resulting
state and record safe evidence; ambiguous execution is not success or a retry cue.

## Staged fielding and stop rules

| Signal | Measure / review cadence | Pause/review threshold | Authorized response / owner |
|---|---|---|---|
| Consent/privacy or participant concern | [source and human reviewer] | Any critical incident | [containment, active-session plan, support/escalation] |
| Technical failure/dropout | [denominator, path/device/language] | [pilot-informed threshold] | [pause new entrants and investigate] |
| Data/AI quality | [human review of flags, probes, usable responses] | [predeclared criterion] | [review before exclusion; no automatic incentive denial] |
| Coverage and duplicates | [unique eligible people/declared unit by segment] | [coverage/duplicate rule] | [adjust only with fresh authorization] |
| Burden and budget | [duration spread, incentive/total spend] | [approved ceiling] | [stop expansion; verify current costs] |

Start with [approved limited wave]. Expand only after [review evidence] and
[explicit approval]. Do not use a universal wave size or quality cutoff.

Outset help states pausing blocks new entrants but **does not interrupt ongoing
sessions**. Verify an active-session incident plan; do not call pause a kill switch.
Do not close irreversibly as a routine pause.

## Changes, closeout and evidence handoff

- On material change: obtain authorized pause/change actions, version all affected
  materials/settings, record collection boundaries, retest and seek new approval.
  Do not silently pool incompatible versions.
- Close collection only under explicit authority; verify state and budget/participant
  obligations. Distinguish produced packet, approved version and published study.
- Preserve provenance and safe source links. Reconcile unique included/excluded,
  incomplete and duplicate records against collected totals before reporting.
- Human-check AI themes/quotes/translations against originals and contrary cases.
  Report bias, missingness and unavailable metadata alongside findings.
- Apply approved access/retention/deletion and withdrawal procedures; do not invent
  platform controls or claim deletion/participant payment without confirmation.
