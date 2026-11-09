# TrustRocket

TrustRocket 是 RocketOS 下的客户服务、交付支持与客户成功标准体系，与 SpecRocket、GrowthRocket 处于业务执行层同级。

它不是 CRM、工单系统、客服 SaaS、知识库产品或 Agent 平台。它定义可由 Human、AI Agent、Script、Automation、External Service 或人机组合执行的业务契约、项目结构、创世能力与协作规则。

## 核心模型

TrustRocket 只设四个稳定业务域：

| 业务域 | 使命 | 典型产物 |
|:--|:--|:--|
| 装备材料 | 把组织能力转为一线、渠道、客户可直接使用的装备 | 指南、SOP、FAQ、Checklist、培训与验收材料 |
| 技术支持 | 让问题被识别、定位、解决、升级并闭环 | 标准问题描述、诊断记录、处置方案、研发反馈 |
| 案例沉淀 | 把一次性经验转为可复用的组织能力 | 故障案例、交付案例、根因分析、最佳实践、反模式 |
| 一线运营 | 持续掌握客户、POC、交付、售后与客户成功的真实状态 | 风险、重大事项、健康度、趋势与运营汇报 |

四域形成循环：

```mermaid
flowchart LR
    E[装备材料] --> O[一线执行与运营]
    O --> S[技术支持]
    S --> C[案例沉淀]
    C --> E
    O -->|风险与产品反馈| X[外部协作体系]
    S -->|确认产品缺陷| X
```

跨体系只交换标准 Handoff，不依赖其他 Rocket 的内部实现。

## 仓库结构

```text
TrustRocket/
├── AGENTS.md                         # 框架维护协作入口
├── CLAUDE.md                         # Claude Code 引用入口
├── README.md                         # 项目入口
├── SKILL.md                          # /trust-rocket 命令规范
├── trust-rocket                      # Genesis 与 Validator CLI
├── trustrocket-convention.zh.md      # 方法论正文
├── trustrocket-contract.zh.md        # 人可读总契约
├── trustrocket-contracts.json        # 四域能力与 Handoff 机器契约
├── execution-contract.schema.json    # 执行契约 Schema
├── handoff.schema.json               # 交接契约 Schema
└── template/                         # 业务项目最小骨架
```

框架仓库与初始化后的业务项目是两个层次。四大业务内容目录只存在于 `template/` 和由 Genesis 创建的业务项目中，不用于承载框架源码。

## 快速开始

在当前空目录初始化：

```bash
/path/to/TrustRocket/trust-rocket genesis init .
```

创建新项目：

```bash
/path/to/TrustRocket/trust-rocket genesis init ./customer-success
```

分析已有项目：

```bash
/path/to/TrustRocket/trust-rocket genesis normalize ./existing-project
```

安全补齐入口文件和四域资源目录，不移动或覆盖现有内容：

```bash
/path/to/TrustRocket/trust-rocket genesis normalize ./existing-project --apply
```

校验项目：

```bash
/path/to/TrustRocket/trust-rocket validate ./customer-success
```

以上命令不会执行 `git init`、提交、推送、打标签或发布。

## Genesis 产物

初始化项目包含：

```text
project/
├── AGENTS.md
├── CLAUDE.md
├── README.md
├── TRUSTROCKET.md
├── .trustrocket.json
├── 装备材料/{source,cut}/
├── 技术支持/{source,cut}/
├── 案例沉淀/{source,cut}/
└── 一线运营/{source,cut}/
```

Genesis 不生成空业务模板文档；业务内容在真实需求出现时创建。

## Skill 命令

`SKILL.md` 以与 SpecRocket 相同的单一 Skill 入口组织以下能力：

| 命令 | 能力 |
|:--|:--|
| `/trust-rocket genesis` | 初始化或规范化业务项目 |
| `/trust-rocket equipment` | 创建、改写、校验装备材料 |
| `/trust-rocket support` | 问题受理、诊断、解决、升级和验证 |
| `/trust-rocket case` | 检索、创建、合并、改进案例并反哺装备 |
| `/trust-rocket operations` | 收集外部状态、识别风险和分发反馈 |
| `/trust-rocket validate` | 校验目录、Markdown、素材、状态与配置边界 |

Skill 是执行说明，不是业务事实源。权威规则位于 `trustrocket-contract.zh.md` 与 `trustrocket-contracts.json`；没有 AI 时，人也可直接按契约执行。

## 规则优先级

1. 使用者对当前任务的明确指令
2. 目标项目的 `TRUSTROCKET.md` 与 `.trustrocket.json`
3. 本仓库的 TrustRocket 人类契约、机器契约与 Schema
4. 适用的 Capability 与 Handoff Contract
5. `SKILL.md` 的执行指南
6. 行业方法与执行者经验

行业术语不得覆盖明确业务规则。

## 文本与素材

- 默认使用 Markdown、JSON、YAML、TOML、CSV、Mermaid 与脚本。
- 二进制原件放入业务域的 `source/`；从原件切出的独立资源放入 `cut/`。
- 用户提供的素材使用 `user-` 前缀；公共来源不使用该前缀。
- 业务内容采用“平铺 Markdown + `source/` + `cut/`”，不得私自增加其他子目录。
- 默认不生成 DOCX、XLSX、PPTX、PDF 或图片包装；使用者明确要求时可以生成，同时优先保留文本事实源。

## Git 边界

TrustRocket 及其 Skills 默认只允许读取 Git 状态与历史。提交、推送、标签、合并、变基和发布必须由使用者明确要求；Genesis 与 Validator 不执行任何 Git 写操作。
