# GitHub Trending 日报 · 2026-05-26

> 数据来源：GitHub Trending（全语言）+ Python Trending  
> 报告日期：2026-05-26（周一）  
> 上次报告：2026-05-25（间隔 1 天）  
> 输出文件：github_trending_report_2026-05-26.md / .html

---

## 元信息

| 指标 | 数值 |
|---|---|
| Top 12 累计 Stars | ~597k |
| 今日新上榜 | 5 |
| 重回 Top 12 | 1（FinceptTerminal）|
| 持续上榜 | 6 |
| 今日 #1 | Lum1104/Understand-Anything（Day 3！+4,422，+16.3%）|
| 今日最高 Stars 新入 | affaan-m/ECC（192,527！本系列日报新入榜 Stars 最高纪录）|
| 今日持续最长 | multica-ai/andrej-karpathy-skills（Day 7！155,178）|
| Explore 最大 | garrytan/gstack（102,560，YC CEO Claude Code setup）|

---

## 今日 Top 12 一览

| 排名 | 仓库 | Stars | 语言 | 状态 |
|---|---|---|---|---|
| #01 | Lum1104/Understand-Anything | 31,575 | Python | Day 3（连续 #1！）|
| #02 | anthropics/knowledge-work-plugins | 15,593 | Markdown | Day 2 |
| #03 | rohitg00/ai-engineering-from-scratch | 18,823 | Python | Day 2 |
| #04 | affaan-m/ECC | 192,527 | Markdown | 今日新上榜！本系列最高新入 |
| #05 | mukul975/Anthropic-Cybersecurity-Skills | 9,322 | Markdown | Explore→Top 12 首入！|
| #06 | colbymchenry/codegraph | 25,407 | TypeScript | Top 12 Day 2（+2,545）|
| #07 | manaflow-ai/cmux | 19,534 | Swift | Day 2 |
| #08 | multica-ai/andrej-karpathy-skills | 155,178 | Markdown | Day 7！最长坚守 |
| #09 | Fincept-Corporation/FinceptTerminal | 23,916 | C++ | 重回 Top 12 |
| #10 | paperless-ngx/paperless-ngx | 41,369 | Python | 今日新上榜 |
| #11 | anthropics/claude-cookbooks | 44,062 | Python | 今日新上榜（Anthropic 第三官方仓）|
| #12 | Leonxlnx/taste-skill | 19,842 | Markdown | 今日新上榜（Anti-Slop 设计 Skills）|

---

## 今日洞察

### 1. 🏆 affaan-m/ECC（#4，192,527 ⭐）——本系列新入榜 Stars 最高记录，Anthropic Hackathon 获奖项目

"The harness-native operator system for agentic work." 192,527 Stars，29,792 forks，170+ 贡献者，12 语言生态，Anthropic Hackathon Winner。

ECC 不是简单的配置文件——它是一套完整的 agent harness 操作系统：
- **Skills**：主要工作流界面，可直接调用、自动建议、供 subagents 复用
- **Hooks**：工具事件触发（如 Edit/Bash 事件时自动执行代码质量检查）
- **Rules**：common（通用原则）+ 语言专用（TypeScript/Python/Go/Swift/PHP/ArkTS）
- **Agents**：有限范围委托任务的 subagents
- **AgentShield**：安全审计模块
- **Continuous Learning v2**：持续学习系统

跨 7 个 harness 支持：Claude Code、Codex、Cursor、OpenCode、Gemini、Zed、GitHub Copilot。v2.0.0-rc.1（Apr 2026）新增 Hermes operator story。MIT 开源，ECC Pro $19/seat/mo（私有仓 GitHub App 增强）。

今日以 192k Stars 首入 #4——是本系列日报迄今为止新入榜项目 Stars 最高记录（超越昨日 66 分此前最大的 karpathy-skills 入榜时的 Stars）。

---

### 2. 🎨 Skills 生态今日达到历史浓度峰值 —— 6 个 agent configuration/skill 类项目同日上榜

今日 Top 12 + Explore 同时出现 6 个 Skills/配置类项目，是本系列日报中这一方向项目密度最高的一天：

| 项目 | 排名 | Stars | 定位 |
|---|---|---|---|
| affaan-m/ECC | #4 | 192k | 完整 harness 操作系统（多 harness，10+ 月维护）|
| mukul975/Anthropic-Cybersecurity-Skills | #5 | 9k | 安全专域 Skills（754 项，5 框架映射）|
| multica-ai/andrej-karpathy-skills | #8 | 155k | 行为配置单文件（Karpathy 洞见，Day 7）|
| Leonxlnx/taste-skill | #12 | 20k | 前端/设计反 slop Skills（UI 品味）|
| hardikpandya/stop-slop | Explore #16 | 4k | 散文反 slop skill（去除 AI 语气）|
| garrytan/gstack | Explore #17 | 103k | CEO/产品视角 complete sprint setup（YC CEO）|

从 karpathy-skills 05-20 首入 Top 12 触发关注，到今日"Skills 六连"上榜——agent configuration 生态在 1 周内完成了"单点突破→百花齐放"的跃迁。Skills 文件（Markdown 配置）正在成为 2026 AI 工程师生产力的核心基础设施。

---

### 3. 📐 garrytan/gstack（#17 Explore，102,560 ⭐）—— YC CEO 的 Claude Code setup：2026 生产率 810× 2013

Garry Tan（Y Combinator 总裁兼 CEO，前 Palantir 工程师，Posterous 联创）发布其 Claude Code 完整配置 gstack，102,560 Stars，仅以第 17 位差一步入 Top 12。

核心理念：gstack 是一个**流程**，而非工具集合。Sprint 流程：`Think → Plan → Build → Review → Test → Ship → Reflect`，23 个专业角色 slash command（/office-hours、/plan-ceo-review、/plan-eng-review、/qa、/review、/ship、/retro...），GBrain 持久知识系统，并行 sprint 支持（10-15 个并行 sprint）。

"In the last 60 days: 3 production services, 40+ shipped features, part-time, while running YC full-time. My 2026 run rate is ~810× my 2013 pace (11,417 vs 14 logical lines/day)."

今日形成**三角格局**——三个重量级 individual developer Claude Code setup：
- **ECC**（#4，192k）：系统工程视角，harness-native operator system，强调 hooks/rules/agents 技术基础设施
- **karpathy-skills**（#8，155k）：工程师行为视角，单文件 CLAUDE.md，最小化认知负担
- **gstack**（Explore，103k）：CEO/产品视角，sprint 流程完整闭环，强调从 idea 到 ship 的全链路

三者定位各异，用户群不同，共同构成 2026 Claude Code setup 生态的主干。

---

### 4. ⚡ Understand-Anything Day 3 守 #1，+4,422（+16.3%），3天累计 +9,592（+43.9%）

05-24（21,983）→ 05-25（27,153，+5,170）→ 05-26（31,575，+4,422）。连续 3 天守住 #1（05-24 是首次进入 Top 12 的 #12 末位，但 05-25 和 05-26 连续 #1）。

今日与 codegraph（#6，+2,545，+11%）继续保持"代码知识图谱双入 Top 12"格局，是继"Skills 六连"之外今日另一个方向性强信号。codegraph 3天 Top 12 增量：22,862→25,407，+2,545（Top 12 累计 +6k in 3 days of Top 12）。

---

## Top 12 详情

### #01 · Lum1104/Understand-Anything

**⚡ Day 3 · 连续 #1 · +4,422（+16.3%）· 3 天累计 +9,592（+43.9%）**

- **仓库**：https://github.com/Lum1104/Understand-Anything
- **Stars**：31,575（05-24：21,983 → 05-25：27,153 → 05-26：31,575）| Forks：2,594
- **语言**：Python
- **编辑点评**：连续 3 天 #1！05-24 进入 Top 12 当天还是 #12 末位，05-25 就跳至 #1，05-26 再次 #1。3天累计增量 +9,592（+43.9%！），在本系列日报中是 3 天内增幅最快的项目。今日 codegraph（#6，+2,545）继续"代码知识图谱双入"。

---

### #02 · anthropics/knowledge-work-plugins

**Day 2 · Anthropic 官方 · 知识工作者职能域插件 · +1,360（+9.6%）**

- **仓库**：https://github.com/anthropics/knowledge-work-plugins
- **Stars**：15,593（昨日 14,233，+1,360）| Forks：1,880
- **语言**：Markdown
- **编辑点评**：Day 2，+1,360（+9.6%）稳定增速。今日 Anthropic 同时有 3 个官方仓入 Top 12：knowledge-work-plugins（#2）+ claude-cookbooks（#11，今日新入）+ 昨日的 claude-plugins-official 已退出榜单。Anthropic 今日将 claude-cookbooks 带入 Top 12，三仓并立：知识工作者插件 + 开发者插件 + 场景示例。

---

### #03 · rohitg00/ai-engineering-from-scratch

**Day 2 · +2,165（+13%）**

- **仓库**：https://github.com/rohitg00/ai-engineering-from-scratch
- **Stars**：18,823（昨日 16,658，+2,165）| Forks：3,184
- **语言**：Python
- **编辑点评**：Day 2，+2,165（+13%）持续强劲。今日与 Understand-Anything（#1）+ codegraph（#6）三项"从零学/从底层理解"项目同时在 Top 12，加上 Explore 的 garrytan/gstack（"CEO 视角的工程提速"）——今日"深度理解 + 完整方法论"信号在 Top 12 内持续强化。

---

### #04 · affaan-m/ECC

**🏆 今日新上榜 · 192,527 ⭐ · 本系列新入榜最高 Stars · Anthropic Hackathon Winner**

- **仓库**：https://github.com/affaan-m/ECC
- **Stars**：192,527 | Forks：29,792 | Releases：13
- **语言**：Markdown
- **描述**：The agent harness performance optimization system. Skills, instincts, memory, security, and research-first development for Claude Code, Codex, Opencode, Cursor and beyond.
- **核心组件**：
  - **Skills**：主要工作流界面，直接调用 / 自动建议 / subagents 复用
  - **Hooks**：工具事件触发（Edit/Bash/Read 等事件 → 自动代码质量/安全检查）
  - **Rules**：common（语言无关通用原则）+ TypeScript / Python / Go / Swift / PHP / ArkTS 专项规则目录
  - **Agents**：有限范围委托任务的 subagents（含 code-reviewer 示例）
  - **AgentShield**：安全审计模块
  - **Continuous Learning v2**：持续学习系统
- **跨 harness 支持**：Claude Code / Codex / Cursor / OpenCode / Gemini / Zed / GitHub Copilot
- **版本**：v2.0.0-rc.1（Apr 2026）新增 Hermes operator story + ECC 2.0 Alpha
- **商业模式**：OSS 永久 MIT 免费，ECC Pro $19/seat/mo（私有仓 GitHub App，PR 审计）
- **规模**：182K+ stars | 28K+ forks | 170+ contributors | 12+ language ecosystems
- **编辑点评**：本系列日报迄今为止新入榜项目 Stars 最高记录（192k，首入即 #4！）。ECC 从 2025 年底 Anthropic Hackathon 起持续维护 10+ 个月，每周跨 7 个 harness 出货。"Not just configs. A complete system"——ECC 与 karpathy-skills（单文件行为配置）和 gstack（CEO 视角 sprint 流程）构成今日 agent setup 三角格局。ECC 的定位：**技术系统层**，最完整的 hooks + rules + agents + skills 体系。

---

### #05 · mukul975/Anthropic-Cybersecurity-Skills

**🏅 Explore→Top 12 首入 · +800（+9.4%，1天）**

- **仓库**：https://github.com/mukul975/Anthropic-Cybersecurity-Skills
- **Stars**：9,322（昨日 Explore 8,522，+800，+9.4%）| Forks：1,140
- **语言**：Markdown
- **描述**：754 structured cybersecurity skills for AI agents · MITRE ATT&CK + NIST CSF 2.0 + MITRE ATLAS + D3FEND + NIST AI RMF · 26 security domains · Apache 2.0
- **编辑点评**：今日从 Explore 升入 Top 12！05-24（7,514）→ 05-25（8,522，+1,008，+13%）→ 05-26（9,322，+800，+9%），3天 +1,808（+24%！）。是今日"Skills 六连"中唯一一个垂直安全方向的项目，也是继 andrej-karpathy-skills（通用）+ ECC（全功能系统）+ gstack（流程）+ taste-skill（设计）+ stop-slop（散文）之后，Skills 垂直化最完整的一天。

---

### #06 · colbymchenry/codegraph

**Top 12 Day 2 · +2,545（+11%）**

- **仓库**：https://github.com/colbymchenry/codegraph
- **Stars**：25,407（昨日 22,862，+2,545，+11%）| Forks：1,408
- **语言**：TypeScript
- **描述**：Pre-indexed code knowledge graph for Claude Code, Codex, Cursor, OpenCode, and Hermes Agent — fewer tokens, fewer tool calls, 100% local
- **编辑点评**：Top 12 Day 2，+2,545（+11%），持续高增速。总在榜增量（从 05-22 Explore #4 计）：14,599 → 25,407，+10,808（+74%！，5天）。今日与 Understand-Anything（#1）继续"代码知识图谱双入"格局。

---

### #07 · manaflow-ai/cmux

**Day 2 · +427**

- **仓库**：https://github.com/manaflow-ai/cmux
- **Stars**：19,534（昨日 19,107，+427）| Forks：1,474
- **语言**：Swift
- **编辑点评**：Day 2，增速放缓（+427 vs 首日的巨量）。macOS 原生 Ghostty terminal 专为 AI coding agents 优化，作为今日唯一 Swift 项目持续在榜。

---

### #08 · multica-ai/andrej-karpathy-skills

**🏆 Day 7！本系列持续最长纪录 · 155,178 · +2,496**

- **仓库**：https://github.com/multica-ai/andrej-karpathy-skills
- **Stars**：155,178（昨日 152,682，+2,496）| Forks：15,912
- **语言**：Markdown
- **7天增长轨迹**：
  - 05-20（138,654）→ 05-21（140,969，+2,315）→ 05-22（144,035，+3,066）→ 05-24（149,900，+5,865 in 2d）→ 05-25（152,682，+2,782）→ 05-26（155,178，+2,496）
  - 7天累计：+16,524 Stars（+11.9%）
- **编辑点评**：Day 7！本系列日报持续在榜最长纪录。今日降至 #8（昨日 #5），被 ECC（#4，192k 入榜）等新项目稀释，但仍以 2,496/天的稳定增速维持。在今日"Skills 六连"中，karpathy-skills 是"最小复杂度"代表——单文件 CLAUDE.md，而 ECC（192k）是"最完整系统"代表。两者的分工意味着不同开发者偏好的分化已经清晰。

---

### #09 · Fincept-Corporation/FinceptTerminal

**重回 Top 12 · C++ + Python · 金融分析终端**

- **仓库**：https://github.com/Fincept-Corporation/FinceptTerminal
- **Stars**：23,916 | Forks：3,288
- **语言**：C++ + Python（C++20 + Qt6 + Python 数据层）
- **描述**：Modern finance application offering advanced market analytics, investment research, and economic data tools
- **编辑点评**：05-24 Top 12 #11 → 05-25 Python-only（All-language 退出）→ 05-26 重回 Top 12 #9。与昨日的 paperless-ngx（#10，文档管理）一起构成今日"非 AI 工具类"双入 Top 12：一个是金融分析（Fincept），一个是文档管理（paperless-ngx）——在 AI agent 工具浪潮中，**生产力基础设施**方向稳定在 Trending 内占据席位。

---

### #10 · paperless-ngx/paperless-ngx

**今日新上榜 · 社区驱动文档管理系统 · 41k Stars**

- **仓库**：https://github.com/paperless-ngx/paperless-ngx
- **Stars**：41,369 | Forks：2,748
- **语言**：Python
- **描述**：A community-supported supercharged document management system: scan, index and archive all your documents
- **编辑点评**：今日唯一的纯"非 AI"经典工具类项目新入榜（Fincept 已有 AI 分析功能）。41,369 Stars，2,748 forks，说明文档自动化管理需求持久。在 AI agent 工具主导的 Trending 中，paperless-ngx 的出现是"AI 辅助管理本地文档"需求的信号——用 AI agent 搭配 paperless-ngx 实现全自动文档归档是一个自然的使用场景。

---

### #11 · anthropics/claude-cookbooks

**今日新上榜 · Anthropic 官方 · 第三个本周入 Top 12 的 Anthropic 仓**

- **仓库**：https://github.com/anthropics/claude-cookbooks
- **Stars**：44,062 | Forks：5,052
- **语言**：Python（Jupyter Notebook）
- **描述**：A collection of notebooks/recipes showcasing some fun and effective ways of using Claude.
- **编辑点评**：今日 Anthropic 第三个官方仓库本周入 Top 12（本周：claude-plugins-official 05-24~05-25，knowledge-work-plugins 05-25~05-26，claude-cookbooks 今日入）。claude-cookbooks 是"实战 demo 层"——具体用法示例/Notebook，和 knowledge-work-plugins（"插件生态层"）以及 claude-plugins-official（"开发者插件目录层"）互补，完整覆盖 Claude 官方的"展示→配置→实操"三个信息层。44,062 Stars，5,052 forks，是今日 Anthropic 三仓中 Stars 最高的。

---

### #12 · Leonxlnx/taste-skill

**今日新上榜 · Anti-Slop Frontend Framework · 设计品味 Skills**

- **仓库**：https://github.com/Leonxlnx/taste-skill
- **Stars**：19,842 | Forks：1,659
- **语言**：Markdown
- **描述**：Taste-Skill - gives your AI good taste. stops the AI from generating boring, generic slop
- **核心定位**：
  - "The Anti-Slop Frontend Framework for AI Agents"——Portable Agent Skills，升级 AI 构建的界面：更强的布局 / 排版 / 动效 / 间距，避免模板化 boilerplate UI
  - 包含图像生成 Skills（参考板：web/mobile/brand kits）
  - 配合 ChatGPT Images → Codex / Cursor / Claude Code 实现全链路
- **编辑点评**：今日"Skills 六连"中定位最独特的一个——专门针对 **UI/设计品味**领域。其他 Skills 关注的是"代码质量/安全/流程/行为"，taste-skill 是"让 AI 产生的 UI 有美感"。与同日 Explore 的 hardikpandya/stop-slop（散文品味）共同指向：AI 生成内容的"质量/美感"已经成为独立的优化方向，不再只是功能性正确性。

---

## 语言分布

| 语言 | 项目数 | 占比 | 项目 |
|---|---|---|---|
| Markdown | 5 | 42% | ECC / andrej-karpathy-skills / knowledge-work-plugins / Cybersecurity-Skills / taste-skill |
| Python | 4 | 33% | Understand-Anything / rohitg00 / paperless-ngx / claude-cookbooks（Jupyter）|
| TypeScript | 1 | 8% | codegraph |
| Swift | 1 | 8% | cmux |
| C++ | 1 | 8% | FinceptTerminal（C++20 + Qt6）|

今日 Markdown 超越 Python 成为占比最高语言，是本系列日报首次。5 个 Markdown 项目全部是 Skills/配置/插件类项目，印证了 Markdown-as-infrastructure 趋势：**Markdown 文件正在成为 agent 行为的编程语言**。

---

## GitHub Explore 精选

### Explore #1 · garrytan/gstack

- **Stars**：102,560 | Forks：15,295
- **语言**：Markdown
- **描述**：Use Garry Tan's exact Claude Code setup: 23 opinionated tools that serve as CEO, Designer, Eng Manager, Release Manager, Doc Engineer, and QA
- **作者**：Garry Tan，Y Combinator President & CEO，前 Palantir 工程师，Posterous 联创（sold to Twitter）
- **Sprint 流程**：Think → Plan → Build → Review → Test → Ship → Reflect（23 个专业角色 slash command）
- **生产力数据**："2026 run rate ~810× my 2013 pace（11,417 vs 14 logical lines/day）"；"In last 60 days: 3 production services, 40+ shipped features, part-time while running YC full-time"
- **GBrain**：持久知识体系，10-15 个并行 sprint 支持
- **分析**：102,560 Stars，仅以第 17 位差一步入 Top 12。今日与 ECC（#4，192k）和 karpathy-skills（#8，155k）构成 agent setup 三角格局：技术系统层（ECC）/ 工程行为层（karpathy-skills）/ CEO 产品流程层（gstack）。MIT 开源，所有内容皆 Markdown + slash commands。

### Explore #2 · moeru-ai/airi

- **Stars**：39,768 | Forks：4,023
- **语言**：TypeScript
- **描述**：Self hosted, you-owned Grok Companion — Self hosted AI waifu/companion capable of realtime voice chat, Minecraft, Factorio playing. Web / macOS / Windows supported.
- **分析**：今日 #13，39,768 Stars，4,023 forks。在 AI agent 工具主导的 Trending 中，airi 代表了"AI companion"方向——与 MiroFish（社会模拟）、frigate（本地视觉）一起，是 AI agent 技术向消费者/娱乐方向应用的信号。"Neuro-sama's altitude"——目标是实现 VTuber 级别的 AI 交互品质。Self-hosted，用户自主控制数据。

### Explore #3 · hardikpandya/stop-slop

- **Stars**：4,458 | Forks：385
- **语言**：Markdown
- **描述**：A skill file for removing AI tells from prose
- **分析**：今日 #16，4,458 Stars。与 Leonxlnx/taste-skill（#12，UI 品味）共同构成"Anti-Slop 双入"：taste-skill 消除 UI slop，stop-slop 消除 prose slop。两个方向都指向同一需求：**AI 生成内容的"去 AI 味"**，让输出真正有品位而非通用模板。这是 Skills 生态进入"内容质量"优化阶段的信号，从"功能正确性"到"表达品质"的升维。

### Explore #4 · sansan0/TrendRadar（Python Trending）

- **Stars**：58,289 | Forks：24,415
- **语言**：Python
- **描述**：AI-driven public opinion & trend monitor with multi-platform aggregation, RSS, and smart alerts. AI 舆情监控助手：聚合多平台热点 + RSS 订阅，AI 分析简报直推手机，支持 MCP 架构，Docker，微信/飞书/钉钉/Telegram/邮件等通知渠道。
- **分析**：58,289 Stars，24,415 forks（极高 fork 率！），Python Trending 今日高位。AI 驱动的信息聚合工具，支持 MCP 架构（可接入 Claude Code 等 agent），数据本地/云端自持。在 AI agent 工具生态中，TrendRadar 代表了"信息摄取层"——agent 需要聚合多源信息，TrendRadar 正好填补这个位置。中国团队出品，中英双语。

### Explore #5 · microsoft/agent-governance-toolkit（Python Trending）

- **Stars**：2,264 | Forks：394
- **语言**：Python
- **描述**：AI Agent Governance Toolkit — Policy enforcement, zero-trust identity, execution sandboxing, and reliability engineering for autonomous AI agents. Covers 10/10 OWASP Agentic Top 10.
- **分析**：微软官方，Python，"One pip install, any framework"。今日 Python Trending，Public Preview。随着 ECC（192k，Skills + AgentShield）入 Top 12，今日最重要的新信号之一是：**agent 安全治理**从可选项变为主流配置。Cybersecurity-Skills（#5，安全专域）+ microsoft/agent-governance-toolkit（OWASP Agentic Top 10）+ ECC AgentShield（安全模块）= 今日 agent 安全三角。

---

## 今日 vs 昨日（05-25）对比

### 留榜项目（1天增量）

| 项目 | 05-25 Stars | 05-26 Stars | +1天 | 排名变化 |
|---|---|---|---|---|
| Lum1104/Understand-Anything | 27,153（#1）| 31,575 | **+4,422（+16.3%）** | #1→#1 |
| anthropics/knowledge-work-plugins | 14,233（#4）| 15,593 | +1,360（+9.6%）| #4→#2 |
| rohitg00/ai-engineering-from-scratch | 16,658（#2）| 18,823 | +2,165（+13%）| #2→#3 |
| multica-ai/andrej-karpathy-skills | 152,682（#5）| 155,178 | +2,496 | #5→#8 |
| colbymchenry/codegraph | 22,862（#8）| 25,407 | +2,545（+11%）| #8→#6 |
| manaflow-ai/cmux | 19,107（#11）| 19,534 | +427 | #11→#7 |
| Fincept-Corporation/FinceptTerminal | Python-only | 23,916 | — | 重回 #9 |

### 今日退出（05-25 Top 12 → 05-26 未入 Top 12）

claude-plugins-official（#3，27k）、earendil-works/pi（#6，54k）、free-claude-code（#7，29k）、multica/multica（#9，33k）、Kronos（#10，26k，降至 #14）、MiroFish（#12，62k，降至 Python Trending）

---

*报告生成：2026-05-26 · 数据来源：https://github.com/trending + https://github.com/trending/python?since=daily*
