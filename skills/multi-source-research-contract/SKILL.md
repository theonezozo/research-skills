---
name: multi-source-research-contract
description: Establish a reproducible contract and evidence matrix before joining or synthesizing evidence across two or more independent sources or datasets. Use only for multi-source research joins, reconciliations, or cross-source synthesis; do not trigger for analysis contained within one source.
---

# Multi-Source Research Contract

Do not retrieve, join, or synthesize multi-source evidence until the analysis
contract is explicit. Keep unknowns visible rather than inventing a bridge
between sources.

## Define the analysis contract

Record:

1. **Question or decision** the analysis will inform.
2. **Unit of analysis** used for every result.
3. **Identity resolution and deduplication** rules, including account-family
   handling and the safe join key.
4. **Source totals and reconciliation** expectations, including how unmatched
   records will be counted and reported.
5. **Time or attribution window** and the event date used for inclusion.
6. **Exclusions and missingness** rules.
7. **Claim strength** permitted by the design: descriptive, associative, or
   causal.
8. **Evidence gaps** that could change or limit the conclusion.

If any field is undecided, mark it unresolved and constrain the planned claim.
Obtain separately authorized access to each source; a synthesis request does
not authorize exporting, linking or publishing restricted records.

Define identity resolution from authorized evidence, never name similarity
alone. Document join cardinality and duplicate-key handling before a join.
Keep linking keys in approved restricted storage; export only necessary
audience-safe evidence. Pseudonyms, truncated IDs and company names can still
identify people or reveal confidential business information. Review quotations,
links, hidden metadata and indirect identifiers before any sharing.

Keep unknown, refusal, not applicable and zero separate. Show counts and full
distributions for individual ordinal items; do not assume storage codes imply
equal intervals. State uncertainty and sampling limits. Prespecify comparison
families and corrections when making inferential claims. Association or agreement
between sources does not establish causation. No companion skill is required.

## Build the evidence matrix

Create the matrix before writing synthesis prose:

```yaml
- claim_or_finding:
  source_or_immutable_reference:
  safe_unit_or_account_key:
  population_and_denominator:
  date_or_window:
  evidence_or_measure:
  confidence_and_basis:
  contradictions_or_gaps:
```

Use one matrix entry per independently supported claim-source pair. Do not treat
repeated prose derived from the same evidence as independent corroboration.

## Reconcile before synthesis

1. Reconcile each source independently: total input records = excluded records +
   duplicate records removed + retained unique records. Within retained units,
   report matched + unmatched, including missing-key cases. State whether totals
   refer to records or people/organizations; never mix the units.
2. Resolve material discrepancies or report them as evidence gaps.
3. Check the matrix for contradictory measures, populations, dates, and units.
4. Draft only claims supported at the contract's permitted strength.
5. Report denominators and gaps beside the conclusion they constrain.

If reconciliation fails, stop at a bounded findings report; do not present a
cross-source prevalence ranking or causal conclusion.

## Synthetic reconciliation check

Source A contains 12 records: 1 is excluded, 1 repeats a retained unit, and 10
unique units remain. Source B contains 9 unique units. Eight units match:
A has 8 matched + 2 unmatched; B has 8 matched + 1 unmatched. These are separate
source totals, not 17 independent people. A one-to-one inner join must have 8
rows. A larger result requires investigating duplicate keys or a deliberately
modeled many-to-many relationship before interpreting it.
