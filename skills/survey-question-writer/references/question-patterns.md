# Question patterns

Use these original, hypothetical examples as adaptable patterns, not validated
scales or customer evidence. Adapt periods, task definitions, and categories to
the measurement brief. Source keys refer to [Sources](sources.md).

## Rewrite common defects

| Defect | Avoid | Prefer | Design note |
|---|---|---|---|
| Leading wording and assumed benefit | "How much has our powerful agent improved your productivity?" | If investigation time is the intended outcome: "Compared with your previous approach, how much time did you spend investigating the most recent incident using the agent?" | Confirm this narrowing of "productivity" rather than silently changing the construct. Propose: Much less / Somewhat less / About the same / Somewhat more / Much more / No previous approach to compare / Don't know. Screen for use. This is perceived change, not causal evidence. |
| Double-barreled judgment | "How satisfied are you with setup and troubleshooting?" | Separate "How satisfied or dissatisfied are you with the setup process?" from the troubleshooting item. | Ask each only of people with that experience; use a balanced satisfaction scale. |
| Vague frequency | "Do you regularly use the agent?" | "On how many of the past 7 days did you use the agent to investigate an incident?" | Propose single-select 0 through 7, plus Don't remember. The unit is days, not incidents. Confirm the proposed window fits the decision. |
| Assumed experience | "How easy was configuring an alert?" | First ask whether they attempted configuration in the defined period; then ask how easy or difficult that attempt was. | Include unsuccessful attempts rather than screening only for completion. |
| Acquiescence | "I agree that the recommendations are trustworthy." | "How much, if at all, do you trust the agent's recommendations when investigating an incident?" | Use Not at all / A little / Somewhat / A lot / Completely, plus Not enough experience to judge where needed. Pretest what "trust" means. |
| Overlapping categories | "0-5 / 5-10 / 10-20 incidents" | "0 / 1-4 / 5-9 / 10-19 / 20 or more" | Specify actor, incident definition, and period. These are illustrative bins, not an established standard. |
| Predictive overclaim | "Would you definitely adopt this feature?" | Ask current workflow and unmet need; if intention is required, describe a concrete offer and ask likelihood in a defined future period. | Label the result stated intention, not expected conversion. Select a dedicated pricing method if price or packaging drives the decision. |
| Pressure to disclose | "Explain the outage and name who caused it." | "What, if anything, made investigating that incident difficult? Do not include names, identifiers, or confidential details." | Optional text; ask only if relevant. Avoid blame and speculative attribution. |
| Primed unaided response | Show a feature list, then ask "What improvements come to mind?" | Ask the open-ended improvement item before the feature list. | Preserve the distinction between unaided discovery and prompted endorsement. |

Apply neutral, single-concept wording and exposure filters from P1 and G1.

## Choose a response format

| Measurement need | Starting format | Caution |
|---|---|---|
| One factual category | Single-select multiple choice | Cover all plausible states; do not force a category outside the respondent's knowledge. |
| Count or amount respondents can retrieve | Numeric text entry with units, or defensible nonoverlapping bands | Match precision to recall. Do not block legitimate high values with an arbitrary maximum. |
| Satisfaction or difficulty | Fully labeled bipolar item | Balance both directions; a neutral point is not "Not applicable." |
| Intensity, such as confidence | Labeled unipolar item | Start at absence; do not invent a negative counterpart solely for symmetry. |
| Occurrence/prevalence for several events | Separate occurrence item for each event | Use specific labels such as "Experienced this" / "Did not experience this"; consider unknown/refusal. Budget for extra burden. |
| Broad inventory with limited burden | Select all that apply | Include explicit exclusive "None" when meaningful; do not interpret an entirely skipped checklist as all-negative. |
| Relative priority | Ask for the most important item or up to a small number | Selecting up to three is not a complete ranking or a prevalence estimate. Long full rankings are burdensome. |
| Unknown categories or explanation | Short optional text entry | Plan how answers will be coded and protect against identifying disclosures. |

### Per-item occurrence versus select-all-that-apply

P2 found higher reporting in a randomized U.S. adult study of undesirable events.
The accuracy argument relied on underreporting being more plausible than false
positive reports in that context. Do not conclude every yes/no battery is more
accurate for every topic, or that a higher percentage proves accuracy.

Recommend per-item responses when event prevalence is the decision-critical
measure and burden is acceptable. Use construct-specific labels to reduce
acquiescence. Consider a checklist for a concise inventory when its limitations
are acceptable; disclose the trade-off. Do not silently switch formats in a
longitudinal measure. Neither format requires mandatory answering.

### Scale selection

For a new satisfaction item, a possible five-point scale is Very dissatisfied /
Somewhat dissatisfied / Neither satisfied nor dissatisfied / Somewhat satisfied /
Very satisfied. Add a separate experience/knowledge option only if routing does
not already resolve it. Treat this as a starting design, not a universal rule.

Choose the number of points based on meaningful distinctions, respondent burden,
mode, and comparability. Preserve an established measure's anchors and scoring.
Do not mechanically add reverse-worded items or remove a neutral midpoint to
"improve" responses. Pretest interpretation, especially across translations.

Do not use 99 for "Don't know" and then average it into a satisfaction score.
Keep substantive responses, unknown, inapplicable, refusal, and blank distinct;
retain their labels and document analysis eligibility (A1).

## Worked routing example

For a survey about incident investigation, propose the following only after
confirming that a 30-day window and personal usage are appropriate:

1. **USE_30D:** "In the past 30 days, did you personally use the agent to
   investigate an incident?" Options: Used it / Did not use it / Don't remember.
2. **INVESTIGATION_EASE:** Show only for Used it. "Thinking about the most recent
   incident you investigated with the agent in the past 30 days, how easy or
   difficult was investigating that incident?" Options: Very difficult / Somewhat
   difficult / Neither easy nor difficult / Somewhat easy / Very easy /
   Don't remember well enough to judge.
3. **DIFFICULTY_DETAIL:** Optional text, shown only after a difficult rating:
   "What, if anything, made investigating that incident difficult? Do not include
   names, identifiers, or confidential details."

Send Did not use it, Don't remember, and a skipped USE_30D past the experience
items; do not reinterpret the latter two as nonusers. Report ease among eligible
users providing a substantive rating and separately report missing/unknown.
This measures investigation difficulty during use, not the agent's causal effect.
