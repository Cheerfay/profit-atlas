# Company Skill — No-Skill Baseline

Tested in fresh contexts without access to the local Profit Atlas files on 2026-10-21.

## Observed strengths

- Refused to infer segment profit from segment revenue alone.
- Located an insurance claims-automation project in the operating workflow and treated revenue impact as indirect without evidence.
- Distinguished underwriting income, investment income, operating cost, risk, and customer experience at a high level.

## Observed gaps

- The direct BYD answer interpreted “two layers” as a customer value chain followed by an enterprise value chain, rather than the intended Layer 1 company-economics table plus Layer 2 value-to-cash workflow.
- The BYD answer made company-specific economic claims without labeling disclosed, calculated, and inferred statements or providing a minimum financial spine.
- It did not produce the required decision-point table for revenue, cost, risk, and trust/experience.
- It compressed profit-source evidence into a narrative and could leave the reader unable to distinguish strategic importance from disclosed profit contribution.
- Without a named insurer, the project answer appropriately stayed generic, but a stable skill should state what company-specific evidence is missing before applying company-level conclusions.

## Skill requirements derived from the baseline

- Define Layer 1 and Layer 2 structurally so “two layers” cannot be reinterpreted.
- Require the Layer 1 table, one-sentence essence, Layer 2 arrow chain, and decision-point table.
- Keep the financial spine minimal but evidence-labeled.
- Preserve the refusal to rank undisclosed segment profits.
- Keep project impact conditional on an explicit mechanism and scale linkage.

## Post-skill verification

The same three boundary cases were rerun in fresh contexts with the canonical skill supplied.

- **Direct BYD request:** returned the required Layer 1 company-economics table, one-sentence essence, a single Layer 2 value-to-cash chain, and the revenue/cost/risk/experience decision table. It no longer reinterpreted the two layers as separate customer and internal value chains.
- **Insurance claims project:** first established how an insurer lives and the main operating chain, then located claims automation between reporting and payment. It treated revenue effects as indirect and made company-level importance conditional on coverage, straight-through processing, unit cost, leakage, rejection error, complaints, and renewal evidence.
- **Undisclosed segment profit:** refused to rank segment profit from revenue-only disclosures, separated strategic importance from proven profit contribution, and stated which additional segment cost, margin, or profit evidence would be needed.

Result: the canonical skill fixes the structural failures while preserving the baseline model's useful evidence restraint.

