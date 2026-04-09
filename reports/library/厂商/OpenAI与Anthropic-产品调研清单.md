# OpenAI 与 Anthropic — 产品调研清单

**用途**：第一方产品全量 backlog；状态随深度研究文档更新。  
**最后更新**：2026-03-30（增补 Claude 多入口场景总览索引）

**官方链接结构化索引（Claude / Anthropic 文档 · 博客 · 案例）**：见同目录 `Claude与Anthropic-官方文档与资源导航.md`。

---

## Anthropic

| 产品 / SKU | 说明 | 深度研究文档 |
|------------|------|----------------|
| **Claude（Claude.ai）** | 消费者与专业用户对话助手、Artifacts、长上下文 | `../产品/通用助手/Claude.md` |
| **Claude Code** | 终端 / IDE / 桌面 / Web / Slack 等场景的编码代理（含 CLI） | `../产品/编程与构建/Claude Code.md` |
| **Claude Cowork** | 面向知识工作的桌面代理，Claude Code 同源能力泛化到文件与办公任务 | `../产品/编程与构建/Claude Cowork.md` |
| **Claude API / Console** | 开发者 API、密钥、用量、模型目录、与 Team/Enterprise 集成 | `../产品/编程与构建/Anthropic Claude API 与 Console.md` |
| **Claude 订阅与计划** | Free / Pro / Max / Team / Enterprise 等档位与权益边界 | 见 `Anthropic Claude API 与 Console.md` 内「商业与计划」；总体验见 `Claude.md` |
| **Claude Desktop** | 桌面客户端（承载 Cowork、Code 等能力的宿主之一） | 见 `Claude Cowork.md`、`Claude Code.md` |
| **安全与合规叙事** | Constitutional AI、滥用防护、企业合规材料 | 分散于官网与 docs；API 篇汇总入口 |

---

## OpenAI

| 产品 / SKU | 说明 | 深度研究文档 |
|------------|------|----------------|
| **ChatGPT** | 消费者助手、多模态、项目、深度研究等 | `../产品/通用助手/ChatGPT.md` |
| **ChatGPT 内 Agent / Operator（CUA）** | 计算机使用代理、浏览器式任务执行（能力与入口随版本整合在 ChatGPT） | `../产品/编程与构建/OpenAI Operator 与计算机使用代理.md` |
| **GPTs / GPT Store** | 自定义 GPT、生态分发 | 见 `ChatGPT.md`；细分可再拆篇 |
| **OpenAI Codex** | 编码代理：CLI、IDE 扩展、桌面 App、云端任务、企业治理 | `../产品/编程与构建/OpenAI Codex.md` |
| **OpenAI API / Platform** | Chat Completions、Responses、Batch、Files、推理与多模态模型目录等 | `../产品/编程与构建/OpenAI API 与开发者平台.md` |
| **Realtime API** | 低延迟语音与实时会话 | `OpenAI API 与开发者平台.md` 内章节 |
| **图像生成 API** | `gpt-image` 等图像模型（DALL·E 系列迁移以官方 deprecation 为准） | 同上 |
| **视频 / Sora** | Sora 产品与 Videos 相关 API（生命周期以官方公告为准） | `../产品/视频与数字人/Sora.md` |
| **Whisper** | 语音转写 API | `OpenAI API 与开发者平台.md` 内章节 |
| **Agent 构建栈** | Agent Builder、Agents SDK、ChatKit 等 | `OpenAI API 与开发者平台.md` 内章节 |
| **ChatGPT Business / Enterprise / Edu** | 团队与机构计划 | 见 `ChatGPT.md`；Codex 权益见 `OpenAI Codex.md` |

---

## 系统向对比（CLI / 桌面代理 / 编码）

| 主题 | 文档 |
|------|------|
| Claude 系列：Chat / 桌面 / CLI / IDE 插件等入口与场景 | `../品类/Claude系列-多入口与适用场景总览.md` |
| Claude Code vs OpenAI Codex vs Claude Cowork 定位与交互 | `../品类/编码与桌面代理系统-Claude Code-Codex-Cowork-对比.md` |

---

## 待跟进（to verify）

- 各产品在具体地区的上架情况、定价与套餐名称变更。
- Sora / 部分 API 的 deprecation 时间表与替代模型名称，以 [OpenAI 官方 deprecation 页面](https://platform.openai.com/docs/deprecations) 为准。
- Cowork 可用范围（计划档位、研究预览边界）以 [Anthropic Cowork 产品页](https://www.anthropic.com/product/claude-cowork) 为准。
