# Respondent burden and response quality

Use prevention before detection and review before irreversible exclusion.
Distinguish an honest mistake, an uninterpretable answer, temporary inattention,
misrepresented eligibility, duplicate participation, and automated spam. None is
interchangeable with the others. Source keys refer to [Sources](sources.md).

## Contents

- [Reduce fatigue before adding checks](#reduce-fatigue-before-adding-checks)
- [Prevent and accommodate honest mistakes](#prevent-and-accommodate-honest-mistakes)
- [Decide when and where to add a check](#decide-when-and-where-to-add-a-check)
- [Write fair attention and comprehension checks](#write-fair-attention-and-comprehension-checks)
- [Use red-herring answers cautiously](#use-red-herring-answers-cautiously)
- [Layer spam controls without overclaiming](#layer-spam-controls-without-overclaiming)
- [Prespecify review and exclusion](#prespecify-review-and-exclusion)

## Reduce fatigue before adding checks

1. Budget effort by route, not just question count. Include reading, recall,
   calculations, selecting among options, grids, and typing on mobile. Delete
   low-value items before adding another detector. Keep essential outcomes early
   enough to avoid predictable late-survey attrition while preserving priming and
   experiment-order requirements.
2. Use relevance filters, short blocks, concise instructions, and few purposeful
   open ends. Avoid repetitive large grids and long full rankings. Do not shrink
   a validated scale or change response labels merely to shorten the survey.
3. Give an honest completion-time estimate based on a representative pilot, not
   a promise derived only from word count. If pauses/resumption are supported,
   explain them accurately; do not promise saved progress without checking.
4. Inspect breakoffs, item nonresponse, abbreviated text, and response patterns
   by page position, route, device, and language where available. Compare like
   routes: a short eligible path can legitimately finish much faster. Late
   straightlining can indicate fatigue, but identical ratings can also be true.
5. Treat rising failures at one page as a prompt to inspect that page's wording,
   rendering, and burden, not evidence that every affected respondent is bad.

G1 supports respondent-centered burden reduction and cognitive/usability testing.
Q14 reports increased breakoff beyond about 12 minutes, or 9 on mobile, and
declining completion beyond three open-text boxes in its data. Use these as
vendor warning heuristics, not universal limits, causal thresholds, or grounds
to exclude slower people. Test your population and routes. Do not assume a
progress bar improves completion or show misleading progress on branched routes.

## Prevent and accommodate honest mistakes

- Clarify who, what, units, reference period, and selection limits in place.
  Support zero, unknown, not applicable, and refusal when meaningful.
- Make controls readable and usable by keyboard and assistive technology; test
  translated instructions and errors. Avoid tiny targets, preselected answers,
  double negatives, and memory instructions buried several pages earlier.
- Use format/range validation to explain an actual input problem, not to force a
  preferred substantive answer. For a surprising but possible value, consider an
  explicit confirmation rather than a hard rejection. Record any correction
  accurately; do not infer intent from an initial typo.
- Investigate apparent contradictions for different periods, actors, or meanings.
  Distinguish omission from an explicit negative. Do not code a skipped optional
  check as a failure or infer that someone declining personal data is fraudulent.
- Do not add reverse-worded items solely to catch straightlining; they can
  introduce interpretation errors. Do not remove outliers merely for disagreeing
  with the expected findings or choosing consistently negative ratings.

## Decide when and where to add a check

Treat these as starting recommendations, not universal empirical thresholds.

| Situation | Starting choice | Placement and action |
|---|---|---|
| Short, low-incentive survey of invited known customers | Usually no added trap; clear purpose and proportionate passive review | Resolve burden and confusing items first. Known recruitment reduces some risks but does not guarantee quality. |
| Broad opt-in or incentivized recruitment with plausible careless responding | Consider one brief, explained instructed-response item or a courteous thoughtful-response request | Place early after consent/basic orientation; pilot first. An early pass says little about later attention or truthful identity. |
| High incentive or scarce professional eligibility with evidence of overclaiming | Consider one low-ambiguity eligibility/falsification check; a verified fictitious option may be appropriate | Place in the relevant early screener before an extensive burden. Review the flag with other evidence; do not secretly change payment rules. |
| Long survey with worsening late responses | Shorten or split the instrument first; optionally diagnose attention at a natural later break if the research needs it | Do not bury traps at the end of exhausting grids. Treat early/late differences as a design diagnostic, not an automatic whole-response rejection. |
| Experiment depends on seeing or understanding a stimulus | Use a brief comprehension/exposure check if justified | Place immediately after the relevant material, not a distant trivia test. It measures comprehension, not general honesty. Consider priming and post-treatment selection. |
| Public link, suspected automation, or repeated submissions | Use recruitment/access controls and appropriate Qualtrics bot/duplicate controls | Configure before launch and monitor during fieldwork. Another attention question is not a bot-defense substitute. |

V1 recommends one early check for many surveys and discusses fictitious brands
for higher-incentive falsification risk. Use this as vendor guidance, not a rule
requiring a check in every study. Do not add one every fixed number of questions.
R1 found instructed-response items associated with other quality indicators, but
excluding failures did not change substantive results in that study. R2 found
some respondents deliberately refused the instruction and that explaining the
reason improved compliance. Effects depend on population and implementation.

## Write fair attention and comprehension checks

Use one clear task and one unambiguous correct response. Put the instruction at
the point of response, make it accessible in every survey language, and use a
respectful explanation. Avoid trivia, arithmetic, local cultural facts, hidden
instructions, contradictory directions, or "do not answer this required item."
Do not require respondents to recognize a color visually or to remember an
arbitrary word from the introduction.

**Illustrative instructed-response item, not a validated instrument:**

> This item helps us check that the survey instructions are clear. For this
> question only, select "Somewhat disagree."

Options: Strongly disagree / Somewhat disagree / Neither agree nor disagree /
Somewhat agree / Strongly agree. Keep this administrative item separate from
substantive scale scoring; its agree/disagree format is an instruction-following
task, not an attitude measure. Retain pass, fail, missing, and not shown distinctly.
Do not force the correct choice through validation or default selection.

An alternative is a short request such as "Your thoughtful answers help us make
better decisions. Take the time you need, and use 'Don't know' when appropriate."
Treat this as an engagement prompt, not an identity check or proof of quality.
V1 provides evidence for commitment requests in one panel study; do not promise
that this adapted wording reproduces its effects.

For a comprehension check, if a concept card states that an action requires
human approval, ask which approval rule the card described, with clear alternatives
and Don't remember. Classify the result as comprehension of that card. Do not
infer fraud from failure or silently replace the experimental population with
only people who understood the treatment. Prespecify any clarification/retry;
an immediate reminder changes subsequent exposure and is not a neutral correction.

Do not rely on arbitrary "impossible" statements such as never having made a
mistake, absurd occupations, or improbable life events: figurative interpretation,
rare genuine cases, and misreading can all occur. One failure is a review signal.
Passing is not proof of thoughtful responding throughout the questionnaire.

## Use red-herring answers cautiously

Define a **red herring** here as a fictitious or verified inapplicable option
inserted among real choices to detect overclaiming, not an ordinary distractor in
a knowledge test. It is a falsification/overclaiming check, not pure attention.
An unfamiliar real product or rare behavior is not a valid fictitious option.

Before recommending one:

1. Establish why falsely claimed experience is a material risk, such as paid
   recruitment of scarce specialists. Prefer authentic, non-sensitive screening
   evidence and a clear experience question where these suffice.
2. Verify the candidate does not exist and is not easily confused with a real
   brand, acronym, internal tool, translation, or neighboring category. If that
   cannot be established adequately, do not use it as an exclusion check. Do not
   assume an invented-sounding name is globally unique.
3. Ask bounded personal experience, such as which tools were personally used in
   the past 30 days, rather than vague recognition ("heard of") or desired future
   use. Include truthful None/Don't know choices as appropriate.
4. Pretest whether genuine target respondents misread or reasonably endorse it.
   Keep wording/visual treatment comparable with other choices and define its
   placement/randomization. Exclude it from product-preference scoring and
   downstream carry-forward evaluations, while preserving its quality flag.
5. Do not insert fake offerings into a satisfaction/roadmap measure or imply that
   the sponsor sells or endorses them. Assess deception, trust, consent, and any
   required ethics/debriefing review before fielding; do not claim approval.
6. Flag an endorsement for corroboration, not instant fraud attribution. A click
   error is plausible, and a skilled fraudster can avoid the option.

**Design-only template:** "Which of these tools, if any, did you personally use
to investigate incidents in the past 30 days? Select all that apply."
Choices: [real tools from the study] / [candidate fictitious tool, verified and
pretested before use] / None / Don't remember. Keep None and Don't remember
exclusive and anchored. Do not field the bracketed placeholder as an actual item.

P4 used a made-up social platform called Fizzypress in its 2024 fieldwork,
reported in 2026. That illustrates the method, not a reusable validated trap:
do not assume the name is still nonexistent or undisclosed. The study's one-fail
screening rule is not this skill's default. It lacked ground truth for each
respondent, and improvements varied by metric.

## Layer spam controls without overclaiming

Reduce exposure through the authorized recruitment design: consider controlled
invitations or individual participation links when compatible with privacy and
sampling, rather than making an incentive-bearing open link the default.
Prespecify the participation unit and permitted repeats; one corporate IP is
not one person, and a longitudinal participant may legitimately return.

Combine appropriate bot/duplicate controls with scoped content review. Examine
multiple unrelated nonsensical answers, implausible experience combinations,
distinctive duplicated text, and unexpected source/time clusters. Short shared
phrases such as "none" or "not sure" are not duplicate evidence by themselves.
Do not diagnose AI authorship from polished writing, grammar, or a style score,
or equate non-native language, assistive tooling, privacy protection, or demographic
membership with fraud. Do not add intrusive identifiers merely to validate identity.

P3 found that most cases it classified as bogus passed an instructed attention
check and a speed check. P4 found no universally effective screening approach;
identity matching removed many genuine respondents who withheld identifying
information. A bot or dishonest human can pass a clear attention check. Keep
screening fallibility visible and do not promise a "fraud-free" sample.

## Prespecify review and exclusion

1. Write a quality plan before seeing outcome effects: purpose, fields, exposure,
   timing, thresholds, treatment of missing/error states, review process, and
   consequences. Pilot rules with genuine target respondents across relevant
   routes/devices/languages; choose thresholds for that design, not a generic
   seconds-per-question rule.
2. Separate **flags**, **adjudication**, **analytic exclusion**, and **payment**.
   Default a failed check to review, not deletion. Use converging signals from
   different failure modes; two correlated speed metrics are not two independent
   confirmations. Do not turn "two flags" into a universal validity rule.
3. Review without looking at preferred substantive results or treatment effects
   where feasible. Consider legitimate explanations and scope: one misunderstood
   item may justify item-level missingness, not removal of the whole respondent.
   Apply prespecified duplicate handling rather than retaining the most favorable
   answer. Preserve originals and a reason-coded derived inclusion decision.
4. For experiments, prefer prespecified eligibility/quality gates before assignment
   when appropriate. Failures after assignment can be caused by the treatment;
   preserve the intended randomized comparison and disclose sensitivity analyses.
   Do not condition the main effect on a post-treatment comprehension score
   without a defensible analysis plan.
5. Report the initial eligible/exposed population, flags, overlapping reasons,
   reviewed/excluded unique respondents, and final denominators. Compare key
   conclusions with and without uncertain exclusions; inspect differential
   attrition without treating demographic membership as a screening rule.
6. Honor disclosed consent, provider, and compensation terms. Do not retroactively
   deny payment or alter incentives based on newly invented quality rules.
   Obtain authorization before blocking participants, publishing changes,
   deleting data, or changing payment behavior.

Do not label any process human-validated because a model simulated respondents.
Use simulated inputs only to exercise logic, and clearly distinguish a rule
coverage check from measured false-positive/false-negative rates.
