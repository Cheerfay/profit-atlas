# Company Value Chain Review — Evaluation Cases

Use these cases to test activation, evidence boundaries, and the required two-layer output.

## 1. Direct named-company request

**Prompt**

> 用两层价值链方法分析比亚迪靠什么活着，以及价值如何从客户需求变成收入和现金。

**Expected**

- Activates the company skill.
- Produces Layer 1 and Layer 2 by default.
- Answers in Chinese.
- Uses a minimum financial spine rather than a generic company profile.
- Links material company-specific claims to current primary sources and states their reporting periods; if source access is unavailable, says what remains unverified.

## 2. Indirect company-essence request

**Prompt**

> 美团表面上业务很多，它本质上靠什么赚钱？哪个经营环节决定收入、成本、风险和用户体验？

**Expected**

- Activates without requiring the phrase “两层价值链”.
- Separates revenue scale, profit contribution, strategic importance, and cash.

## 3. Industry-first negative activation

**Prompt**

> 研究中国新能源汽车产业链的利润主要集中在哪里，并寻找外部创业切入点。

**Expected**

- Routes to `industry-profit-pool-research`, not this skill.

## 4. Project-to-workflow bridge

**Prompt**

> 我在一家保险公司做过理赔自动化项目。请先说明公司靠什么活，再判断这个项目位于哪段核心工作流、影响收入成本风险还是体验。

**Expected**

- Produces both company layers before locating the project.
- Distinguishes direct company-level impact from local efficiency or experience improvement.
- Does not claim profit impact without evidence and scale linkage.

## 5. Undisclosed segment profit

**Prompt**

> 公司只披露了各业务收入，没有分业务成本。请告诉我哪个业务利润最高。

**Expected**

- States that segment profit is not separately disclosed.
- Does not infer profit rank from revenue rank.
- Identifies what can be disclosed, calculated, or only inferred.

## 6. Multiple companies

**Prompt**

> 腾讯、网易和三七互娱哪家公司最赚钱，分别靠什么赚钱？

**Expected**

- Uses a consolidated Layer 1 comparison.
- Gives a compact Layer 2 chain for each company.
- Explains comparability limits between a diversified platform and game-focused companies.

