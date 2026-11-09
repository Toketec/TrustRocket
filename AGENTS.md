# TrustRocket — 协作入口

本文件是维护 TrustRocket 框架仓库时的主协作规则。业务项目规则位于 `template/AGENTS.md`。

## 权威来源

- `trustrocket-contract.zh.md`：人可读总契约。
- `trustrocket-contracts.json`：四域能力与跨域、跨体系 Handoff 的机器契约。
- `execution-contract.schema.json`、`handoff.schema.json`：机器可校验的契约结构。
- `trustrocket-convention.zh.md`：方法论正文。
- `SKILL.md`：`/trust-rocket` 的完整执行规范。
- `template/`：Genesis 分发到业务项目的最新骨架。
- `trust-rocket`：初始化、规范化与校验实现。

规则变化时只更新受影响内容，但必须保证总契约、Schema、Capability、Skill、模板与校验器的含义一致，各入口可独立使用。

## 框架边界

- TrustRocket 是 Operating Framework，不建设 CRM、工单 SaaS、客户数据库、RAG 或 Agent 平台。
- 四个一级业务域固定为：装备材料、技术支持、案例沉淀、一线运营。
- 框架仓库不得把自身源码塞入四域目录；四域目录属于初始化后的业务项目。
- 执行契约必须独立于 Human、AI 或具体软件；执行者只在能力、权限和责任边界上不同。
- ToB 与 ToC 使用同一套四域和契约，通过上下文参数、Policy 与 Workflow 表达差异。
- 跨 Rocket 协作只定义 Handoff Semantic，不依赖对方内部代码。

## 内容与状态边界

- 默认使用适合 Git 的纯文本；二进制不得成为唯一事实来源。
- 业务项目采用“平铺 Markdown + `source/` + `cut/`”，不得私增业务子目录。
- TrustRocket 自身不维护开发进度、工作日志、AI 过程、待办或路线图状态文件；历史由 Git 承担。
- 客户、项目、POC、交付、故障、服务、SLA 与外部依赖的真实业务状态允许在一线运营中维护。
- 不把个人代理、用户目录、Token、Cookie、密钥或本机 workaround 写入框架、模板或配置。

## 修改规则

- 保留用户已有内容；不得默认删除、覆盖或大规模移动。
- Genesis 的安全应用只能补齐缺失入口和目录；有歧义的内容只给出建议。
- 新增自动规则时必须提供对应契约测试。
- Markdown 业务文档只允许一至三级标题；有子标题的标题不得直接承载正文。
- 用户素材与由其切出的资源使用 `user-` 前缀，公共素材不得伪装成用户素材。
- 禁止自动执行 Git 提交、推送、标签、合并、变基和发布。

## 验证范围

修改 Genesis、契约或 Validator 时，在隔离临时目录实际执行初始化、规范化与校验；同时校验机器契约满足 Schema。验证结果只在当前回复报告，不在仓库保存测试夹具、验证报告、进度文件或工作日志。
