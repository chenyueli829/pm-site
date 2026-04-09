# PM Site

产品经理个人网站，包含个人介绍、工作经历、技能矩阵、产品案例与深度研究报告。

## 在线访问

- **网站地址**：https://skill-deploy-tdzzilkm9q.vercel.app

## 项目结构

```
pm-site/
├── index.html          # 主页（Hero / 关于 / 经历 / 技能 / 项目 / 研究 / 联系）
├── report.html         # 研究报告阅读器（Markdown 渲染 + 目录导航）
├── reports/
│   ├── hermes-agent.md # Hermes Agent 深度研究报告
│   ├── mem-ai.md       # Mem AI 产品深度研究报告
│   └── claude-code-pm.md # Claude Code PM 效率提升研究
└── README.md
```

## 技术方案

- 纯静态站点（HTML + CSS + JS），无构建步骤
- [marked.js](https://github.com/markedjs/marked) CDN 实现 Markdown 渲染
- 通过 Vercel Claimable Deploy 部署，无需登录

## 部署

```bash
bash ../vercel-deploy-claimable/scripts/deploy.sh .
```

## 功能特性

- 暗色主题 + 渐变动效背景
- 滚动 reveal 动画、数字计数动效
- 响应式布局（移动端适配 + 汉堡菜单）
- 研究报告阅读器：阅读进度条、自动目录、Markdown 全格式支持
