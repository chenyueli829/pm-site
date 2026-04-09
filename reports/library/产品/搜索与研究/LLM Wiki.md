# LLM Wiki — 深度研究（Karpathy 模式与开源实现）

**品类**：搜索与研究（个人知识编译 / 第二大脑） · **最后更新**：2026-04-09

- **模式原文（官方思想源）**：https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f（Andrej Karpathy《LLM Wiki》）
- **操作说明 / 实现文档**：https://github.com/SamurAIGPT/llm-wiki-agent（README、`CLAUDE.md` / `AGENTS.md` / `GEMINI.md` 为 agent 行为规格）
- **体验入口**：克隆仓库后在 **Claude Code / Codex / Gemini CLI 等** 中打开，按 README 使用 `/wiki-ingest`、`/wiki-query` 等（无独立 SaaS 控制台）

**说明**：「LLM Wiki」在 GitHub 上**不是单一官方产品仓库**，而是 Karpathy 提出的**可复用模式** + 多个**开源 Agent/Skill 实现**。下文以 **gist 模式** 为产品定义，以 **SamurAIGPT/llm-wiki-agent** 为代表实现（Star 与文档完整度较高，MIT）；另有 `nvk/llm-wiki`、`atomicmemory/llm-wiki-compiler` 等变体。选型对比见 **十四、与竞品的对比** 末表。

---

## 一、摘要

| 字段 | 内容 |
|------|------|
| 一句话介绍 | Andrej Karpathy 通过 **gist** 提出的 **LLM Wiki** 模式（约 2024 年前后公开讨论，确切节点 `to verify`），以 **开源 Agent 实现**（如 `llm-wiki-agent`）为载体，面向研究者与知识工作者，用 LLM **增量维护互链 Markdown 维基**，将知识从「每次临时 RAG」变为 **可累积、可审计的编译产物**。 |
| 目标用户 | 长期深耕主题的研究者、严肃阅读者、PKM 爱好者、竞争情报/投研、可用 Markdown + Git 的小团队。 |
| 核心工作流 | **Ingest**（`raw/` → 更新实体/概念/来源与索引）→ **Query**（基于维基综合，可**回写**）→ **Lint**（矛盾、孤儿、缺口）→ 可选 **Graph**（wikilink + 语义边）。 |

---

## 二、为何重要

- **相对 RAG 的「编译一次、持续复利」**：传统 RAG 多在查询时从碎片拼答案；LLM Wiki 强调 **维基是持久制品**，交叉引用与总览随新源更新。
- **对 PM**：同一 LLM 可把叙事从 **问答** 迁到 **可版本化知识制品**；**Schema 与 slash 命令** 即产品 SKU。
- **生态位**：与 **NotebookLM**、**Obsidian Copilot**、纯向量库 RAG 形成「沉淀形态」上的对照。

---

## 三、目标用户与使用场景

### 3.1 用户类型

| 类型 | 特征 |
|------|------|
| 研究者 / 投研 | 多源论文与报告，需要可链接的概念史与矛盾标注 |
| PKM 深度用户 | 接受本地文件 + Agent 维护成本 |
| 小团队 | Git 协作与审计优先于 SaaS |

### 3.2 高频场景

- 新项目/书籍：持续 ingest 源材料，维基随阅读生长。
- 复习与写作：Query 基于已整理页输出，好答案回写为合成页。
- 健康检查：Lint 与 graph 防止维基腐烂。

---

## 四、核心工作流与交互模型

### 4.1 心智模型

**Raw（只读真相） / Wiki（LLM 可写） / Schema（纪律）** 三层；把对话约束为 **知识库维护者**。

### 4.2 主路径与界面

在 **Claude Code / Codex / Gemini CLI** 中通过 slash 命令驱动 ingest、query、lint；人用 **Obsidian** 等读维基与图谱（gist 推荐）。

### 4.3 局限

需 **coding agent 环境**；非注册即用 SaaS；规模变大时成本与延迟上升。

---

## 五、核心产品功能

### 5.1 模块与入口

| 模块 | 作用 | 备注 |
|------|------|------|
| Raw 资料层 | 论文、剪藏、会议纪要等 | 不可变源 |
| Wiki 正文 | `sources/`、`entities/`、`concepts/`、`syntheses/` 等 | schema 因实现而异 |
| index.md / log.md | 目录与时间线 | 中等规模可不依赖向量库 |
| Ingest / Query / Lint | 维护与查询闭环 | 核心 SKU |
| Graph（可选） | `graph.html` 等 | `llm-wiki-agent` |

### 5.2 边界

强项在**个人/小团队可审计知识库**；不替代企业全域搜索（对照 **Glean**）或封闭笔记本 UI（对照 **NotebookLM**）。

### 5.3 套餐与版本

开源 **MIT** 等为主；**无平台订阅**；模型消耗为用户自接 API（`to verify` 各实现条款）。

---

## 六、关键技术分析

**整体结论**：价值在 **「文件树 + Git + schema 约束的批量写维」** ，非单次对话 state。

### 6.1 架构

长上下文任务从「答一题」变为 **多文件读写**；记忆落在 **仓库与历史**。

### 6.2 难点与突破

| 难点 | 要点 |
|------|------|
| 一致性 | schema 规定何时更新实体、总览、互链 |
| 综合与回写 | Query 读结构化页；好答案归档为新页 |
| 规模 | 可选 CLI 搜索（如 `qmd`，gist 提及） |

### 6.3 壁垒

**Schema 与命令设计**、社区模板；**非**独占模型或数据。

---

## 七、首次使用与重复使用

### 7.1 首次钩子

厌倦答案不沉淀；希望 **可链接、可演进** 的个人维基。

### 7.2 复访

新资料 ingest；lint/graph 维护；Obsidian 中直接消费成果。

### 7.3 弱点

上手门槛高；幻觉写入若无人复核会污染库。

---

## 八、痛点与缺口

### 8.1 已解决

文件夹堆料与跨文档脑补成本下降；结构化互链与日志可追溯（见 Q&A）。

### 8.2 未解决或部分解决

多文件写入的 **延迟与费用**；fork 标准不统一；依赖 **Agent 宿主** 政策；大众渗透率低于云产品。

---

## 九、差异化与护城河

### 9.1 关键差异化

**编译型知识制品** vs 会话型 RAG；**本地优先 + Git** vs 云账号体系。

### 9.2 护城河

个人/团队的 **资料与维基历史**；迁移实现有成本。

### 9.3 风险

见第八节与第十一节。

---

## 十、商业模式与增长

- **Karpathy gist**：思想开源，无商业产品。
- **实现仓库**：多为 MIT；增长靠 GitHub、叙事传播与 **Claude Code / Codex** 生态绑定。

---

## 十一、风险、弱点与待验证

- **幻觉写入**污染库；需人工复核与 lint。
- **无统一标准**，fork 互操作性差。
- **to verify**：各实现与模型厂商条款变更对 slash 命令的影响。

---

## 十二、PM 启示

### 12.1 启示

- **「检索即产品」vs「编译即产品」** 的叙事切换。
- **Schema 即产品**：`AGENTS.md`、slash 命令是交付物。
- **回写闭环** 是飞轮关键。

### 12.2 可关注点

与 **Obsidian**、**Cursor**、笔记本类产品的打包与分销关系。

---

## 十三、Product Q&A

| 问题 | 回答 |
|------|------|
| 什么会促使用户第一次使用？ | 厌倦「每次重新问、答案不沉淀」；想建可链接、可演进维基。 |
| 用户第二次为什么还会回来？ | 新资料 ingest；lint/graph 维护；Obsidian 读成果。 |
| 旧工作流痛点？ | 文件夹堆 PDF/笔记；RAG 不自动维护实体与矛盾。 |
| 核心护城河？ | 个人/团队资料与维基历史；切换实现有迁移成本。 |
| 聊天 vs 任务？ | **任务型**：ingest/query/lint 明确工作流。 |
| AI 是主角还是嵌入？ | **主角**：LLM 当维基维护者；阅读在 Obsidian/浏览器。 |
| 产出可编辑/可验证/可分享/可复用？ | Markdown **可编辑、可 Git diff**；事实须回溯 **raw** 核验。 |
| 变现？ | 开源多免费；**API 费用**用户自担；无平台抽成。 |

---

## 十四、与竞品的对比

| 维度 | **NotebookLM** | **典型向量 RAG** | **LLM Wiki** |
|------|----------------|------------------|----------------|
| 知识单元 | 笔记本内源 | 切片 | **维基页 + 链接网络** |
| 复利 | 会话/笔记本内 | 隐式索引 | **显式 markdown 仓库** |
| 协作 | Google 账号 | 因栈而异 | **Git** |

| 维度 | **Obsidian 纯笔记** | **LLM Wiki** |
|------|----------------------|--------------|
| 维护 | 人多手工 | **LLM 批量写改维**（人策展） |

### 相关仓库（选型参考）

| 仓库 | 说明 |
|------|------|
| [SamurAIGPT/llm-wiki-agent](https://github.com/SamurAIGPT/llm-wiki-agent) | 多 agent、slash、graph，MIT |
| [nvk/llm-wiki](https://github.com/nvk/llm-wiki) | Claude Code 插件向 |
| [atomicmemory/llm-wiki-compiler](https://github.com/atomicmemory/llm-wiki-compiler) | Knowledge compiler 叙事 |

*最后更新：2026-04-09*
