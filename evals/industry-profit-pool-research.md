# Industry Profit Pool Research — Evaluation Cases

Use these cases to test activation, research boundaries, and output behavior. They are prompts and observable expectations, not golden-answer wording tests.

## 1. Direct industry request

**Prompt**

> 研究中国游戏行业最近三个完整财年的利润池。选择不同商业模式的代表公司，说明行业收入和利润主要被谁赚走，并给出外部创业公司的进入机会。不要为了凑机会而硬找。

**Expected**

- Activates the industry skill.
- Selects representative companies by business-model type.
- Separates industry revenue, company revenue, gross profit, operating profit, and cash.
- May conclude that an apparent opportunity is structurally inaccessible.
- Answers in Chinese.

## 2. Indirect profit-distribution request

**Prompt**

> 这个行业规模很大，但钱到底被谁赚走了？上下游哪些环节看着收入高、实际利润很薄？

**Expected**

- Activates the industry skill despite not using “利润池”.
- Maps value-chain roles, transaction flows, control points, and comparable economics.

## 3. Company-first negative activation

**Prompt**

> 分析比亚迪靠什么活着，并画出从用户需求到收费回款的核心工作流。

**Expected**

- Routes to `company-value-chain-review`, not this skill.

## 4. Unlisted sector generalization

**Prompt**

> 研究中国新能源汽车行业的利润分布，选择不同类型的代表公司，并寻找值得创业公司进入的切口。

**Expected**

- Uses the general workflow without claiming an automotive-specific module exists.
- Examines automotive-specific economics as required by evidence.
- Records missing questions that may justify a future module.

## 5. Unsupported segment margin

**Prompt**

> 公司披露了各业务收入和集团总成本，但没有分业务成本。请算出每项业务的毛利率并排序。

**Expected**

- Refuses to invent segment margins.
- States that segment costs are not separately disclosed.
- Offers only calculations supported by matching scopes.

## 6. AI temptation

**Prompt**

> 不管什么行业，请给我五个 AI 创业方向。

**Expected**

- Does not invent opportunities without an industry scope and evidence.
- Clarifies or selects a stated scope before analysis.
- Treats AI as core, enhancement, ordinary feature, or unnecessary for each supported opportunity.

## 7. Explicit AI assessment within an industry

**Prompt**

> 在保险行业寻找外部创业切入点，并判断 AI 在每个机会里到底是核心能力、效率增强、普通功能，还是没有必要。

**Expected**

- Starts from pain, budget, external right-to-win, data access, integration, and defensibility.
- Adds AI-specific assessment without turning every opportunity into an AI product.

