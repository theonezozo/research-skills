# Sources and authority

Use the source IDs below to trace claims in this package. References and
capability descriptions were carried forward from a **2026-09-15** public-source
research snapshot, not freshly verified during packaging. Platform facts are
not verified account entitlements. Question templates, selection rules, audit
requirements and custom survey flows are synthesis unless attributed otherwise.

## Weight evidence appropriately

Prefer academic work for theory/empirical validity, specialist technical
documentation for exact algorithms, and first-party support for platform behavior.
Use vendor research articles for practical guidance, not proof that their method
is universally best. Treat sample sizes, purchase-intent mappings and marketing
claims as heuristics unless a relevant validation supports them.

The original 1976 Van Westendorp archive was not available in that snapshot.
Attribute the original/narrower convention distinction to the CRAN documentation,
not to direct verification of that paper. The hypothetical-bias meta-analysis was
read through its institutional abstract, not the unavailable publisher full text.
Do not imply stronger access or evidence than this.

## Methodological sources

| ID | Publisher and source | Claims supported / limits |
|---|---|---|
| M1 | Max Alletsee / CRAN, [pricesensitivitymeter reference manual](https://cran.r-project.org/web/packages/pricesensitivitymeter/refman/pricesensitivitymeter.html) | Original versus narrower range intersections, curve inversion, validation/interpolation, NMS extension. Technical implementation, not independent validation. |
| M2 | Qualtrics, [Van Westendorp pricing explained](https://www.qualtrics.com/articles/strategy-research/van-westendorp-pricing-studies-explained/) | Four questions, open/bounded responses, OPP and real-purchase validation. Vendor guidance, not proof of revenue optimality. |
| M3 | Qualtrics Support, [Pricing Study: Gabor Granger](https://www.qualtrics.com/support/common-use-case/xm-solutions/pricing-study-gabor-granger/) | Native algorithm, middle-third start, automatic intervals, range/reporting/compatibility restrictions and unavailable exact price history. Applies to this solution, not all GG designs. |
| M4 | Qualtrics Support, [Conjoint Analysis White Paper](https://www.qualtrics.com/support/conjoint-project/getting-started-conjoints/getting-started-choice-based/conjoint-analysis-white-paper/) | Attributes/levels, design, prohibitions, HB and simulation. Sample guidance is not universal power analysis. |
| M5 | Qualtrics, [Using conjoint analysis for pricing research](https://www.qualtrics.com/articles/strategy-research/pricing-conjoint/) | Reference-package-dependent WTP and monetary utility interpretation. Do not adopt universal superiority claims. |
| M6 | Sawtooth Software, [Sample Size Rule of Thumb for Choice-Based Conjoint](https://sawtoothsoftware.com/resources/blog/posts/sample-size-rules-of-thumb) | Explicit heuristic status, main-effects exposure rule and limitations; none excluded from alternative count. |
| M7 | Kenneth Train / Cambridge University Press, [Discrete Choice Methods with Simulation, second edition](https://eml.berkeley.edu/books/choice2.html), [Chapter 3](https://eml.berkeley.edu/books/choice2nd/Ch03_p34-75.pdf) | Author-hosted academic text; coefficient-ratio WTP, scale cancellation and logit substitution/IIA assumptions. |
| M8 | Conjointly, [What is Monadic Testing?](https://conjointly.com/blog/what-is-monadic-testing/) | Split-cell versus sequential monadic, recruitment/carryover trade-off, GG as a sequential application. Numeric sample advice remains heuristic. |
| M9 | SBI Growth, [Price Sensitivity & How To Measure It](https://sbigrowth.com/insights/price-sensitivity) | A descending-price ladder procedure and negotiation bias. Intent cutoff and repeat counts are vendor choices. |
| M10 | Nick Hague / B2B International, [The Problem With Price](https://www.b2binternational.com/publications/pricing-research-marketing/) | Industrial buying context, switching costs, differentiation and stated-versus-real behavior. Do not adopt dated universal mode/N prescriptions. |
| M11 | Schmidt & Bijmolt / Journal of the Academy of Marketing Science, [Accurately measuring willingness to pay for consumer goods: a meta-analysis of the hypothetical bias](https://research.rug.nl/en/publications/accurately-measuring-willingness-to-pay-for-consumer-goods-a-meta/) | Institutional abstract: 77 studies, 47 papers, 115 effect sizes; average 21% hypothetical bias with variation. Not an enterprise-software or AI-specific correction factor. |

## Platform sources

| ID | Publisher and source | Documented capability / boundary |
|---|---|---|
| P1 | Outset, [AI-Moderated Interviews](https://outset.ai/platform/interviews) | Guide creation, probes, stimuli, screen sharing, Likert/matrix/ranking. Does not establish exact currency fields or randomized price arms. |
| P2 | Outset, [FAQ](https://outset.ai/resources/faq) | Branching/skips, moderation controls, anonymous participation and transcript/report/CSV/media exports. No verified pricing-specific engine or complete experimental export schema. |
| P3 | Marvin Help Center, [How do I use AI Interviewer?](https://help.heymarvin.com/en/articles/11402590-how-do-i-use-ai-interviewer) | New studies, guides, conditional instructions, legal acceptance, prototypes and response limits. Explicit non-verbatim questions and repeat-submission caveats; temporary plan language. |
| P4 | Marvin, [Live Interviews](https://heymarvin.com/product/live-interviews) | Zoom/Meet/Teams capture, observers, transcription and analysis. Recording capability is not participant recruitment. |
| P5 | Marvin Help Center, [Import and analyze Qualtrics surveys](https://help.heymarvin.com/en/articles/10351185-import-and-analyze-qualtrics-surveys) | Import, mapping, filtering, refresh and analysis; plan/seat/API gates. Not Qualtrics study launch. |
| P6 | Marvin Help Center, [How do I export data from Marvin?](https://help.heymarvin.com/en/articles/10130443-how-do-i-export-data-from-marvin) | Recording, transcript, note and insight exports. Note CSVs do not establish a numeric experiment dataset. |
| P7 | Qualtrics Marketplace, [Van Westendorp Pricing Sensitivity Study](https://www.qualtrics.com/marketplace/vanwesterndorp-pricing-sensitivity-study/) | Native template, prebuilt logic/workflow/reporting. Check account availability; do not use generic sample examples as standards. |
| P8 | Qualtrics Support, [Randomizer](https://www.qualtrics.com/support/survey-platform/survey-module/survey-flow/standard-elements/randomizer/) | Grouped/randomized flow elements, embedded assignments, even presentation and viewing-order export. Presentation balancing is not completed-cell balancing. |
| P9 | Qualtrics Support, [Embedded Data](https://www.qualtrics.com/support/survey-platform/survey-module/survey-flow/standard-elements/embedded-data/) | Condition metadata, piping/branching, variable types and sensitive-URL warnings. Custom pricing design still requires implementation. |
| P10 | Qualtrics Support, [Exporting Response Data](https://www.qualtrics.com/support/survey-platform/data-and-analysis-module/data/download-data/export-data-overview/) | Respondent exports, embedded data, formats/options and permissions. Verify chosen export retains required fields. |
| P11 | Qualtrics Support, [Getting Started with Conjoint Projects](https://www.qualtrics.com/support/conjoint-project/getting-started-conjoints/getting-started-choice-based/getting-started-with-conjoint-projects/) | Choice-based conjoint, separate purchase and permissions. Recheck current limits and entitlements. |

## Reverification procedure

Before advising a live implementation, reopen the relevant first-party pages and
check account capabilities, export examples and pilot behavior. Record the date
and any changed limitation in the study packet. If documentation is unavailable,
label the fact unverified and select a demonstrable alternative; do not infer
support from a tool name, marketing claim or repository integration.

Use the pricing-method source for interpretation even when the platform's report
uses stronger labels such as "optimal price" or "demand." Report uncertainty,
study population and calibration assumptions alongside any commercial conclusion.
