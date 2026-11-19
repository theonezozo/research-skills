# Qualtrics playbook

Use native Survey Platform features first. Verify the project type, survey-taking
experience, permissions, and actual configuration before promising availability.
Treat the source-backed details below as a 2026-09-23 snapshot, not proof that a
specific account or survey has been inspected. Source keys link through
[Sources](sources.md).

## Contents

- [Question construction](#question-construction)
- [Routing and carry forward](#routing-and-carry-forward)
- [Response requirements](#response-requirements)
- [Export and coding safeguards](#export-and-coding-safeguards)
- [Mobile and accessibility](#mobile-and-accessibility)
- [Quality flags and fraud controls](#quality-flags-and-fraud-controls)
- [Preflight scenarios](#preflight-scenarios)

## Question construction

| Design intent | Native implementation | Guardrail |
|---|---|---|
| Choose one response | Multiple Choice, Single Answer | Use a vertical list as a mobile-friendly starting point; do not preselect an answer. |
| Choose all applicable responses | Multiple Choice, Multiple Answer | Make contradictory options such as None or Prefer not to answer exclusive, when included (Q2). |
| Allow an unlisted category | Allow Text Entry on an Other choice | Do not require elaboration without a reason. This feature is not compatible with dropdown multiple choice (Q2). |
| Rate a construct | Single-answer item; short Matrix Table only when justified | Keep ordered scale points in order. Avoid large grids solely to fit more items on one screen. |
| Reduce unordered-list position effects | Choice Randomization, Advanced Randomization | Put substantive options in Randomize Choices; keep Other/None/unknown/refusal in Fixed Display Order as appropriate (Q1). |
| Repeat a previously randomized list | Carry Forward plus documented order-preservation setup | Q1 explicitly supports preserving randomization order; do not incorrectly claim it is impossible. Test the actual setup. |
| Ask only about prior selections | Carry Forward Selected Choices | Exclude non-substantive choices from follow-up evaluation; handle zero eligible choices explicitly (Q4). |

Do not confuse a random subset with random ordering of the full list. Subsetting
changes who had an opportunity to select each item; preserve exposure information
and use item-specific denominators. Do not randomize numeric bands or shuffle
ordinal scale categories. If a design deliberately reverses a scale, preserve
the full order and test consistent presentation and coding (Q1).

## Routing and carry forward

Use **Display Logic** for a question or answer choice, **Branch Logic** for a
block/path in Survey Flow, and **Skip Logic** for forward navigation to another
question in the same block or an ending (Q3, Q5). Specify conditions and
destinations, not merely "add branching."

- Place the source answer before dependent logic. Use a page boundary when
  needed; do not assume every dependency works dynamically on one page.
- Display Logic normally inserts a page break after the affected question unless
  In Page is enabled. In Page has incompatibilities, including carry-forward
  choices and answer-choice display logic; heed builder warnings (Q3).
- Branch Logic disables the back button on the first page of the following block.
  At a nonterminal branch's end, respondents continue to the next flow element;
  do not assume separate branches automatically behave like an if/else (Q5).
- Carry Forward supports only one source set per destination question. Most EX
  projects do not support it; verify project compatibility (Q4).
- Specify Selected, Displayed, Unselected, or another documented carry-forward
  condition deliberately. Unselected is not synonymous with explicitly rejected.
- If only None/unknown was selected, hide the evaluation follow-up instead of
  displaying an empty required question. Define a path for skipped source items.
- Test changes to previous answers wherever backward navigation is available;
  do not assume hidden prior answers are removed from exports.

## Response requirements

Distinguish these controls (Q6):

- **No requirement:** allow a skipped answer.
- **Request Response:** remind the respondent but permit continuing unanswered.
- **Force Response:** block progression until answered. Reserve for a justified
  requirement, such as recording a consent choice; always let refusal exit.
- **Content validation:** check an appropriate input format.
- **Custom validation:** enforce a condition with a clear error message.

**Custom validation is not compatible with Request Response and acts like a
required response; it cannot simply be described as an optional-item check.**
For an optional "up to three" item, first verify whether the native question
type's limits permit skipping. If not, propose a different format or seek approval
for the changed requirement. Never silently make the question mandatory.

Use "up to" rather than "exactly" unless the analysis requires an exact count.
Write human-readable errors and test empty input, boundaries, exclusive choices,
and translations. Do not reject truthful answers to manufacture clean data.
Do not use Force Response merely because the method is called "forced choice."

## Export and coding safeguards

Document proposed item IDs and choice codes separately from actual Qualtrics
internal IDs; never invent live QIDs or claim a configuration was deployed.

- Inspect **Exclude from Analysis** on every special choice. Qualtrics can
  automatically enable it for text such as None of the Above, N/A, Not Applicable,
  and Don't Know. The setting hides values from outputs including exports, rather
  than deleting them. Explicit None may be a substantive result that must remain
  available; inspect and verify an export instead of trusting defaults (Q2).
- Preserve labels and stable recodes. Carry-forward source and destination choices
  can have different recodes/variable names; map them explicitly (Q4).
- Export randomized viewing order when exposure/order matters (Q1). Retain routing
  or exposure fields needed to distinguish not asked from item nonresponse.
- Keep refusal and unknown separate from a neutral rating. Retain original values;
  perform documented exclusions in analysis rather than losing the audit trail.
- Before editing a survey that has responses, preserve its instrument and code
  map. Do not delete choices or change their meaning casually; flag trend breaks
  and obtain authorization for live changes (Q2, Q3).

## Mobile and accessibility

Prefer concise vertical lists and small question groups over wide grids, long
rankings, or drag-only tasks. Qualtrics recommends against horizontally scrollable
matrices. The new survey-taking experience is mobile-friendly and may enable
some settings automatically; legacy menus are not universal instructions (Q7).

Check the active experience before applying accessibility guidance. Qualtrics'
checker uses different standards for legacy versus new experiences and does not
evaluate every aspect of appearance. Test actual keyboard and screen-reader use,
contrast, font size, meaningful images/alt text, labels, errors, and translations.
Do not equate a passed ExpertReview with end-to-end accessibility (Q8).

## Quality flags and fraud controls

Use the risk/placement rules in [Respondent burden and response quality](response-quality.md)
before adding controls. The following are platform capabilities, not automatic
instructions to exclude people. Verify licensing and enable relevant settings
before collecting data; never claim retrospective bot detection.

| Need | Qualtrics implementation | Important limit |
|---|---|---|
| Flag a purpose-written attention check | Use an ordinary Single Answer item; evaluate its answer in subsequent Survey Flow branches and set study-defined embedded fields such as `qc_attention_1`. | Use explicit pass/fail/missing/not_shown states, not a default pass. Define exposure from the actual route. These are proposed study fields, not reserved Qualtrics fields or automatically generated scores (Q3, Q5). |
| Observe burden and implausible speed | Put a hidden Timing question on a relevant page; examine Page Submit and the route taken. | Page visits accumulate; `Q_TotalDuration` includes time away. Page time is not per-item time unless isolated, and not proof of reading. Question randomization can disrupt page breaks. Do not add mandatory delays merely to defeat speed flags (Q13). |
| Review native response-quality signals | Inspect Response Quality in Data & Analysis; use issue-specific filters. | "Filter Out Poor Quality Responses" excludes any flagged issue, not a considered multiple-signal rule. Some checks require licensing or opt-in and are not on by default (Q10, Q11). |
| Flag possible automation | Enable Bot Detection and verify security fields are included in responses; inspect `Q_RecaptchaScore` together with `Q_RecaptchaStatus` and, when present, `Q_RecaptchaError`. | The documented flag is below 0.5; higher scores suggest human activity, not verified authenticity. An execution error can leave a default score of 1: disregard it. Missing/error means unknown, not failed or passed. Bot Detection alone does not block completion (Q10, Q12). |
| Add an interactive bot obstacle | Consider a CAPTCHA question for an exposed recruitment channel. | Unlike passive Bot Detection, it requires a successful challenge to proceed. Assess burden/accessibility and do not promise it eliminates fraud or validates eligibility (Q12). |
| Detect same-browser repeat participation | Configure Prevent Multiple Submissions; prefer its continue-and-flag option when false positives require review. | It uses a browser cookie; cleared cookies or other devices evade it, while shared devices may affect legitimate people. `Q_BallotBoxStuffing` can support in-survey logic when configured in Survey Flow (Q12). |
| Identify likely duplicates after completion | Use Duplicate Detection with Flag Response; inspect `Q_DuplicateRespondent`. | This field is set **after submission** and cannot drive in-survey branching. The do-not-record option irretrievably deletes suspected duplicates and is not the default recommendation here (Q12). |
| Avoid email/SMS security scanners starting sessions | Consider Security Scan Monitor where available. | This is distinct from malicious fraud. A start-page roadblock permits a wrongly flagged human to continue; it is not an attention test (Q12). |

Do not build new controls on `Q_RelevantID*`: Qualtrics documents RelevantID as
deprecated from June 30, 2025, and warns against trusting newly recorded legacy
values. Preserve historical data and migrate with field-timing differences in
mind, not by substituting a post-submission field into an old live branch (Q12).

Treat native thresholds as vendor defaults, not scientific exclusion rules:
the documented speeding flag requires at least 100 qualifying responses and
uses duration relative to the median and standard deviation; it can change
during collection. Qualtrics advises waiting until collection ends to filter
speeders. Straightlining support exists, but is not available to every customer
or enabled by default; its documented rule requires at least three straightlined
Likert matrix questions and 80% of matrices. Do not add grids to obtain that
flag or conclude a survey without enough matrices is free of careless responding
(Q10).

Do not validate an attention item so only the "correct" answer can be submitted:
that teaches the answer and hides the signal. Default exports may show only the
saved answer, not every attempted choice; do not invent first-attempt or retry
logs. If a correction/retry is part of the design, specify and test how its
initial response and retry outcome will actually be retained.

Keep device/IP processing within consent, privacy, and account settings.
Duplicate Detection uses device/browser metadata and may collect IP where
permitted; a shared corporate network or privacy tool is not proof of fraud.
Define whether legitimate repeated waves are allowed and configure the duplicate
window accordingly. Do not weaken anonymity or enable external identity matching
merely to get cleaner-looking data (Q12, P4).

## Preflight scenarios

Use full-survey Preview for flow tests, not question/block preview alone. Disable
**Ignore Validation** when testing requirements. Desktop mobile preview does not
exercise device-based logic: test on an actual phone (Q9).

| Scenario | Expected result to verify |
|---|---|
| Eligible user; ineligible user; unknown; skipped screener | Each reaches its specified path without irrelevant experience ratings. |
| None combined with substantive choices | Exclusive selection prevents contradiction. |
| Zero, one, and many eligible carry-forward selections | Follow-up options and visibility are correct; no empty mandatory item. |
| Several fresh preview runs | Unordered choices vary; anchors and ordered scales remain correct. |
| Empty optional answer; invalid entry; boundary values | Skip remains possible where promised; real requirements/errors behave as specified. |
| Change an earlier answer, where navigation permits | Routing and any retained downstream data are understood and documented. |
| Keyboard, screen reader, real phone, each survey language | Questions, labels, instructions, errors, and navigation remain usable. |
| Export preview responses | Labels, codes, exclusions, exposure/order, and missing states match the design. |
| Pass, fail, skip, or never see an attention item | Each produces its intended distinct flag, without forcing the correct answer. |
| Change an attention response or take a retry | Retained data reflect the documented capture behavior; no fictitious attempt history. |
| Bot-check error, missing status, or default score | No classification as proven bot or proven human; retain unknown for review. |
| Shared device, repeated authorized wave, flagged duplicate | No unintended irreversible deletion; review uses the defined participation unit/window. |

Preview responses can appear in results and increment quotas. Account for them
without deleting real data or changing quota counts without authorization.
Do not send preview links as production participation links or put sensitive data
in shared preview bookmarks (Q9). Use synthetic inputs only for software checks;
schedule separate cognitive pretests and an authorized respondent pilot.
Native Response Quality excludes preview, generated test, and synthetic responses
from its analyses (Q10). Use preview to test routing and field capture, not to
claim the detectors' effectiveness or thresholds were validated; assess those in
an authorized pilot with genuine respondents and minimize stored metadata.
