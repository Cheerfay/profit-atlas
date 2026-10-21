---
name: company-value-chain-review
description: Use when a request starts from one or more named companies and asks what the business lives on, who pays, how it makes money, where core profit comes from, or which workflow turns customer value into cash. Also use to compare company business models or position a supplied project inside a company's real value chain. Do not use for an industry-first profit-pool or startup-entry study.
---

# Company Value Chain Review

Use this skill to answer two questions only:

1. **What does this company live on?**
2. **What is the core workflow that turns value into cash?**

Do not start from company history, mission statements, org charts, or a list of projects.

Respond in the user's language unless the user asks for another language.

## Scope

- Analyze one company or compare several companies.
- Default to the latest three complete fiscal years when financial evidence is needed.
- If the user already supplied reliable financial analysis, reuse it instead of repeating the full research.
- If deeper industry profit-pool research is required, compose with `industry-profit-pool-research` first, then return here to synthesize the two layers.
- When the request starts from an industry or value chain and asks where profit accumulates or which startup entry points are credible, use `industry-profit-pool-research` instead.

## Evidence standard

Prioritize:

1. Audited annual reports and financial statements.
2. Official investor-relations materials and regulatory filings.
3. Authoritative industry or regulatory sources for context.

Separate three kinds of statements:

- **Disclosed:** directly stated in a source.
- **Calculated:** derived from disclosed numbers; show the formula or reasoning when material.
- **Inferred:** a business interpretation; label it clearly.

Never assign a profit or margin to a business line when the company reports only revenue or combines several lines in one segment. Say that the data is not separately disclosed.

## Workflow

### Step 1: Establish the minimum financial spine

Collect only what is needed to understand the business:

- Core revenue sources and their share.
- Core gross-profit or operating-profit sources.
- Major operating costs.
- Material balance-sheet or cash-flow risks.
- Any non-operating item that materially changes net profit.

Avoid turning this step into a complete financial-report summary.

### Step 2: Answer Layer 1 — What does the company live on?

Layer 1 is a company-economics view, not a customer journey. It establishes the payer, payment reason, revenue mechanism, core revenue and profit sources, costs, and risks.

For each company, answer:

- Who pays the company?
- Why does that customer pay?
- How is revenue generated: product sale, subscription, commission, spread, premium, advertising, service fee, licensing, financing, or another mechanism?
- Where does the company spend most of its money?
- Which business creates the most gross or operating profit, if disclosed?
- Which business is strategically indispensable even when it is not a proven profit source?
- What is the most important business risk?

End with exactly one compressed sentence in this form:

> This company fundamentally uses **[core capability/mechanism]** to help **[customer]** solve **[important problem]**, thereby earning **[type of money]**.

Do not use vague phrases such as “provides high-quality services” or “creates value for users.”

### Step 3: Answer Layer 2 — What is the core workflow?

Map one main chain from value creation to cash collection. Do not reproduce the full organization.

Layer 2 is the operating value-to-cash chain. Do not reinterpret the two layers as separate customer and internal value chains.

Use this generic skeleton only as a starting point:

> Customer need → acquisition/sales → product or service delivery → risk/quality control → billing/collection → retention/repurchase

Adapt it to the business. Examples:

- Insurance: product design and pricing → channel sales → underwriting → policy service → claims → renewal.
- Automotive: user insight → vehicle definition → R&D and sourcing → manufacturing → sales → delivery and service → repurchase/referral.
- Securities: client acquisition → account/funding → transaction or advisory execution → risk/compliance → settlement → recurring assets or trading activity.

Then identify:

- Which step primarily determines revenue?
- Which step primarily determines cost?
- Which step primarily determines risk?
- Which step primarily determines user experience or trust?

If different business models coexist, draw at most two chains and explain why both are necessary. Do not list every secondary workflow.

### Step 4: Compare companies when relevant

Use a comparison table with these columns:

| Company | Value-creation core | Main way it gets paid | Main profit engine | Largest cost/risk | Core operating contradiction |

The “core operating contradiction” should expose the tension in the model, such as:

- Service experience creates pricing power but consumes gross profit.
- Hardware creates users but software creates profit.
- High-margin technical services are profitable but customer-concentrated.
- A business relies on hit products and lacks a second profit engine.

### Step 5: Optional bridge to project review

Only when the user provides a project or asks to connect a project to the company:

- Locate the project in the core workflow.
- State whether it mainly affects revenue, cost, risk, user experience, or several of them.
- Distinguish direct business impact from local efficiency or experience improvement.
- Do not inflate a project into a company-level profit driver without evidence.

Use this sentence pattern:

> The project sits in **[workflow step]** and primarily changes **[revenue/cost/risk/experience]** by **[mechanism]**. Its company-level importance depends on **[required linkage or scale]**.

## Required output

For one company, produce:

1. **Layer 1 table** covering payer, reason to pay, revenue mechanism, core revenue, core profit, major cost, key risk, and the one-sentence essence.
2. **Layer 2 workflow** as a single arrow chain.
3. **Decision-point table** for revenue, cost, risk, and experience.
4. A short synthesis of the company's core operating contradiction.

For multiple companies, first provide the consolidated Layer 1 comparison, then one compact Layer 2 section per company, and finish with the cross-company differences.

Use the detailed question bank and output template in `references/review-template.md` when a fuller review is needed.

## Quality checks

Before answering, verify:

- Revenue source and profit source are not being confused.
- Gross profit, operating profit, net profit, and cash flow are distinguished.
- Strategic importance is not automatically called profitability.
- The workflow begins with a real customer need and ends with collection or retention.
- The chain contains only the few steps that truly determine value.
- Internal processes not supported by evidence are marked as inference.
- The final one-sentence description is specific enough to distinguish the company from its competitors.
