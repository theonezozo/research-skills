# Public evidence and attribution

## Contents

- [Use of sources](#use-of-sources)
- [Source inventory](#source-inventory)
- [Interpretation limits](#interpretation-limits)
- [Reverification](#reverification)

## Use of sources

This package combines public information-design, accessibility and product
guidance with explicit methodological synthesis. It does not establish a
universally best chart or measured performance improvement. The public references
below were retained from a 2026-10-13 research snapshot, not freshly retrieved
during packaging. Verify current pages before extending attributed claims.

Use one claim-source pair as the evidence unit. Treat secondary summaries as
derivatives, not independent confirmation of the original author's views.
Do not treat failed access as proof a feature or recommendation does not exist.

## Source inventory

| Source | Supported use | Limits |
|---|---|---|
| [Edward Tufte](https://www.edwardtufte.com/) | Primary author overview of information-design topics, including small multiples. | A course overview is not direct access to every argument or an empirical validation. |
| [The Visual Display of Quantitative Information](https://www.edwardtufte.com/book/the-visual-display-of-quantitative-information/) | Publisher description of data-ink and graphical deception topics. | The full copyrighted book is not bundled or claimed as inspected here. |
| [Chartbuddy: Tufte's principles](https://chartbuddy.io/blog/tuftes-principles-for-graphical-integrity) | Secondary explanation of context, comparisons and the lie-factor concept. | Not the author's original text. Do not adopt a fixed numeric lie-factor tolerance or observational causality claim as a universal standard. |
| [GeeksforGeeks: Tufte's principles](https://www.geeksforgeeks.org/data-visualization/mastering-tuftes-data-visualization-principles/) | Secondary discussion of proportionality and reducing distracting decoration. | Some advice is overbroad; do not delete essential labels or demand zero for every position-based axis. |
| [Power BI dashboard design tips](https://learn.microsoft.com/en-us/power-bi/create-reports/service-dashboards-design-tips) | Public first-party guidance on audience, consistent scales/colors and avoiding decorative 3D. | Product-specific recommendations; one-screen guidance does not justify unreadable text. |
| [Power BI visualization overview](https://learn.microsoft.com/en-us/power-bi/visuals/power-bi-visualizations-overview) | Public chart-type definitions. | The package's selection table adds judgment, not a quoted vendor decision algorithm. |
| [Accessible Power BI reports](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-accessibility-creating-reports) | Public examples of alt text, tab order, non-color cues and accessible tables. | A custom renderer must implement and test its own equivalent behavior. |
| [W3C: Understanding contrast minimum](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html) | Text contrast thresholds and large-text definitions. | Explanatory guidance; applying one criterion is not whole-product conformance. |
| [W3C: Understanding non-text contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html) | Required control/state and graphical information against adjacent colors, with exceptions. | Not a requirement for every possible pair of palette colors to differ by 3:1. |

These are public citations, not dependencies on a vendor account, private
design system, product integration or proprietary source.

## Interpretation limits

- Require zero for bars and filled-area magnitude. Permit a disclosed nonzero
  position-based line/dot axis when it improves the intended task without
  misleading the reader.
- Keep necessary labels, focus indicators, uncertainty and accessible alternatives
  even when reducing decoration.
- Prefer aligned panels or explicitly indexed series to arbitrary dual axes.
  If a secondary axis is essential, identify both units/ranges and their series.
- Do not infer causation from a chart, temporal annotation or before/after pattern.
- Treat operational monitoring rules, missingness, ordinal handling, lie-factor
  edge cases and worked examples as synthesis, not quotations attributed to a
  single cited author.
- Match inferential claims to a defensible analysis plan. Report comparison
  families, adjusted and raw p-values, effect sizes and local valid-case counts;
  do not infer equivalence from nonsignificance.

## Reverification

Reopen relevant original pages when implementing changing product behavior.
Inspect the actual renderer for keyboard access, screen-reader meaning, text
and non-text contrast, data-table parity, responsive layout and theme behavior.
Report inaccessible documentation and checks not run. A static specification,
automated pass or public reference does not certify the resulting experience.
