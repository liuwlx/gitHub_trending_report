---
name: skill-github-trending-report
version: 0.8.0
description: 抓取 GitHub Trending 与 Explore 数据，先由 Markdown 报告写作 agent 生成本地 Markdown 底稿，再由 UI/UX 守门员 agent 与前端开发 agent 基于固定成品模板 reference/fixedBaseTemplate_2026-03-16.html 生成 HTML 日报。
---

# Skill: GitHub Trending Report

这个 skill 现在采用固定模板优先的工作方式：

- 先抓 GitHub Trending / Explore 与重点仓库公开信息
- 先生成本地 Markdown 内容底稿
- 再基于 `2026-03-16` 已验收成品页生成 HTML

当前目标不是“做一张新的日报页面”，而是“继续用用户已经认可的那张页面，只替换成当天内容”。

## Hard Rules

- `reference/user-rules.md` 是最高优先级约束
- `reference/fixedBaseTemplate_2026-03-16.html` 是固定 UI 底板，不是灵感参考
- 必须先生成本地 Markdown 底稿，再进入 HTML 阶段
- 最终 HTML 必须由当前 AI 直接写出或改写，不允许交给 Python 或本地渲染脚本代写
- 不允许重新设计主题、区块顺序、展开详情结构、关键 class 名称或交互命名
- `项目摘要 / 核心特性 / 适用场景 / 一句话推荐` 必须从用户视角出发，说人话，降低认知负荷
- 如果 GitHub 仓库页与 README 不足以解释项目，必须继续查看官网、文档页或公开搜索结果
- 如果运行环境不支持真实 subagent，也必须依次读取 `agents/` 中的角色定义，严格模拟其职责，不允许跳过

## Required References

执行时优先读取：

1. `reference/user-rules.md`
2. `reference/fixedBaseTemplate_2026-03-16.html`
3. `reference/uiEngineeringSpec.md`
4. `reference/reportMarkdownTemplate.md`
5. `agents/markdown-report-writer-agent.md`
6. `agents/ui-ux-designer-agent.md`
7. `agents/frontend-engineer-agent.md`
8. `examples/github-trending-report-example.md`
9. `tests/evals_github_trending_report.yaml`

## Current Output Philosophy

最终页面必须满足这几个判断：

- 用户一眼能看出今天最值得看的项目方向
- Top 12 仍然能先扫读、再展开深读
- 详情区的布局、命名、阅读顺序与 `03-16` 成品页保持一致
- Explore 仍然是补充列表，而不是第二套主舞台
- 页面看起来像同一套产品，而不是每次换一张皮

如果最终 HTML 虽然“能打开”，但看起来已经不是 `03-16` 那套 UI，就算失败。

## Data Sources

建议按下面顺序补证：

1. GitHub Trending
2. GitHub Explore
3. GitHub 仓库页 / README / About
4. 仓库主页或官方文档
5. 公开搜索结果

优先回答这些问题：

- 它本质上是什么
- 它主要解决什么问题
- 谁最该关注它
- 第一次打开它应该先看什么

## Workflow

### Step 1. 读取规则和固定模板

先读取：

- `reference/user-rules.md`
- `reference/fixedBaseTemplate_2026-03-16.html`
- `reference/uiEngineeringSpec.md`

确认当前任务的目标是“忠实复用固定底板”，不是重新设计页面。

### Step 2. 抓取数据与补证

- 抓 GitHub Trending
- 抓 GitHub Explore
- 抓重点仓库页、README、About、Homepage
- 如果仓库描述仍然模糊，继续做公开资料补证

如果证据仍不足，要在后续 Markdown 与 HTML 中明确保留 `Honest Caveat`。

### Step 3. 启动 Markdown Report Writer Agent

读取并使用：

- `agents/markdown-report-writer-agent.md`
- `reference/reportMarkdownTemplate.md`

目标：

- 先落一份本地 Markdown 内容底稿
- 文件名建议：`github_trending_report_YYYY-MM-DD.md`
- 输出目录默认与最终 HTML 相同，通常为 `github/`

这份 Markdown 是后续 HTML 的内容事实基线。
如果 Markdown 还没写完整，不允许提前进入 HTML 阶段。

### Step 4. 启动 UI/UX Designer Agent

读取并使用：

- `agents/ui-ux-designer-agent.md`

目标：

- 基于固定模板审校内容映射
- 只给出模板内的密度、层级、长度控制建议
- 不做新设计，不改页面骨架

### Step 5. 启动 Frontend Engineer Agent

读取并使用：

- `agents/frontend-engineer-agent.md`

目标：

- 基于 `reference/fixedBaseTemplate_2026-03-16.html` 产出当天 HTML
- 保留固定模板的主题、样式、交互、区块顺序和关键 class 命名
- 忠实映射 Markdown 底稿，不做二次“简化改写”

### Step 6. 直接编写最终 HTML

最终 HTML 必须：

- 由当前任务直接写出或改写
- 明显继承 `03-16` 成品模板
- 保留 `toggleDetail` 与 `toggleTheme`
- 保留 Top 详情的 5 个固定小节顺序

禁止：

- 调用 Python 生成最终 HTML
- 重新发明一套 Bootstrap 页面
- 改成新的展开布局、卡片体系或命名体系

### Step 7. 验收

交付前至少确认：

- 已生成本地 Markdown 底稿
- 最终 HTML 明显基于固定模板
- `reference/user-rules.md` 的验收项全部满足
- Top 12 的展开详情仍保留：
  - 项目摘要
  - 核心特性
  - 技术栈
  - 适用场景
  - 一句话推荐
- 页面没有把 Markdown 底稿中的详细中文文案重新压缩成空话

## Legacy Notes

以下旧参考已不再参与当前主流程：

- `reference/htmlTemplate.md`
- `reference/bootstrapLayoutExample.html`

如果旧文档、旧测试或旧经验中还提到它们，当前版本默认忽略，以固定模板工作流为准。

## Failure Handling

- Trending 抓取失败：终止，并说明 GitHub 页面结构或网络可能异常
- Explore 抓取失败：允许降级，但必须在 Markdown 与 HTML 中写明
- 项目证据不足：诚实降级，不编造能力
- 模板映射冲突：优先遵循 `reference/user-rules.md`

## Test Prompts

1. 帮我生成今日日报，输出到 github 目录下
2. 先生成本地 md 文档，再基于 2026-03-16 成品模板生成 html
3. 不要重做 UI，只改 03-16 模板里的文案和数据
4. 如果项目看不明白就继续查官网和公开资料，不要糊弄
