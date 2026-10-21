# Profit Atlas Repository Design

## Purpose

Profit Atlas is an open-source plugin for evidence-based profit research. It helps users answer two related questions from different starting points:

1. Where does an industry's profit accumulate, and which external startup entry points are credible?
2. What does a specific company live on, and how does value become revenue and cash?

The repository packages these questions as separate skills so that each remains easy to discover, invoke, test, and maintain.

## Repository Structure

```text
profit-atlas/
├── plugin.json
├── README.md
├── README.zh-CN.md
├── LICENSE
├── skills/
│   ├── industry-profit-pool-research/
│   │   ├── SKILL.md
│   │   ├── agents/openai.yaml
│   │   └── references/
│   └── company-value-chain-review/
│       ├── SKILL.md
│       ├── agents/openai.yaml
│       └── references/
├── examples/
│   ├── industry/
│   └── company/
└── evals/
```

Only files with an immediate use are added. No build system or runtime dependency is needed because both skills are instruction-and-reference packages.

## Original-Source Preservation

Before canonicalization, copy the original ZIP packages, expanded skill, and example folders into a dated backup directory beside the new Git repository. Keep that backup outside version control. Canonical skills are built from copies, never by moving or rewriting the original files in place.

## Skill 1: Industry Profit Pool Research

### Trigger

Use when the user starts from an industry, market, or value chain and wants to understand revenue pools, profit distribution, representative business models, structural risks, or external startup entry points.

### Responsibilities

- Define the industry scope and value chain.
- Select representative companies by business-model type rather than fame alone.
- Compare disclosed or safely derived economics across comparable scopes.
- Distinguish large revenue pools from attractive profit pools.
- Identify who controls customers, data, distribution, licenses, capital, inventory, and fulfillment.
- Evaluate external startup entry rights without assuming that AI is the answer.

### Opportunity Output

The general output is `external startup entry points`, not `AI startup opportunities`. For each opportunity, identify the appropriate solution form and classify AI as:

- Core capability.
- Important enhancement.
- Ordinary, replicable feature.
- Unnecessary.

When the user explicitly requests AI opportunities, add AI-specific analysis of data access, evaluation, model cost, workflow integration, incumbent replication, and defensibility.

### Sector Modules

The first release retains the existing modules for securities, insurance, real estate, games, e-commerce, and local services. Other industries use the general framework. Automotive remains a test case before becoming a dedicated module.

## Skill 2: Company Value Chain Review

### Trigger

Use when the user starts from one or more named companies and wants to understand what the business lives on, who pays, how revenue is generated, where core profit comes from, and which operating workflow turns value into cash.

### Responsibilities

- Build only the minimum financial spine required to understand the business.
- Produce Layer 1: payer, reason to pay, revenue mechanism, core revenue/profit, major costs, key risks, and a one-sentence company essence.
- Produce Layer 2: the smallest defensible workflow from customer need to billing, collection, retention, or repurchase.
- Identify which workflow steps determine revenue, cost, risk, and trust or user experience.
- Optionally position a supplied project inside the workflow without inflating local impact into company-level profit.

The skill remains `company-value-chain-review`; it is not renamed to `company-profit-engine-analysis` unless its future scope changes to a deeper, comprehensive profit-module decomposition.

## Composition Rules

- A request that starts from an industry is owned by the industry skill, even when it analyzes representative companies.
- A request that starts from a company is owned by the company skill, even when it adds industry context.
- Representative-company analysis inside an industry report supports cross-company comparison; it does not turn the output into a collection of standalone company reports.
- Both skills may reuse the same evidence principles, but each must remain independently usable.

## Language Strategy

The canonical `SKILL.md` files use English instructions and stable English folder names, then respond in the user's language. Chinese and English instructions will not be maintained as four independent source packages because duplicated sources drift. Repository documentation provides both English and Chinese entry points, and Chinese examples verify Chinese output quality.

## Documentation

The English and Chinese READMEs must explain:

- The two entry points and when to use each.
- Natural-language and explicit invocation examples.
- Installation from the repository.
- How the two skills compose.
- Evidence and non-investment-advice limitations.
- The included examples and eval cases.

## Examples and Evaluation

### Existing Example

Publish the Chinese game-industry report as a full industry example, preserving citations and its research date.

### Automotive Test

Use an automotive-industry prompt to test whether the general framework handles manufacturing economics without a dedicated module. Record:

- What the general skill covers correctly.
- Which automotive-specific questions it misses.
- Which misses are industry-general rather than company-specific.
- Whether a dedicated automotive module is justified.

Do not add an automotive module merely to make the sector list look complete.

### Activation Tests

Each skill receives representative cases for:

- Direct activation.
- Indirect activation.
- Incomplete input.
- Requests that should activate the other skill.
- Unsupported inference and data-gap handling.

## Validation

- Run the bundled skill validator against each skill.
- Check plugin manifest syntax.
- Scan for absolute local paths, secrets, placeholders, and `.DS_Store` files.
- Verify backup ZIP checksums against the original ZIP files.
- Verify all referenced files exist.
- Test representative prompts before declaring the repository ready.

## Out of Scope for the First Release

- An MCP server or live financial-data integration.
- A custom installer or build system.
- A dedicated automotive module before the automotive test.
- Separate Chinese and English copies of every skill.
- Publishing to GitHub, creating a remote repository, or pushing without a separate explicit request.
