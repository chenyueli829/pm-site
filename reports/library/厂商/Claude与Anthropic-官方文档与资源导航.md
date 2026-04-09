# Claude 与 Anthropic — 官方文档与资源导航（结构化索引）

**用途**：按产品线整理的官网、文档、博客、案例等链接；便于检索与维护。  
**维护提示**：Claude Code 文档页量大且更新快，**完整机器可读索引**以官方为准：  
https://code.claude.com/docs/llms.txt  
**最后更新**：2026-03-30

---

## 0. 域名与分工（速查）

| 域名 / 入口 | 角色 |
|-------------|------|
| https://www.anthropic.com | 公司品牌、研究、新闻、客户案例、招聘、法律 |
| https://claude.ai | 消费者网页端 Claude（对话、Code Web 等） |
| https://claude.com | 定价、部分产品落地页与跳转（与 Claude 品牌统一） |
| https://docs.anthropic.com | **Claude API / 模型能力** 主文档站 |
| https://console.anthropic.com | API 密钥、用量、计费等控制台 |
| https://code.claude.com | **Claude Code** 产品站 + 文档（终端 / IDE / 桌面 / 集成） |
| https://platform.claude.com | **Claude Platform**：Agent SDK 等开发者文档与 Console 相关能力 |
| https://alignment.anthropic.com | 对齐与安全方向研究博客（Alignment Science） |

---

## 1. 消费端产品（Chat · 桌面 · 移动 · 定价）

### 1.1 使用入口

- 网页 Claude：https://claude.ai  
- Claude Code（浏览器）：https://claude.ai/code  
- 桌面应用下载（官方跳转，以页面为准）：  
  - https://www.anthropic.com/download  
  - 或自 https://code.claude.com/docs/en/overview 内「Desktop app」安装链接  

### 1.2 移动应用

- iOS：https://apps.apple.com/app/claude-by-anthropic/id6473753684  
- Android：https://play.google.com/store/apps/details?id=com.anthropic.claude  

### 1.3 定价与计划

- https://claude.com/pricing  
- Anthropic 侧定价总览（含产品筛选）：https://www.anthropic.com/pricing  

### 1.4 产品落地页（Anthropic）

- Claude 总览：https://www.anthropic.com/claude  
- Claude Cowork：https://www.anthropic.com/product/claude-cowork  
- Claude Code：https://www.anthropic.com/claude-code  
- 从其他助手导入记忆（若仍提供）：https://www.anthropic.com/import-memory  

---

## 2. Claude API 与 Console（开发者 · 模型调用）

### 2.1 控制台

- https://console.anthropic.com  

### 2.2 主文档站 `docs.anthropic.com`（入口与常见路径）

- 文档首页：https://docs.anthropic.com  
- Claude API 概览与指南（具体路径以左侧导航为准），常用锚点包括：  
  - API 参考、Messages、工具使用、批处理、文件、提示缓存、安全等（**请以站内最新目录为准**）  
- Claude Code（在 docs 站内的说明章节）：  
  - https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview  

> 说明：`docs.anthropic.com` 的章节会随模型与 API 形态调整；做集成时以 **Console 内链到当前版文档** 为准。

### 2.3 与云厂商集成（Claude Code 侧文档）

- Amazon Bedrock：https://code.claude.com/en/amazon-bedrock  
- Google Vertex AI：https://code.claude.com/en/google-vertex-ai  
- Microsoft Foundry：https://code.claude.com/en/microsoft-foundry  

---

## 3. Claude Code — 文档结构（`code.claude.com`）

### 3.1 产品与总入口

- 产品 / 营销首页：https://code.claude.com/  
- 文档总览（英文）：https://code.claude.com/docs/en/overview  
- **全量文档索引（llms.txt）**：https://code.claude.com/docs/llms.txt  

### 3.2 入门与概念

- Quickstart：https://code.claude.com/en/quickstart  
- Overview：https://code.claude.com/en/overview  
- How Claude Code works：https://code.claude.com/en/how-claude-code-works  
- Common workflows：https://code.claude.com/en/common-workflows  
- Best practices：https://code.claude.com/en/best-practices  
- Features overview（扩展能力总览）：https://code.claude.com/en/features-overview  
- Changelog：https://code.claude.com/en/changelog  

### 3.3 各运行环境

- 终端 / 安装与进阶：https://code.claude.com/en/setup  
- VS Code：https://code.claude.com/en/vs-code  
- JetBrains：https://code.claude.com/en/jetbrains  
- Desktop：https://code.claude.com/en/desktop  
- Desktop quickstart：https://code.claude.com/en/desktop-quickstart  
- Web：https://code.claude.com/en/claude-code-on-the-web  
- 平台与集成对比：https://code.claude.com/en/platforms  

### 3.4 CLI 与交互

- CLI reference：https://code.claude.com/en/cli-reference  
- Commands（内置命令）：https://code.claude.com/en/commands  
- Interactive mode：https://code.claude.com/en/interactive-mode  
- Terminal config：https://code.claude.com/en/terminal-config  
- Keybindings：https://code.claude.com/en/keybindings  
- Status line：https://code.claude.com/en/statusline  
- Voice dictation：https://code.claude.com/en/voice-dictation  

### 3.5 权限、安全与合规

- Permissions：https://code.claude.com/en/permissions  
- Permission modes：https://code.claude.com/en/permission-modes  
- Security：https://code.claude.com/en/security  
- Sandboxing：https://code.claude.com/en/sandboxing  
- Legal and compliance：https://code.claude.com/en/legal-and-compliance  
- Data usage：https://code.claude.com/en/data-usage  
- Zero data retention：https://code.claude.com/en/zero-data-retention  

### 3.6 记忆、技能、钩子、MCP、插件

- Memory（CLAUDE.md / auto memory）：https://code.claude.com/en/memory  
- Skills：https://code.claude.com/en/skills  
- Hooks guide：https://code.claude.com/en/hooks-guide  
- Hooks reference：https://code.claude.com/en/hooks  
- MCP：https://code.claude.com/en/mcp  
- Plugins：https://code.claude.com/en/plugins  
- Plugins reference：https://code.claude.com/en/plugins-reference  
- Discover plugins：https://code.claude.com/en/discover-plugins  
- Plugin marketplaces：https://code.claude.com/en/plugin-marketplaces  
- `.claude` 目录说明：https://code.claude.com/en/claude-directory  

### 3.7 子代理、团队、自动化

- Sub-agents：https://code.claude.com/en/sub-agents  
- Agent teams：https://code.claude.com/en/agent-teams  
- GitHub Actions：https://code.claude.com/en/github-actions  
- GitLab CI/CD：https://code.claude.com/en/gitlab-ci-cd  
- Code Review：https://code.claude.com/en/code-review  
- Scheduled tasks（会话内）：https://code.claude.com/en/scheduled-tasks  
- Web scheduled tasks（云端定时）：https://code.claude.com/en/web-scheduled-tasks  
- Headless / 程序化运行：https://code.claude.com/en/headless  

### 3.8 协作与外部系统

- Slack：https://code.claude.com/en/slack  
- Chrome（beta）：https://code.claude.com/en/chrome  
- Remote Control：https://code.claude.com/en/remote-control  
- Channels：https://code.claude.com/en/channels  
- Channels reference：https://code.claude.com/en/channels-reference  

### 3.9 模型、成本、观测

- Model configuration：https://code.claude.com/en/model-config  
- Costs：https://code.claude.com/en/costs  
- Fast mode：https://code.claude.com/en/fast-mode  
- Context window（说明/模拟）：https://code.claude.com/en/context-window  
- Monitoring / OpenTelemetry：https://code.claude.com/en/monitoring-usage  
- Analytics（团队用量）：https://code.claude.com/en/analytics  

### 3.10 企业与部署

- Third-party integrations / enterprise overview：https://code.claude.com/en/third-party-integrations  
- Network config：https://code.claude.com/en/network-config  
- LLM gateway：https://code.claude.com/en/llm-gateway  
- Server-managed settings：https://code.claude.com/en/server-managed-settings  
- Dev container：https://code.claude.com/en/devcontainer  
- Authentication：https://code.claude.com/en/authentication  

### 3.11 工具与参考

- Tools reference：https://code.claude.com/en/tools-reference  
- Checkpointing：https://code.claude.com/en/checkpointing  
- Output styles：https://code.claude.com/en/output-styles  
- Environment variables：https://code.claude.com/en/env-vars  
- Settings：https://code.claude.com/en/settings  
- Troubleshooting：https://code.claude.com/en/troubleshooting  

---

## 4. Claude Platform — Agent SDK（`platform.claude.com`）

> 与 Claude Code 同源工具与代理循环，面向 **代码集成 / 自动化管线**。

- 文档根（按需从站内导航展开）：https://platform.claude.com/docs  
- Agent SDK overview：https://platform.claude.com/docs/en/agent-sdk/overview  
- Quickstart：https://platform.claude.com/docs/en/agent-sdk/quickstart  
- Migration guide（自旧 Claude Code SDK 迁移）：https://platform.claude.com/docs/en/agent-sdk/migration-guide  
- 站内常见子主题（路径以侧边栏为准）：Hooks、Subagents、MCP、Permissions、Sessions、Skills、Slash commands、Plugins、User input / approvals 等  

### 4.1 Client SDK（直接调 API，自管工具循环）

- Anthropic Client SDK 说明：https://platform.claude.com/docs/en/api/client-sdks  

### 4.2 开源与问题反馈（SDK）

- TypeScript SDK Issues：https://github.com/anthropics/claude-agent-sdk-typescript/issues  
- Python SDK Issues：https://github.com/anthropics/claude-agent-sdk-python/issues  

---

## 5. 客户案例（Customers）

- 案例列表首页：https://www.anthropic.com/customers  
- 销售联系：https://www.anthropic.com/contact-sales  

以下为索引页中出现的部分案例详情页（**更多条目以 /customers 列表为准**）：

- https://www.anthropic.com/customers/slack  
- https://www.anthropic.com/customers/postman  
- https://www.anthropic.com/customers/circleci  
- https://www.anthropic.com/customers/descript  
- https://www.anthropic.com/customers/asana-qa  
- https://www.anthropic.com/customers/thomson-reuters-qa  
- https://www.anthropic.com/customers/epic-systems  
- https://www.anthropic.com/customers/airtree  
- https://www.anthropic.com/customers/anything  
- https://www.anthropic.com/customers/yoodli  
- https://www.anthropic.com/customers/pressmaster  
- https://www.anthropic.com/customers/cogent  
- https://www.anthropic.com/customers/esentire  
- https://www.anthropic.com/customers/zingage  
- https://www.anthropic.com/customers/tasklet  
- https://www.anthropic.com/customers/attention  

---

## 6. 新闻、博客与大众内容

### 6.1 新闻室 / 博客（同一内容流常见入口）

- Newsroom / Blog：https://www.anthropic.com/blog  
- 新闻列表（带参数时可能为筛选视图）：https://www.anthropic.com/news  

### 6.2 研究（公司站内）

- Research 首页：https://www.anthropic.com/research  
- 团队介绍：  
  - Alignment：https://www.anthropic.com/research/team/alignment  
  - Economic Research：https://www.anthropic.com/research/team/economic-research  
  - Interpretability：https://www.anthropic.com/research/team/interpretability  
  - Societal Impacts：https://www.anthropic.com/research/team/societal-impacts  

### 6.3 对齐科学博客（独立站）

- https://alignment.anthropic.com  

### 6.4 教育向 / 解释向内容

- Claude Explains：https://www.anthropic.com/claude-explains  

### 6.5 大型用户研究示例

- 81k 访谈项目：https://www.anthropic.com/81k-interviews  

---

## 7. 法律、信任、支持

- 商业条款等法律索引：https://www.anthropic.com/legal/commercial-terms（及站内 Legal 导航）  
- Cookie 政策等在各页脚「Legal」链出  
- 支持：请使用官网页脚 **Support** 或帮助中心入口（具体子域以官网展示为准）；通用联系：press / support 邮箱见 Newsroom 页面说明  

---

## 8. 与研究资料库的衔接

- Claude 多入口场景说明：`../品类/Claude系列-多入口与适用场景总览.md`  
- 单品深度研究：`../产品/通用助手/Claude.md`、`../产品/编程与构建/Claude Code.md`、`../产品/编程与构建/Claude Cowork.md`、`../产品/编程与构建/Anthropic Claude API 与 Console.md`  
- OpenAI / Anthropic 总清单：`OpenAI与Anthropic-产品调研清单.md`  

---

## 9. 变更说明

- 若某链接 404 或跳转，优先查 **对应站点的站内搜索** 或 **llms.txt / Changelog**。  
- JetBrains 插件市场：`https://plugins.jetbrains.com/plugin/27310-claude-code-beta-`（名称与 ID 以市场为准）。  

---

*文档为人工整理索引，不替代官方站点；引用以 Anthropic 当前页面为准。*
