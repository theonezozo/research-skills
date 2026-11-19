---
name: jtbd-definition-creator
description: Identifies and writes Jobs to Be Done statements from research evidence using "When [situation], I want to [motivation], so I can [expected outcome]." Use to analyze transcripts, survey open text or supplied notes, extract per-participant jobs, build a consolidated summary and cluster cross-participant themes while preserving evidence and uncertainty.
---

# JTBD Definition Creator

Read authorized research data and extract the **Jobs to Be Done (JTBD)** each
participant expresses in a consistent, evidence-grounded format. Apply the
method to the supplied domain without assuming a particular product or workflow.

## The JTBD formula

> **When [situation], I want to [motivation], so I can [expected outcome].**

- **When [situation]** — the context or trigger in which the job arises.
- **I want to [motivation]** — the task or goal the participant is trying to accomplish.
- **So I can [expected outcome]** — the result or benefit they expect.

Example: *When I am commuting to work, I want to listen to my favorite podcasts, so I can stay informed and entertained during my journey.*

Read [the JTBD guide](references/jtbd-guide.md) for hypothetical examples,
good-versus-weak patterns, quality checks and the output template.

## Workflow

### Step 1 — Identify the input source
Use supplied notes, transcripts, survey open text or explicitly authorized
research-system records. Confirm source scope when ambiguous. Search only within
that scope; do not assume repository folders, a vendor integration or access to
other studies. Search summaries locate evidence but do not replace reading it.
Keep a source inventory and trace derivatives to originals.

If the participant set or scope is unclear, ask one targeted question before proceeding.

### Step 2 — Extract jobs per participant
For each participant:
1. Read their content and find moments where they describe a need, goal, frustration, workaround, or desired outcome.
2. For each distinct job, fill the three slots (situation / motivation / outcome) from what they actually said. Do **not** invent slots that are unsupported.
3. If the data supports the motivation but not the situation or outcome, write the parts you can and mark the missing slot as `[not stated]` rather than fabricating it.
4. Capture a source reference and brief evidence excerpt only when approved for
   the intended audience. Otherwise provide a privacy-reviewed paraphrase, label
   it as such, and keep restricted provenance in authorized storage. Never turn
   a paraphrase into a quotation.

Keep statements outcome-focused and solution-agnostic — describe the job, not a specific feature or tool.

### Step 3 — Build the consolidated summary table
Compile every JTBD across participants into one table with columns:
`Participant code | Situation | Motivation | Expected outcome | Evidence reference / approved excerpt or paraphrase`

### Step 4 — Cluster into cross-participant themes
Group related jobs into as many themes as the evidence supports; do not force
a fixed count. For each theme give a short name, participant codes, a one-line
synthesis and, where useful, a representative rolled-up job. Preserve minority
and contradictory jobs. Count unique participants or purchasing units using a
declared denominator, not mentions, duplicate notes or repeated interviews.

### Step 5 — Output
Produce, in this order:
1. **Per-participant detail** — job statements with evidence references and approved excerpts or labeled paraphrases.
2. **Consolidated summary table** (Step 3).
3. **Cross-participant themes** (Step 4).

Follow the template in `references/jtbd-guide.md`. Note any participants for whom no clear JTBD could be derived.

## Rules
- Ground every JTBD in the data; never fabricate situations, motivations, or outcomes. Mark gaps as `[not stated]`.
- Preserve the participant's own framing and language where possible.
- Keep jobs solution-agnostic (the job, not the feature).
- Minimize data; review direct and indirect identifiers, company confidentiality,
  rare role/context combinations, source links and metadata before sharing.
  Participant codes are pseudonyms, not guaranteed anonymization. Verify consent,
  access and retention for each destination. Do not publish raw transcripts or
  assume quotation permission from research-participation consent.
- Use only necessary safe attribution. No companion skill or vendor tool is
  required; the source evidence, not the output template, determines the job.
