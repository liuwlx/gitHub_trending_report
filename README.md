# GitHub Trending Report

一个面向中文读者的 GitHub Trending 每日报告仓库。

项目每天读取仓库内的 `skill-github-trending-report`，抓取 GitHub Trending、Explore 与重点仓库公开资料，先生成可审计的 Markdown 内容底稿，再复用固定 HTML 模板生成适合浏览的日报页面。

它不是把 Trending 榜单机械翻译一遍，而是尽量回答四个更有用的问题：

- 这个项目到底是什么？
- 它主要解决什么问题？
- 谁值得点进去看？
- 当前结论有哪些证据边界？

## 最新报告

<!-- latest-report:start -->
- 报告日期：**2026-07-20**
- [查看 Markdown 报告](md/github_trending_report_2026-07-20.md)
- [查看 HTML 源文件](html/github_trending_report_2026-07-20.html)
- [查看项目架构分析](analysis/2026-07-20/README.md)
- 深度解析：[Wigolo](analysis/2026-07-20/KnockOutEZ__wigolo.md) · [Jcode](analysis/2026-07-20/1jehuang__jcode.md) · [Kimi CLI](analysis/2026-07-20/MoonshotAI__kimi-cli.md)
<!-- latest-report:end -->

> GitHub 默认会把 HTML 当作源码显示。下载 `.html` 文件后用浏览器打开，可以查看完整的主题切换和项目详情展开效果。

## 项目特点

- **Trending + Explore**：关注当天全语言趋势榜，并使用 Explore 作为补充信号。
- **证据优先**：除仓库描述外，还会读取 README、About、Homepage、Release 和官方文档。
- **先 Markdown，后 HTML**：Markdown 是内容事实基线，HTML 只负责忠实映射，不在渲染阶段重新编故事。
- **固定模板**：后续日报继续复用已经验收的 `2026-03-16` 页面底板，不每天换一张皮。
- **Top 12 深度解读**：每个项目都保留“项目摘要、核心特性、技术栈、适用场景、一句话推荐”。
- **诚实降级**：证据不足、Explore 获取失败或性能数据未经独立验证时，会明确说明。
- **历史归档**：Markdown 与 HTML 按日期分别保存在 `md/` 和 `html/`。

## 工作流程

```text
读取 user-rules 与固定模板
          ↓
抓取 GitHub Trending / Explore
          ↓
读取重点仓库与官方资料补证
          ↓
Markdown Writer 生成完整内容底稿
          ↓
UI/UX Agent 审校信息层级与密度
          ↓
Frontend Agent 映射到固定 HTML 模板
          ↓
结构、交互、事实与降级说明验收
          ↓
推送 Markdown、HTML 并更新最新报告链接
```

核心约束：

1. 必须先生成 Markdown，再进入 HTML 阶段。
2. 不允许重新设计固定模板的主题、区块顺序和展开交互。
3. 不允许用 Python 或固定渲染器代写最终 HTML。
4. 不确定的能力和数据必须保留 `Honest Caveat`，不能脑补。
5. GitHub Trending 原始排名与 Stars Today 增速需要分开理解。

## 仓库结构

```text
.
├── .codex/
│   └── skills/
│       └── skill-github-trending-report/
│           ├── SKILL.md
│           ├── README.md
│           ├── README.zh-CN.md
│           ├── agents/
│           │   ├── markdown-report-writer-agent.md
│           │   ├── ui-ux-designer-agent.md
│           │   └── frontend-engineer-agent.md
│           ├── reference/
│           │   ├── user-rules.md
│           │   ├── fixedBaseTemplate_2026-03-16.html
│           │   ├── uiEngineeringSpec.md
│           │   └── reportMarkdownTemplate.md
│           ├── examples/
│           └── tests/
├── md/                       # 每日 Markdown 内容底稿
├── html/                     # 每日 HTML 日报
├── DAILY_TASK_PLAN.md        # 每日自动任务契约
└── README.md
```

## Skill 入口

主流程定义在：

[` .codex/skills/skill-github-trending-report/SKILL.md`](.codex/skills/skill-github-trending-report/SKILL.md)

执行时的规则优先级：

1. `reference/user-rules.md`
2. `reference/fixedBaseTemplate_2026-03-16.html`
3. `reference/uiEngineeringSpec.md`
4. 当天生成的 Markdown 内容底稿
5. `reference/reportMarkdownTemplate.md`

## 手动生成日报

在支持读取 Codex Skill 和 GitHub 仓库的 Agent 环境中，可以使用类似指令：

```text
读取当前仓库中的 .codex/skills/skill-github-trending-report/SKILL.md，
严格遵守 user-rules 和固定模板工作流，生成今天的 GitHub Trending 日报。
先写入 md/github_trending_report_YYYY-MM-DD.md，
验收通过后再写入 html/github_trending_report_YYYY-MM-DD.html，
最后更新 README 的最新报告链接。
```

生成文件命名：

```text
md/github_trending_report_YYYY-MM-DD.md
html/github_trending_report_YYYY-MM-DD.html
```

## 每日自动任务

默认任务计划：

| 设置 | 内容 |
|---|---|
| 频率 | 每天一次 |
| 时间 | 日本时间 09:00 左右 |
| 数据范围 | GitHub Trending · Repositories · Any language · Today |
| 输出 | Markdown + HTML |
| 发布位置 | `main` 分支下的 `md/` 与 `html/` |
| 最后动作 | 更新本 README 的“最新报告”区块 |

完整执行步骤、幂等规则、失败处理和验收标准见：

[DAILY_TASK_PLAN.md](DAILY_TASK_PLAN.md)

## 报告页面固定结构

最终 HTML 始终保留以下阅读顺序：

1. 主题切换按钮
2. Header / Hero
3. 4 张统计卡
4. 今日洞察
5. 今日热门 Top 12
6. 编程语言分布
7. GitHub Explore 精选
8. Footer

Top 12 的每个项目支持展开阅读，详情顺序固定为：

1. 项目摘要
2. 核心特性
3. 技术栈
4. 适用场景
5. 一句话推荐

## 数据说明

- GitHub Trending 是动态页面，同一天不同时间看到的数据可能不同。
- GitHub 没有公开 Trending 的完整排名算法，报告不会把排名解释成严格的质量评分。
- Stars Today 适合观察热度变化，但不能单独证明项目成熟度、安全性或生产可用性。
- 项目方自行披露的性能数据会标明来源，未经独立验证时不会作为确定事实下结论。

## 失败策略

- Trending 抓取失败：终止当日报告，不用旧数据冒充新数据。
- Explore 抓取失败：允许降级，但必须在 Markdown 和 HTML 中说明。
- 项目资料不足：保留能确认的事实，并写明 `Honest Caveat`。
- GitHub 写入失败：明确指出失败文件和阶段，不声称已经发布成功。

## 后续方向

- 增加连续上榜天数和昨日排名变化。
- 增加 Star 增速异常提醒。
- 增加语言或技术领域专项榜单。
- 通过 GitHub Pages 提供可直接浏览的历史报告站点。
- 增加日报生成和模板结构的自动验收。

---

本仓库中的报告基于公开信息整理，仅用于技术观察和项目发现，不构成安全审计、投资建议或生产选型结论。
