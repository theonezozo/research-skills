# FigJam Drafting

## Method foundation

The drafting model follows three complementary public guides:

- [Figma, "What is a user journey map?"](https://www.figma.com/resource-library/user-journey-map/)
  distinguishes product-focused user journeys from broader customer lifecycles, separates
  current-state from future-state maps, and recommends personas/goals, touchpoints, phases,
  actions/responses, research, and iterative validation.
- [Nielsen Norman Group, "Journey Mapping 101"](https://www.nngroup.com/articles/journey-mapping-101/)
  defines a journey map around one actor and one scenario, with scenario-derived phases, actions,
  mindsets, emotions, and opportunities.
- [Harvard Business School Online, "How to Create a Customer Journey Map"](https://online.hbs.edu/blog/post/customer-journey-map)
  emphasizes touchpoints, motivations, explicit and latent pains, stage metrics, cross-functional
  business use, research grounding, and ongoing maintenance.

Together, these sources converge on a research-grounded actor/persona, scenario/objective,
phases, actions/touchpoints, thoughts/emotions, pains, and opportunities. Apply the stricter
evidence rules in this skill: label synthesis, never infer emotion as observation, preserve
contradictions, and expose future-state uncertainty.

## Choose the delivery branch

### Write-capable FigJam/Figma tool

Require explicit approval for the exact content and target board before writing.
Tool availability or a request for a build packet is not write authorization.
Do not install integrations, change sign-in or broaden sharing merely to finish.

1. Inspect the target file, page, sections, template, permissions, and existing map before writing.
2. Create or reuse five sections: scope/legend, main journey, evidence ledger,
   assumptions/contradictions/gaps, and opportunities/validation plan.
3. Batch-create phase headers, row labels, cards/stickies, evidence IDs, emotion points, and links.
4. Apply the layout and accessibility rules below.
5. Re-read or inspect the created objects. Verify text, phase order, section placement, links, and
   visibility; correct any truncation or overlap.
6. Return the actual board URL and a brief description of what was created.

Prefer batched writes over one-object-at-a-time calls. Never claim success from tool acceptance
alone; verify the resulting board.

### Authorized browser-only path

Use browser interaction only when it is available and authorized for the target board. Follow the
same section structure, batching where the interface permits. Visually verify the final content
and return the actual URL.

### No write path

Do not fabricate a board, URL, file key, or creation claim. Produce the complete build packet
below so a collaborator can assemble the board without reinterpreting the research.

## Board layout

- Use five sections in this order:
  1. Scope and legend
  2. Main journey
  3. Evidence ledger
  4. Assumptions, contradictions, and gaps
  5. Opportunities and validation plan
- Use phase columns approximately 260-320 px wide.
- Keep fixed row labels at the left of the main matrix.
- Keep 3-5 concise items per cell; move detail to evidence cards.
- Show evidence IDs directly on each claim card.
- Plot an emotion line only where evidence exists; leave unknown points blank and label the gap.
- Make current and future states visually distinct. In hybrid maps, never blend an observation and
  a hypothesis on one card.
- Use labels, icons, borders, or patterns in addition to color. Maintain readable contrast and
  logical reading order.

## Visual legend

Use these semantic labels regardless of color:

- `[E]` evidence-backed observation
- `[I]` synthesized interpretation
- `[A]` assumption/future-state hypothesis
- `[G]` gap
- `[C]` contradiction
- `MOT` moment of truth

Suggested colors may be adapted to the board palette: evidence blue, interpretation violet,
assumption yellow, gap gray, contradiction red outline, opportunity green. Never rely on color
alone.

## FigJam-ready build packet

Output every section in this order:

### 1. Map metadata

Provide the complete metadata record from the schema, including version, research cutoff, and
validation checkpoint.

### 2. Main journey matrix

Use one table with phase columns and these rows: goals, actions, touchpoints, thoughts, emotions,
pains, needs, opportunities, and evidence/confidence. Prefix every item with its claim label and
append evidence IDs where applicable.

### 3. Ordered sticky manifest

Provide a table with:

`Order | Object ID | Section | Phase | Row | Claim label | Sticky text | Evidence IDs | Style`

Order objects by section, then phase left-to-right, then row top-to-bottom. Keep sticky text short
enough to paste directly.

### 4. Emotion points

Provide:

`Phase | Score/position | Stated emotion | Evidence ID | Confidence | Gap note`

Use a documented scale only if supported. Leave unsupported phases blank rather than interpolating.

### 5. Evidence ledger

Provide every field from the evidence-record schema, using privacy-safe excerpts or paraphrases
and working source links where sharing policy permits.

### 6. Assumptions, contradictions, and gaps

For each `A`, provide validation question, method, owner if known, and priority. For each
contradiction, show competing evidence IDs and the unresolved context. For each `G`, show impact
and the next research action.

### 7. Pain-to-opportunity links

Provide:

`Pain/need ID | Opportunity | Evidence IDs | Intended outcome | Candidate metric | Confidence`

Do not include unlinked solution ideas in the opportunity section.

### 8. Visual legend

List claim labels, border/icon treatment, state treatment, and accessible color suggestions.

### 9. Manual assembly steps

1. Create the five sections.
2. Build the matrix using fixed row labels and one 260-320 px column per phase.
3. Paste stickies in manifest order.
4. Add evidence IDs and connect cards to ledger entries.
5. Plot only evidenced emotion points and connect them in phase order.
6. Add contradiction, gap and assumption cards with validation actions. Do not
   connect emotion points across unsupported phases as if the missing values
   had been observed; show and label gaps in the line.
7. Link pains/needs to opportunities and metrics.
8. Check contrast, non-color labels, spacing, phase order, and current/future separation.
9. Review privacy and sharing permissions before publishing.
10. Stamp the version, research cutoff, owner, and next validation checkpoint.
