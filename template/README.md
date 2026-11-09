# TrustRocket 业务项目

本项目按 TrustRocket 管理客户服务、交付支持与客户成功内容。

## 四个业务域

| 目录 | 用途 |
|:--|:--|
| `装备材料/` | 面向客户、一线、渠道、实施和售后的可执行材料 |
| `技术支持/` | 问题标准化、诊断、解决、升级、反馈和验证 |
| `案例沉淀/` | 把一次性经验转成可检索、可复用能力 |
| `一线运营/` | 维护客户、POC、交付、售后、风险和健康度等外部业务状态 |

每个业务域采用“平铺 Markdown + `source/` + `cut/`”。不要自行增加其他子目录。

## 使用入口

- 人工执行先读 `TRUSTROCKET.md`。
- Agent 协作先读 `AGENTS.md`。
- 机器配置与素材来源登记位于 `.trustrocket.json`。
- 校验项目使用 TrustRocket 框架仓库的 `trust-rocket validate <项目目录>`。

默认使用 Markdown 和其他纯文本。正式 Word、Excel、PDF、PPT 或图片只有在明确要求时生成，并优先保留文本事实源。
