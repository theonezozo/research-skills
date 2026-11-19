# Instruments and deliverables

## Contents

- [Study brief and offer card](#study-brief-and-offer-card)
- [Interview and AI guide](#interview-and-ai-guide)
- [Pricing question modules](#pricing-question-modules)
- [Finite-ladder specification](#finite-ladder-specification)
- [Data and analysis contract](#data-and-analysis-contract)
- [Reporting template](#reporting-template)
- [Selection acceptance scenarios](#selection-acceptance-scenarios)

Use these as adaptable design templates, not instruments already validated for
every market. Replace bracketed fields only from supplied/approved facts.
Use [Methods](method-selection.md) for interpretation and [Platforms](platform-playbooks.md)
for execution gates. All questions below are paraphrased design suggestions.

## Study brief and offer card

```text
Decision:
Primary estimand/outcome:
Primary method and why:
Runner-up and why not:
Population, purchasing occasion, recruitment channel:
Respondent role and independent buying unit:
Segments and separate customer/prospect/renewal cohorts:
Sample per arm/segment and precision/power rationale:
Offer/price range basis and unresolved assumptions:
Channel and documented capability / implementation proposal:
Inference limits:
Unresolved preflight gates and authorization status:
```

Freeze an offer card before price measurement:

```text
Offer version / package:
Customer outcome and credible capability description:
Included and excluded features, support and implementation:
Currency / taxes:
Price per [seat, account, resource, incident, usage unit]:
Billing interval / contract term / minimum commitment:
Included quantity and usage / overage rate:
Total bill at the stated quantity and usage:
Discounts or introductory terms / renewal basis:
Purchasing occasion and time horizon:
Relevant incumbent, alternative, delay or no-purchase option:
```

Keep outcome claims neutral and supported; do not promise unproven savings.
Ask participants to explain what they would receive and pay. Correct factual
misunderstandings without coaching preferences. Mark cases that still cannot
interpret the offer rather than forcing monetary answers.

## Interview and AI guide

Screen for involvement in the relevant purchase, knowledge of current spending,
and access to the approval process. Do not assume an enthusiastic user controls
the budget.

Use neutral discovery prompts:

- "How is this problem handled today, and what does that involve?"
- "What spending or internal effort does the current approach require?"
- "How would a purchase like this be evaluated and approved?"
- "Which charging unit would make the bill predictable? What makes it difficult?"
- "What would have to change for this to be worth considering?"

After a pricing response, probe "What did you base that answer on?" and
"What, if anything, would prevent a purchase even at that price?" Keep reasons
separate from the recorded measurement. Do not translate every feature request
into an outcome or every threshold into an actual budget.

Use this moderator guardrail as a **proposal, not proof of platform control**:

```text
Explain that this is research, not a sales negotiation or binding quote.
Use the approved offer and purchasing scenario.
Do not invent features, savings, discounts, prices or contract terms.
Do not suggest an answer, negotiate, or seek agreement after refusal.
Allow "cannot estimate", "not my decision" and skipping.
Ask neutral clarification without changing the recorded numeric answer.
Use only approved price exposures and routing.
Record misunderstanding, ambiguity and protocol deviation.
Keep explanatory probes after the fixed measurement block.
```

Audit actual questions, stimuli and responses. Marvin's non-verbatim behavior and
unverified Outset numeric controls mean these instructions alone do not qualify
an AI interview as a controlled price experiment.

## Pricing question modules

### Van Westendorp

Repeat the same currency, billing basis and offer reference for each question:

1. "Below what price would this offer seem so inexpensive that you would doubt
   its quality?"
2. "At what price would you consider this offer a bargain or good value?"
3. "At what price would this offer start to seem expensive, although you might
   still consider buying it?"
4. "At what price would this offer become too expensive to consider buying?"

Use open monetary responses and an explicit inability-to-estimate option.
Preserve raw answers. If checking inconsistent ordering during collection,
use a neutral correction opportunity and retain edits; do not force a pleasing
curve. Specify original/narrower PSM conventions in the analysis plan. [M1-M2]

### GG or standardized price ladder

"At [price and billing basis] for the offer shown, would your organization
purchase it within [time horizon]?"

Use yes/no plus a separately represented unknown/not-qualified response when
appropriate. Fix the decision meaning: organizational purchase is not personal
liking or willingness to recommend. Route only through the prespecified design.
Do not let explanatory probes create a revised offer mid-ladder.

### Monadic

Show one assigned price and ask the same purchase outcome in every arm.
If using a likelihood scale, retain a balanced labeled ordinal distribution,
for example definitely would not / probably would not / unsure / probably would /
definitely would. Include "not able to judge" separately from substantive scale
positions if needed.

Ask reasons after the outcome. Define any top-box before analysis; do not turn
scale codes into purchase probabilities or average them as a default.
Use actual conversion only when a real, authorized transaction is measured.

### Bracketing and direct WTP

For threshold bracketing, use the same fixed-offer acceptance question at a
prespecified price, then approved higher/lower questions. Preserve accepted and
rejected bounds.

For exploratory budget-range elicitation, ask:
"What range, if any, could your organization realistically consider for this
offer on the stated terms?" Follow with the basis and approval constraints.
Label this a reported budget range, not a mathematically identified reservation
price interval.

For direct WTP, ask:
"What is the most your organization could justify paying for this exact offer
over [period]? It is fine if you cannot estimate that."

### Conjoint task shell

"For your next [purchase occasion], which option would you choose?"

Show offers from the approved experimental design, with understandable attributes
and consistent price bases. Include current arrangement/no purchase when
appropriate. Do not improvise attribute combinations or replace the design with
this text template. Store task/alternative IDs and the complete attribute levels.

## Finite-ladder specification

Use this **custom design proposal**, not a description of Qualtrics native GG:

```text
Inputs: strictly increasing finite prices; offer version; randomized start rule.
Record: start assignment, each displayed price, response, order, timestamps.
If yes: record accepted bound; ask an untested higher price if needed.
If no: record rejected bound; ask an untested lower price if needed.
After bounds exist: test between them until adjacent on the price grid.
Stop: adjacent bounds, highest accepted, lowest rejected, or unknown/refusal.
Unknown/refusal: stop or use the approved missingness route; never convert to no.
Output: observed exposures, bound interval, censoring, terminal reason.
```

Specify exactly which eligible untested price is next, such as a prespecified
midpoint-index rule; do not leave it to the moderator. Prohibit revisiting a price
unless testing consistency is explicitly part of the protocol.
For inconsistent answers, preserve evidence and apply the planned sensitivity
rule rather than silently repairing data.

## Data and analysis contract

Preserve immutable raw data and create decoded/normalized derivatives.

| Field group | Required meaning |
|---|---|
| Identity and unit | Pseudonymous response ID, participant ID, independent buying-unit ID, duplicate rule |
| Eligibility | Role, purchasing knowledge, cohort, source, segment, exclusions with reasons |
| Design | Study/offer/instrument version, channel/mode, arm, start assignment, assignment unit |
| Exposure | Task/sequence/alternative ID, actual shown price, currency, period, quantity, complete stimulus |
| Response | Raw answer, decoded value/label, observed versus inferred, timestamps where needed |
| Missingness | Not asked, skipped, unknown, ineligible, technical loss; distinguish each from no |
| Thresholds | PSM four amounts, or accepted/rejected bounds and left/right censoring |
| Audit | Prompt/stimulus deviations, interruptions, completion, consent/retention status |

Store repeating exposures as separate rows or uniquely named fields; preserve a
stable link to the participant/account record. Record zero WTP separately from
unknown. If a native solution lacks required fields, document the loss and decide
before collection whether it is acceptable.

Predefine:

- Primary outcome/contrast, valid-case rules, denominator, independent unit,
  intent box definition, and subgroup/multiple-comparison policy.
- Missingness, threshold ordering, inconsistent answers, outliers and censoring.
- PSM convention/ties/interpolation; GG observed/inferred acceptance model;
  monadic allocation and contrasts; conjoint estimator/design validation.
- Uncertainty at participant/account level, selection/mode limitations and
  sensitivity to exclusions or model choice.
- Commercial assumptions separating acceptance, quantity, revenue and costs.

Reconcile source totals: invited, started, eligible, assigned, completed, excluded,
exported, imported, matched and unmatched. Explain material gaps. Do not count
ten choices by one buyer as ten buyers or silently drop non-buyers.

## Reporting template

```text
Decision and recommendation:
Evidence type: acceptability / stated response / modeled choice / observed behavior
Method, cohort, independent buyer N and segment/cell Ns:
Offer, currency, units, time horizon and alternatives:
Estimates and uncertainty; candidate-price differences:
Reasons and buying constraints, with traceable evidence:
Missingness, exclusions, unmatched records and sensitivity:
What the result does NOT establish:
Commercial assumptions and needed behavioral validation:
Unresolved decision gates:
```

Use counts with percentages for small samples. For interview-only work, report
themes, ranges and uncertainty without a population demand curve.
Do not label a PSM intersection "the recommended launch price" without a separate
commercial argument and validation.

## Selection acceptance scenarios

Use these synthetic scenarios to check the recommendation before delivery:

| Request | Expected recommendation | Reject this failure |
|---|---|---|
| Eight technical users; unfamiliar usage-based product; choose launch price | Discover comprehension, value metric and buyer authority; generate hypotheses | "Eight interviews establish revenue-maximizing price" |
| Mature fixed offer; three candidate prices; adequate independent buyers | Monadic for isolated comparison; GG alternative if curve information outweighs repeated-exposure risk | Split an inadequate sample and claim precision |
| Features, tiers, competitors and price all vary | Designed conjoint with credible levels and outside option | Ad hoc identical offers at different prices called conjoint |
| Familiar offer; only plausible acceptability range needed | PSM with named convention and interval uncertainty | OPP interpreted as profit optimum |
| AI-only interviews; exact numeric ladder and complete exposure logs required | Demonstrate controls; otherwise separate survey measurement or report unmet gate | Assume moderator prose enforces randomization |
| Native Qualtrics GG; every shown price must be auditable | Custom finite ladder or explicitly unresolved requirement | Promise complete native exposure history |
| Several respondents from each enterprise customer | Define autonomous buying units; cluster/deduplicate appropriately | Count users as independent customer demand |
