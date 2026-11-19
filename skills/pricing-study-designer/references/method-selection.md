# Method selection and analysis

## Contents

- [Selection matrix](#selection-matrix)
- [Van Westendorp](#van-westendorp)
- [Gabor-Granger and price ladders](#gabor-granger-and-price-ladders)
- [Monadic designs](#monadic-designs)
- [Conjoint and discrete choice](#conjoint-and-discrete-choice)
- [Bracketing and direct WTP](#bracketing-and-direct-wtp)
- [Sampling and commercial inference](#sampling-and-commercial-inference)

Resolve source IDs in [Sources and authority](sources.md). Treat the selection
rules as a synthesis, not a claim that a vendor endorses every recommendation.

## Selection matrix

| Method | Choose for | Avoid or qualify for | Output and burden |
|---|---|---|---|
| Van Westendorp (PSM) | Perceived price thresholds for a clear offer in a familiar category | Unfamiliar offer; meaningless "too cheap"; revenue optimization | Acceptability curves/range; short questionnaire, substantive interpretation |
| Gabor-Granger (GG) | Stated purchase response to prices of a fixed offer | Simultaneous package redesign; strong non-price competitive effects | Conditional acceptance curve and stated revenue index; routing required |
| Price laddering | Threshold discovery and reasons; standardized price sequence if measuring | Negotiation-like interviews used as demand estimates | Qualitative threshold narrative or GG-like output, depending on specification |
| Split-cell monadic | A few candidate prices, isolated price exposure | Scarce sample spread over many arms | Between-arm stated response; larger recruitment requirement |
| Sequential monadic | Several separate evaluations when carryover is tolerable | Claims of unanchored independent-cell effects | Within-person responses; lower recruitment, greater exposure/analysis burden |
| Choice-based conjoint | Feature-price-package trade-offs and alternatives | Poorly understood attributes; price-only identical alternatives; unsupported sample/design | Conditional utility, choice simulation and WTP; greatest design/modeling burden |
| Price bracketing | Bounded budget/threshold elicitation | Undefined protocol; treating interval midpoint as exact WTP | Interval or range; efficient but anchor/censoring-sensitive |
| Direct WTP | Discovery, reference prices, candidate range generation | Sole basis for launch price or demand forecast | Stated amount and rationale; simple but potentially biased |
| Controlled market test | Real purchasing behavior | Insufficient traffic, long sales cycles, contamination, unauthorized price discrimination | Observed response in tested context; operationally demanding |

Choose discovery before quantification when buyers cannot understand the offer.
A novel product in a familiar category may still support PSM; maturity alone is
not the gate. Test comprehension, budget knowledge and plausible alternatives.
For enterprise software, incorporate switching costs, implementation, security,
service and procurement constraints rather than treating price as the only lever.
[M2, M8, M10]

## Van Westendorp

Collect four monetary thresholds for the **same offer and price basis**:
too cheap to trust quality, cheap/good value, expensive but still worth considering,
and too expensive to consider. Use the question template in
[Instruments](instruments-and-analysis.md). Allow inability to estimate; do not
force a meaningful "too cheap" threshold for a free/subsidized or unfamiliar offer.

Prefer open numeric inputs when avoiding a supplied range is important. Bounded
sliders reveal the researcher's range and can anchor responses. Inspect ordering,
currency errors, rounding and outliers; do not silently reorder respondents'
answers. Prespecify equal-threshold handling and report exclusions/sensitivity.
[M1, M2]

### Curves and explicit conventions

Let respondent thresholds be `TC_i, C_i, E_i, TE_i`. For a common valid-case cohort,
define these proportions at price `p`:

| Curve | Definition | Direction as price increases |
|---|---|---|
| Too cheap | `TC(p) = proportion(TC_i >= p)` | Decreasing |
| Cheap | `C(p) = proportion(C_i >= p)` | Decreasing |
| Expensive | `E(p) = proportion(E_i <= p)` | Increasing |
| Too expensive | `TE(p) = proportion(TE_i <= p)` | Increasing |
| Not cheap | `NC(p) = 1 - C(p)` | Increasing |
| Not expensive | `NE(p) = 1 - E(p)` | Decreasing |

Declare tie inequalities, common denominator, interpolation and crossing rules.
Other implementations can use different endpoint conventions. Do not mix their
results without reconciliation.

Use the **original convention as documented in the CRAN implementation** by
default; name the alternative if using a provider's narrower four-curve range:

| Statistic | Original convention | Narrower convention |
|---|---|---|
| Marginal cheapness / lower bound (PMC) | `TC = NC` | `TC = E` |
| Marginal expensiveness / upper bound (PME) | `TE = NE` | `TE = C` |
| Indifference price (IPP/IDP) | `C = E` | Same |
| "Optimal price point" (OPP) | `TC = TE` | Same |

**Not cheap is not synonymous with expensive.** Do not mix one convention's
lower bound with the other's upper bound. Attribute these definitions to M1,
not to a claim of having read the original 1976 paper.

For step curves, crossings may fall between observed values or span an interval.
Report the estimation/interpolation convention and ambiguity. If no unique
supported crossing exists, report that limitation rather than manufacturing a
point. Resample respondents/accounts for uncertainty, retaining failed/ambiguous
crossings in the uncertainty report rather than silently discarding them.

Use OPP only as the conventional label for balanced too-cheap/too-expensive
proportions. It is **not a revenue or profit optimum**, nor proof of maximum
purchasing. Newton-Miller-Smith adds purchase-intent modeling; it is a separate
extension whose probability calibration must be justified. [M1, M2]

### Synthetic mathematical sanity check

Use thresholds `Z, Z+20, Z+40, Z+60`, where `Z` is continuously uniform on
`[0,100]`, to check curve direction and convention. This is not customer data.

| Price | TC | C | E | TE | NC | NE |
|---|---:|---:|---:|---:|---:|---:|
| 60 | .40 | .60 | .20 | .00 | .40 | .80 |
| 70 | .30 | .50 | .30 | .10 | .50 | .70 |
| 80 | .20 | .40 | .40 | .20 | .60 | .60 |
| 90 | .10 | .30 | .50 | .30 | .70 | .50 |
| 100 | .00 | .20 | .60 | .40 | .80 | .40 |

Expect original bounds `60,100`, narrower bounds `70,90`, and OPP/IPP `80`.
Finite empirical samples need not reproduce these exact continuous results.

## Gabor-Granger and price ladders

Fix the offer, buying occasion and response question. Specify candidate prices
or generation algorithm, starting assignment, yes/no/unknown routing, stopping
rule and endpoint behavior **before** collection. Do not improvise a cheaper
price to obtain acceptance. Vendor implementations differ; the Qualtrics native
algorithm is one implementation, not the definition of GG. [M3]

For a finite monotonic ladder, seek the boundary between an accepted lower price
and a rejected higher price. A random starting price can reduce a shared initial
anchor and allow start-effect checks; it does not remove range learning. Preserve
all exposures and distinguish observed from monotonicity-inferred responses.

Estimate stated acceptance at each price only under declared assumptions.
Adaptively exposed participants are not interchangeable with randomized monadic
cells: raw yes/exposed fractions may be selected by previous responses. Specify
the threshold reconstruction/model rather than naively pooling exposure rows.

Keep all-reject participants in the intended buyer denominator. Treat unknown,
not asked and missing differently from rejection. Inspect nonmonotonic answers;
use a prespecified handling/sensitivity policy rather than silently forcing a
monotonic curve. Preserve repeated-response dependence in uncertainty estimates.

Report `price * stated acceptance probability` as a **stated revenue index**
under a one-unit/common-period assumption, not forecast revenue. Select tested
candidate prices with uncertainty; do not extrapolate a smooth peak as fact.

Use "price laddering" for explicit sequential prices and response thresholds.
Descending ladders can resemble bargaining and encourage waiting for a discount.
Specific numbers of repeats or intent cutoffs are vendor heuristics. [M9]

Distinguish qualitative **means-end laddering**: probe how an attribute changes
work, why the consequence matters, and what outcome it serves. Use it to explain
value or develop conjoint attributes, not to estimate a numeric demand curve.

## Monadic designs

For split-cell monadic testing, randomly assign comparable eligible buyers to
one price, keeping every other intended stimulus feature constant. Ask the same
outcome questions. Power/precision must apply per arm, not just total N.
This avoids exposure to the other **test prices**, not all anchoring. [M8]

For sequential monadic testing, present offers individually to the same person.
Randomize/counterbalance order; store sequence and position. Account for repeated
measures, carryover and fatigue. Do not analyze the evaluations as independent
participants. GG can be sequential-monadic, but not every sequential-monadic
design is GG. A first-exposure-only sensitivity analysis can be informative.

Randomizing hypothetical price exposure supports causal comparisons of the
measured survey response under that design, not automatic claims about actual
sales. Separate intent outcomes from real purchase behavior.

## Conjoint and discrete choice

Use conjoint when buyers trade off attributes and price, not merely to add
complexity to a fixed-offer price test. Derive credible attributes and levels from
buyer research. Establish an estimable experimental design, level coverage,
plausible interactions, respondent burden and prohibited combinations. Too many
restrictions can confound effects. Obtain statistical design/modeling support
when these checks cannot be performed. [M4]

Represent no purchase, delay or the incumbent when realistic. An incumbent with
existing expenditure is not necessarily the same as spending nothing. Forced
choice measures preference conditional on selecting one displayed alternative;
an outside option alone does not calibrate actual purchase incidence.

Do not show otherwise identical alternatives distinguished only by price and
claim feature trade-offs: the cheapest usually dominates. A randomized offer at
one price versus no purchase is a useful binary-response design, not evidence
about unvaried features.

Prespecify estimator, respondent clustering, exclusions and validation. Check
holdout prediction, model fit/convergence, price response and sensitivity.
Hierarchical Bayes does not cure insufficient independent participants. Consider
logit's substitution/IIA assumptions when offers are close substitutes. [M4, M7]

For linear price utility, conditional compensating WTP for a feature change is
`-beta_feature * feature_change / beta_price`. State baseline package, alternatives,
outside option, units, tested range and uncertainty. Near-zero price coefficients
make ratios unstable. Nonlinear price specifications require appropriate
compensating-variation calculations, not this ratio blindly. Do not extrapolate,
sum WTP across interacting attributes, or equate simulated preference shares
with market shares. Ratios of average coefficients need not equal average
individual WTP. [M5, M7]

## Bracketing and direct WTP

Define "price bracketing" operationally: selecting an interval, answering adaptive
higher/lower questions, or discussing a plausible budget range. The reviewed
sources do not establish a single standardized method under this label.
Adaptive threshold questions can overlap GG; state the actual procedure. [M3]

Under a stable monotonic threshold model, accepting 100 and rejecting 150 implies
`WTP in [100,150)`, **not WTP = 125**. Retain left-censoring when the lowest price
is rejected and right-censoring when the highest is accepted. Use interval-censored
estimation or transparent bounds; distinguish elicited belief ranges from purchase
threshold intervals. Report tested range and starting/sequence effects.

Use direct maximum WTP and "cannot estimate" to discover reference points. Probe
current spending, alternatives and approval requirements separately. Do not
assume bias always points downward, or turn an aspirational amount into a binding
budget commitment. Triangulate with other evidence. [M10, M11]

## Sampling and commercial inference

Define the independent buying unit, eligibility, acquisition channel, time
horizon, exclusions and segments. Count both respondents and unique buying units.
Multiple users in one account do not create independent budgets. Deduplicate
corporate families according to purchasing autonomy, or explicitly model
informants nested within accounts.

Separate users' preferences from budget owners' decisions; distinguish new
purchase, expansion and renewal. Do not pool customer/prospect or human/AI modes
without checking comparability. Link interviews to survey outcomes only through
approved identifiers, with unmatched records and differing populations reported.

Choose N from desired interval width or the commercially meaningful contrast,
baseline rates, arm allocation and subgroup needs. Simulate conjoint design and
estimation under plausible preferences. If mentioning Sawtooth's `n >= 500c/(t*a)`
main-effects heuristic, label it a heuristic: `c` is maximum attribute levels,
`t` tasks, `a` alternatives excluding none. It is not a power analysis or a
guarantee for individual-level or subgroup estimates. [M6]

Report ordinal intent distributions with counts/denominators; prespecify any
top-box and uncertainty. Avoid universal intent-to-conversion mappings.
Report practical differences, uncertainty and exploratory multiple comparisons.
Neither large N nor narrow intervals repair a biased recruitment frame.

Keep `revenue(p) = p * Q(p)` separate from `profit = revenue - relevant costs`.
Stated acceptance is not market quantity Q: population, incidence, units, time,
channel and calibration assumptions are still needed. For subscriptions, account
for retention, discounting, delivery/support and acquisition costs where relevant.

Use observed purchase evidence for consequential decisions when feasible and
authorized. M11's consumer-goods meta-analysis finds average hypothetical
overstatement; its reported 21% is **not** a correction factor for enterprise
software, another study, or AI moderation.
