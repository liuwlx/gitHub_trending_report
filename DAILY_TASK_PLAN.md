# GitHub Trending 每日任务计划

本文档定义 `gitHub_trending_report` 仓库的每日自动报告流程。任务的核心原则是：**先读取仓库内的 skill，先生成 Markdown 内容底稿，通过验收后再生成 HTML，最后把产物推送回本仓库。**

## 1. 调度设置

| 项目 | 设置 |
|---|---|
| 执行频率 | 每天 1 次 |
| 默认时间 | 09:00（Asia/Tokyo，日本时间） |
| 时间模式 | 宽松执行，可在目标时间前后约 1 小时内运行 |
| 目标分支 | `main` |
| 目标仓库 | `liuwlx/gitHub_trending_report` |

## 2. 必须读取的仓库内容

每次任务开始时，必须从当前 `main` 分支重新读取以下文件，不得使用历史缓存代替：

1. `.codex/skills/skill-github-trending-report/SKILL.md`
2. `.codex/skills/skill-github-trending-report/reference/user-rules.md`
3. `.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html`
4. `.codex/skills/skill-github-trending-report/reference/uiEngineeringSpec.md`
5. `.codex/skills/skill-github-trending-report/reference/reportMarkdownTemplate.md`
6. `.codex/skills/skill-github-trending-report/agents/markdown-report-writer-agent.md`
7. `.codex/skills/skill-github-trending-report/agents/ui-ux-designer-agent.md`
8. `.codex/skills/skill-github-trending-report/agents/frontend-engineer-agent.md`

低优先级文件与 `user-rules.md` 冲突时，以 `user-rules.md` 为准。

## 3. 数据范围

默认抓取：

- GitHub Trending：Repositories / Any language / Today
- GitHub Explore
- Top 项目的仓库页、README、About、Homepage、Release 或官方文档
- 必要时使用公开搜索补充证据

重点回答：

- 项目本质上是什么
- 解决什么问题
- 谁最应该关注
- 第一次打开项目应该先看哪里
- 当前结论有哪些证据边界

## 4. 每日执行步骤

### Step 1：运行前检查

- 确认当天日期，以 `Asia/Tokyo` 为准。
- 检查以下同名文件是否已经存在：
  - `md/github_trending_report_YYYY-MM-DD.md`
  - `html/github_trending_report_YYYY-MM-DD.html`
- 如果当天报告已经完整存在，不重复创建；如内容不完整，先读取现有文件并谨慎修复。

### Step 2：抓取 Trending 与 Explore

- 抓取当天 GitHub Trending 排名、语言、累计 Stars 和 Stars Today。
- 保留 GitHub 原始排名，不把“原始排名”和“增星速度”混为一谈。
- 抓取 Explore 作为补充；Explore 获取失败时允许降级，但必须在报告中明确说明。

### Step 3：补充项目证据

- 对 Top 12 项目逐一读取仓库公开资料。
- 仓库描述不足时，继续查看官网、文档或公开资料。
- 不把 README 目录、Topics 数量、Examples 数量直接写成用户收益。
- 无法确认的能力必须写入 `Honest Caveat`，不得脑补。

### Step 4：先生成 Markdown

按 skill 的 Markdown 模板生成：

`md/github_trending_report_YYYY-MM-DD.md`

Markdown 必须完整包含：

- Meta 与页面意图
- 4 个统计指标
- 3–4 条今日洞察
- Top 12 完整字段
- 编程语言分布
- Explore 精选
- Rendering Notes
- Evidence Notes 与 Honest Caveat

Markdown 未通过验收，不得进入 HTML 阶段。

### Step 5：进行 UI/UX 映射审校

只做固定模板内的信息层级与文案长度把关：

- 不重新设计主题和布局
- 不删除关键信息
- Top 3 保持克制高亮
- Explore 保持紧凑编号列表
- 所有证据不足之处保留诚实说明

### Step 6：生成固定模板 HTML

基于：

`.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html`

生成：

`html/github_trending_report_YYYY-MM-DD.html`

必须保留：

- 主题切换按钮
- Header / Hero
- 4 张 Stats Cards
- 今日洞察
- 今日热门 Top 12
- 编程语言分布
- GitHub Explore 精选
- Footer
- `toggleTheme()`
- `toggleDetail(btn)`

每个 Top 项目的展开详情顺序固定为：

1. 项目摘要
2. 核心特性
3. 技术栈
4. 适用场景
5. 一句话推荐

### Step 7：发布前验收

至少检查：

- Markdown 和 HTML 日期一致
- Top 12 数量完整
- 12 套展开详情均存在
- 关键 class 和两个交互函数仍存在
- HTML 内容忠实映射 Markdown
- Explore 仍为列表
- 不存在编造的能力、数据或性能结论
- 文件编码为 UTF-8

### Step 8：推送仓库

验收通过后，将文件写入 `main`：

- `md/github_trending_report_YYYY-MM-DD.md`
- `html/github_trending_report_YYYY-MM-DD.html`

推荐提交信息：

```text
report: add GitHub Trending daily report YYYY-MM-DD
```

最后更新 `README.md` 中以下标记之间的“最新报告”内容：

```html
<!-- latest-report:start -->
<!-- latest-report:end -->
```

README 更新必须最后执行，避免首页链接指向尚未成功写入的报告。

## 5. 失败处理

### Trending 抓取失败

- 终止当次任务。
- 不生成伪造报告。
- 不覆盖已有同名文件。
- 返回明确错误说明。

### Explore 抓取失败

- 允许继续生成报告。
- Markdown 与 HTML 中必须注明 Explore 数据降级。

### 项目证据不足

- 写出已确认事实。
- 把不确定部分写入 `Honest Caveat`。
- 不用“功能完整、生态丰富、值得关注”等空话补洞。

### GitHub 写入失败

- 保留已经生成的内容摘要。
- 明确指出失败文件和失败阶段。
- 不声称已经推送成功。

## 6. 幂等规则

- 每个日期只能有一份正式 Markdown 和一份正式 HTML。
- 同日重复运行时，优先校验已有文件，不盲目追加副本。
- 只有在已有报告不完整、数据明显错误或用户明确要求重跑时才更新同名文件。
- README 的最新报告链接只在两个报告文件均成功写入后更新。

## 7. 完成标准

一次任务只有同时满足以下条件才算成功：

- 已读取仓库当前版本 skill 与规则
- 已生成完整 Markdown
- 已基于固定模板生成 HTML
- 两份文件已推送到仓库
- README 最新报告链接已更新
- 最终返回报告日期、文件路径和提交结果
