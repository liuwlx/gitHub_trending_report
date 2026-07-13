# GitHub Trending 每日任务计划

本文档定义 `gitHub_trending_report` 仓库的每日自动报告流程。任务遵循两层输出：

1. 先生成适合快速阅读的 GitHub Trending Markdown 与 HTML 日报。
2. 再为日报中值得研究的开发项目生成独立的系统架构与源码解析文档。

核心原则是：**每次都读取仓库当前版本的 Skill 和 Agent；先形成内容事实基线，再做架构研究和固定模板渲染，最后推送仓库。**

## 1. 调度设置

| 项目 | 设置 |
|---|---|
| 执行频率 | 每天 1 次 |
| 默认时间 | 09:00（Asia/Tokyo，日本时间） |
| 时间模式 | 宽松执行，可在目标时间前后约 1 小时运行 |
| 目标分支 | `main` |
| 目标仓库 | `liuwlx/gitHub_trending_report` |

## 2. 每次必须重新读取的内容

任务开始时必须从当前 `main` 分支重新读取，不得使用历史缓存：

1. `.codex/skills/skill-github-trending-report/SKILL.md`
2. `.codex/skills/skill-github-trending-report/reference/user-rules.md`
3. `.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html`
4. `.codex/skills/skill-github-trending-report/reference/uiEngineeringSpec.md`
5. `.codex/skills/skill-github-trending-report/reference/reportMarkdownTemplate.md`
6. `.codex/skills/skill-github-trending-report/agents/markdown-report-writer-agent.md`
7. `.codex/skills/skill-github-trending-report/agents/ui-ux-designer-agent.md`
8. `.codex/skills/skill-github-trending-report/agents/frontend-engineer-agent.md`
9. `agents/project-architecture-analyst-agent.md`

低优先级文件与 `reference/user-rules.md` 冲突时，以 `user-rules.md` 为准。项目深度解析则严格遵循根目录架构分析 Agent 的证据和输出规则。

## 3. 数据范围

默认抓取：

- GitHub Trending：Repositories / Any language / Today
- GitHub Explore
- Top 项目的仓库页、README、About、Homepage、Release 和官方文档
- 必要时使用公开搜索补充证据

为项目深度解析额外读取：

- 仓库目录树和主要源码目录
- 依赖清单与构建文件
- 程序、服务或 CLI 入口
- 核心服务、路由、任务执行器、插件接口和数据层
- Docker、Compose、Kubernetes、CI 和部署配置
- API、协议、Schema、事件或消息定义

## 4. 每日执行步骤

### Step 1：运行前检查

- 以 `Asia/Tokyo` 确定当天日期。
- 检查以下文件或目录是否存在：
  - `md/github_trending_report_YYYY-MM-DD.md`
  - `html/github_trending_report_YYYY-MM-DD.html`
  - `analysis/YYYY-MM-DD/README.md`
- 同日文件已经完整存在时不得重复创建。
- 文件存在但内容不完整时，先读取现有内容，只修复必要部分。

### Step 2：抓取 Trending 与 Explore

- 抓取当天 GitHub Trending 原始排名、语言、累计 Stars 和 Stars Today。
- 保留 GitHub 原始排名，不将排名与增星速度混为一谈。
- 抓取 Explore 作为补充。
- Explore 获取失败时允许降级，但必须在 Markdown 与 HTML 中明确说明。

### Step 3：补充日报项目证据

- 对 Top 12 逐一读取仓库公开资料。
- 仓库描述不足时继续查看官网、文档、Release 或公开资料。
- 不把 README 目录、Topics 数量或 Examples 数量直接写成用户收益。
- 无法确认的能力写入 `Honest Caveat`，不得脑补。

### Step 4：先生成 Markdown 日报

按 Skill 模板生成：

`md/github_trending_report_YYYY-MM-DD.md`

必须完整包含：

- Meta 与页面意图
- 4 个统计指标
- 3–4 条今日洞察
- Top 12 完整字段
- 编程语言分布
- Explore 精选
- Rendering Notes
- Evidence Notes 与 Honest Caveat

Markdown 未通过验收，不得进入架构分析或 HTML 阶段。

### Step 5：驱动 Project Architecture Analyst Agent

读取并严格执行：

`agents/project-architecture-analyst-agent.md`

#### 5.1 项目选择

从日报 Top 12 中选择 3–5 个具有可分析系统实现的开发项目。

优先选择：

- 原始排名靠前的软件、框架、库、基础设施或开发工具。
- Stars Today 增长显著且具有实际代码系统的项目。
- 架构新颖、权限较大、性能主张突出或需要额外验证的项目。
- AI Agent、数据库、安全、运行时、构建工具和工程框架类项目。

默认排除：

- Awesome List、链接合集、书单和纯资源导航。
- 纯 Prompt、模板、图片、数据集或模型权重仓库。
- 纯教程、笔记、文档镜像或没有可分析程序实现的项目。

不得为了凑满数量分析没有架构证据的项目。

#### 5.2 生成项目解析

每个入选项目写入：

`analysis/YYYY-MM-DD/owner__repo.md`

必须包含：

1. 项目概览
2. 系统架构与 Mermaid 架构图
3. 核心模块、职责、代码位置和关键依赖
4. 主线流程与 Mermaid 流程图或时序图
5. 技术栈分层说明
6. 创新点、收益、证据和代价
7. 适合、可以尝试、暂不建议的应用场景
8. 第一次阅读与验证路径
9. 安全、性能、许可证和生产可用性风险
10. Evidence Notes
11. Honest Caveat
12. Architecture / Flow / Innovation 三项可信度

#### 5.3 生成当日索引

写入：

`analysis/YYYY-MM-DD/README.md`

索引必须列出：

- 当天日报链接
- 入选项目及选择原因
- 每个解析文档的相对链接
- 三项可信度摘要
- 被跳过项目及简短原因
- 成功、失败、跳过和降级数量

#### 5.4 架构分析幂等与失败规则

- 同日同项目文档完整存在时不重复创建。
- 内容不完整时先读取再谨慎修复。
- 不得根据目录名虚构调用关系。
- 不得虚构数据库、缓存、队列、微服务或部署组件。
- 单个项目失败时继续处理其他项目，并在索引中记录原因。
- 分析阶段部分失败时将阶段状态标记为 `DEGRADED`，但不阻止已合格的日报发布。

### Step 6：进行 UI/UX 映射审校

只做固定模板内的信息层级和长度把关：

- 不重新设计主题和布局
- 不删除关键信息
- Top 3 保持克制高亮
- Explore 保持紧凑编号列表
- 所有证据不足之处保留诚实说明

项目独立解析文档不需要塞进日报卡片正文，避免破坏日报扫读效率。

### Step 7：生成固定模板 HTML

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

不得使用 Python、本地渲染器或固定脚本代写最终 HTML。

### Step 8：发布前验收

至少检查：

- Markdown 与 HTML 日期一致。
- Top 12 数量完整。
- 12 套展开详情均存在。
- 关键 class 和两个交互函数存在。
- HTML 忠实映射 Markdown。
- Explore 仍为列表。
- 当日分析索引存在。
- 分析索引中的成功项目均有对应独立文件。
- 每份项目解析均包含架构、流程、技术栈、创新点和应用场景。
- Mermaid 图和关键判断存在证据支撑。
- Evidence Notes、Honest Caveat 和可信度均存在。
- 不存在编造的能力、数据、性能或系统组件。
- 文件编码为 UTF-8。

### Step 9：推送仓库

验收通过后写入 `main`：

- `md/github_trending_report_YYYY-MM-DD.md`
- `html/github_trending_report_YYYY-MM-DD.html`
- `analysis/YYYY-MM-DD/README.md`
- `analysis/YYYY-MM-DD/owner__repo.md`

推荐提交信息：

```text
report: add GitHub Trending daily report YYYY-MM-DD
analysis: add project architecture reports YYYY-MM-DD
```

最后更新 `README.md` 中以下标记之间的最新日报内容：

```html
<!-- latest-report:start -->
<!-- latest-report:end -->
```

README 更新必须最后执行，避免首页链接指向尚未成功写入的日报。

## 5. 失败处理

### Trending 抓取失败

- 终止任务。
- 不生成伪造日报或项目分析。
- 不使用历史数据冒充当天数据。
- 不更新 README。

### Explore 抓取失败

- 允许继续。
- Markdown 与 HTML 必须标记降级。

### 日报项目证据不足

- 写出已确认事实。
- 不确定部分写入 `Honest Caveat`。

### 架构分析证据不足

- 降低对应可信度。
- 明确哪些部分来自源码，哪些是有限推断。
- 不得用宣传文案填补架构空白。

### 单个项目架构分析失败

- 不影响其他项目继续执行。
- 在当日分析索引中记录失败项目与原因。
- 最终状态标为 `DEGRADED`。

### GitHub 写入失败

- 明确失败路径和阶段。
- 不声称未写入的文件已经发布。
- README 只在 Markdown 和 HTML 均成功写入后更新。

## 6. 幂等规则

- 每个日期只有一份正式 Markdown 日报和一份正式 HTML 日报。
- 每个日期每个项目只有一份正式架构解析文件。
- 同日重复运行优先校验已有文件，不盲目追加副本。
- 只有文件不完整、数据明显错误或用户明确要求重跑时才更新同名文件。
- 当日分析索引必须与实际项目文件一致。

## 7. 完成标准

一次任务的日报主流程只有同时满足以下条件才算成功：

- 已读取仓库当前版本 Skill、规则与四个 Agent。
- 已生成完整 Markdown 日报。
- 已执行项目架构分析阶段并生成当日索引；部分失败时已标记 `DEGRADED`。
- 已基于固定模板生成 HTML。
- Markdown 与 HTML 已写入仓库。
- README 最新日报链接已更新。
- 最终汇报报告日期、日报路径、分析目录、入选项目、成功/失败/跳过数量、可信度分布、提交 SHA 和降级原因。
