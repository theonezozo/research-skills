---
name: pricing-study-designer
description: Select, design, and interpret pricing research and willingness-to-pay studies. Use when choosing between conjoint/discrete choice, Van Westendorp price sensitivity, Gabor-Granger, price laddering, monadic or sequential-monadic testing, price bracketing, and direct WTP; planning price, packaging, billing-metric, or subscription research; drafting live customer interviews, Outset or Marvin AI-moderated studies, or Qualtrics pricing surveys; or reviewing a pricing study's sampling, instrument, analysis, and evidence limits.
---

# Pricing Study Designer

Design for the pricing decision, not a preferred questionnaire. Separate perceived
acceptability, stated purchase response, feature-price trade-offs, and observed
purchasing behavior. Never substitute one for another.

Use this workflow to recommend a method, produce a fieldwork-ready specification,
or interpret supplied evidence. Default to **design only**: do not recruit, launch,
publish, change prices, spend money, configure integrations, or transfer participant
data without authorization for that operation.

## 1. Establish the decision

Extract supplied facts first. Ask one focused question at a time only when an
unresolved decision materially changes the design. Keep unavailable facts unknown.

Establish:

- **Decision and outcome:** acceptable range, candidate price comparison, feature
  or package trade-off, charging metric, acquisition, renewal, or actual conversion.
- **Offer readiness:** concept familiarity, credible alternatives, current spending,
  demonstrated value, and whether participants can understand the purchase.
- **Price basis:** currency, taxes, billing period, commitment, quantity, unit,
  usage allowance, overage, discounts, implementation and support.
- **Buyer and unit of analysis:** user, evaluator, budget owner, procurement,
  organization or independently purchasing business unit.
- **Population:** prospects versus customers, purchasing occasion, segments,
  recruitment source, available sample, and account duplication.
- **Decision constraints:** candidate prices, commercial effect worth detecting,
  deadline, budget, approved channels, platform entitlements and data handling.

For usage-based software, establish both the rate and a plausible total bill.
Do not confound a new billing metric, new feature bundle, and new price unless
the experimental design deliberately separates their effects.

## 2. Select the primary method

Read [Method selection and analysis](references/method-selection.md) before
recommending a method. Give the primary choice, why it fits, the strongest
alternative and why it loses, and the conclusions the study cannot support.

| Decision | Starting choice | Important gate |
|---|---|---|
| Understand value, budgets, charging units, or unfamiliar concepts | Live or AI-moderated discovery; direct WTP only as a probe | Do not promise an optimal price from interviews |
| Establish a perceived range in an understood category | Van Westendorp | Requires meaningful reference prices and four interpretable thresholds |
| Compare a few fixed-offer prices without exposing competing test prices | Randomized split-cell monadic | Needs sufficient independent buyers per arm |
| Trace stated response across prices for a fixed offer | Gabor-Granger or a defined price ladder | Repeated exposure, routing and hypothetical-response limitations |
| Trade off features, packages, competitors and price | Choice-based conjoint / discrete choice | Needs a defensible experimental design and model |
| Elicit a bounded threshold rather than a precise number | Explicitly defined bracketing | Preserve interval censoring and starting-price effects |
| Determine actual purchasing response | Authorized controlled market test | Needs real offer, traffic/accounts, operational and ethical review |

Treat sequential monadic as a distinct repeated-exposure design, not a cheaper
equivalent of independent cells. Clarify whether "laddering" means changing prices
or probing attributes, consequences and values. Clarify what "bracketing" means;
the label does not specify an algorithm.

When a staged study is warranted, explain each stage's decision contribution:
discovery to establish the offer, measurement to compare options, behavioral
validation to test consequential assumptions. Do not require every stage by rote.

## 3. Match the method to a collection channel

Read [Platform playbooks](references/platform-playbooks.md). Distinguish:

- **Live interviews:** researcher-led discovery, procurement context and cognitive
  pilots; optionally standardized tasks administered without improvisation.
- **Static unmoderated surveys:** fixed stimuli, numeric responses, programmed
  assignment and routing.
- **AI-moderated interviews with real people:** adaptive qualitative conversations.
  Outset and Marvin both collect these; Marvin is not merely a repository.
- **Synthetic respondents:** software checks or labeled simulations, never human
  willingness-to-pay evidence.

Use a controlled survey or experimental system that demonstrably preserves every
required control and export field. Qualtrics is one optional implementation
covered by this package, not a prerequisite or universal preferred vendor. Do not
treat instructions to an AI moderator as proof of deterministic behavior.

Treat platform facts as a **2026-09-15 public-documentation snapshot**, not a
guarantee of account access. Verify current permissions, compatible experience,
stimulus behavior and exports before fieldwork. In particular, check Marvin's
non-verbatim moderation and native Qualtrics Gabor-Granger's exposure-log limit.

## 4. Produce the study packet

Use [Instruments and deliverables](references/instruments-and-analysis.md) for
adaptable questions, an offer card, routing specification, data dictionary,
analysis plan, and report outline. Supply the parts needed for the requested scope:

1. Decision brief and method recommendation, including rejected alternative.
2. Buyer screener, recruitment/cohort definition, sample rationale and exclusions.
3. Invariant offer card and participant-facing instrument.
4. Assignment/routing specification and permitted interviewer/AI probes.
5. Export schema, analysis plan, uncertainty and claim boundaries.
6. Preflight checks, unresolved gates and launch authorization status.

Label invented examples as synthetic. Do not fill unknown prices, sample sizes,
owners, dates or platform capabilities with plausible-looking facts.

## 5. Pilot before collection

Test comprehension with actual target buyers, then test programming and exports.
Cover every arm, all-accept/all-reject, missing/unknown, contradictory answers,
boundary prices, repeat participation, interruption and device/language variation.

Verify numeric currency/period/quantity interpretation and total-bill arithmetic.
Inspect actual AI prompts and stimuli for drift, negotiation or added features.
If an invariant cannot be maintained, reclassify the session as qualitative or
move the quantitative task to controlled collection; do not silently pool modes.

Check consent for AI moderation, recording, transcription, observers, processing,
retention and withdrawal. Minimize identifiers; approve each destination and
transfer. Never expose confidential prototypes publicly merely to fit a tool.

## 6. Analyze within the design's limits

Preserve source exports. Decode labels, normalize without overwriting originals,
reconcile records, then interpret. Count independent buyers/accounts, not choice
tasks or repeated interviews, as the sample.

Plan sample size from decision-relevant precision or power per arm/segment;
simulate conjoint designs where needed. Do not impose a universal minimum N.
Report uncertainty without implying that intervals cure convenience-sample bias.

Prespecify ordinal purchase-intent distributions and any top-box definitions.
Do not map an intent scale to conversion probabilities without applicable
calibration. Resample at the independent respondent/account level for repeated
responses. Keep acceptability, modeled preference, stated revenue indices,
actual revenue and profit distinct.

For a single ordinal item, report counts and full labeled distributions rather
than default means. Prespecify comparison families, report effect sizes and
uncertainty, and distinguish missingness from zero. Keep personal contact and
payment information separate from responses. Review direct and indirect
identifiers, confidential company information, links and metadata for the exact
intended audience. Pseudonyms, truncated IDs and company-only attribution do not
guarantee anonymity. This package requires no companion skills.

## Evidence discipline

Use [Sources and authority](references/sources.md) for claim-specific references.
Distinguish methodological evidence, technical implementation documentation,
vendor advice and this skill's recommendations. Recheck changing platform facts;
never present inaccessible originals as directly verified or vendor heuristics
as universal research standards.
