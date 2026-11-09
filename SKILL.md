---
name: trust-rocket
description: "斜杠命令 /trust-rocket — 客户服务、交付支持与客户成功标准体系。子命令：genesis, equipment, support, case, operations, validate。"
license: MIT
metadata:
  version: "1.0.0"
---

# `/trust-rocket` — TrustRocket 执行指南

TrustRocket 是人可执行、机器友好的业务标准。Skill 负责把请求路由到权威 Contract 并指导执行，不取代 Contract，也不假定执行者一定是 AI。

## 权威来源与读取顺序

1. 当前任务中使用者的明确要求。
2. 目标项目的 `TRUSTROCKET.md`、`AGENTS.md` 和 `.trustrocket.json`。
3. 框架 `trustrocket-contract.zh.md`。
4. `trustrocket-contracts.json` 中对应的 Capability 与 Handoff。
5. 本 Skill 的流程说明。

只读取当前任务需要的域和关联内容；信息不足时再扩大范围。不得把 Prompt、工具习惯或行业术语当成高于业务契约的事实源。

## 命令

| 命令 | 用途 |
|:--|:--|
| `/trust-rocket genesis [init|normalize]` | 初始化空项目或安全规范化已有项目 |
| `/trust-rocket equipment` | 创建、改写、校验和反哺装备材料 |
| `/trust-rocket support` | 标准化、诊断、解决、升级和闭环问题 |
| `/trust-rocket case` | 检索、创建、合并、改进和反哺案例 |
| `/trust-rocket operations` | 收集外部状态、识别风险、汇总与分发反馈 |
| `/trust-rocket validate` | 校验目录、Markdown、素材、状态、二进制和配置边界 |

## 通用执行协议

所有命令先形成当前任务的最小 Execution Contract：

| 字段 | 必须回答的问题 |
|:--|:--|
| Goal | 要产生什么业务结果？ |
| Trigger | 为什么现在执行？ |
| Input | 已有事实、材料和证据是什么？ |
| Preconditions | 权限、信息、安全和环境前提是什么？ |
| Procedure | 哪些步骤能被合格执行者复现？ |
| Output | 产物是什么，放在哪里？ |
| Acceptance | 如何判断完成？ |
| Exception | 缺失、失败、冲突或不适用怎么办？ |
| Escalation | 何时升级，交给什么角色，带什么信息？ |
| Permission | 哪些可做、需审批或禁止？ |

执行者可以替换，但上述语义不变。AI 只在获授权范围内执行低风险动作；删除、覆盖、生产高风险操作、核心配置、安全策略、商业承诺、合同责任、重大客户沟通、事故定级和高风险恢复必须停在审批点。

## 通用内容规则

- 四域固定为装备材料、技术支持、案例沉淀、一线运营。
- 业务 Markdown 平铺在域根部；原件进 `source/`，切出资源进 `cut/`。
- 除 `source/` 与 `cut/` 外，不在业务域新增子目录。
- 用户素材和从中切出的资源使用 `user-` 前缀；公共素材不使用该前缀。
- 新增素材时在 `.trustrocket.json` 的 `materials` 登记相对路径、`origin` 和必要的 `approved_binary`。
- 默认写 Markdown 或其他纯文本；未经明确要求，不生成 DOCX、XLSX、PPTX、PDF 或图片包装。
- 截图优先保留原图；流程或关系只有在可无损表达时才转为 Mermaid、表格、列表或 ASCII。
- 业务 Markdown 最多三级标题；有子标题的标题不得直接有正文。
- 禁止创建 TrustRocket 自身进度、日志、待办、路线图状态或 AI scratchpad。
- 不把个人代理、本机用户目录、Token、Cookie、密钥、私有 DNS 和临时 workaround 写入项目。
- 未经使用者明确要求，不执行 Git 提交、推送、标签、合并、变基或发布。

## `/trust-rocket genesis`

### 初始化空项目

执行：

```bash
./trust-rocket genesis init <目标目录>
```

步骤：

1. 确认目标不存在或为空；系统元数据可忽略。
2. 从框架 `template/` 复制最小入口和四域资源目录。
3. 不创建空业务文档，不初始化 Git，不提交。
4. 运行 `./trust-rocket validate <目标目录>`。
5. 报告生成位置和校验结果。

如果当前不在 TrustRocket 仓库，先定位已安装或已克隆的 TrustRocket；没有可信模板时停止并请使用者提供框架位置，不凭记忆重建模板。

### 规范化已有项目

先只读执行：

```bash
./trust-rocket genesis normalize <目标目录>
```

按以下语义分类：

| 内容 | 候选去向 |
|:--|:--|
| 指南、手册、SOP、FAQ、培训、验收 | 装备材料 |
| 故障、问题、工单、诊断、日志处置 | 技术支持 |
| 案例、复盘、最佳实践、根因、经验 | 案例沉淀 |
| 客户、POC、交付、售后、风险、周运营 | 一线运营 |
| Word、Excel、PDF、截图、日志、配置、邮件导出 | 对应域 `source/` |
| 从原件切出的图片、页面、图表和附件 | 对应域 `cut/` |

文件名只能给出候选，不能代替内容判断。默认不移动、不覆盖、不删除。使用者要求安全补齐时执行：

```bash
./trust-rocket genesis normalize <目标目录> --apply
```

`--apply` 只创建缺失入口、四域、`source/` 和 `cut/`；归属有歧义的材料保持原位并输出建议。不可逆整理必须另行获得明确授权。

## `/trust-rocket equipment`

读取 `trustrocket-contracts.json` 中 `tr-cap-equipment`，然后执行：

1. 确认目标读者、使用场景、期望结果、版本、环境和风险。
2. 检索已有装备、案例和支持事实，确定新建、改写或校验。
3. 核对原件与来源；用户原件进入 `source/` 并使用 `user-` 前缀。
4. 选择最短可执行结构，不机械套模板。
5. 写清场景所需的前提、操作、正常结果、异常处理和升级条件。
6. 保留关键信息原图；只在无损时转为文本结构。
7. 校验标题、叶子标题、目录、权限、安全、事实和最小充分信息。
8. 判断是否需向案例、技术支持或一线运营形成 Handoff。

装备材料禁止大量背景铺垫、概念堆砌、重复总结、显而易见事项的长篇解释和为了完整增加章节。目标是让普通技术人员快速解决问题。

## `/trust-rocket support`

读取 `trustrocket-contracts.json` 中 `tr-cap-support`。不把技术支持简化成工单字段，也不把分类当成目的。

### 受理与标准化

至少确定：问题或请求、期望与实际、首次时间、当前状态、版本、部署、环境、配置、最近变化、影响、证据、已尝试动作、权限、敏感等级和响应期望。

入口可来自 IM、邮件、电话、工单、项目群、现场、AI、API 或监控；进入 Contract 后使用相同语义。

### 诊断与处置

1. 依据处理方式分类，可使用 Incident、Service Request、Problem、Defect、Configuration、Environment、Usage、Security 或 Requirement。
2. 判断影响、紧急程度、安全和升级路径。
3. 搜索已有案例与装备，核对适用版本、环境和限制。
4. 在授权范围复现和收集证据，区分事实、假设与未知。
5. 提出临时或永久方案，说明风险、回退、验证和审批点。
6. 由合格执行者执行；高风险动作必须先审批。
7. 按期望行为验证结果并反馈相关方。

### 关闭与反馈

关闭前必须判断：

- 是否要创建、合并或改进案例；
- 是否要新建或修正装备材料；
- 是否要更新一线运营中的外部业务状态；
- 是否确认或高度疑似产品缺陷，需要输出 `product-defect-to-specrocket` Handoff。

信息不足时输出缺口和最小补充清单；无法复现时保留证据和观测方案；不得虚构根因或验证。

## `/trust-rocket case`

读取 `trustrocket-contracts.json` 中 `tr-cap-case`，遵循“使用 → 解决 → 修正或创建 → 再复用”的知识循环。

1. 先检索近似案例，决定复用、修正、合并或新建。
2. 整理场景、目标或问题、环境、判断、处置、原因与结果。
3. 区分证实根因、工作假设、临时方案与永久方案。
4. 写清复用步骤、适用条件、不适用条件和反模式。
5. 处理客户身份、安全、配置和日志中的敏感信息。
6. 形成装备更新、支持引用、一线推广或外部 Rocket Handoff。

案例不是会议纪要；只记录发生过程而不能让下一位人员判断和执行的内容不满足验收。重复案例优先收敛到单一当前事实，历史由 Git 保存。

## `/trust-rocket operations`

读取 `trustrocket-contracts.json` 中 `tr-cap-operations`。本命令维护外部业务对象状态，不维护 TrustRocket 自身状态。

1. 确认对象、场景、事实来源、当前状态、影响、依赖和时间。
2. 区分事实、判断、建议与未知。
3. 识别风险、重大事项、长期未闭环、等待客户或等待研发。
4. 明确下一动作、负责人角色、等待方、截止条件和升级阈值。
5. 根据使用者需要输出一线或管理层最小充分汇报。
6. 把问题路由到技术支持、案例沉淀、装备材料或外部 Rocket。

ToB 的项目、POC、交付、SLA、续费与企业健康度，以及 ToC 的用户规模、服务质量、故障影响、留存与自助效果均使用同一 Contract，不创建两套目录。

## `/trust-rocket validate`

执行：

```bash
./trust-rocket validate <项目目录>
```

校验器必须只读项目并检查：

- 四域和每域 `source/`、`cut/`；
- 业务域非法子目录；
- Markdown 四级及更深标题；
- 非叶子标题直接正文；
- `.trustrocket.json` 素材来源与 `user-` 前缀；
- 未明确许可的生成型二进制包装；
- `STATUS.md`、`PROGRESS.md`、`WORKLOG.md`、`TODO.md` 等框架状态文件；
- 个人代理、本机路径、Token、Cookie、密钥等疑似泄漏；
- `TRUSTROCKET.md`、`AGENTS.md` 与机器配置入口。

原始 `source/` 中的个人配置命中作为警告，因为它可能是诊断证据；规则、配置和业务 Markdown 中的命中作为错误。`一线运营/客户A项目状态.md` 等外部业务状态合法。

验证失败只报告具体路径、规则和修复方向，不自动修改内容。

## Handoff 路由

| 场景 | 使用的 Handoff |
|:--|:--|
| 重复或可复用技术问题 | `tr-ho-repeated-issue-to-case` |
| 案例可转为一线装备 | `tr-ho-case-to-equipment` |
| 装备需要推广与观察 | `tr-ho-equipment-to-operations` |
| 产品缺陷交研发 | `tr-ho-product-defect-to-specrocket` |
| 普遍需求或机会 | `tr-ho-operations-demand-routing` |

Handoff 只定义来源、目标、触发、输入、输出、验收、责任角色和敏感等级。不得把跨体系交接实现成对目标体系内部脚本、目录或数据库的依赖。

## 完成报告

完成命令后只报告实际产物、关键判断、验证结果、未完成项与需要使用者决定的风险。不要创建进度文档、工作日志或 AI 报告来证明工作。

如果修改具有清晰原子性，可以建议人工提交并给出 commit message，但不得自行提交。
