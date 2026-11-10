<p align="center">
  <img src="https://img.shields.io/github/license/Toketec/TrustRocket?style=flat-square" alt="License">
  <img src="https://img.shields.io/badge/PRs-welcome-ff69b4?style=flat-square" alt="PRs Welcome">
</p>

<p align="center">
  🇨🇳 <b>中文</b> · <a href="README.en.md">🇬🇧 English</a>
</p>

<h1 align="center">🛡️ TrustRocket</h1>

<p align="center">
  <b>客户服务体系框架</b><br>
  <i>把「客户成功 / 客服 / 交付」从堆人手，变成一套人和 AI 都能遵守的内容规范</i>
</p>

<p align="center">
  **👤 Tony Wang (王圣滔)** — FLYKITES AI×Web3 资深技术专家 · 大湾区连续创业者 · 前鼎捷软件资深专家
</p>

<p align="center">
  <a href="#-快速开始">⚡ 快速开始</a> •
  <a href="#-为什么是-trustrocket">🎯 为什么</a> •
  <a href="#-四大核心价值">💎 核心价值</a> •
  <a href="#-命令一览">📟 命令</a> •
  <a href="#-适用场景">🏗️ 场景</a> •
  <a href="#-项目进度">🗺️ 进度</a>
</p>

---

## 🤯 痛点：服务体系的散沙困境

### 场景一：客户换了对接人，一切从头再来

```
客户：  "上次你们那个小王说好的交付流程，现在谁负责？"
你：    "小王离职了，我看看……群聊里应该有记录……"
        （翻了 20 个群、3 个邮箱、2 个网盘）
你：    "找到了……哦不对，这是三个月前的版本。"
```

SOP、话术、手册、客户档案散在群聊、邮件、个人脑子里。**人走了，服务就断档了。**

### 场景二：AI 想帮忙，却无从下手

```
你：    "帮我把这个客户的支持过程整理一下。"
AI：    "好的，请问 SOP 在哪？客户档案在哪？历史沟通记录在哪？"
你：    "……你自己找找？"
AI：    "我找不到结构化的东西，只能一问一答。"
```

没有结构化内容，AI Agent 只能被动回答，无法主动接手一整套服务动作。

### 场景三：文档写了一堆，谁都不看

```
一线：  "这个手册 30 页，我客户都等急了，没空看。"
渠道：  "你们到底该怎么做？给我一个能直接照着干的东西。"
新同事："入职一周了，还在自己摸索每个文档放在哪。"
```

没有规范的内容，既不好找、不好引，更沉淀不成可复用的技能。

### 核心问题

**所有问题的根因都一样：服务体系没有「单一事实源」，人和 AI 各说各话。**

- 知识散落 → 换人断档，AI 用不上
- 目录混乱 → 人找不到，AI 也找不到
- 内容无边界 → 写出来没人看，也复用不了

**TrustRocket 对这个问题的答案：**

> **一套内容规范，让人和 AI 站在同一份事实源上工作 —— 谁来都能接上，缺人了 AI 立刻顶岗。**

---

## 👤 作者的话

我是 **Tony Wang（王圣滔）**。现 FLYKITES PTE LTD（Singapore）AI×Web3 资深技术专家，大湾区连续创业者。

8 年从企业软件走到 AI Native——前鼎捷软件资深专家，主导过多个企业级 AI Native 落地项目。在把 AI 真正用进研发、用进业务的过程中，我反复撞见同一个现象：**研发能用 SpecRocket 标准化，但「卖出去之后」的客户服务，还是一片靠人肉堆出来的散沙。**

于是有了 TrustRocket。它和 SpecRocket 同源——**同一套「角色边界 + 产出物契约 + 流程闭环」的底层范式**，只是把战场从「造产品」移到了「留客户」。

它不是实验室理论，是从真实客户交付里磕出来的答案。欢迎提 Issue、提 PR，一起让它更好。

---

## 🎯 为什么是 TrustRocket

| # | 它解决什么 | 怎么解决的 |
|:-:|:----------|:----------|
| 1 | **知识散落** | 单一事实源（SSOT）——同一份内容，人与 AI 最大化复用，不重复造轮子 |
| 2 | **AI 用不上** | 结构化目录 + 内容规范——AI Agent 能读、能找、能接手整套服务动作 |
| 3 | **目录混乱** | 四大板块 + sources/cuts/apps/skills 约定——人好找，AI 也好找 |
| 4 | **内容难复用** | 内容生产规范——写出来能预览、能引用、能沉淀成技能 |
| 5 | **换人断档** | 目录结构能跟踪、能解释——人走了，事实还在 |
| 6 | **工具锁定** | 不是插件、不是 CLI 依赖，纯文件结构——**任何终端 + Git = 工作** |

> 💡 **它不是又一个文档模板。它是服务体系的人机协作协议。**

### 🔮 未来视角：即使 AI 内化了这套规范

有一天，AI 也许能自动整理客户资料、自动生成 SOP——你只需说"按标准流程来"。

那 TrustRocket 还有用吗？

**有，而且更重要了。** 因为你需要的不是一个"会做客服的 AI"，而是一套**团队能看懂的稳定事实源**：

| 场景 | 有 TrustRocket | 没有（AI 黑箱） |
|:----|:-------------|:--------------|
| 👥 **新人接手** | 打开四大板块目录，看「当前事实」即可上手 | "先跟前任聊一遍……" |
| 🤖 **AI 顶岗** | AI 读 `sources/` 和 `cuts/`，直接接手服务动作 | AI 一问三不知，只能闲聊 |
| 📄 **内容复用** | `cuts/` 切好的资源，随时引用、随时导出 | 每次重新找图、重新写 |
| 🔍 **追溯解释** | 目录结构能跟踪、能解释，人改和 AI 改都有迹可循 | "这文档是谁放的？放这干什么？" |
| 🏗️ **沉淀技能** | 成熟的流程沉淀进 `skills/`，下次一键复用 | 每次手忙脚乱重新摸索 |

**TrustRocket 交付的不是"整理文件"，而是「人能看懂、人能交接、AI 能接手」的实体工作产品。** 这些目录和 Git 一样久，比任何人的记忆都长。

即使明天所有 AI 都消失了，你的服务体系依然结构清晰、文档依然完整、换个人依然知道该做什么。

> **TrustRocket 的价值不在于教 AI 怎么做客服，而在于把该看的、该管的、该交接的东西，白纸黑字落进了目录。**

---

## 💎 四大核心价值

| 价值 | 说明 | 落点 |
|:----|:----|:----|
| **SSOT（单一事实源）** | 同一份内容，人与 AI 最大化参考复用，不重复造轮子 | 目录结构 + 文档维护边界 |
| **清晰可变的目录结构** | 四大板块自由生长，但约定让结构清晰、可追踪、可解释 | `sources/` `cuts/` `apps/` `skills/` 约定 |
| **优质的内容生产规范** | 人和 AI 写内容都有边界和引导，产出可复用、可预览、易协作 | 内容生产规范 |
| **先进的生产模式与管理经验沉淀** | 一套先进的客服体系生产模式与管理经验，随框架持续优化而沉淀为长期优势 | 框架本身（持续迭代中） |

> **判断任何一条新规则是否该加，标准只有一个：它是否让内容更可复用、让结构更好找、让生产更有边界。否则不加。**

---

## ⚡ 快速开始

### 📟 手动使用（没有 AI 工具）

```bash
git clone https://github.com/Toketec/TrustRocket.git
cd TrustRocket
./init.sh "我的服务体系"   # 或 ./init.sh（在当前目录初始化）
cd 我的服务体系
```

完成后项目骨架就位——四大板块目录（装备材料 / 技术支持 / 案例沉淀 / 一线运营）+ `skills/`，可直接开始往里放内容。

### 🤖 AI 使用（有 AI 工具）

先让 AI 拿到 `SKILL.md`（告诉它「这是你的工作规范」），AI 就能识别 `/trust-rocket` 命令：

**场景 A：新项目（空目录）**

```chat
你：/trust-rocket init "我的服务体系"
AI：复制骨架 → 引导式初始化（4 个问题：名称/服务对象/服务范围/现成材料）
→ 建好四大板块 + 按需先建子目录
```

**场景 B：有一堆杂乱材料**

```chat
你：/trust-rocket migrate ~/杂乱的客服文件
AI：扫描 → 按四大板块语义归类复制（零数据丢失）→ 生成映射表核对
```

> **斜杠命令是 AI 对话中的快捷指令**，像聊天一样输入，AI 自动识别执行。

---

## 📟 命令一览

| 命令 | 效果 | 执行方式 |
|:----|:-----|:---------|
| `init` | 建骨架 + git init + **引导式初始化**（4 问：名称/服务对象/服务范围/现成材料，可留空） | 📟 手动 / 🤖 斜杠命令 |
| `migrate` | **完整迁移**外部杂乱目录，按四大板块归类复制，**滴水不漏、零数据丢失**，源目录保留不动 | 🤖 AI 斜杠命令 |
| `preview` | 生成内容组织架构预览页 | 🤖 AI 斜杠命令 |
| `update` | 一键更新本地 skill + 升级老项目到最新模板 | 📟 手动 / 🤖 斜杠命令 |

---

## 📦 仓库结构

```
TrustRocket/
├── AGENTS.md                      ← 本仓库通用 AI 协作入口（只讲如何维护框架本身）
├── CLAUDE.md                      ← Claude Code 入口（引用 AGENTS.md）
├── SKILL.md                       ← 标准 skill 文件（AI 斜杠命令入口）
├── init.sh                        ← 手动 init 脚本（无 AI 时用）
├── trust-rocket                   ← CLI 脚本（init / migrate / preview / update）
├── trustrocket-convention.zh.md   ← 完整方法论正文（仅主仓库，不进入项目模板）
├── template/                      ← 项目模板框架（init/migrate 复制此目录）
│   ├── 装备材料/                    ← 板块一（客户可直接用的 SOP/手册/模板）
│   ├── 技术支持/                    ← 板块二（产品技术文档/故障排查/答疑）
│   ├── 案例沉淀/                    ← 板块三（成功案例/复盘/客户故事）
│   ├── 一线运营/                    ← 板块四（日常运营/客户跟进/进展状态）
│   ├── skills/                     ← 已确认可复用的技能
│   ├── AGENTS.md                   ← 完整项目执行规范
│   ├── CLAUDE.md
│   ├── README.md
│   └── .gitignore
├── README.md                      ← 🇨🇳 中文版
├── README.en.md                   ← 🇬🇧 English version
└── LICENSE                        ← MIT License
```

---

## 🏗️ 适用场景

| 场景 | 推荐路径 |
|:----|:---------|
| 🆕 **新建客服体系** | 📟 `./init.sh` 或 🤖 `/trust-rocket init` → 引导式初始化 |
| 🔄 **整理杂乱材料** | 🤖 `/trust-rocket migrate` → 归类复制 → 核对确认 |
| 👀 **看整体架构** | 🤖 `/trust-rocket preview` → 生成预览页 |
| ⬆️ **升级框架** | 📟 `./trust-rocket update` 更新 skill → 升级老项目 |
| 👥 **团队协作** | 四大板块目录 + `skills/`，人改和 AI 改都有迹可循 |
| 🤖 **AI 顶岗** | 缺人时 AI Agent 读 `sources/` `cuts/` 接手服务动作 |

---

## 🤖 Agent 兼容性

TrustRocket 设计为 **任何 AI 编码代理均可驱动**。只要你的 AI 工具能读文件，就能用。

| Agent | 识别方式 |
|:------|:---------|
| **Hermes Agent** | `SKILL.md` 标准格式 |
| Claude Code | `CLAUDE.md` 引用 `AGENTS.md`；斜杠命令读取 `SKILL.md` |
| Cursor / Windsurf / Cline / Roo Code | `AGENTS.md`；斜杠命令读取 `SKILL.md` |
| Trae / Codex CLI / Aider / OpenClaw | `AGENTS.md`；斜杠命令读取 `SKILL.md` |

> 不挑 AI，不锁平台。**`AGENTS.md` 是项目协作主入口，`SKILL.md` 是 TrustRocket 斜杠命令入口。**

---

## 🗺️ 项目进度

> 本节是 TrustRocket 整体功能进度的唯一维护位置，只记录粗粒度能力，不描述实现细节。

- [x] `init`（含 brainstorm 引导）/ `migrate` / `preview` / `update` 斜杠命令
- [x] 方法论正文（`trustrocket-convention.zh.md`）
- [x] 框架层 + 模板层结构
- [ ] 英文版 README（README.en.md）
- [ ] 英文版方法论正文

---

## 🤝 参与贡献

TrustRocket 是一个社区驱动的项目。欢迎各种形式的贡献：

- ⭐ **Star 仓库** — 最好的支持
- 🐛 **提 Issue** — 反馈 bug 或建议
- 🔧 **提交 PR** — 代码 / 文档 / 翻译
- 💬 **分享** — 写文章、录视频、发推

```bash
git clone https://github.com/Toketec/TrustRocket.git
cd TrustRocket
# 改完提 PR！
```

修改核心方法论时，请同步检查规范手册、Skill、项目模板、中英文 README 和命令实现中受影响的表达；它们必须各自独立可用，且语义一致。

---

## ❓ FAQ

### Q1: TrustRocket 和 SpecRocket 是什么关系？

**同源，不同战场。** 两者都遵循 RocketOS 的同一套底层范式——**角色边界 + 产出物契约 + 流程闭环**，让人和 AI 可以在同一套体系内无缝替换。

| | SpecRocket | TrustRocket |
|:-|:----------|:-----------|
| **战场** | 研发域（造出可卖的东西） | 服务域（让客户用出价值并留存） |
| **产出物** | spec 四文件、可交付代码 | SOP、客户档案、服务动作 |
| **角色** | PM / Dev / Ops | 客户成功 / 交付 / 客服 |

**一句话：SpecRocket 管「造」，TrustRocket 管「留」。** 两者同属于 RocketOS 这个大框架。

### Q2: TrustRocket 是一个「文档模板」吗？

**不是。** 它是一套**服务体系的人机协作协议**。

文档模板只是「给你一份现成的格式」，用完就结束了。TrustRocket 给的是**一套持续的约定**：目录怎么长、内容怎么写、人和 AI 怎么协作、技能怎么沉淀——它不是一次性的，是服务体系每天运转的骨架。

### Q3: 没有 AI，TrustRocket 还能用吗？

**能，这正是它的设计初衷。** TrustRocket 底层是一套**纯文件 + 目录约定**，和 AI 解耦：

- **有 AI** → AI 按 `AGENTS.md` / `SKILL.md` 接手服务动作，缺人时顶岗
- **没有 AI** → 团队照样按同一套目录和规范协作，人改人维护

AI 只是「执行层」里可替换的一员，不是这套体系成立的前提。

---

**MIT** — 属于 [Toketec](https://github.com/Toketec) 组织。

想干什么干什么。商用、改、二次分发，都可以。

---

<p align="center">
  <b>TrustRocket — 让客户成功，从堆人手变成一套规范。</b><br>
  <a href="https://github.com/Toketec/TrustRocket">GitHub</a> •
  <a href="https://github.com/Toketec/TrustRocket/issues">Issues</a> •
  <a href="https://github.com/Toketec/TrustRocket/discussions">Discussions</a>
</p>

<p align="center">
  <sub>🔥 如果这个项目对你有帮助，<a href="https://github.com/Toketec/TrustRocket">点个 ⭐</a> 让更多人看到</sub>
</p>
