---
name: user-journey-mapping
description: Create evidence-grounded current- or future-state user and customer journey maps from authorized research. Use to map actions, touchpoints, thoughts, emotions, pain points, moments of truth and opportunities across a scenario, or prepare a board-ready build packet. Includes optional FigJam drafting guidance without requiring a vendor integration.
---

# User Journey Mapping

Create a traceable journey map for exactly one actor and one scenario. Ground the current state
in research, distinguish synthesis from observation, and publish to FigJam only through an
available authorized write path.

## Establish scope

Obtain or resolve these required inputs:

- actor or segment
- scenario and goal
- map state: `current`, `future`, or `hybrid`
- journey start and end boundaries
- product-only or broader service/lifecycle scope
- named research scope or permission to discover sources
- desired delivery: text matrix/build packet or an explicitly authorized shared board

Accept these optional inputs when available: persona/profile, cohort, known phases, research date
window, channels, template, business objective and metrics, constraints, audience, and
accessibility needs. If a missing input would materially change the map, ask one focused question.
Otherwise, state the chosen default in map metadata.

## Load guidance progressively

- Read [journey-map-schema.md](references/journey-map-schema.md) before extracting evidence or
  structuring a map.
- Read [evidence-and-research-discovery.md](references/evidence-and-research-discovery.md) when
  finding, retrieving, ranking, normalizing, or deduplicating research.
- Read [figjam-drafting.md](references/figjam-drafting.md) before drafting a board or producing a
  build packet.
- Read [quality-checklist.md](references/quality-checklist.md) before sharing any output.
- Review direct and indirect identifiers, confidential company information, small
  cohorts, excerpts, source links and hidden metadata before any shared output.
  Use audience-approved excerpts or labeled paraphrases, not raw transcripts.
  Codes and abbreviated names are not guaranteed anonymous. Keep raw linking
  keys in access-controlled storage with appropriate consent and retention.
  Treat a shared board as a publication surface. No companion skill is required.

## Preserve evidence semantics

Label every mapped claim:

- `E` — evidence-backed observation
- `I` — interpretation synthesized from one or more evidence records
- `A` — assumption requiring validation
- `G` — evidence gap that limits the map

Never present `I`, `A`, or `G` as observed fact. Never infer emotion as `E`; emotion requires
directly expressed or behaviorally measured evidence. Label unsupported future-state content as
a hypothesis (`A`). Preserve contradictory and minority evidence instead of averaging it away.

## Build the map

1. **Scope** one actor, one scenario, explicit boundaries, state, and product/lifecycle scope.
2. **Inventory** candidate sources and create a lineage map. Prefer direct evidence and trace
   derivatives to their underlying sources.
3. **Extract** atomic evidence records with stable IDs. Capture source, date, actor, phase,
   access class, excerpt or faithful paraphrase, confidence, and lineage parent.
4. **Gate evidence readiness before synthesis.** Validate unique stable IDs and `E`/`I`/`A`/`G`
   fields; observed emotion only from direct expression or measurement; complete quantitative
   population/numerator/denominator/window/exclusions/deduplication/caveat metadata; exact
   supported issue/comment citations; and join reconciliation with named unmatched populations.
   Check these fields directly in the evidence ledger and reconcile join
   cardinality/totals before synthesis. A structural check does not establish
   semantic support, privacy or permission.
5. **Normalize and deduplicate** repeated evidence, account families, and derivative summaries.
   Do not count a profile, report, and source transcript as three independent observations.
6. **Segment** evidence by actor/scenario and exclude adjacent actors or scenarios.
7. **Derive phases** from evidenced transitions in this scenario. Four to seven
   is a readability starting point, not an evidence requirement; do not force a
   generic funnel or invent transitions to fill a template.
8. **Populate `E` first** across goals, actions, touchpoints, thoughts, emotions, pains, and needs.
   Add `I`, `A`, and `G` only after the evidence layer is visible.
9. **Synthesize** moments of truth, friction, needs, and opportunities. Link every opportunity to
   a pain or need, and every interpretation to its evidence IDs.
10. **Draft** through the best available FigJam path described in the drafting reference.
11. **Review and validate** the complete map against the full quality checklist, record a version and research
    cutoff date, and define the next validation checkpoint.

For quantitative claims, include numerator, denominator, measurement date/window, deduplication
unit, and caveat. Count unique customers or companies when reporting prevalence unless another
unit is explicitly required.

## Deliver honestly

Only after explicit approval for the exact content and destination, if a
write-capable FigJam/Figma integration exists, inspect or create the target sections,
batch-create the structured content, verify placement and text, and return the real board URL.
If authorized browser interaction is the only write path, use it and verify the result.

If no write path exists, do not fabricate a URL or imply that a board was created. Produce the
complete FigJam-ready build packet specified in
[figjam-drafting.md](references/figjam-drafting.md), including the matrix, ordered sticky
manifest, emotion points, evidence ledger, assumptions, gaps, contradictions, pain-to-opportunity
links, visual legend, and manual assembly steps.
