# Profit Atlas v0.1 Regression Cases

These are minimal manual regression prompts for a fresh chat after installing the plugin. They test routing, bilingual output, and financial evidence boundaries; they are not a model leaderboard.

## Routing cases

| ID | Prompt | Expected route |
|---|---|---|
| zh-industry | `研究东南亚电商行业的利润池、履约成本，并提出外部创业切入点。` | `industry-profit-pool-research` |
| en-industry | `Map Southeast Asia e-commerce profit pools, fulfillment costs, and credible external startup wedges.` | `industry-profit-pool-research` |
| zh-company | `分析 Shopee 靠什么赚钱，以及核心工作流如何把价值变成现金。` | `company-value-chain-review` |
| en-company | `Compare how Shopee and PDD make money and which workflows turn value into cash.` | `company-value-chain-review` |
| mixed | `研究跨境电商行业利润池，并比较 Shopee、拼多多和阿里国际的收入与利润来源。` | Industry first; company review may compose for the named companies |

## Evidence-boundary cases

| ID | Prompt | Required behavior |
|---|---|---|
| zh-evidence | `已知交易服务收入100、广告收入50、经营利润30、经营现金流35，但未披露分部成本。请用 Profit Atlas 做小结。` | Respond in Chinese; label disclosed/calculated/inferred; do not assign profit to either revenue line; distinguish operating profit from operating cash flow. |
| en-evidence | `Revenue is 100 from transaction services and 50 from ads; operating profit is 30 and operating cash flow is 35; segment costs are undisclosed.` | Respond in English; label disclosed/calculated/inferred; do not assign segment profit; distinguish operating profit from operating cash flow. |

## Manual acceptance record

- Clean GitHub marketplace install: verified in an isolated `CODEX_HOME`.
- Chinese company route: verified; `company-value-chain-review` loaded.
- Chinese mixed/industry routes: verified; `industry-profit-pool-research` selected for industry-first prompts.
- Chinese evidence boundary: verified; output preserved disclosed/calculated/inferred labels and refused an unsupported segment-profit claim.
- English evidence boundary: verified; output preserved Disclosed/Calculated/Inferred labels and refused an unsupported segment-profit claim.
