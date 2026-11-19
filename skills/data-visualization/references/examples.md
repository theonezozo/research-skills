# Worked examples and review checks

All data in this file are **synthetic demonstrations**, not customer findings.
Examples are skill synthesis; attribution and limits are in the evidence reference.

Contents: [baselines](#bars-versus-lines-the-baseline-is-encoding-dependent),
[area](#proportional-area), [Likert](#diverging-likert-without-hiding-neutral-or-missing),
[monitoring](#monitoring-rank-is-not-incident-severity),
[accessibility](#dark-theme-and-interaction-audit),
[documentation gap](#library-documentation-unavailable),
[acceptance](#acceptance-checklist-for-a-real-deliverable).

## Bars versus lines: the baseline is encoding-dependent

**Input:** completed tasks in two periods: 100 and 110.

- **Bad:** bars start at 90, leaving visible lengths 10 and 20 and suggesting a
  doubling.
- **Better:** bars start at zero, lengths 100 and 110. Label the change as 10
  tasks, or 10% relative to 100.
- **Audit:** graphic relative effect `(20-10)/10 = 1`; data relative effect
  `(110-100)/100 = 0.1`; lie factor `1/0.1 = 10`. Corrected zero-based bars
  yield `0.1/0.1 = 1`.
- **Contrast case:** a daily latency line between 100 and 110 ms may use a
  disclosed 95–115 ms domain to show variation. Label axis/ticks and absolute
  values; do not call that line a tenfold increase or demand every axis start
  at zero. Keep comparable service panels on the same domain.
- **Edge case:** 100 → 100 has zero change, so the lie-factor ratio divides by
  zero. Check equal marks and exact mapping; do not report LF = 0 or infinity.
  For 0 → 10, report +10, not a relative percent increase from zero.

## Proportional area

**Input:** two values 25 and 100.

- **Bad:** bubble radii 5 and 20. Areas differ by 16× although values differ 4×.
- **Better:** radii 5 and 10; areas differ 4×. Supply a size key and exact values.
- **Check:** doubling radius quadruples area. Use bars/dots instead if readers
  need precise comparisons, or if overlapping bubbles conceal small values.

## Diverging Likert without hiding neutral or missing

**Input:** 22 eligible people; 20 answered one five-category ordinal item.
Counts from strongly disagree to strongly agree: `[2, 3, 5, 6, 4]`; two missing.

- **Bad:** mean score alone; four-color bars drop the five neutral answers; or
  percentages silently use 22 although labeled "among respondents."
- **Better:** show `[10%, 15%, 25%, 30%, 20%]` of valid responses with `n=20`;
  disclose `2 of 22 missing`. Preserve the five ordered labels and counts.
- **Diverging options:** place the neutral segment in an explicitly labeled
  center, or on a consistently disclosed non-endorsement side. If split around
  a centerline for layout, keep it one 25% neutral category, not two categories.
  A split neutral rectangle is geometry, not fractional respondents.
- **Check:** counts sum to 20 and exact shares sum to 100%; positive share is
  `10/20 = 50%`, negative `5/20 = 25%`, neutral `5/20 = 25%`. Color is not
  evidence of endorsement; labels/order and the table carry the same meaning.
- **Host precedence:** preserve an existing report's explicitly documented
  neutral placement and color grammar when those remain truthful and accessible.

## Monitoring: rank is not incident severity

**Input:** service A has 2 errors from 100 requests (2%); B has 10 errors from
1,000 requests (1%). A configured error-rate threshold is 1.5%.

- **Bad:** percentile heatmap paints B most alarming because its error count is
  highest; a green average hides A's breach.
- **Better:** show rates beside counts and exposure, threshold 1.5%, the
  measurement window, freshness, and recent history. A breaches this synthetic
  threshold; B does not. Do not infer business impact from this threshold alone.
- **Check:** distinguish absolute threshold states from relative rank; label
  status and add an icon/pattern. Preserve sustained breach duration if the
  actual alert policy specifies one; do not invent an SLO.
- **Missing:** an unreported interval is a gap/unknown, not zero errors. Disclose
  aggregation and sampling; a daily average may hide a short spike.

## Dark theme and interaction audit

**Input:** two line series differ only in red/green; pale legend text is
unreadable on the dark surface; all values are hover-only.

- **Better:** choose verified theme-aware semantic styles, distinct line
  patterns/markers plus direct labels, readable text, and contrasting required
  marks. Supply keyboard/focus/tap inspection and a structured value table.
- **Check:** measure actual rendered text/background and mark/adjacent-color
  ratios in each theme. Normal-size text at 4.49:1 fails 4.5:1; 4.50:1 passes.
  Measure required non-text features against adjacent colors, not every possible
  palette pair. Verify overlays, selection, focus, and forced-color states too.
- **Check:** keyboard users can reach filters, inspect equivalent values, change
  series visibility, reach the table, and leave the chart without a trap.
  Screen readers receive names, units, filter state, and updated descriptions.
  Do not claim these checks passed without exercising the actual renderer.

## Library documentation unavailable

**Input:** a request for a chart using a project's component library, but the
installed version's documentation cannot be accessed.

- **Bad:** invent a chart export, palette prop or token and call it verified.
- **Better:** specify chart type, encodings, data contract, semantic styling
  roles, responsive behavior and accessibility expectations. State which API
  details remain unverified. Do not change sign-in or install a dependency merely
  to finish a specification.
- **Check:** no undocumented component code and no claim that another library
  automatically meets this application's theme or version requirements.

## Acceptance checklist for a real deliverable

- Reconcile every displayed chart total to the filtered source; expose local n.
- Check representative minimum, maximum, zero, negative, missing, and boundary
  values; ensure sort/filter operations preserve category identities and totals.
- Confirm bar zero baseline, legitimate line-axis disclosure, comparable panel
  domains, area proportionality, and annotated transformations.
- Confirm full ordinal distribution and neutral/missing handling; separate
  observed differences, uncertainty, hypotheses, and causal evidence.
- Test all required contrast pairs, keyboard paths, screen-reader descriptions,
  and data alternatives in supported themes and narrow/wide layouts.
- Check visible labels, tooltips, accessible names/table, and exported/print
  values agree after rounding and filtering.
- Report each check as passed, failed, blocked, or not run. Document synthetic
  examples as examples, not evidence that an implementation is accessible.
