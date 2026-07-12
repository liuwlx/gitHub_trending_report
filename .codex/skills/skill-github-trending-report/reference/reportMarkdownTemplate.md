# GitHub Trending Report Markdown Template

这份模板定义了 GitHub Trending 日报在生成 HTML 之前必须先落地的本地 Markdown 文档结构。

作用不是给用户直接阅读，而是作为：

- 数据整理的本地中间产物
- Markdown 报告写作 agent 的主产物
- UI/UX 设计 agent 的内容输入
- 前端开发 agent 的实现输入
- 最终 HTML 的唯一内容基线

## 输出要求

- 文件名建议：`github_trending_report_YYYY-MM-DD.md`
- 输出位置建议：与最终 HTML 放在同一个输出目录
- 编码：UTF-8
- 语言：中文为主，仓库名、技术名、链接保持原样
- 文案要求：用户视角、说人话、降低认知负荷
- HTML 阶段不得再把这份底稿里的核心内容压缩成更短、更空的模板文案
- 最终 HTML 默认要映射到 `reference/fixedBaseTemplate_2026-03-16.html`

## 模板

```md
# GitHub Trending 日报内容底稿

## Meta

- Report Date: YYYY-MM-DD
- Generated At: YYYY-MM-DD HH:mm:ss
- Output Markdown: /absolute/path/to/github_trending_report_YYYY-MM-DD.md
- Planned HTML: /absolute/path/to/github_trending_report_YYYY-MM-DD.html
- Fixed Base Template: /absolute/path/to/reference/fixedBaseTemplate_2026-03-16.html
- User Rules: /absolute/path/to/reference/user-rules.md
- Sources:
  - GitHub Trending
  - GitHub Explore
  - Repo README / About / Homepage / Public Web Search

## Page Intent

- 今日主线：
- 适合谁阅读：
- 页面重点：
- 需要诚实降级说明的地方：

## Stats

- Trending 项目数：
- 今日累计新增 Stars：
- 编程语言数：
- AI 相关项目数：

## Editorial Insights

### Insight 1
- Title:
- Body:

### Insight 2
- Title:
- Body:

### Insight 3
- Title:
- Body:

### Insight 4
- Title:
- Body:

## Top Projects

### Rank 01 - owner/repo
- Repo URL:
- Tagline:
- Stars:
- Stars Today:
- Forks:
- Language:
- License:
- Homepage:
- Topics:
- 技术栈:
- Why It Matters Today:
- 项目摘要:
- 核心特性:
  1.
  2.
  3.
- 适用场景:
- 一句话推荐:
- Evidence Notes:
- Honest Caveat:

### Rank 02 - owner/repo
- Repo URL:
- Tagline:
- Stars:
- Stars Today:
- Forks:
- Language:
- License:
- Homepage:
- Topics:
- 技术栈:
- Why It Matters Today:
- 项目摘要:
- 核心特性:
  1.
  2.
  3.
- 适用场景:
- 一句话推荐:
- Evidence Notes:
- Honest Caveat:

### Rank 03 - owner/repo
- Repo URL:
- Tagline:
- Stars:
- Stars Today:
- Forks:
- Language:
- License:
- Homepage:
- Topics:
- 技术栈:
- Why It Matters Today:
- 项目摘要:
- 核心特性:
  1.
  2.
  3.
- 适用场景:
- 一句话推荐:
- Evidence Notes:
- Honest Caveat:

### Rank 04 - owner/repo
- Repo URL:
- Tagline:
- Stars:
- Stars Today:
- Forks:
- Language:
- License:
- Homepage:
- Topics:
- 技术栈:
- Why It Matters Today:
- 项目摘要:
- 核心特性:
  1.
  2.
  3.
- 适用场景:
- 一句话推荐:
- Evidence Notes:
- Honest Caveat:

<!-- Rank 05 ~ Rank 12 保持同样结构 -->

## Language Distribution

- Language 1:
  - Count:
  - Percent:
  - Color Hint:
- Language 2:
  - Count:
  - Percent:
  - Color Hint:
- Language 3:
  - Count:
  - Percent:
  - Color Hint:
- Other:
  - Count:
  - Percent:
  - Color Hint:

## Explore Highlights

### Explore 1
- Title:
- URL:
- Kind:
- Meta:
- Short Reason:

### Explore 2
- Title:
- URL:
- Kind:
- Meta:
- Short Reason:

<!-- 继续到 6 ~ 8 条 -->

## Rendering Notes

- Hero 主标题建议：
- Hero 副标题建议：
- Top 3 高亮原因：
- 需要在 HTML 中诚实提示的降级点：
- 不允许省略的区块：
- 必须保留的固定模板结构：
  - Header / Hero
  - 4 张 Stats Cards
  - 今日洞察
  - 今日热门 Top 12
  - 编程语言分布
  - GitHub Explore 精选
  - Footer
- Top 详情固定顺序：
  1. 项目摘要
  2. 核心特性
  3. 技术栈
  4. 适用场景
  5. 一句话推荐
```

## 质量检查

在进入 HTML 阶段之前，Markdown 底稿至少要满足：

- 8 个页面区块的数据都已具备
- Top 12 项目都有完整字段
- `项目摘要 / 核心特性 / 适用场景 / 一句话推荐` 已经写完
- `技术栈` 已能支撑展开详情里的 tech tags
- 证据不足项目已写 `Honest Caveat`
- Explore 缺失时已写降级说明

如果这份 Markdown 还只是“字段半成品”，不要进入 HTML 阶段。
