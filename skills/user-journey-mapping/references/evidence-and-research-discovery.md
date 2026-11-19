# Evidence and Research Discovery

Discover research adaptively. Repository paths differ; treat folder names as heuristics, not
requirements.

## Discovery sequence

1. **Read indexes first.** Inspect root and relevant directory READMEs, research indexes,
   catalogs, profile tables, study summaries, and link collections to learn the local taxonomy.
2. **Search names and concepts.** Search filenames, then content for the actor, company/segment,
   scenario, goal, journey terms, channels, and known products.
3. **Retrieve actual evidence.** Open the referenced profiles, reports, transcripts, surveys,
   notes, GitHub issues/comments, and Marvin records rather than relying on search snippets.
4. **Build an inventory and lineage map.** Classify each candidate source before extracting
   claims. Mark derivatives and their underlying evidence.

Likely repository locations include directories named `research`, `customers`, `profiles`,
`reports`, `interviews`, `transcripts`, `surveys`, `notes`, or `insights`, but never assume this
layout universally.

## Source priority

Use this order:

1. **Direct evidence:** participant statements, observations, survey responses, support records,
   behavioral/operational metrics, and original GitHub issue/comment testimony.
2. **Structured derivatives:** profiles, coded observations, or summaries that retain source
   links and participant-level evidence.
3. **Cross-source syntheses:** reports and thematic analyses with traceable inputs.
4. **Discovery-only artifacts:** indexes, READMEs, decks, search snippets, and uncited summaries.

Use discovery-only artifacts to locate evidence, not to substantiate a claim. Prefer the closest
available source to the observed behavior. A derivative may clarify context but must retain
lineage to the underlying source.

## Efficient retrieval

- Inventory metadata before loading full content.
- For large transcripts, surveys, or Marvin projects, retrieve summaries first to triage and
  fetch full content only for relevant sources.
- For Marvin, list projects/files, read file or insight summaries, then retrieve full transcript,
  survey response, note, or nested insight content only as needed.
- For GitHub, search issues and comments by actor/company, scenario, product, and journey terms.
  Read the full issue and relevant comment thread; preserve distinct commenters and dates.
- Record inaccessible or missing sources as `G`, including likely impact.
- Respect access controls; do not copy restricted evidence into a broader publication surface.

## Inventory and lineage

Assign source IDs such as `SRC-001`. Record title, type, date, actor/cohort, direct/derivative
status, access class, location, parent sources, and relevance.

Build lineage before prevalence counts. Examples:

- transcript -> profile -> cross-customer report
- survey response -> survey analysis -> executive summary
- issue comment -> customer issue -> pipeline tracker

Treat each chain as one underlying observation unless independent evidence exists. Keep both a
derived claim and its source only when the derivative adds analysis; never count them twice.
Deduplicate account families and repeated interviews according to the requested unit of analysis.

## Atomic extraction

Create one evidence record per action, touchpoint, thought, stated emotion, pain, need, goal,
motivation, metric, or transition. Preserve:

- the actor and scenario context
- phase or tentative sequence
- source date and access class
- faithful wording or privacy-safe paraphrase
- confidence and lineage parent
- minority and contradictory evidence

Do not combine multiple claims into one excerpt. Do not fill missing context by intuition. Mark it
as `G`, or use `A` with a validation plan when a working hypothesis is needed.

## Normalization and synthesis

1. Normalize synonymous labels without erasing the participant's wording.
2. Collapse exact/rephrased duplicates through lineage.
3. Separate distinct actors, scenarios, cohorts, and time periods.
4. Preserve contradictions and test whether channel, role, maturity, geography, or date explains
   them.
5. Derive phases from sequence changes, goals, handoffs, decisions, or channel transitions.
6. Populate evidence-backed rows before interpreting patterns.
7. Report prevalence by unique customer/company unless another denominator is specified.

For every quantitative statement, retain numerator, denominator, date/window, exclusions,
deduplication method, and caveat. Do not use repeated mentions as a proxy for prevalence.

## Privacy gate

Review excerpts, attributions, filenames, source references, board metadata,
hidden details and URLs before any tracked or shared output. Verify the exact
audience, consent/purpose and access controls. Treat shared boards as publication
surfaces. Use minimal permitted attribution; omit direct identifiers and
confidential details, and paraphrase when necessary. Check reidentification from
role, employer, unusual events and linked sources. A pseudonym, initials or
company-only attribution is not guaranteed anonymous. Do not copy raw linking
keys, credentials, contacts or participant rosters into the map.
