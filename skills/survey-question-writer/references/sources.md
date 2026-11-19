# Sources and evidence limits

These public references and capability descriptions were carried forward from
a **2026-09-23** research snapshot; they were not freshly verified during this
packaging pass. Use original pages, not search-engine summaries. Recheck platform
documentation before implementation because menus, experiences and account
entitlements change.
Recommendations combine these sources with research judgment; the examples in
this skill are newly written illustrations, not validated questionnaire items.

## Survey methodology

| Key | Source | Supported use and limit |
|---|---|---|
| P1 | Pew Research Center, [Writing Survey Questions](https://www.pewresearch.org/writing-survey-questions/) | Neutral, specific, single-concept wording; open/closed formats; ordered scales; acquiescence; question/order effects; pretesting; trend comparability. Randomization distributes order effects, not eliminates them. Do not transplant telephone-specific choice-count guidance into a universal web-survey limit. |
| P2 | Pew Research Center, [When Online Survey Respondents Only "Select Some That Apply"](https://www.pewresearch.org/methods/2019/05/09/when-online-survey-respondents-only-select-some-that-apply/), May 9, 2019 | Randomized comparison of per-item responses versus checklists for undesirable experiences, with burden and acquiescence trade-offs. The accuracy inference assumes underreporting is more plausible in that setting; it is not a universal validation of every yes/no battery. |
| G1 | UK Government Analysis Function / Office for National Statistics, [Questionnaire design guidance](https://analysisfunction.civilservice.gov.uk/policy-store/questionnaire-design-guidance/) | Decision/data requirements, respondent-centered design, clear wording, recall periods, sensitive items, filters, cognitive/usability testing, and pilots. Tailor to the population and mode rather than adopting every example mechanically. |
| A1 | American Association for Public Opinion Research, [Best Practices for Survey Research](https://aapor.org/standards-and-ethics/best-practices/) | Preserve item nonresponse separately from None, Don't know, or refusal and be transparent in analysis. The retrieved section was about analysis; do not cite it as evidence for uninspected questionnaire-design sections. |
| P3 | Pew Research Center, [Two common checks fail to catch most bogus cases](https://www.pewresearch.org/methods/2020/02/18/two-common-checks-fail-to-catch-most-bogus-cases/), February 18, 2020 | Most cases classified as bogus passed attention and speeding checks; duplicate adjudication used multiple open ends, not shared short phrases or IP alone. Findings concern this study's definitions and samples, not current detector accuracy. |
| P4 | Pew Research Center, [No Easy Fix for Bogus Respondents in Online Opt-In Polls](https://www.pewresearch.org/methods/2026/08/27/no-easy-fix-for-bogus-respondents-in-online-opt-in-polls/), August 27, 2026 | Compares trap questions, prescreening, and voter-file matching in 2024 fieldwork; includes a fictitious platform option and shows privacy-related loss of genuine respondents. No respondent-level ground truth; do not copy its one-fail exclusion rule, rare-event traps, or population-specific findings as universal policy. |
| R1 | Gummer, Rossmann, and Silber, [Using Instructed Response Items as Attention Checks in Web Surveys: Properties and Implementation](https://www.ssoar.info/ssoar/handle/document/85346), 2021; DOI 10.1177/0049124118769083 | Peer-reviewed repository abstract inspected: instructed-response failures associated with other quality indicators; exclusion did not change substantive analyses in that study; no detected response-behavior effect from mere exposure. Do not infer optimal number or placement from the abstract. |
| R2 | [The Issue of Noncompliance in Attention Check Questions: False Positives in Instructed Response Items](https://www.ssoar.info/ssoar/handle/document/85091), Field Methods, 2022; DOI 10.1177/1525822X221115830 | Peer-reviewed repository abstract inspected: some failures were deliberate noncompliance; explaining a comprehensible reason improved compliance. Failure is not equivalent to not reading. Do not generalize the study's proportions to all surveys. |

## Vendor research and design guidance

| Key | Source | Supported use and limit |
|---|---|---|
| V1 | Qualtrics, [Using Commitment Requests Instead of Attention Checks for Data Quality](https://www.qualtrics.com/articles/strategy-research/attention-checks-and-data-quality/) | Vendor panel experiment and practice guidance: thoughtful-response requests, simple early checks, avoiding memory/trivia traps and fatigue-inducing grids, and fake-brand checks for higher-incentive falsification risk. Effects are study-specific; the skill does not adopt automatic one-fail rejection, assume typed words defeat modern bots, or treat vendor advice as a universal rule. |

## Qualtrics first-party support

| Key | Official page | Snapshot detail to recheck |
|---|---|---|
| Q1 | [Choice Randomization](https://www.qualtrics.com/support/survey-platform/survey-module/question-options/choice-randomization/) | Advanced randomization, fixed positions, subsets, scale reversal, preserving order through carry forward, and exporting viewing order. |
| Q2 | [Formatting Answer Choices](https://www.qualtrics.com/support/survey-platform/survey-module/editing-questions/formatting-answer-choices/) | Text entry, answer exclusivity, automatic Exclude from Analysis for certain special-choice text, and risks when changing choices after data collection. |
| Q3 | [Display Logic](https://www.qualtrics.com/support/survey-platform/survey-module/question-options/display-logic/) | Conditional questions/choices, page breaks, In Page incompatibilities, and hiding rather than deleting choices with data. |
| Q4 | [Carry Forward Choices](https://www.qualtrics.com/support/survey-platform/survey-module/question-options/carry-forward-choices/) | Source modes, one source set per destination, project limitations, and potentially different source/destination recodes. |
| Q5 | [Branch Logic](https://www.qualtrics.com/support/survey-platform/survey-module/survey-flow/standard-elements/branch-logic/) | Block-level paths, continuing after a branch, back-button effects, and distinction from display/skip logic. |
| Q6 | [Response Requirements & Validation](https://www.qualtrics.com/support/survey-platform/survey-module/editing-questions/validation/) | Force versus Request Response, format checks, custom-validation requirements and incompatibility with optional responses. |
| Q7 | [Mobile Survey Optimization](https://www.qualtrics.com/support/survey-platform/survey-module/mobile-survey-optimization/) | Mobile layouts, large-grid/scrolling concerns, vertical lists, and differences with the new survey-taking experience. |
| Q8 | [Survey Accessibility](https://www.qualtrics.com/support/survey-platform/survey-module/survey-tools/check-survey-accessibility/) | Experience-specific checker standards, limitations of automated checks, and responsibility for actual survey accessibility. |
| Q9 | [Previewing Surveys](https://www.qualtrics.com/support/survey-platform/survey-module/preview-survey/) | Validation bypass, recorded preview data and quotas, real-device testing, full-flow preview, and why preview links are not production links. |
| Q10 | [Response Quality](https://www.qualtrics.com/support/survey-platform/survey-module/survey-checker/response-quality/) | Speeding prerequisites, optional straightlining/missingness/text flags, licensing caveats, and exclusions of preview/test/synthetic data from native analyses. Vendor flags are not conclusive evidence of fraud. |
| Q11 | [Response Quality Functionality](https://www.qualtrics.com/support/survey-platform/data-and-analysis-module/data/response-quality-functionality/) | Issue-specific review filters and the broader filter that excludes responses matching any flagged parameter. Do not mistake this union filter for a multiple-signal adjudication policy. |
| Q12 | [Fraud Detection](https://www.qualtrics.com/support/survey-platform/survey-module/survey-checker/fraud-detection/) | Cookie-based repeat controls, bot score/status/errors, CAPTCHA distinction, Security Scan Monitor, post-submission duplicate detection, irreversible discard, licensing, metadata, and RelevantID deprecation. Errors are unknown, not human/bot evidence. |
| Q13 | [Timing Question](https://www.qualtrics.com/support/survey-platform/survey-module/editing-questions/question-types-guide/advanced/timing/) | Page-level metrics, accumulated repeat visits, total duration including time away, and page-break/randomization interactions. Elapsed time is not attentive reading time. |
| Q14 | [Survey Methodology & Compliance Best Practices](https://www.qualtrics.com/support/survey-platform/survey-module/survey-checker/survey-methodology-compliance-best-practices/) | ExpertReview duration, text-entry, grid, and readability warnings. Treat vendor duration/open-text thresholds as heuristics, not universal research limits or exclusion rules. |

## Use evidence proportionately

- Attribute empirical results to their population, format, and context. Do not
  generalize findings from sensitive personal events to every product survey.
- Treat five-point scales, proposed recall windows, and example answer bins as
  design candidates. Choose and pretest them; do not claim universal optimality.
- Separate source-backed platform behavior from untested account configuration.
  If a page is inaccessible, state the gap; do not invent UI steps or API fields.
- Preserve established instruments, permission requirements, and original scoring.
  An adaptation is not automatically validated or comparable to a benchmark.
- Analyze single ordinal items using counts and full distributions by default.
  Separate unknown/refusal from substantive ratings. Use composite scores only
  with a prespecified construct, defensible scoring, missingness rules and
  reliability/dimensionality checks. A vendor platform does not enforce these
  methodological safeguards automatically.
- Treat the risk table, flag-first policy, and adjudication workflow as this
  skill's conservative synthesis, not a single validated detection algorithm.
  Calibrate locally and report uncertainty and potential selection effects.
