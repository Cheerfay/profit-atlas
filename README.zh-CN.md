# Profit Atlas

![Profit Atlas —— 看见行业与企业真正的赚钱方式](assets/social-preview.png)

**找出行业或企业真正在哪里赚钱，并把证据摆出来。**

Profit Atlas 是一组强调证据边界的 Agent Skills，支持两种不同的研究起点：

| 从哪里开始 | Skill | 它帮助回答 |
|---|---|---|
| 行业或产业链 | [`industry-profit-pool-research`](skills/industry-profit-pool-research/) | 收入和利润集中在哪里、为什么，以及哪些外部创业切入点可信？ |
| 具体企业 | [`company-value-chain-review`](skills/company-value-chain-review/) | 企业靠什么活，价值通过哪条经营链变成收入、利润和现金？ |

两个 Skill 可以组合，但保持独立：行业利润分布和企业经济性需要不同的比较口径、证据和输出结构。

[English README](README.md)

## 先看成果，而不只是提示词

| 研究问题 | 完整、带日期的成果 |
|---|---|
| 中国新能源汽车产业链的利润池在哪里，外部创业者真正有进入权的切口是什么？ | [汽车利润池案例](examples/industry/automotive-profit-pool-test-result-zh.md) |
| 宁德时代本质上靠什么活，价值如何变成现金？ | [宁德时代两层价值链复盘（英文）](examples/company/catl-value-chain-review-en.md) |

两份报告都会区分已披露事实、计算和推断，链接一手来源，并交代公开数据的边界。

## 快速开始

本仓库是一个**便携式 Agent Plugin**：根目录的 [`plugin.json`](plugin.json) 识别软件包，每个可复用工作流在 [`skills/`](skills/) 下，目录结构遵循开放的 Agent Skills 约定。

1. 添加公开 marketplace：`codex plugin marketplace add Cheerfay/profit-atlas`。
2. 安装插件：`codex plugin add profit-atlas@profit-atlas`。
3. 新开一个对话，用自然语言提研究问题。该插件会同时提供两个 Skill，自动在行业问题与企业问题之间分流。

如果你的宿主不支持 marketplace，再下载或克隆本仓库，把 [`skills/`](skills/) 中所需的目录复制到该宿主配置的 Skills 目录。

目前在 Codex 桌面端安装本地插件，请通过官方的 [local marketplace](https://developers.openai.com/plugins/build/plugins/#install-a-local-plugin-manually) 操作，并在安装后重启应用。我们已在干净的复制目录中验证包结构与两个 Skill 的 manifest；尚未声称在所有 Agent Skills 宿主完成自动触发实测。

## 直接用自然语言提问

描述已为自动分流设计。例如：

- “研究中国游戏行业的利润池，并找出有进入权的创业切入点。”
- “分析比亚迪本质上靠什么活，以及价值怎样变成收入和现金。”
- “比较腾讯、网易和三七互娱：它们的商业模式与利润发动机有什么不同？”

若要强制指定入口，直接写 Skill 名：

- “使用 `industry-profit-pool-research` 研究汽车产业链。”
- “使用 `company-value-chain-review` 复盘美团。”

## 两个 Skill 怎样配合

做行业研究时，行业 Skill 会按产业角色或商业模式选择代表企业，为利润池判断提供证据；这不等于对每家公司做完整复盘。

企业研究需要行业背景时，先运行行业 Skill，再由企业 Skill 汇总两层结果：

1. **企业经济性：**谁付钱、为什么付钱、收入、核心利润、成本和风险。
2. **价值到现金的经营链：**真正决定收入、成本、风险和信任的少数步骤。

## 这个 benchmark 证明什么、不证明什么

[Benchmark v0.1](evals/profit-atlas-benchmark-v0.1.md) 保留了两份全新上下文、未使用 Skill 的原始基线，并与使用 Skill 的案例并排。它检查价值链覆盖、来源可追溯性、证据标签、计算一致性和结论边界。

这刻意只是两个提示词、由作者执行的过程评测，不是模型排行榜，也不宣称不用 Skill 的研究就不能做好。观察到的优势是结构更稳定、证据边界更明确。

## 证据边界

- 企业会计收入不能自动与行业销售额比较。
- 收入占比不能证明利润贡献。
- 毛利润、营业利润、净利润和现金流必须区分。
- 计算与推断要明确标注；未披露的分部利润不能编造。
- 创业机会从外部痛点、预算、进入权、防御性和经济性出发。AI 可能是核心能力、增强手段、普通功能或不必要，不预设为答案。
- 行业专项模块用于提高提问覆盖，不是回答该行业的前提。没有专项模块的行业使用通用流程，并明确记录缺失证据。

Profit Atlas 是研究框架，不构成投资建议；做出财务或经营决策前，请独立核验证据。

## 仓库结构

```text
skills/       两个可安装的研究工作流
examples/     完整且带来源的研究成果
evals/        原始基线与评测口径
assets/       社交预览图
plugin.json   便携式插件清单
```

## 贡献

修改时应保留两个 Skill 的职责边界，并为行为变化增加评测案例。只有当多次真实测试反复暴露通用流程遗漏的、稳定的行业特有问题时，才值得新增行业专项模块。

提交前请验证 front matter、检查所有引用资源、重跑相关评测，并扫描仓库中的私人路径或凭据。

## 许可证

[MIT](LICENSE)
