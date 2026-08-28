# 银溪用户研究 Skill

一套面向教学的用户研究工作流 Skill：从业务目标出发，完成研究、用户画像与设计方向的推导。它强调 AI 先协助建立假设，再由真实用户访谈进行验证。

## 包含什么

| Skill | 是否必装 | 用途 |
| --- | --- | --- |
| `yinxi-user-research-loop` | 是 | 主工作流。按 S1–S7 推进，从候选 Persona、访谈方案、校准、需求到设计方向，并汇总研究报告。 |
| `yinxi-user-research-interview` | 可选 | 仅用于无法接触真实用户时的模拟访谈演练；必须在独立对话中扮演被访者，避免研究方的假设被模型复述。 |

## 安装

请使用支持安装 GitHub Skill 的 AI Agent，并把以下链接直接交给它。

主工作流（必装）：

```text
https://github.com/lifafa0616/yinxi-user-research-skills/tree/main/Skill/yinxi-user-research/yinxi-user-research-loop
```

模拟访谈（仅在需要模拟演练时安装）：

```text
https://github.com/lifafa0616/yinxi-user-research-skills/tree/main/Skill/yinxi-user-research/yinxi-user-research-interview
```

在 Codex 中，可以对 Agent 说：“请从这个 GitHub 链接安装 Skill”，再粘贴对应链接。安装完成后，通常在下一轮对话生效。

## 怎么使用

1. 新开对话，说明产品/服务、业务目标与当前阶段；如果产品可从公开资料识别，Skill 会先检索公开信息，再补问无法公开确认的内容。
2. 跟随主工作流完成 S1 的候选用户与访谈重点，并在闸口确认后生成一份独立的 Markdown《访谈计划与提问清单》。
3. 能接触真实用户时，实际完成访谈后把完整记录带回原对话，继续校准与后续分析。
4. 不能接触真实用户时，才在一个**独立对话**中使用模拟访谈 Skill，粘贴主流程生成的《访谈身份交接包》，由学生逐题访谈；模拟结果只可作为待验证假设。

每次生成或修订某一步的产物后，主流程都会提示当前进度、下一步动作以及需要回传的材料；修订不会让工作流中断。

## 访谈能力边界

本包输出的是 20–30 分钟的**纯问答式深度访谈**：问题会围绕业务目标、已知产品信息、用户特性与待验证假设定制，并包含背景、使用习惯、驱动与障碍等必要模块。它不提供任务式可用性测试或任务设计；这类研究需要掌握具体产品流程、界面和任务体系，应由熟悉产品的研究者另行设计。

## 目录

```text
Skill/yinxi-user-research/
├── yinxi-user-research-loop/       # 主工作流
├── yinxi-user-research-interview/  # 可选：模拟被访者
└── 说明.md                          # 包内使用说明
```

## 适用场景

- 用户研究、Persona、需求与设计方向相关课程作业
- 需要从业务目标逐步推到可执行设计方向的产品研究
- 需要在真实访谈与模拟访谈之间明确区分证据强度的教学场景

本项目中的 Skill 规则为通用用户研究方法，不绑定某个行业或产品。
