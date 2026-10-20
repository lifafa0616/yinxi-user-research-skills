# 用户研究工作流

> AI First + Human Validation 的用户研究教学流程，从业务目标出发，做研究 → 输出用户画像 → 输出设计方向。

## 项目结构

```
用户研究工作流/
├── README.md          ← 本文件（项目地图）
├── HANDOFF.md         ← 交接文档（背景、架构、决策、状态、待办）
├── 当前阶段产出.md     ← 关键规则速查（原为内容快照，已改为速查表）
└── Persona质量条例-待落地.md ← 2026-10-18 的条例讨论记录
```

本目录记录决策、状态与速查，不复制规则原文。规则原文在本仓库的 `Skill/yinxi-user-research/`。

## Skill 包：yinxi-user-research

两个 Skill 协同工作，合称 `yinxi-user-research`：

| Skill | 角色 |
|-|-|
| `yinxi-user-research-loop` | 主流程（S1-S7 + 3 闸门 + 回传） |
| `yinxi-user-research-interview` | 被访者（独立对话防自证） |

### 项目源文件与已安装 Skill

| 用途 | 路径 |
|-|-|
| **项目源文件**（规则原文、版本管理） | `~/Documents/yinxi-user-research-skills/Skill/yinxi-user-research/` |
| **已安装 Skill**（Factory / Codex / Workbuddy 加载） | `~/.factory/skills/yinxi-user-research-loop/` 和 `~/.factory/skills/yinxi-user-research-interview/` |

以后只在项目源文件目录修改 Skill 并推送本公开仓库。已安装 Skill 保持独立；需要在本机使用新版本时，再从源目录更新安装。

### Skill 目录结构

```
~/Documents/yinxi-user-research-skills/Skill/yinxi-user-research/
├── 说明.md                        ← 面向人阅读的包说明
├── yinxi-user-research-loop/      ← 主流程
│   ├── SKILL.md
│   ├── references/
│   │   ├── persona质量条例.md
│   │   ├── s1-假设与persona.md
│   │   ├── s2-访谈方案.md
│   │   ├── s3-校准.md
│   │   ├── s4-需求.md
│   │   ├── s5-功能与kano.md
│   │   └── s6-方向.md
│   └── assets/
│       └── 报告骨架.md
└── yinxi-user-research-interview/ ← 被访者
    └── SKILL.md
```

两个 Skill 的已安装副本分别位于 `~/.factory/skills/` 下。源文件更新后，已安装副本需要单独更新。

## 快速了解

1. 先读 **HANDOFF.md**：项目背景、架构决策、两轮审查的修复清单、当前状态与待办
2. 需要查具体参数时读 **当前阶段产出.md**（关键规则速查）
3. 要看规则原文，读 `~/Documents/yinxi-user-research-skills/Skill/yinxi-user-research/` 下的对应文件
4. 要了解 Skill 包整体，读 `~/Documents/yinxi-user-research-skills/Skill/yinxi-user-research/说明.md`

## 怎么用

学生在 Factory / Codex / Workbuddy 里说要做用户研究，主 skill 自动激活。走到访谈时，主 skill 会输出每个候选一份不含题目的《访谈身份交接包》，以及只给学生参考的《访谈计划与提问清单》；学生新建对话粘贴身份包，再按清单逐题访谈，**访谈结束后把记录粘回主会话**，流程继续。

## 当前状态

- **两个 skill 主体设计完成**，已经过两轮对抗式审查：第一轮修复 11 处，第二轮修复 4 个阻断问题 + 7 个重要问题 + 1 个交互问题（清单见 HANDOFF.md §4）
- **Skill 与项目文档已合并到本公开仓库**，Skill 工作目录为 `~/Documents/yinxi-user-research-skills/Skill/yinxi-user-research/`；本机已安装 Skill 保持独立
- **待试跑验证**：拿一个案例从 S1 跑到闸门①，重点看闸门卡片、交接包可复制性、候选可区分性
- **飞书原文档**：全程未修改，处理方式待定
