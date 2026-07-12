# GitHub Trending Report User Rules

这份文档用于承接用户追加的规则、约束和验收口径。

当前版本的核心目标只有一个：
把 `2026-03-16` 那份已经被用户认可的成品页面，固定为后续 GitHub Trending 日报的 UI 底板；之后生成 HTML 时，只允许替换内容与数据，不允许重新设计页面。

## 优先级

生成 HTML 时，必须按下面的优先级执行：

1. `reference/user-rules.md`
2. `reference/fixedBaseTemplate_2026-03-16.html`
3. `reference/uiEngineeringSpec.md`
4. 本次任务先生成的本地 Markdown 底稿
5. `reference/reportMarkdownTemplate.md`

如果低优先级文档和高优先级文档冲突，一律以高优先级为准。

## 固定底板规则

- 固定 UI 成品模板路径：`reference/fixedBaseTemplate_2026-03-16.html`
- 模板来源页：`github/github_trending_report_2026-03-16.html`
- 该模板视为“已验收 UI 成品”，后续任务不得把它当作灵感参考重新设计，而要把它当作直接复用的工程底板。

## 允许修改的范围

后续生成 HTML 时，只允许修改这些内容：

- 页面标题、副标题、日期、数据源文案
- 统计卡数字与标签内容
- 今日洞察的标题和正文
- Top 12 项目的链接、简介、数据、topics、展开详情文案
- 编程语言分布条的名称、数量、比例、颜色
- Explore 精选条目的文字、链接和降级说明
- 页脚中的生成时间、来源说明和当次报告补充说明

允许为当日数据替换文案和数值，但不允许借这个机会重做版式、主题、命名或组件结构。

## 严禁事项

- 严禁重新设计主题、配色、页面骨架、阅读节奏或整体布局
- 严禁把页面改成另一套 Bootstrap 页面、卡片墙、营销页、瀑布流、标签页或多栏 dashboard
- 严禁把 Top 榜单的“展开详情”改成别的交互形态
- 严禁替换或删除固定模板里的关键 class 命名与交互函数命名
- 严禁为了“精简”而把 Markdown 底稿里已经写清楚的内容再次压缩、改写成空话或口号
- 严禁使用 Python、本地脚本或固定渲染器生成最终 HTML
- 严禁绕过本地 Markdown 底稿直接凭空拼 HTML

## 必须保留的结构

页面必须保留以下区块顺序：

1. 顶部主题切换按钮
2. Header / Hero
3. Stats Cards
4. 今日洞察
5. 今日热门 Top 12
6. 编程语言分布
7. GitHub Explore 精选
8. Footer

## 必须保留的关键命名

以下结构、命名和交互约定默认不可改：

- `.theme-toggle`
- `.container`
- `.header`
- `.stats-grid`
- `.stat-card`
- `.section`
- `.section-title`
- `.project-card`
- `.project-card.top-card`
- `.project-header`
- `.project-rank`
- `.project-info`
- `.project-meta`
- `.topics`
- `.topic-badge`
- `.detail-toggle`
- `.project-details`
- `.detail-section`
- `.feature-list`
- `.tech-tags`
- `.tech-tag`
- `.recommend-quote`
- `.lang-chart`
- `.lang-bar-row`
- `.trending-list`
- `.trending-item`
- `.footer`
- `toggleDetail(btn)`
- `toggleTheme()`

如果确实需要额外辅助 class，只能新增，不能替换或删除上面这些约定。

## 展开详情固定顺序

每个 Top 项目的展开详情，必须继续遵循 `03-16` 成品页的阅读顺序：

1. `📖 项目摘要`
2. `✨ 核心特性`
3. `🔧 技术栈`
4. `🎯 适用场景`
5. `💬 一句话推荐`

不允许改成别的标题顺序，也不允许把这些内容并回封面态。

## 文案约束

- Markdown 底稿是内容事实基线，HTML 阶段必须忠实映射
- `项目摘要 / 核心特性 / 适用场景 / 一句话推荐` 必须保持“用户视角、说人话、降低认知负荷”
- 不允许把 `README 很完整 / topics 很聚焦 / 有 docs/examples/integrations` 这种仓库结构观察直接写给读者
- 如果项目靠 README 无法解释清楚，必须继续看仓库主页、官网、公开资料或公开搜索结果
- 如果最终证据仍不足，必须保留诚实降级说明，而不是脑补

## 验收标准

交付前至少逐项确认：

- 已先生成本地 Markdown 底稿，再进入 HTML 阶段
- HTML 是基于 `reference/fixedBaseTemplate_2026-03-16.html` 改写出来的，不是另起一套页面
- 页面主题、配色、区块顺序、展开详情交互与 `03-16` 成品模板保持一致
- 关键 class 名称和 `toggleDetail / toggleTheme` 函数仍然存在
- Top 12 详情区仍然保留 `项目摘要 / 核心特性 / 技术栈 / 适用场景 / 一句话推荐`
- Markdown 底稿中的关键信息没有在 HTML 阶段被二次简化成难懂或空洞的文案
- Explore 仍然是紧凑列表，不是卡片墙
- 如有降级说明，已经明确写在 HTML 中

## 未来扩展约定

后续如果用户还要追加约束，请直接继续写在这份文档里。
后续任务在开始生成 HTML 前，必须先读取并遵循这份文档的全部规则。
