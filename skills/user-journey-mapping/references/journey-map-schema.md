# Journey Map Schema

Use this schema as the canonical intermediate model for either a FigJam board or a build packet.

## Map metadata

Record:

| Field | Requirement |
|---|---|
| Title and version | Stable map name plus version/date |
| Actor | Exactly one actor, role, or coherent segment |
| Scenario and goal | Exactly one sequenced situation and desired outcome |
| State | `current`, `future`, or `hybrid` |
| Boundary | Explicit start trigger and end condition |
| Scope | Product interaction or broader service/customer lifecycle |
| Research scope | Included sources, cohort, date window, and exclusions |
| Business objective | Optional decision, outcome, owner, and metrics |
| Research cutoff | Latest evidence date included |
| Access class | Intended audience and sharing constraints |
| Validation checkpoint | Next study, review, metric, or refresh date |

For a hybrid map, visibly separate current evidence from future hypotheses in every phase.

## Evidence record

Assign a stable ID such as `E-001` to each atomic record:

| Field | Rule |
|---|---|
| `id` | Unique and stable within the map |
| `source_id` | Stable source inventory ID |
| `source_type` | Interview, transcript, survey, analytics, note, profile, report, issue, comment, or other |
| `source_ref` | Privacy-safe file path, URL, issue/comment link, or citation |
| `source_date` | Source or observation date; mark unknown explicitly |
| `actor` | Actor/cohort represented |
| `phase` | Phase ID or `unassigned` during extraction |
| `claim_type` | Action, touchpoint, thought, emotion, pain, need, goal, motivation, metric, or transition |
| `content` | Minimal excerpt or faithful paraphrase |
| `confidence` | `high`, `medium`, or `low`, with a short reason |
| `access_class` | Sharing/privacy classification |
| `lineage_parent` | Underlying source ID when this record comes from a derivative |
| `contradicts` | IDs of conflicting records, if any |

Keep raw participant material in approved access-controlled storage with consent,
retention and withdrawal handling. Ignore rules alone do not secure a file.
Review identifiability and confidentiality before copying anything to a map,
ledger, tracked file or shared board. Keep restricted provenance separate when
its source links would disclose identities to the board audience.

## Claim labels

| Label | Meaning | Required support |
|---|---|---|
| `E` | Evidence-backed observation | One or more evidence IDs |
| `I` | Synthesized interpretation | Supporting evidence IDs and confidence |
| `A` | Assumption or future-state hypothesis | Validation question, method, and owner if known |
| `G` | Material evidence gap | Impact on the map and an action to close it |

Use `I`, not `E`, when combining observations into a pattern. Do not infer an emotion from an
action, tone, or pain point. Plot emotion only when a participant expresses it directly or a
valid measure captures it.

## Phase model

Create phases from actual transitions in the scoped scenario; use 4-7 only as
a readability starting point, never a fixed requirement. Each phase contains:

- phase ID, short name, entry trigger, and exit condition
- phase goal
- actions
- touchpoints and channels
- thoughts, questions, or motivations
- evidenced emotion, optionally with a scale and evidence ID
- pains and friction
- needs
- opportunities
- evidence IDs and confidence

Prefer concise phase names expressed from the actor's perspective. Generic lifecycle phases are
starting hypotheses only; replace them with evidence-derived transitions.

## Core matrix

Use phase columns and these fixed rows:

1. Goals
2. Actions
3. Touchpoints
4. Thoughts
5. Emotions
6. Pains
7. Needs
8. Opportunities
9. Evidence and confidence

Keep 3-5 concise items per cell. Put qualifications, excerpts, lineage, and longer context in the
evidence ledger rather than overloading the matrix.

## Synthesis objects

Record separately:

- **Moment of truth:** phase, decision/expectation at stake, evidence IDs, consequence.
- **Pain-to-opportunity link:** pain/need ID, opportunity, evidence support, intended outcome,
  candidate metric, owner if known, and confidence.
- **Contradiction:** competing evidence IDs, affected claim, plausible segmentation or context,
  and validation action. Do not resolve disagreement without evidence.
- **Quantitative claim:** numerator, denominator, unit, date/window, population, exclusions,
  deduplication rule, and caveat.
- **Gap/assumption:** affected phase, impact, validation question, method, owner, and priority.

## Confidence rubric

- **High:** multiple independent direct sources, or strong direct evidence plus a matching metric.
- **Medium:** one strong direct source or converging derivatives with verified lineage.
- **Low:** sparse, old, indirect, or conflicting evidence; show the limitation.

Confidence describes support, not importance. Preserve a low-frequency but high-impact pain.
