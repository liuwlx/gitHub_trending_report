---
name: skill-github-trending-report
version: 0.9.0
description: 抓取 GitHub Trending 与 Explore 数据，先生成 Markdown 日报，再驱动项目架构分析 Agent 产出独立技术档案，最后由 UI/UX 与前端 Agent 基于固定模板生成 HTML 日报。
---

# Skill: GitHub Trending Report

这个 skill 采用固定模板优先、证据优先和分层阅读的工作方式：

- 抓取 GitHub Trending / Explore 与重点仓库公开信息。
- 先生成本地 Markdown 内容底稿。
- 从日报中筛选值得深挖的开发项目，生成独立架构解析文档。
- 再基于 `2026-03-16` 已验收成品页生成 HTML。

当前目标不是重新设计日报，而是持续复用已经认可的页面，只替换当天内容，并在日报之外沉淀可检索的项目技术档案。

## Hard Rules

- `reference/user-rules.md` 是 HTML 生成的最高优先级约束。
- `reference/fixedBaseTemplate_2026-03-16.html` 是固定 UI 底板，不是灵感参考。
- 必须先生成 Markdown 日报，再执行项目架构分析和 HTML 阶段。
- 最终 HTML 必须由当前 AI 直接写出或改写，不允许交给 Python 或本地渲染脚本代写。
- 不允许重新设计主题、区块顺序、展开详情结构、关键 class 名称或交互命名。
- `项目摘要 / 核心特性 / 适用场景 / 一句话推荐` 必须从用户视角出发，说人话，降低认知负荷。
- 项目架构分析必须以源码、配置、依赖清单和官方文档为证据，不得根据目录名脑补调用关系。
- 如果 GitHub 仓库页与 README 不足以解释项目，必须继续查看源码、官网、文档或公开搜索结果。
- 如果运行环境不支持真实 subagent，也必须依次读取各 Agent 定义并严格模拟其职责，不允许跳过。

## Required References

执行时优先读取：

1. `reference/user-rules.md`
2. `reference/fixedBaseTemplate_2026-03-16.html`
3. `reference/uiEngineeringSpec.md`
4. `reference/reportMarkdownTemplate.md`
5. `agents/markdown-report-writer-agent.md`
6. `agents/ui-ux-designer-agent.md`
7. `agents/frontend-engineer-agent.md`
8. 仓库根目录 `agents/project-architecture-analyst-agent.md`
9. `examples/github-trending-report-example.md`
10. `tests/evals_github_trending_report.yaml`

## Current Output Philosophy

最终产物必须满足：

- 用户一眼能看出今天最值得看的项目方向。
- Top 12 仍然能够先扫读，再展开深读。
- 详情区布局、命名、阅读顺序与 `03-16` 成品页保持一致。
- Explore 仍然是补充列表，不是第二套主舞台。
- 页面看起来属于同一套产品，而不是每天换皮。
- 对 3–5 个值得研究的开发项目，额外生成独立技术解析，而不是把源码细节全部塞进日报。

如果最终 HTML 虽然能打开，但已经不像 `03-16` 那套 UI，视为失败。

## Data Sources

日报补证顺序：

1. GitHub Trending
2. GitHub Explore
3. GitHub 仓库页 / README / About
4. 仓库主页或官方文档
5. 公开搜索结果

架构解析额外读取：

1. 仓库顶层目录与主要源码目录
2. 依赖清单与构建文件
3. 程序、服务或 CLI 入口
4. 路由、核心服务、任务执行器、插件接口和数据层
5. Docker、Compose、Kubernetes、CI 与部署配置
6. API、协议、Schema、事件和消息定义

优先回答：

- 它本质上是什么。
- 它主要解决什么问题。
- 谁最该关注它。
- 第一次打开项目应该先看什么。
- 系统由哪些模块组成，主线流程如何运行。
- 当前结论有哪些证据边界。

## Workflow

### Step 1. 读取规则和固定模板

先读取：

- `reference/user-rules.md`
- `reference/fixedBaseTemplate_2026-03-16.html`
- `reference/uiEngineeringSpec.md`

确认目标是忠实复用固定底板，不是重新设计页面。

### Step 2. 抓取数据与补证

- 抓取 GitHub Trending。
- 抓取 GitHub Explore。
- 抓取重点仓库页、README、About、Homepage 和 Release。
- 如果仓库描述仍然模糊，继续读取官网、文档或公开资料。

如果证据仍不足，在 Markdown、HTML 或架构解析中明确保留 `Honest Caveat`。

### Step 3. 启动 Markdown Report Writer Agent

读取并使用：

- `agents/markdown-report-writer-agent.md`
- `reference/reportMarkdownTemplate.md`

目标：

- 先生成完整的本地 Markdown 内容底稿。
- 文件名：`md/github_trending_report_YYYY-MM-DD.md`。
- Markdown 是后续架构解析和 HTML 的内容事实基线。

Markdown 未写完整或未通过验收，不允许进入后续阶段。

### Step 4. 启动 Project Architecture Analyst Agent

读取并使用仓库根目录：

`agents/project-architecture-analyst-agent.md`

目标：

- 从日报 Top 12 中选择 3–5 个具有可分析软件实现的开发项目。
- 默认排除资源合集、纯文档、纯数据、模型权重和无系统实现的仓库。
- 读取仓库源码结构、依赖清单、入口文件、核心模块、配置、部署文件和协议定义。
- 为每个入选项目生成：
  - `analysis/YYYY-MM-DD/owner__repo.md`
- 生成当日索引：
  - `analysis/YYYY-MM-DD/README.md`
- 每份文档必须包含系统架构、主线流程、技术栈、创新点、应用场景、风险、Evidence Notes、Honest Caveat 和可信度。

分析结果是独立技术档案，不得为了塞进 HTML 而压缩成空话。分析阶段部分失败时允许日报继续发布，但必须明确标记 `DEGRADED` 并列出失败项目。

### Step 5. 启动 UI/UX Designer Agent

读取并使用：

`agents/ui-ux-designer-agent.md`

目标：

- 基于固定模板审校日报内容映射。
- 只给出模板内的信息密度、层级和长度控制建议。
- 不做新设计，不改页面骨架。

### Step 6. 启动 Frontend Engineer Agent

读取并使用：

`agents/frontend-engineer-agent.md`

目标：

- 基于 `reference/fixedBaseTemplate_2026-03-16.html` 产出当天 HTML。
- 保留固定模板主题、样式、交互、区块顺序和关键 class。
- 忠实映射 Markdown 底稿，不做二次简化改写。

### Step 7. 直接编写最终 HTML

最终 HTML 必须：

- 由当前任务直接写出或改写。
- 明显继承 `03-16` 成品模板。
- 保留 `toggleDetail` 与 `toggleTheme`。
- 保留 Top 详情的五个固定小节顺序。

禁止：

- 调用 Python 生成最终 HTML。
- 重新发明 Bootstrap 页面或新组件体系。
- 改成新的展开布局、卡片体系或命名体系。

### Step 8. 验收与发布

发布前至少确认：

- 已生成并验收 Markdown 日报。
- 已读取并执行项目架构分析 Agent。
- 已生成当日分析索引；入选项目的独立文档数量与索引一致。
- 架构图与流程图存在可追踪证据，没有将推断写成事实。
- 最终 HTML 明显基于固定模板。
- `reference/user-rules.md` 的验收项全部满足。
- Top 12 展开详情仍保留：项目摘要、核心特性、技术栈、适用场景、一句话推荐。
- HTML 没有把 Markdown 详细文案压缩成空话。

正式输出：

- `md/github_trending_report_YYYY-MM-DD.md`
- `html/github_trending_report_YYYY-MM-DD.html`
- `analysis/YYYY-MM-DD/README.md`
- `analysis/YYYY-MM-DD/owner__repo.md`

## Legacy Notes

以下旧参考不参与当前主流程：

- `reference/htmlTemplate.md`
- `reference/bootstrapLayoutExample.html`

如果旧文档、旧测试或旧经验中仍提到它们，默认忽略，以当前固定模板工作流为准。

## Failure Handling

- Trending 抓取失败：终止，不发布当日报告，不复用旧数据。
- Explore 抓取失败：允许降级，但必须在 Markdown 与 HTML 中写明。
- 日报项目证据不足：诚实降级，不编造能力。
- 架构分析证据不足：降低可信度，明确推断边界；不得虚构模块、数据库、队列或调用链。
- 单个项目架构分析失败：其他项目继续，索引中记录失败原因，任务标记为 `DEGRADED`。
- 模板映射冲突：优先遵循 `reference/user-rules.md`。

## Test Prompts

1. 帮我生成今日日报，并为其中值得研究的开发项目生成架构解析。
2. 先生成本地 Markdown，再生成 `analysis/YYYY-MM-DD/` 技术档案，最后基于固定模板生成 HTML。
3. 不要重做 UI，只改 `03-16` 模板中的文案和数据。
4. 项目看不明白时继续查源码、官网和公开资料，不要糊弄。
5. 架构分析必须说明证据、可信度和 Honest Caveat。
