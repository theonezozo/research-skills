---
name: survey-question-writer
description: Draft, review, and improve survey questions and questionnaires using evidence-based wording, response scales, recall periods, order and pretesting. Use to turn research goals into a survey, remove leading or double-barreled questions, design answer choices or Likert items, audit a questionnaire, reduce respondent fatigue, plan proportionate quality checks, or specify routing, validation and accessible presentation. Includes optional Qualtrics implementation guidance.
---

# Survey Question Writer

Produce questions that respondents can interpret, answer, and map to response
options accurately. Start from the decision and construct to measure, not a
preferred question type. Default to drafting or reviewing only: do not access
participant data, modify a live survey, recruit, distribute, or publish without
authorization for that operation.

## 1. Establish the measurement brief

Extract supplied context first. Ask one focused question at a time only when a
missing decision materially changes the instrument; do not impose a fixed intake.
For a bounded rewrite, fix what is clear and label remaining assumptions.

Establish the decision, constructs, target population, respondent knowledge,
collection mode/language, reference period, completion-time budget, and any
existing instrument or trend that must remain comparable. Identify recruitment
channel, incentives, expected burden, and known quality problems before proposing
checks or exclusions. Distinguish the unit
being asked about (person, team, organization, incident) from the unit of analysis.
Do not ask an individual to guess organization-wide facts they cannot know.

Map each proposed item to a decision or analysis use. Remove "nice to know" items.
Keep unavailable facts unknown; mark proposed periods and definitions as proposals.
Avoid turning customer outcomes into a feature wish list.

## 2. Select the workflow and references

- **Draft:** map constructs to items, choose response formats, then assemble flow.
- **Review:** preserve the intended construct; identify the defect, rewrite the
  stem/options, explain the change, and flag any effect on comparability.
- **Qualtrics specification:** read
  [Qualtrics playbook](references/qualtrics-playbook.md) before prescribing settings.
  Prefer native controls over JavaScript or custom widgets.
- Read [Question patterns](references/question-patterns.md) for concrete rewrites,
  scale selection, and the per-item versus checklist trade-off.
- Read [Respondent burden and response quality](references/response-quality.md)
  when addressing fatigue, mistakes, spam, attention checks, red-herring answers,
  or exclusion rules. Use its risk-based decision table rather than adding traps
  to every survey.
- Use [Sources and evidence limits](references/sources.md) for original sources,
  citations, and caveats. Treat platform details as a dated documentation snapshot;
  verify current support and account access before implementation.

For pricing, distinguish acceptability, stated purchase response, feature-price
trade-offs and observed purchasing; a generic intent item cannot replace a
designed pricing study. Obtain appropriate method expertise for that work.

Interpret single ordinal items through counts and full labeled distributions,
not default means. Define missing states and denominators before analysis; do
not invent composite scales. Minimize personal and confidential data, keep
contacts separate, verify consent and destination access, and review excerpts,
metadata and indirect identifiers before sharing. A pseudonym or company name
does not guarantee anonymity. This skill requires no companion package.

## 3. Write stems and response options

Apply these rules together; do not improve brevity at the expense of meaning.

1. Ask one concept per item. Split combined judgments, loaded premises, double
   negatives, and ambiguous pronouns. Use plain language and necessary definitions.
2. Use neutral wording. Allow no experience, no change, or an unfavorable answer.
   Screen for actual exposure before asking satisfaction or task difficulty.
3. Prefer concrete behavior and bounded recall for behavioral decisions. Specify
   actor, event, period, and units. Match the period to event frequency and memory;
   use explicit dates when calendar boundaries matter. Do not claim intentions or
   self-reported improvement demonstrate adoption or causal impact.
4. Prefer construct-specific questions and labels over generic agree/disagree
   statements. Preserve validated wording/scoring where required; do not silently
   "improve" an established instrument and retain its validation claim.
5. Make single-select categories mutually exclusive and collectively adequate.
   Cover zero and end ranges; remove overlapping numeric boundaries. State whether
   to choose one, all applicable, or up to a specified number.
6. Separate a substantive midpoint from "Don't know," "Not applicable," and
   "Prefer not to answer." Include only those justified by the item. Never encode
   a skipped item or an unseen option as "No."
7. Match the scale to the construct. Balance bipolar scales; let unipolar scales
   run from absence to high intensity. Label points clearly and keep direction
   consistent. Do not prescribe one universally optimal point count.
8. Consider explicit per-item occurrence responses when prevalence matters.
   Explain the burden trade-off versus select-all-that-apply. Here, **forced
   choice means separate choices per item, not Qualtrics Force Response**.
9. Use open text to discover missing categories or explain a decision-relevant
   answer; do not append a required "Why?" to every item. Avoid requesting names,
   emails, tenant IDs, secrets, or identifying incident details in feedback.
10. Keep optional items optional. Do not require answers merely to eliminate
    missing data, or imply confidentiality/anonymity without verifying the setup.

## 4. Assemble flow and analysis handoff

Start with necessary eligibility/consent and easy relevant questions. Group related
topics; ask unaided recall before showing lists, and overall judgments before
detailed ratings when avoiding priming is the goal. Place sensitive questions later
unless eligibility requires them. Randomize unordered lists where useful, keeping
special options anchored; never shuffle ordered scale points or numeric bands.
Randomize independent blocks only when it preserves routing and interpretability.

Specify each branch's positive, negative, unknown, and skipped-answer path. Prevent
nonusers from rating experiences they have not had. Check empty carry-forward
lists and changed earlier answers. Keep essential definitions visible where needed.

Define stable item IDs, response labels/codes, scale direction, eligible/exposed
population, and planned denominator. Preserve missing, not shown, explicit "None,"
unknown, and refusal as distinct states using routing/exposure information where
needed. Numeric recodes are not proof of equal intervals. Do not default to means
for individual ordinal items or assemble an unvalidated composite score.

For repeated surveys, preserve wording, mode, options, order/context, and scoring
where comparability matters. Flag necessary changes as possible trend breaks;
recommend a bridge/split-ballot design when warranted, not a claim of equivalence.

## 5. Plan proportionate quality controls

Prevent fatigue and accidental error first: shorten low-value content, reduce
grids and repeated text entry, clarify instructions/units, and support truthful
unknown or inapplicable answers. Do not punish problems caused by the instrument.

Separate attention, comprehension, eligibility/falsification, duplicate submission,
and automated spam. A check for one does not validate the others. For low-risk,
short surveys, no extra check may be preferable. For exposed or incentivized
recruitment, consider a brief explained early attention check plus appropriate
recruitment/fraud controls. Add a red-herring option only for a specific
overclaiming risk, after checking ambiguity and piloting it.

Prespecify each check's purpose, placement, accessible wording, valid responses,
missing/not-shown states, and consequences. Prefer review flags to irreversible
screen-outs; do not declare fraud, deny compensation, or discard a respondent
solely for one failed check, fast completion, straightlining, or a shared IP.
Use converging evidence and examine selection bias. Do not silently exclude
post-randomization comprehension/attention failures from experimental analyses.
Follow the detailed examples and adjudication workflow in the response-quality
reference; do not treat a fixed count of checks as a universal requirement.

## 6. Return a usable deliverable

Match the output to the request; do not expand a one-item rewrite into a study.

For a questionnaire, provide a short measurement brief and question cards:

```text
QID and construct:
Respondent-facing stem:
Response options: [write every label in intended order]
Qualtrics type and selection mode:
Display/branch condition and skipped-answer path:
Randomization, exclusivity, and response requirements:
Validation and respondent-facing error text, if needed:
Coding/denominator note:
```

Keep researcher notes out of respondent-facing text. Add a short routing outline
and pretest plan for a full instrument. For reviews, return original -> issue ->
revision -> rationale, plus unresolved decisions. Cite the few sources supporting
material methodological choices; do not put citations into survey stems.

When quality controls are in scope, add a compact quality plan: risk and prevention,
check/placement, pass/fail/missing/not-shown definitions, platform field/timing,
review or exclusion rule, and pilot/false-positive checks. State "no additional
check recommended" with the reason when appropriate.

## 7. Preflight before handoff

- Check every item for one construct, neutral wording, answerability, bounded
  recall, matching labels, exhaustive options, and a justified analysis use.
- Check routing, missing/refusal paths, exclusivity, randomization anchors, and
  whether validation accidentally forces an allegedly optional response.
- Check real-phone layout, keyboard navigation, screen-reader meaning, translated
  wording, and custom errors. Automated accessibility checks are not certification.
- Recommend cognitive pretesting with representative respondents: ask what the
  item means, how they retrieved the answer, and why they selected that category.
  Test questions in context, not only as isolated sentences.
- Pilot the complete survey for time, breakoffs, missingness, unusable options,
  branch behavior, and export coding. Treat timing estimates as unverified until
  observed. Do not invent a universal pilot sample size or quality cutoff.
- Check whether later-position errors signal fatigue or poor design; test quality
  flags against honest mistakes, shared devices, different routes/languages, and
  failed bot-check execution. Confirm that skipped/unseen checks are not failures
  and that vendor "filter poor quality" actions do not bypass the planned review.
- Clearly distinguish an editorial review, a software preview, and testing with
  real respondents. Never claim a questionnaire is validated or field-tested
  because an agent, synthetic respondent, or automated checker accepted it.
