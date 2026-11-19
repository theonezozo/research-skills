---
name: data-visualization
description: "Choose, create, review and style truthful, accessible charts, data tables and dashboards. Use for chart selection, axis and encoding decisions, graphical-integrity audits, data storytelling, operational monitoring and accessible interaction. Covers evidence contracts, missingness, uncertainty, scales and review checks without requiring a particular rendering framework."
---

# Data visualization

Start with the reader's decision, not a chart gallery. Prefer the simplest
encoding that preserves the relevant comparison, context, and uncertainty.

## 1. Establish the input and evidence contract

- State audience, question, intended action, and what must be understood at a
  glance versus on inspection. For review, identify the claim being audited.
- Confirm authorized source/version, unit of observation, field meanings, units,
  cohort, time window/time zone, denominator, exclusions, deduplication, and
  missing-value codes. Record filters, aggregations, transformations, and rounding.
- Separate unknown, not applicable, suppressed, and observed zero. Do not impute,
  interpolate, drop outliers, or join gaps silently.
- Reconcile counts/totals to the source before drawing. Use unique customers or
  companies for customer prevalence, not mentions or repeated interviews.
- Keep raw precision for geometry and calculations; format only display values.
  Report percentage-point changes separately from relative percentage changes.
- Mark unavailable evidence unknown; use clearly labeled synthetic data only for
  demonstrations, never as research findings.

For multi-source synthesis, define source totals, units, join keys/cardinality,
duplicate rules, time windows, exclusions and claim limits before retrieval.
Reconcile matched and unmatched populations without counting repeated sources
as independent observations. Use only separately authorized inputs. Review direct
and indirect identifiers, small cells, confidential business information, links
and hidden metadata for the intended audience. An aggregate or pseudonym is
not automatically anonymous. No companion skills are required.

## 2. Choose the native deliverable and chart

Use the requested medium: spreadsheet, Power BI, slide, static figure, document,
or application. Do not turn every request into HTML or React. Retain the host's
visual system and interaction conventions.

Treat this selection table as **methodological synthesis**, informed by public
chart definitions, not a verbatim prescription from a cited author or vendor.

| Reader's question | Default | Check or alternative |
|---|---|---|
| Which category is larger? | Aligned bars or position-based dots | Sort by value for rank, by natural order for ordered categories; horizontal bars for long labels. |
| How does it change over time? | Line with genuine temporal spacing | Columns for discrete period totals; gaps for missing observations; small multiples for many series. |
| How are values distributed? | Histogram, dot/strip plot, box plot | State bins and sample size; show points for small samples; explain box/whisker definition. |
| Are two measures related? | Scatterplot | Label units, show overlap/density and uncertainty as appropriate; association is not causation. |
| What makes up a whole? | Stacked bar or 100% stacked bar | Verify disjoint, exhaustive parts and local denominator. Pie/donut only for a few clearly distinguishable parts, not precise ranking. |
| How do ordered responses differ? | Ordered or diverging stacked Likert bars | Preserve full categories and counts/local n; explicitly position neutral and exclude missing separately. |
| Where are patterns in a matrix? | Heatmap plus scale and values/table | Sequential magnitude or meaningful diverging midpoint; distinguish absent from minimum. |
| What changed from start to finish? | Waterfall or paired dots/slope | Waterfall contributions must reconcile; slope needs the same units and comparable endpoints. |
| Is performance within a target? | Value + target/reference + trend | Prefer an aligned bullet/linear display; gauge only if it improves the task. |
| Where is a spatial pattern? | Map only when geography matters | Normalize rates for exposure/population where appropriate; do not map counts as rates. |
| What are the exact values? | Table, optionally with restrained in-cell marks | Align numbers, expose units, retain accessible headers and sorting. |

For one ordinal Likert item, lead with the response distribution; do not default
to a mean. State count and denominator beside small-sample percentages.
Differentiate confidence/credible/prediction intervals, ranges, and standard
deviations; label method/level and never invent uncertainty from aggregates.
Order categories by verified meaning, not numeric storage codes. Keep category
colors stable across panels and regeneration. A neutral-looking visual position
for "Not sure" is not an ordinal midpoint or a scoring assumption; distinguish
uncertainty from substantive ratings. Define labels, ordering and category colors
in the current data dictionary rather than borrowing another survey's schema.

For report-wide chart inference, declare the full comparison family and label
post-hoc exploration; use Holm-adjusted p-values for charted association claims,
not isolated raw p-values. Show counts, denominators and effect sizes, separating
full-cohort answered n from pair-complete tested n and exclusions. Follow
the declared analysis plan, retaining test definitions and raw p-values for
provenance; never label nonsignificance as "no relationship."

For operational monitoring, distinguish absolute policy/threshold breaches from
relative rank. Show the configured threshold, units, exposure, measurement window,
freshness, and recent history; preserve breach-duration semantics. Never invent
an SLO or let an aggregate hide an important spike without disclosing aggregation.

## 3. Preserve graphical integrity

- **Baseline:** start bars and magnitude-encoding filled areas at zero; negative
  values extend from the same zero reference. Do not break/truncate bars.
  Position-based lines/dots may use a nonzero axis to reveal variation: expose
  the range, units, and reason; do not imply length or exaggerated effect.
- **Scale:** use consistent tick spacing and honest temporal spacing. Keep
  comparison panels on common domains, units, and aspect ratios; label any
  independently scaled panels conspicuously and avoid magnitude comparisons.
- **Log:** use only for a meaningful ratio question; label the base and explain
  multiplicative spacing. Do not silently discard zero/negative values or
  present log heights as linear quantities.
- **Dual axes:** prefer aligned panels or explicitly indexed series with a
  stated reference period. If unavoidable, label both units/ranges and bind each
  series to its axis; do not tune scales to manufacture correlation.
- **Geometry:** use position/length for precise comparison. If area represents
  value, scale area, not radius/diameter (`radius ∝ sqrt(value)`). Avoid decorative
  perspective, 3D volume, pictogram scaling, smoothing, or animation that changes
  perceived quantities.
- **Lie-factor audit:** compare relative effect in the graphic to relative effect
  in data: `LF = ((g2-g1)/g1) / ((d2-d1)/d1)`. Use the actual encoded magnitude
  (length or area), the same observations/order, consistent units within each
  pair, and comparable sign conventions. Aim for proportionality, not a magic
  tolerance. If either initial value or the data change is zero, or values cross
  zero, this ratio is undefined or unhelpful: inspect the mapping and absolute
  differences instead. Do not mechanically score a disclosed cropped line axis.
- **Data-ink:** remove redundant decoration, not necessary labels, units, reference
  lines, focus indicators, uncertainty, or accessible alternatives. Treat this as
  a clarity heuristic, never a mandate to maximize an ink ratio numerically.
- **Context:** show relevant baselines, denominators, source/cutoff, and comparison
  periods. Annotate material events and transformations without cherry-picking.
  A visual association or before/after pattern does not establish a cause.

## 4. Style for meaning and accessibility

- Establish title → chart/decision → supporting detail hierarchy. Use consistent
  typography, spacing, alignment, number precision, and restrained gridlines.
  Prefer direct labels when legible; do not hide essential meaning in tooltips.
- Use categorical colors for distinct groups, sequential luminance for magnitude,
  and a diverging scale only around a meaningful reference. Preserve category
  identity across views unless the host explicitly encodes rank instead.
- Reserve status colors for defined states. Add text, marker shapes, line styles,
  patterns, or boundaries; never rely on red/green or color alone.
- Meet text contrast of at least **4.5:1**, or **3:1** for large text (18 pt regular
  or 14 pt bold). Do not round a failing ratio up to the threshold.
- Meet **3:1** against adjacent colors for graphical objects required to understand
  content and required control/state indicators, subject to WCAG exceptions.
  This is not blanket pairwise contrast across every palette entry; use
  contrasting boundaries, labels, or patterns where needed.
- Provide an accessible name, concise description of the question/key pattern,
  and a structured table or equivalent long description with the same values,
  units, filters, and caveats. Keep these synchronized after interactions.
- Make filters, sort, drill-down, and data/tooltip inspection keyboard operable
  with logical focus order, visible focus, and screen-reader state. Provide
  focus/tap alternatives to hover and no keyboard traps. Respect reduced motion.
- Test light/dark and high-contrast/forced-colors where supported. On narrow
  screens reflow panels or offer a table; do not simply shrink unreadable text.

### Implementation boundary

Use the destination application's documented design system and installed library
version. Verify exports, props, semantic tokens, theme support and chart-library
compatibility before generating implementation code. Do not invent an API or
assume a library's accessibility claim certifies the consuming chart.

If documentation or access is unavailable, state the gap and provide a
framework-neutral specification: chart type, encodings, scales, semantic color
roles, responsive behavior and accessible alternatives. Do not install packages
or change credentials merely to make a documentation task appear implemented.
Preserve an existing report's coherent visual grammar when adapting its figures;
do not export that report's special palette to unrelated applications.

## 5. Verify and hand off

Read [worked examples and review checks](references/examples.md) for baseline,
Likert, monitoring, accessibility, and documentation-gap scenarios. Read
[evidence and attribution](references/evidence.md) for source-backed rationale,
source dates, limitations, and disputed secondary advice.

Return the requested artifact or review plus:

1. Question, chart choice, and why the encoding fits.
2. Source/cohort/window, transformations, denominator, and missingness.
3. Scale/legend/uncertainty decisions and accessible alternative.
4. Checks actually run, results, and untested/blocked surfaces.

Recompute representative values, reconcile totals, compare geometry to values,
and test the target renderer's existing accessibility/responsive checks. For a
review, report severity, location, evidence, and a concrete correction; do not
create replacement deliverables or publish changes unless authorized.
