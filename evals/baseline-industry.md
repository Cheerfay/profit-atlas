# Industry Skill — No-Skill Baseline

Tested in fresh contexts without access to the local Profit Atlas files on 2026-10-21.

## Observed strengths

- Correctly recognized a three-company “which company is most profitable” request as company comparison rather than industry research.
- Selected different business-model representatives for games and automotive.
- Distinguished revenue scale from net-profit quality in broad terms.
- When explicitly asked, classified AI as core, enhancement, or unnecessary.
- Avoided manufacturing extra opportunities merely to fill a list.

## Observed gaps

- The automotive answer used one current year rather than the requested three complete years and compared company-wide margins without a full comparability bridge.
- The game answer divided Tencent company-reported game revenue by a domestic industry-sales measure despite acknowledging that scopes differ; a directional caveat does not make the ratio comparable.
- Both industry answers compressed balance-sheet, working-capital, capital-intensity, and cash-conversion analysis.
- Opportunity sections named plausible products but did not consistently prove buyer, budget, external right-to-win, pre-scale data access, integration burden, incumbent replication risk, and defensibility.
- AI-role classification appeared only because the prompt explicitly demanded it; general opportunity analysis needs a stable rule that does not assume AI.

## Skill requirements derived from the baseline

- Enforce three-year audited scope unless the user changes it.
- Forbid ratios across mismatched company and industry accounting scopes, not merely label them directional.
- Require profit-pool comparison to include capital intensity, cash conversion, cyclicality, and control points where material.
- Make external right-to-win and data/workflow access mandatory before recommending an opportunity.
- Treat AI as one possible solution advantage and state when it is unnecessary.

## Post-skill verification

The same three prompts were rerun after applying the canonical skill:

- The game answer stopped calculating a company/industry ratio across incompatible scopes and explicitly separated industry sales, company revenue, and undisclosed game profit.
- The automotive answer used 2023–2025, stated that no automotive module exists, avoided an aggregate industry margin, and classified AI separately from each opportunity's non-AI moat.
- The named-company comparison routed to `company-value-chain-review` and explained why the request was company-first.
- Opportunity outputs identified payer, external right-to-win, data access, incumbent bundling risk, and conditions under which the opportunity should be rejected.

Result: the observed baseline gaps are addressed without adding an automotive-specific module.

