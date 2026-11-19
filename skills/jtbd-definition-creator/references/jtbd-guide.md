# JTBD Guide — Examples, Patterns, Quality Checks, and Output Template

## Contents
- [Hypothetical JTBD examples](#hypothetical-jtbd-examples)
- [Good vs. weak JTBD patterns](#good-vs-weak-jtbd-patterns)
- [Quality checklist](#quality-checklist)
- [Output template](#output-template)

## Hypothetical JTBD examples

These are invented demonstrations, not participant statements or customer
findings. Adapt to actual evidence; do not cite them as research.

- When a production incident is paging me at 2am, I want to quickly understand what changed and why, so I can mitigate impact before it spreads.
- When I'm triaging a noisy alert, I want to know whether it's a real customer-facing problem, so I can decide whether to escalate or suppress it.
- When I onboard onto an unfamiliar service, I want to see its dependencies and recent failure modes, so I can be effective on-call without weeks of ramp-up.
- When I'm reviewing an agent's proposed remediation, I want to see its reasoning and the actions it will take, so I can trust it enough to approve or let it run.
- When a postmortem is due, I want the timeline and contributing factors assembled automatically, so I can focus on prevention instead of evidence-gathering.

## Good vs. weak JTBD patterns

| Weak | Why it's weak | Stronger |
|------|---------------|----------|
| "I want a dashboard for alerts." | Solution, not job; no situation or outcome. | "When alerts spike during a deploy, I want to see which are caused by my change, so I can roll back fast." |
| "When I work, I want things to be easier." | Situation and outcome too vague to act on. | "When I'm handing off on-call, I want a clear summary of open issues, so the next engineer isn't caught off guard." |
| "I want the agent to fix everything automatically." | Outcome is a fantasy, not grounded in stated need. | "When the agent proposes a fix, I want to review its plan first, so I can stay accountable for production changes." |

Principles:
- **Solution-agnostic**: describe the job, not a feature.
- **Grounded**: every slot traces to something the participant said.
- **Specific situation**: a real trigger, not "when I work."
- **Meaningful outcome**: the benefit, not a restated motivation.

## Quality checklist
Before finalizing, verify each JTBD:
- [ ] Follows "When [situation], I want to [motivation], so I can [expected outcome]."
- [ ] Each slot is supported by the data (or marked `[not stated]`).
- [ ] Is solution-agnostic (no specific feature/tool baked in).
- [ ] Has a source reference and audience-approved excerpt or labeled faithful paraphrase.
- [ ] Situation is a concrete trigger; outcome is a real benefit (not a paraphrase of the motivation).

## Output template

```markdown
# Jobs to Be Done: [Study / Source name]

_Source(s): [audience-safe evidence references] · [N] unique participants_

## Per-participant JTBDs

### [Participant code P1; include role/context only if safe and necessary]
1. When [situation], I want to [motivation], so I can [expected outcome].
   - _Evidence:_ [source reference; approved excerpt or labeled paraphrase]
2. When [situation], I want to [motivation], so I can [expected outcome].
   - _Evidence:_ [source reference; approved excerpt or labeled paraphrase]

### [Participant code P2]
1. When [situation], I want to [motivation], so I can [expected outcome].
   - _Evidence:_ [source reference; approved excerpt or labeled paraphrase]

_(Note any participant with no clear JTBD and why.)_

## Consolidated summary

| Participant | Situation | Motivation | Expected outcome | Evidence reference / approved excerpt or paraphrase |
|-------------|-----------|------------|------------------|----------------|
| P1 | ... | ... | ... | [reference and excerpt/paraphrase] |
| P2 | ... | ... | ... | [reference and excerpt/paraphrase] |

## Cross-participant themes

### Theme 1 — [short name]
- **Participants:** P1, P3, P5
- **Synthesis:** [one-line description of the shared job]
- **Rolled-up JTBD:** When [situation], I want to [motivation], so I can [expected outcome].

### Theme 2 — [short name]
- **Participants:** P2, P4
- **Synthesis:** ...
- **Rolled-up JTBD:** ...
```
