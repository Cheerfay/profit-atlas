---
name: industry-profit-pool-research
description: Use when a request starts from an industry, market, or value chain and asks where revenue and profit pools sit, how representative business models compare, why economics changed, or which external startup entry points are credible. Also use for sector-wide comparisons of margins, capital intensity, cash conversion, and control points. Do not use for a company-first two-layer review.
---

# Industry Profit Pool Research

## Objective

Turn company filings and industry data into a decision-oriented answer to four questions:

1. Where does revenue come from?
2. Where does gross profit, operating profit, and cash actually come from?
3. Which costs, liabilities, and working-capital items make the model fragile?
4. Which profit pools are realistically accessible to an external startup?

Never force an entrepreneurial opportunity when the evidence supports exclusion.

Respond in the user's language unless the user asks for another language.

## Workflow

### 1. Set the scope

- Default to the latest three complete audited fiscal years.
- State exact fiscal years and currency.
- Select representative companies by value-chain role and business-model type, not fame alone.
- When the request starts from a named company and asks what it lives on or how value becomes cash, use `company-value-chain-review` instead.
- Separate group economics from a new business segment when the group has multiple businesses.
- Separate audited annual data from unaudited current-year data.

### 2. Use primary sources

Browse for current information. Prefer, in order:

1. Audited annual report, 10-K, 20-F, statutory filing, or exchange filing.
2. Official company results presentation and earnings release.
3. Government statistics, regulator data, or recognized industry association data.
4. High-quality secondary research only when primary data is unavailable.

For PDF filings:

- Inspect the actual PDF, not only search snippets.
- Give the PDF viewer page and printed page when both exist.
- Build a short page index for revenue, cost, segment notes, balance sheet, cash flow, and key accounting notes.

### 3. Build the three-statement skeleton

Normalize amounts into one unit and create a three-year table.

**Income statement**

- Revenue by segment or business line.
- Cost of revenue and gross profit by segment where disclosed.
- Gross margin, operating margin, and net margin.
- R&D, sales and marketing, general and administrative expenses.
- Government grants, fair-value gains, investment income, interest income, tax benefits, and other non-core items.
- Distinguish operating profitability from reported net profit.

**Balance sheet**

- Cash and liquid investments; identify restricted cash.
- Interest-bearing debt and lease liabilities.
- Accounts payable, receivables, inventory, contract liabilities, customer deposits, or sector-specific reserves.
- Current ratio, net cash/debt, equity trend, and major off-balance-sheet commitments when disclosed.
- Explain whether liability growth comes from bank debt, suppliers, customers, policyholders, tenants, or another operating counterparty.

**Cash flow statement**

- Operating cash flow, capital expenditure, rough free cash flow, financing cash flow.
- Reconcile profit to cash.
- Identify the largest working-capital contributors: payables, receivables, inventory, deferred revenue, reserves, deposits, or customer funds.
- Do not call operating cash flow "self-generated cash" when it mainly comes from delayed supplier payment or customer prepayments.

### 4. Reconstruct segment economics carefully

For each business line, label every number as one of:

- **Disclosed:** directly reported by the company.
- **Derived:** calculated from disclosed figures; show the formula.
- **Inference:** a reasoned interpretation; state the evidence and uncertainty.

Never assign a segment margin when segment cost is not disclosed. Do not subtract a mixed cost category from a differently scoped revenue category. When only year-over-year changes are disclosed, calculate only the change in gross profit or cost, not an absolute margin.

Classify each business line as:

- Core profit engine.
- High-margin cash cow.
- Scale business with thin margins.
- Strategic loss leader or infrastructure.
- Ancillary monetization.
- Project-based or cyclical profit.
- Accounting or financial-income contributor rather than operating profit.

### 5. Explain the change, not only the numbers

Test the main drivers:

- Volume, price, mix, utilization, procurement savings, platform reuse, customer acquisition, fulfillment, regulation, product cycle, write-downs, claims, financing cost, and working capital.
- Fixed-cost operating leverage: show how revenue or gross-profit changes interact with R&D, sales, stores, factories, staff, or infrastructure.
- One-off items and timing effects.

Use a simple bridge when useful:

`Profit change = volume effect + price/mix effect + unit-cost effect + operating-expense effect + non-operating effect`

### 6. Map the industry profit pool

Do not equate industry revenue with industry opportunity.

For the value chain:

1. Estimate the total industry revenue using a clearly defined scope.
2. List major participants and transaction flows.
3. Compare representative gross margins, operating margins, capital intensity, cash conversion, and cyclicality.
4. Identify who controls the customer, data, distribution, licenses, inventory, balance sheet, and physical fulfillment.
5. Separate large revenue pools from attractive profit pools.

Use representative companies only when accounting scopes are comparable. Explain important scope differences.

### 7. Apply the external-startup filter

For every proposed opportunity, answer:

- Why will the incumbent not build it internally?
- Why must it be cross-company, neutral, regulated, specialized, or outside the incumbent boundary?
- Who pays, from which budget, and what measurable loss or cost is reduced?
- What proprietary data or workflow access is required?
- Can a startup obtain that access before it has scale?
- Is implementation deeply integrated with enterprise systems?
- Does the model require licenses, capital, inventory, local operations, or a large service network?
- Is demand recurring and is willingness to pay proven?
- Can a platform, manufacturer, insurer, broker, landlord, publisher, or marketplace copy or bundle it?
- Does the business compound through software, data, network effects, or switching costs, or does it reset with every product, customer, city, or SKU?

Score each opportunity qualitatively from 1 to 5, where **5 always means more attractive**. For the two burden criteria, lower sales, integration, capital, or offline burden therefore receives the higher score.

- Pain and budget.
- External right-to-win.
- Data accessibility.
- Sales and integration burden.
- Capital and offline burden.
- Recurrence and margin.
- Defensibility.

A high market size with low external right-to-win is not an attractive startup opportunity.

For each supported opportunity, state the appropriate solution form and classify AI as one of:

- **Core capability:** the product or cost advantage does not work without AI.
- **Important enhancement:** AI materially improves the workflow but is not the primary moat.
- **Ordinary feature:** AI is useful but readily copied or bundled.
- **Unnecessary:** workflow, distribution, service, hardware, licenses, or capital matter more.

When the user explicitly asks for AI opportunities, also test access to training and evaluation data, model reliability, human review, inference cost, workflow integration, and whether incumbents can reproduce the capability. Do not produce a separate AI list when AI does not change the opportunity's quality.

### 8. Use the sector modules

Read `references/sector-question-bank.md` for securities, insurance, real estate, games, e-commerce, and local services. Use only the relevant section.

For industries without a dedicated module, use the general workflow and derive sector-specific questions from primary evidence. Do not imply that a dedicated module exists. Add a new module only after repeated real cases reveal reusable omissions.

Read `references/report-template.md` before producing a full industry report.

## Quality rules

- Cite every current or company-specific factual claim.
- Prefer exact figures over adjectives.
- State data gaps explicitly.
- Avoid false precision and mixed accounting scopes.
- Do not calculate a ratio across mismatched company, geography, gross/net, or industry-sales scopes, even as a directional estimate.
- Do not treat gross margin as net profitability.
- Do not treat revenue growth as cash generation.
- Do not treat a strategic ecosystem activity as an independent profit center without evidence.
- End with a clear judgment: attractive, structurally difficult, or insufficient evidence, and explain why.
