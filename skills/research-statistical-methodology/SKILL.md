---
name: research-statistical-methodology
description: Apply consistent statistical standards to UX research and survey analysis, including ordinal Likert interpretation, uncertainty, small-sample reporting, missing data, multiple comparisons, effect sizes, composite scales, and computational provenance. Use when choosing, reviewing, or describing quantitative methods, verifying a reported statistic, or reconciling conflicting research numbers.
---

# Research Statistical Methodology

## Separate the analysis layers

Treat these as distinct steps:

1. **Acquire** source data without changing its meaning.
2. **Decode** source codes against the authoritative schema or label map.
3. **Normalize** types, missing values, direction, and analysis-ready fields
   while retaining the decoded labels and an audit trail.
4. **Interpret** only after the first three steps are validated.

Never infer statistical meaning from storage codes. A numeric recode can be a
category identifier, an ordered response, or a continuous measurement.
Semantic display order is not a scoring rule: placing an uncertainty category
such as "Not sure" between negative and positive responses does not make it an
ordinal midpoint. Keep such categories distinct from substantive ordered ratings.

## Trace a statistic before reusing it

1. Open the cited source and identify the exact measure, numerator/denominator,
   cohort, time window, and computation. Distinguish odds ratios from risk ratios,
   rates from volumes, and matched pairs from repeated cross-sectional samples.
2. Locate the variable or formula in the authorized computational layer
   (query, script, instrument, or derived data). Repeated prose and a plausible
   citation are not independent verification.
3. If the number is missing or disputed, search the relevant source history with
   `git log -S "measure-token" -- <source-path>` and inspect the introducing change.
   A prose-only introduction is a fabrication risk, not proof by itself.
4. Reproduce from available source data using the stated exclusions and rounding.
   If data or access is unavailable, mark the statistic unverified; do not treat
   missing evidence as a zero or invent a replacement.
5. When correction is authorized, reconcile every occurrence in the publication
   set, including headings, tables, charts, summaries, and generated metadata.
   Preserve dated superseded findings as history rather than presenting them as
   current evidence.

Keep raw participant/account keys in approved access-controlled storage with
appropriate retention and consent. Version-control ignore rules are a useful
additional check, not an access-control or privacy guarantee. Review small cells,
indirect identifiers, confidential business information and source links before
sharing aggregates. Arithmetic agreement alone does not validate the underlying
measure, quoted wording, or event date.

## Ordinal Likert items

For an individual Likert item:

- Lead with counts and the full response distribution.
- Report the median and interquartile range when the labels define a defensible
  order; state the per-item denominator.
- Use prespecified top-/bottom-box summaries only with the numerator,
  denominator, box definition, and uncertainty. Prefer Wilson confidence
  intervals for binomial box proportions.
- Use ordinal or distribution-sensitive comparisons when inference is
  justified. Report effect size and uncertainty, not only a p-value.
- Do not report means, standard deviations, or parametric mean-difference tests
  as the default interpretation of an individual ordinal item.

Small samples require counts beside percentages and directional language.
Display the full distribution because box scores and medians can hide
polarization.

## Composite-scale exception

A mean or sum may be used for a multi-item composite only when all of the
following hold:

1. The construct and scoring rule were specified before inspecting outcomes.
2. Items measure the same construct and are coded in a common direction.
3. Missing-item handling and any minimum answered-item threshold are explicit.
4. Reliability or dimensionality is checked and reported.
5. Item-level distributions remain available, and an ordinal-safe sensitivity
   analysis does not materially change the conclusion.

Call the result a **composite scale**, not a single Likert item. Document each
exception rather than silently applying equal-interval assumptions.

## Derived-statistic provenance

Apply [Trace a statistic before reusing it](#trace-a-statistic-before-reusing-it)
to derived claims as well as quoted ones. Verify grouping/cutoff rationale,
transformations, effect-size definitions and test inputs; never retain a p-value
from a different analysis. Investigate contradictions before interpretation.
Unsupported claims are omitted as quantitative support; absence alone does not
prove fabrication. Use history searches for disputed provenance, not as a
mandatory step for every analysis.

## General reporting contract

- Define the cohort, denominator, exclusions, deduplication rule, and
  attribution window.
- Reconcile joined records to source totals and report unmatched populations.
- Distinguish descriptive differences from inferential results and avoid causal
  language without a causal design.
- Report uncertainty and practical effect size. Correct or clearly label
  exploratory multiple comparisons.
- Preserve raw/source exports and immutable snapshots; make transformations
  reproducible in derived outputs.

## Report-wide chart comparisons

- Declare the inferential family across the report, not only within each chart
  or a favorable subset. Include every comparison supporting the family-level
  claim, and state its size. Label post-hoc exploration explicitly.
- For a family of charted association tests, use Holm-adjusted p-values for
  significance; retain raw p-values and the test method for provenance. Report
  cell counts, denominators, effect sizes and uncertainty where estimable.
- Separate full-cohort answered n from pair-complete tested n. Report missing
  outcomes and factor/category exclusions, reconcile these bases, and explain
  how unknown values enter or stay outside the test.
- Describe nonsignificance as insufficient evidence, not proof of no
  relationship or equivalence; discuss effect uncertainty and sample limits.

Record each report's actual field definitions and comparison family in its
analysis plan; never treat an example schema as universal.

## Minimal analysis handoff

Return the decision, source/version, population and independent unit, acquisition
channel, measurement window, valid-case rules, numerator/denominator, missingness,
estimates/effect sizes, uncertainty method and level, comparison family/correction,
sampling limits and reproducible transformation steps. Count repeated observations
as dependent when they belong to the same person or purchasing unit.

For example, if 20 of 24 eligible people answer one item and 12 select the
prespecified favorable categories, report 12/20 valid answers and 4/24 missing,
not 12/24 favorable without qualification. This example is synthetic; it does not
establish a sample-size requirement or validated benchmark.
