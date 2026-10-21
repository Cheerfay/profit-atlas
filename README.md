# Profit Atlas

Profit Atlas is a small, evidence-first plugin for two different research entry points:

| Start with | Use | It answers |
|---|---|---|
| An industry or value chain | [`industry-profit-pool-research`](skills/industry-profit-pool-research/) | Where does profit accumulate, why, and which external startup entry points are credible? |
| A named company | [`company-value-chain-review`](skills/company-value-chain-review/) | What does the company live on, and which operating chain turns value into cash? |

The skills can be used independently or composed. They remain separate because industry profit distribution and company economics require different evidence, comparison units, and outputs.

[中文说明](README.zh-CN.md)

## Install

Clone or download this repository, then add either folder under `skills/` to a compatible agent's skill directory. Add both if you want automatic routing between industry-first and company-first questions.

The repository also includes a root [`plugin.json`](plugin.json) for clients that support portable agent plugins.

## Ask naturally

The skill descriptions are designed for automatic activation. For example:

- “Map the profit pools in China's game industry and identify defensible startup entry points.”
- “Analyze what BYD fundamentally lives on and how value becomes cash.”
- “Compare Tencent, NetEase, and 37 Interactive: how do their business models and profit engines differ?”

To force a specific route, name the skill in the request:

- “Use `industry-profit-pool-research` to study the automotive value chain.”
- “Use `company-value-chain-review` to review Meituan.”

## How the two skills work together

For an industry study, the industry skill selects representative companies by role or business model and uses them as evidence for profit-pool conclusions. It does not replace the full company review.

For a company study that needs broader context, run the industry skill first, then use the company skill to synthesize:

1. company economics — payer, payment reason, revenue, profit, costs, and risks;
2. the operating value-to-cash chain — the few steps that determine revenue, cost, risk, and trust.

## Evidence boundaries

- Company revenue is not automatically comparable with industry sales.
- Revenue share does not prove profit contribution.
- Gross profit, operating profit, net profit, and cash flow are kept distinct.
- Calculations and inferences are labeled; undisclosed segment profit is not invented.
- Startup opportunities are evaluated from external pain, budget, entry rights, defensibility, and economics. AI is classified as a possible core capability, enhancement, ordinary feature, or unnecessary—not assumed to be the answer.
- Dedicated sector modules improve question coverage but are not required. Unlisted sectors use the general workflow and state the missing evidence explicitly.

Profit Atlas is a research framework, not investment advice; independently verify evidence before making financial or operating decisions.

## Repository map

```text
skills/
  industry-profit-pool-research/
  company-value-chain-review/
evals/
examples/
plugin.json
```

See [`examples/`](examples/) for a completed game-industry study and an automotive generalization test brief. See [`evals/`](evals/) for activation and boundary cases.

## Contributing and testing

Contributions should preserve the boundary between the two skills and add an evaluation case for any changed behavior. A new sector module should be added only after repeated real tests reveal stable, sector-specific questions that the general workflow misses.

Before submitting a change, validate the skill front matter, check every referenced resource, rerun the relevant evaluation cases, and scan the repository for private paths or credentials.

## License

[MIT](LICENSE)
