# TrustRocket 业务项目

本项目按 TrustRocket 管理客户服务、交付支持与客户成功内容。

## 四个业务域

| 目录 | 用途 |
|:--|:--|
| `装备材料/` | 面向客户、一线、渠道、实施和售后的可执行材料 |
| `技术支持/` | 问题标准化、诊断、解决、升级、反馈和验证 |
| `案例沉淀/` | 把一次性经验转成可检索、可复用能力 |
| `一线运营/` | 维护客户、POC、交付、售后、风险和健康度等外部业务状态 |

四域内可以按业务需要建立普通目录。任一目录直接包含 Markdown 时，在同级建立 `source/` 与 `cut/`；没有 Markdown 时默认不建立。基于文档创建的小程序或应用使用代码项目自身的目录结构。

## 项目级 Skills

`skills/` 保存本项目已经跑通、效果经用户确认、后续可重复使用的稳定流程。每个 Skill 使用 `skills/<skill-name>/SKILL.md` 作为入口，可按需携带 `scripts/`、`references/` 和 `assets/`。

临时脚本、一次性过程、未验证方案不进入 `skills/`。Agent 可以提议沉淀，但必须在用户明确确认后才能创建或更新项目级 Skill。

## 使用入口

- 人工执行和 Agent 协作都先读 `AGENTS.md`。
- 机器配置、素材来源和应用目录登记位于 `.trustrocket.json`。
- 校验项目使用 TrustRocket 框架仓库的 `trust-rocket validate <项目目录>`。

默认使用 Markdown 和其他纯文本。正式 Word、Excel、PDF、PPT 或图片只有在明确要求时生成，并优先保留文本事实源。
