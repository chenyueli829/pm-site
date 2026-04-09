# Claude Code 提升产品经理工作效率 — 研究计划

## 研究目标
系统研究 Claude Code 如何提升产品经理（PM）的工作效率，聚焦三个核心问题：
1. **产出方案**：Claude Code 如何加速 PRD、产品策略、需求文档等方案类产出？
2. **竞品调研**：Claude Code 如何自动化竞品分析、市场研究、用户反馈采集？
3. **流程自动化**：如何利用 Skills/Hooks/MCP/Subagents 构建可复用的 PM 自动化工作流？

最终交付物：一份可直接落地的 **PM × Claude Code 效率提升方案**，包含工具配置指南、工作流模板和实践案例。

## 查询类型
深度优先 + 实操导向：聚焦 Claude Code 的 PM 应用场景，深入拆解功能机制和最佳实践，而非广度覆盖产品本身。

## 研究对象判断
- **研究类型**：工具应用方法论研究（非公司/产品分析）
- **所属领域**：AI 生产力工具 × 产品管理工作流
- **重点关注维度**：核心能力机制、PM 场景适配、自动化工作流设计、与竞品工具对比
- **不适用维度**：融资估值、公司治理、市场规模（TAM/SAM/SOM）

## 信息来源策略
| 来源 | 用途 |
|------|------|
| Anthropic 官方文档 (code.claude.com/docs) | 功能机制、API 说明、最佳实践 |
| Sachin Rekhi 博客/视频 | PM 工作流框架、五步法、实操案例 |
| prodmgmt.world / ccforpms.com | PM 专属技巧库、Skills 模板 |
| GitHub (deanpeters/Product-Manager-Skills 等) | 开源 PM Skills 仓库、命令模板 |
| Reddit (r/ClaudeCode, r/ProductManagement) | 真实 PM 用户反馈、工作流分享 |
| Medium / Substack 技术博客 | 深度教程、自动化案例 |
| YouTube | 演示视频、工作流 Walkthrough |
| 中文社区（知乎、即刻、微信公众号） | 中文 PM 视角 |

---

## 动态子任务列表

### 子任务 1：Claude Code 核心能力机制拆解
- **目标**：系统梳理 Claude Code 与 PM 工作相关的核心功能模块及其工作原理
- **重要性**：理解工具能力边界是设计工作流的前提
- **工具/来源**：Anthropic 官方文档、Builder.io 更新总结、Medium 技术文章
- **搜索关键词**：Claude Code features 2026, CLAUDE.md, Skills, Hooks, MCP, Subagents, Custom Commands, AutoDream, Dispatch
- **重点信息点**：
  - CLAUDE.md 项目上下文机制
  - Skills（可复用工作流包）
  - Custom Slash Commands（/命令触发）
  - Hooks（确定性自动执行脚本）
  - MCP（外部服务集成协议）
  - Subagents（并行子任务隔离执行）
  - AutoDream（结构化规划）
  - Cloud Execution & Scheduled Tasks
- **预期输出**：功能模块清单表 + 与 PM 工作的关联映射
- **优先级**：高
- **可否并行**：是

### 子任务 2：PM 核心场景适配 — 方案产出
- **目标**：拆解 Claude Code 在 PRD、产品策略、需求文档等方案类产出中的应用方式
- **重要性**：方案产出是 PM 最耗时的日常工作之一
- **工具/来源**：Sachin Rekhi 指南、prodmgmt.world Skills 库、GitHub PM Skills 仓库
- **搜索关键词**：Claude Code PRD generation, product strategy critique, release notes automation, /pm-prd, /pm-story, product spec template
- **重点信息点**：
  - PRD 自动生成工作流（模板 + 上下文 + 迭代）
  - 产品策略文档撰写与批判
  - 用户故事 & 验收标准生成
  - Release Notes 自动化
  - 会议纪要 → 行动项提取
  - Sachin Rekhi 五步法详解
- **预期输出**：场景 × 工作流对照表 + 实操步骤 + 模板示例
- **优先级**：高
- **可否并行**：是

### 子任务 3：PM 核心场景适配 — 竞品调研
- **目标**：拆解 Claude Code 在竞品分析、市场研究中的自动化能力
- **重要性**：竞品调研是 PM 高频需求，手动耗时巨大
- **工具/来源**：mcpmarket.com 竞品分析 Skill、Reddit 用户案例、Medium 教程
- **搜索关键词**：Claude Code competitive analysis skill, market research automation, competitor pricing scraping, feature comparison matrix
- **重点信息点**：
  - 竞品信息自动采集（Web Search + 网页抓取）
  - 功能对比矩阵自动生成
  - 定价对比自动化
  - 用户评价采集与情感分析
  - 多竞品并行研究（Subagents）
  - 研究报告结构化输出
- **预期输出**：竞品调研自动化工作流 + Skill 模板 + 案例演示
- **优先级**：高
- **可否并行**：是

### 子任务 4：自动化流程设计 — Skills/Hooks/MCP 实操指南
- **目标**：设计一套可直接落地的 PM 自动化工作流体系
- **重要性**：从"单次使用"升级为"系统化自动化"是效率飞跃的关键
- **工具/来源**：Claude Code 官方文档、GitHub 模板仓库、Sachin Rekhi 自动化章节
- **搜索关键词**：Claude Code skill definition, .claude/commands/, hooks setup, MCP Notion Linear, scheduled tasks PM, agent swarm workflow
- **重点信息点**：
  - Skill 编写规范与最佳实践
  - Slash Command 定义方法
  - Hook 触发场景与配置
  - MCP 集成配置（Notion / Linear / Slack / Google Drive）
  - Scheduled Tasks 定期执行
  - 多 Agent 协作（Agent Swarm / Dispatch）
  - CLAUDE.md 上下文工程
- **预期输出**：自动化架构图 + 配置指南 + 推荐 MCP 清单
- **优先级**：高
- **可否并行**：部分依赖子任务 1 的能力梳理，但可先行启动

### 子任务 5：工具对比 — Claude Code vs 其他 PM AI 工具
- **目标**：对比 Claude Code 与 Cursor、ChatGPT、Perplexity、Replit 等在 PM 场景下的优劣
- **重要性**：帮助 PM 选择最适合的工具组合
- **工具/来源**：对比评测文章、Reddit 讨论、prodmgmt.world
- **搜索关键词**：Claude Code vs Cursor PM, Claude Code vs ChatGPT research, PM AI tool stack 2026, Claude Code limitations PM
- **重点信息点**：
  - Claude Code vs Cursor（IDE 内 vs 终端）
  - Claude Code vs ChatGPT/Perplexity（研究深度 vs 即时搜索）
  - Claude Code vs Replit（编码深度 vs 零代码原型）
  - 最佳工具组合推荐
  - Claude Code 的局限性
- **预期输出**：工具对比矩阵 + 场景推荐表 + 组合策略
- **优先级**：中
- **可否并行**：是

### 子任务 6：★ 综合判断与落地建议
- **目标**：整合所有发现，输出可执行的效率提升方案
- **重要性**：研究的最终价值在于可落地性
- **工具/来源**：前 5 个子任务的输出
- **重点信息点**：
  - PM 效率提升量化评估
  - Quick Win（立即可用）vs 长期建设路径
  - 风险与注意事项
  - 推荐的项目文件结构
  - 30 天上手路线图
- **预期输出**：执行方案 + 路线图 + 项目模板
- **优先级**：高
- **可否并行**：否（依赖其他子任务完成）

---

## 子代理分配方案

### SubAgent 1：能力机制 + 方案产出
- **负责子任务**：子任务 1（核心能力拆解）+ 子任务 2（方案产出场景）
- **输入**：官方文档、Sachin Rekhi 指南、PM Skills 仓库
- **职责**：梳理 Claude Code 功能全景，重点拆解方案产出类工作流
- **输出格式**：能力清单表 + 场景工作流 + 模板示例

### SubAgent 2：竞品调研 + 自动化实操
- **负责子任务**：子任务 3（竞品调研）+ 子任务 4（自动化流程设计）
- **输入**：MCP 文档、Skill 模板、自动化案例
- **职责**：设计竞品调研自动化流程，编写可复用的配置指南
- **输出格式**：调研工作流 + Skill 模板 + 配置指南

### SubAgent 3：工具对比 + 综合建议
- **负责子任务**：子任务 5（工具对比）+ 子任务 6（综合判断）
- **输入**：对比文章、用户反馈 + 前两个 SubAgent 的输出
- **职责**：完成工具对比，整合所有发现为可执行方案
- **输出格式**：对比矩阵 + 执行方案 + 路线图
- **依赖**：SubAgent 1 & 2 完成后启动综合建议部分

**并行策略**：SubAgent 1 & 2 可完全并行；SubAgent 3 的工具对比部分可并行，综合建议部分需等待前两个完成。

---

## 信息整合策略
- **交叉验证**：官方文档功能说明 vs 用户实际使用反馈；Sachin Rekhi 等 KOL 推荐 vs Reddit 社区真实体验
- **矛盾识别**：Claude Code 宣称的 PM 能力 vs 实际局限（如深度搜索不如 Perplexity）
- **可信度评估**：优先采信官方文档 + 多人验证的实操经验；单一博客标注"待验证"
- **缺失信息处理**：效率提升的量化数据（节省多少小时）可能缺乏，标注"基于用户自述，未经严格量化"
- **风险点识别**：API 成本、Token 消耗、数据隐私、幻觉风险

---

## 预期报告结构
1. **Executive Summary** — 一段话核心结论
2. **Claude Code 核心能力全景** — 与 PM 工作相关的功能模块清单
3. **场景一：方案产出加速** — PRD/策略/需求文档的工作流详解
4. **场景二：竞品调研自动化** — 从信息采集到报告生成的全流程
5. **场景三：流程自动化体系** — Skills/Hooks/MCP/Subagents 配置指南
6. **工具对比与组合策略** — Claude Code vs 其他工具的最佳搭配
7. **项目模板与文件结构** — 开箱即用的 PM 项目脚手架
8. **30 天上手路线图** — 从入门到系统化的分阶段行动计划
9. **风险与局限** — 成本、隐私、幻觉等注意事项
10. **结论与建议** — 核心判断 + 下一步行动
