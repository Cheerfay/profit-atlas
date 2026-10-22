# Profit Atlas benchmark v0.1

This is a small, author-run **process evaluation**, not a claim that Profit Atlas will always produce better research than an unscripted agent. It compares two fixed prompts in a fresh context without access to this repository against the published example made with the relevant Skill.

## Purpose and limits

- Run date: 2026-10-22.
- Sample: two prompts, one per Skill. This is too small for a statistical result.
- Baseline condition: a fresh agent context was told not to inspect this repository or use Profit Atlas. It had normal web-research capability.
- Skill condition: the corresponding public example in this repository.
- Environment: model/provider implementation, browsing results, and source availability can all change. This run is reproducible as an evaluation design and artifact set, not as an identical-output guarantee.
- Interpretation: the useful observed effect is tighter structure, source discipline, and explicit decision boundaries. The no-Skill outputs are often good; this evaluation does not credit the Skill with facts it did not uniquely discover.

## Prompts and artifacts

| Task | Exact prompt | No-Skill baseline | Skill-guided example |
| --- | --- | --- | --- |
| China NEV profit pools | Research China’s new-energy vehicle value-chain profit pools for 2023–2025. Select representative companies with different roles; explain where revenue and profit mainly accrue and why; then propose credible external startup entry points and classify AI in each as core capability, important enhancement, ordinary feature, or unnecessary. Clearly distinguish facts, calculations, and inference, and state data gaps. | [raw baseline](runs/2026-10-22/automotive-no-skill.md) | [automotive profit-pool case](../examples/industry/automotive-profit-pool-test-result-en.md) |
| CATL economics | Analyze what CATL fundamentally lives on and how value turns into revenue, profit, and cash. Use the latest three complete fiscal years, label disclosed/calculated/inferred claims, and keep group economics separate from pure power-battery economics. | [raw baseline](runs/2026-10-22/catl-no-skill.md) | [CATL value-chain review](../examples/company/catl-value-chain-review-en.md) |

The baseline files are preserved as raw outputs. Scoring is intentionally conservative and based only on visible artifacts.

## Rubric

Each dimension receives 0–2 points.

| Dimension | 0 | 1 | 2 |
| --- | --- | --- | --- |
| Value-chain coverage | No chain or economic roles | Roles/economics appear, but the transaction chain or decision points are incomplete | Roles, transactions, profit drivers, and decision points are explicitly mapped (or, for company work, both required layers are present) |
| Source traceability | Material claims lack a primary source or period | Sources/periods are partial or material evidence relies on mirrors/secondary sources | Material claims identify primary sources and periods, with links or pinpointable citations |
| Evidence labels | Facts, arithmetic, and inference are blended | Labels appear inconsistently | Disclosed/fact, calculated, and inferred claims are consistently separated with caveats |
| Calculation consistency | Scope/denominator mismatch or invalid arithmetic | Some calculations cannot be reconstructed or have an incomplete scope note | Arithmetic is reconstructible and relevant scope boundaries are stated |
| Conclusion credibility | Generic or unsupported | Useful, but missing key boundary, data gap, or entry test | Specific conclusion plus limits, data gaps, and a testable decision/entry boundary |

## Results

| Task | Condition | Coverage | Sources | Labels | Calculations | Conclusions | Total / 10 |
| --- | --- | ---: | ---: | ---: | ---: | ---: | ---: |
| China NEV profit pools | No Skill | 1 | 1 | 2 | 2 | 2 | **8** |
| China NEV profit pools | Profit Atlas industry Skill | 2 | 2 | 2 | 2 | 2 | **10** |
| CATL economics | No Skill | 1 | 2 | 2 | 2 | 2 | **9** |
| CATL economics | Profit Atlas company Skill | 2 | 2 | 2 | 2 | 2 | **10** |

### Scoring notes

**China NEV profit pools.** The raw baseline is specific, transparent about many limitations, and makes credible entry-point distinctions. It scores 1 on coverage because it discusses roles in prose rather than mapping the full chain of transaction, control, and profit mechanisms; it scores 1 on sources because several material figures are supported by a filing mirror or secondary host. The Skill-guided case uses an explicit role map, profit-pool comparison, opportunity test, and directly linked primary disclosures.

**CATL economics.** The raw baseline is especially strong: it separates group from product economics, labels claims, exposes a cash bridge, and anchors material claims in CATL reports. It scores 1 on coverage only because it does not present the Skill’s two explicit review layers: a compact "who pays / why / revenue / core profit" view and a revenue–cost–risk–trust decision table. The Skill-guided example uses those layers, while keeping the same group-versus-power-battery boundary.

## How to use this evaluation

Do not use the totals as a model leaderboard. Use the raw reports to inspect what the Skill changes:

1. Does it force the right economic boundary before arithmetic begins?
2. Can a reader trace material claims to a source and reporting period?
3. Are facts, calculations, and inference visibly distinct?
4. Does the final recommendation state what must be true before someone acts on it?

Add a new row only with the prompt, raw baseline, Skill-guided output, and short score rationale checked into the repository together.
