# 编码与桌面代理系统对比：Claude Code · OpenAI Codex · Claude Cowork

**用途**：回答「有没有像 Claude Cowork、Claude CLI 体系统一的调研」——与单一产品深读配合使用。  
**最后更新**：2026-03-30

---

## 1. 结论先行

| 维度 | Claude Code | OpenAI Codex | Claude Cowork |
|------|-------------|--------------|---------------|
| **默认宿主** | 终端 / IDE / 桌面 / Web / Slack | CLI / IDE / App / 云环境 / 集成 | Claude **桌面应用** |
| **默认上下文** | 代码仓库与命令行环境 | 代码仓库 + 可选云端隔离环境 | 本地文件、文件夹与知识工作文档 |
| **默认用户画像** | 开发者 | 开发者（+ 企业治理角色） | 知识工作者（非以写代码为主） |
| **与「聊天产品」关系** | 与 Claude.ai / 订阅体系打通 | 与 **ChatGPT 档位** 深度捆绑 | 与 Claude 订阅 / 桌面分发打通 |
| **典型竞品参照** | OpenAI Codex、Cursor Agent | Claude Code、IDE 原生代理 | ChatGPT Operator（网页 GUI）、未来办公套件代理 |
| **深度研究文档** | `../产品/编程与构建/Claude Code.md` | `../产品/编程与构建/OpenAI Codex.md` | `../产品/编程与构建/Claude Cowork.md` |

三者共性：**委托式多步任务、工具调用、人在回路审批**；差异主要在 **上下文边界（代码 vs 文件 vs 网页）** 与 **分发宿主**。

---

## 2. 为何分开做产品（PM 视角）

- **代码仓库**：错误成本高，需 **diff 审阅、测试、Git 工作流**——产品形态偏开发者工具。
- **本地知识文件**：错误成本同样高，但用户不会跑 `pytest`——产品形态偏 **交付物（文档/表格）与权限最小化**。
- **浏览器 GUI**：网站不合作、登录态复杂——产品形态偏 **可暂停代理 + 高阶订阅**。

Anthropic 用 **Code** 与 **Cowork** 拆两条线，是在 **复用代理技术** 的同时 **避免一种界面强行服务两类用户**。

OpenAI 用 **Codex** 守开发者入口，用 **Operator/CUA** 守网页代理，并与 **ChatGPT** 合并发现面，是在 **超级 App** 战略下减少独立品牌。

---

## 3. 商业化与包装的异同

- **Claude Code / Cowork**：倾向绑定 **Anthropic 订阅与企业合同**，API 另线（Console）。
- **Codex**：倾向绑定 **ChatGPT 多档位 + 企业治理模块**（含 Security 等），与 **OpenAI Platform** 可形成双轨。
- 三者都面临同一道题：**自动执行权限** 与 **企业安全采购** 的对齐。

---

## 4. 一句话对比（关注点）

- **Claude Code**：「Anthropic 的官方编码代理，终端心智，和 Cowork 共享代理叙事。」
- **OpenAI Codex**：「OpenAI 的编码代理全家桶，开源 CLI + 云任务 + 企业治理，挂在 ChatGPT 权益上卖。」
- **Claude Cowork**：「把 Code 那套委托执行迁到桌面文件与知识工作，非开发者也能用代理出活。」

---

## 5. 相关清单

完整 SKU 与文档索引见：`../厂商/OpenAI与Anthropic-产品调研清单.md`。

---

*最后更新：2026-03-30*
