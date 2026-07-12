# GitHub Trending 日报

## Meta

- 日期：2026-04-30
- 数据来源：https://github.com/trending + https://github.com/trending/python?since=daily
- 文件名：github_trending_report_2026-04-30.md
- 编码：UTF-8
- 语言：中文简体

---

## Page Intent

本报告记录 2026-04-30 GitHub Trending 全语言与 Python 频道的热门项目。与上期（2026-04-29）对比，今日共 **7 个新上榜项目**，涵盖 Agent Skills 工作流方法论、开源 Agent 开发环境、LLM 量化金融应用双料、模型安全消融研究等多条主线，是近期内容多样性最高的一期。

---

## Stats

- 今日关注项目总数：12
- 今日新上榜：7
- 今日持续上榜：5
- 本期最高 Stars：obra/superpowers（173,886 ⭐）
- 语言分布：Python 5 / TypeScript 3 / Rust 1 / Markdown+Shell 2 / JavaScript 1

---

## Editorial Insights

### 洞察一：Agent Skills 工作流基础设施三层生态同日成型

obra/superpowers（173k）提供"工作流方法论"层：TDD 红绿循环、Subagent-Driven Development、Plan-Execute-Review 全流程 skills 自动触发。mattpocock/skills（47k）提供"工程师真实日常"层：TypeScript 专家真实 `.claude` 目录直接开源。ComposioHQ/awesome-codex-skills（5k）提供"工具集成"层：1000+ 应用的动作接入。三个项目同日上榜说明 Agent Skills 生态的三个层次（方法论 / 工作流 / 工具）正同步走向成熟。

### 洞察二：Warp 宣布开源并以 OpenAI 为创始赞助商

warpdotdev/warp（46k）本周将其客户端代码库正式开源，采用 AGPL-3.0 + MIT 双许可。OpenAI 是创始赞助商，新的 agentic 管理工作流由 GPT 模型驱动。Warp 定位从"专有 AI 终端"变为"开源 Agent 开发环境"，支持接入 Claude Code、Codex、Gemini CLI 等外部 Agent，并通过 build.warp.dev 提供数千 Oz Agent 实时施工看板。这是本周最重要的开发环境开源事件。

### 洞察三：LLM 量化金融应用双料上榜，覆盖两个极端

TauricResearch/TradingAgents（56k）以"机构量化仿真"为出发点，复现真实交易公司架构：基本面 / 情绪 / 新闻 / 技术四路分析师 + 多头空头研究员辩论 + 交易 Agent + 风险管理，v0.2.4 已支持 DeepSeek/Qwen/GLM/Azure。ZhuLinsen/daily_stock_analysis（33k）则主打"零成本定时白嫖"：GitHub Actions + 多数据源 + LLM 决策仪表盘 + 多渠道推送，真正的散户 LLM 炒股工具。两个方向同日登榜，说明 LLM 进入投资决策的时代信号已从学术走向工程实践。

### 洞察四：模型安全消融自动化工具引发社区广泛复制

p-e-w/heretic（20k）基于 Arditi et al. 2024 方向性消融理论，结合 Optuna TPE 优化器自动寻找最优消融参数，在最小化 KL 散度（保留原始模型能力）的同时消除拒绝行为。无需理解 Transformer 内部原理即可使用，社区已产出超过 1000 个 Heretic 模型并发布在 HuggingFace，覆盖 Gemma-3、GPT-OSS 20B、Qwen3 等多个模型系列。LLM 安全对齐与本地自由使用之间的博弈正在白热化。

---

## Top 12 Projects

### 01 obra/superpowers

- 仓库：https://github.com/obra/superpowers
- Stars：173,886 | Forks：15,335
- 语言：Shell / Markdown
- 许可：MIT
- 标签：agent-skills, claude-code, codex, cursor, gemini-cli, tdd, subagent-driven-development
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

Superpowers 是一套 Agentic Skills 框架 + 软件开发方法论。当你启动 coding agent 时，它不会直接写代码，而是先帮你把"真正想做什么"从对话中提炼成规格说明，逐段确认，再生成足够清晰的实现计划，然后启动 subagent-driven development 流程——多个子 agent 依次完成任务、互相 inspect 和 review，Claude 通常可以无干预连续自主工作数小时。

**主要特性**

- 自动触发：不需要手动激活，skill 在你开始构建时自动介入
- Skills 库：test-driven-development（RED-GREEN-REFACTOR 完整循环）、systematic-debugging（4 阶段根因分析）、dispatching-parallel-agents（并发子 agent 工作流）、subagent-driven-development（两阶段 review：规格合规 + 代码质量）
- 跨平台安装：Claude Code 官方 Marketplace、OpenAI Codex CLI、Codex App、Cursor、OpenCode、GitHub Copilot CLI、Gemini CLI
- 作者：Jesse（obra），Superpowers GitHub Sponsors 活跃

**技术栈**

Shell / Markdown / Claude Code SKILL 格式 / Subagent 协调机制

**适用场景**

- 需要 AI agent 长时间自主完成复杂工程任务
- 希望把 TDD、YAGNI、DRY 等工程实践内置到 Agent 工作流
- 多平台统一 Agent Skills 管理

**推荐语**

> "不是 Skills 合集，而是方法论。173k stars 背后是：让 agent 真正可以自主工作几小时而不偏离方向。"

---

### 02 mattpocock/skills

- 仓库：https://github.com/mattpocock/skills
- Stars：47,003 | Forks：3,822
- 语言：TypeScript
- 许可：MIT
- 标签：agent-skills, claude-code, typescript, real-engineers
- 是否新上榜：**否（持续上榜）**

**核心摘要**

TypeScript 专家 Matt Pocock 把自己日常工作使用的 `.claude` 目录直接开源，"Skills for Real Engineers"。这不是为了展示而写的 demo，而是真实生产环境里检验过的 AI 编程工作流指令集，一键安装即可使用。

**主要特性**

- 真实性：直接来自 Matt 个人 .claude 目录，非演示项目
- 覆盖：TypeScript 开发常见场景，含类型设计、重构、测试等
- 一键安装：npx 命令支持
- 简洁：不臃肿，只保留真正有效的工作流

**技术栈**

TypeScript / Claude Code SKILL 格式 / npx 安装工具链

**适用场景**

- TypeScript 工程师日常 AI 辅助开发
- 参考真实工程师如何设计 Agent 工作流

**推荐语**

> "Matt Pocock 是 TypeScript 社区标杆，他真实用的 skills 值得每个 TS 开发者看一遍。"

---

### 03 warpdotdev/warp

- 仓库：https://github.com/warpdotdev/warp
- Stars：46,734 | Forks：2,924
- 语言：Rust / TypeScript
- 许可：AGPL-3.0 / MIT（双许可）
- 标签：terminal, agent, agentic-dev-environment, rust, openai
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

Warp 宣布将其客户端代码库正式开源，定位从"专有 AI 终端"升级为"开源 Agentic 开发环境"。OpenAI 是创始赞助商，新的 agentic 管理工作流由 GPT 模型驱动。用户既可以使用 Warp 内置 coding agent，也可以接入 Claude Code、Codex、Gemini CLI 等外部 agent，共享 Warp 的终端 UI 框架和工作流工具。

**主要特性**

- build.warp.dev：实时查看数千 Oz Agent 处理 issues / 编写规格 / 实现变更 / review PRs 的过程，可点进正在运行的 agent session
- UI 框架开源：warpui_core + warpui crate 采用 MIT 许可，核心业务逻辑采用 AGPL-3.0
- 多 Agent 接入：支持 Claude Code、Codex CLI、Gemini CLI 等任意命令行 agent
- 网站：warp.dev，提供平台特定安装文档

**技术栈**

Rust（Diesel ORM，rust-toolchain）/ TypeScript / AGPL-3.0 + MIT 双许可

**适用场景**

- 需要把 AI agent 工作流集成进终端的开发者
- 希望在开源代码基础上定制 Agent 工作环境
- 团队共享 agent 操作可视化看板

**推荐语**

> "Warp 开源不只是代码可见，而是把'AI Agent 在做什么'这件事变成了公开可见的仪表盘——开发环境透明化的里程碑。"

---

### 04 microsoft/VibeVoice

- 仓库：https://github.com/microsoft/VibeVoice
- Stars：45,928 | Forks：5,070
- 语言：Python / TypeScript
- 许可：MIT
- 标签：voice-ai, asr, tts, microsoft, streaming, multilingual
- 是否新上榜：**否（持续上榜）**

**核心摘要**

微软开源的前沿语音 AI 全栈框架，60分钟级别 ASR（自动语音识别）、90分钟多人 TTS（文字转语音）、实时流式 TTS，覆盖 50+ 语言，适合端到端语音应用构建。

**主要特性**

- 超快 ASR：60 分钟音频实时处理
- 多人 TTS：90 分钟长文本转语音
- 流式 TTS：低延迟实时语音生成
- 50+ 语言支持
- 微软工程团队维护，稳定性保障

**技术栈**

Python / TypeScript / Microsoft Azure 生态 / 流式音频处理

**适用场景**

- 构建语音交互应用
- 会议录音转写与摘要
- 多语言语音内容生产

**推荐语**

> "微软 VibeVoice 让'语音 AI'不再是 API 包装，而是可以本地完整运行的工程级全栈框架。"

---

### 05 TauricResearch/TradingAgents

- 仓库：https://github.com/TauricResearch/TradingAgents
- Stars：56,409 | Forks：10,572
- 语言：Python
- 许可：Apache-2.0
- 标签：llm, multi-agent, trading, finance, langgraph, deepseek
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

TradingAgents 是一个模拟真实交易公司架构的多 Agent LLM 金融交易框架。由专业分析师团队（基本面 / 情绪 / 新闻 / 技术四路）、多头空头研究员对抗辩论、交易 Agent、风险管理与组合经理构成，协同评估市场并作出交易决策。v0.2.4 已支持 DeepSeek、Qwen、GLM、Azure，具备 LangGraph checkpoint 断点续跑能力。

**主要特性**

- Analyst Team：基本面分析师（估值/财务）、情绪分析师（社交媒体）、新闻分析师（宏观事件）、技术分析师（MACD/RSI）
- Researcher Team：多头/空头研究员结构化辩论，平衡收益与风险
- Trader Agent：综合分析报告决策交易时机和规模
- Risk Management：持续评估波动率、流动性等风险因子，Portfolio Manager 审批/拒绝交易提案
- v0.2.4：structured-output agents、LangGraph checkpoint resume、persistent decision log

**技术栈**

Python / LangGraph / DeepSeek / Qwen / GLM / Azure / Docker / CLI

**适用场景**

- LLM 量化研究与策略回测
- 多 Agent 协作决策研究
- 金融 AI Agent 原型构建

**推荐语**

> "TradingAgents 把'LLM 能不能做量化'这个问题变成了一个完整的可运行框架——分析师、研究员、交易员、风控全班人马到齐。"

---

### 06 ZhuLinsen/daily_stock_analysis

- 仓库：https://github.com/ZhuLinsen/daily_stock_analysis
- Stars：33,342 | Forks：33,163
- 语言：Python
- 许可：MIT
- 标签：llm, stock-analysis, github-actions, a-share, us-stock, push-notification
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

LLM 驱动的 A/H/美股智能分析器：多数据源行情 + 实时新闻 + LLM 决策仪表盘 + 多渠道推送，设计理念是零成本定时运行（GitHub Actions 免费额度）。已发布 16 个版本，具备 Web 界面和 Agent 策略问股功能。

**主要特性**

- 多市场：A 股、港股、美股全覆盖
- LLM 决策仪表盘：基于行情 + 新闻生成买卖建议与理由
- 多渠道推送：支持微信、钉钉、Telegram、邮件等
- 零成本运行：GitHub Actions 定时触发，无需服务器
- 数据源：SerpAPI、Tavily、Bocha、Brave、MiniMax 等
- Web 界面 + Agent 策略问股：可交互式使用

**技术栈**

Python / GitHub Actions / Tavily / SerpAPI / MiniMax / Docker

**适用场景**

- 个人投资者每日股票智能摘要
- GitHub Actions 无服务器定时任务实践
- LLM 在金融决策场景的应用探索

**推荐语**

> "33k stars 中有一半是认同'零成本 LLM 炒股'这件事可行的人，另一半是真的在用。"

---

### 07 abhigyanpatwari/GitNexus

- 仓库：https://github.com/abhigyanpatwari/GitNexus
- Stars：33,585 | Forks：3,815
- 语言：JavaScript / TypeScript
- 许可：MIT
- 标签：knowledge-graph, graph-rag, browser, code-intelligence, zero-server
- 是否新上榜：**否（持续上榜）**

**核心摘要**

GitNexus 是一个完全客户端运行的代码知识图谱生成器 + Graph RAG Agent。无需部署任何服务器，直接在浏览器中放入 GitHub 仓库链接或 ZIP 文件，即可生成交互式知识图谱，并内置 RAG Agent 进行代码探索问答。

**主要特性**

- 零服务器：纯浏览器端运行，无后端依赖
- 交互式知识图谱：可视化代码结构与依赖关系
- 内置 Graph RAG Agent：基于图结构的代码问答
- 支持 GitHub 仓库 URL 或 ZIP 文件输入

**技术栈**

JavaScript / TypeScript / Browser-side Graph Processing / RAG

**适用场景**

- 快速理解陌生代码仓库结构
- 代码审查前的结构可视化
- 无部署成本的代码智能工具

**推荐语**

> "浏览器里的 Codemap，让每个人都能在 30 秒内看懂一个陌生仓库的结构。"

---

### 08 p-e-w/heretic

- 仓库：https://github.com/p-e-w/heretic
- Stars：20,245 | Forks：2,072
- 语言：Python
- 许可：MIT
- 标签：llm, abliteration, censorship-removal, safety-alignment, optuna, transformer
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

Heretic 是一个全自动 LLM 安全对齐消除工具，基于 Arditi et al. 2024 方向性消融（directional ablation / abliteration）理论，结合 Optuna TPE 参数优化器，在共同最小化拒绝率和与原始模型 KL 散度的条件下自动找到最优消融参数，无需手动调参，无需理解 Transformer 内部结构。社区已基于 Heretic 发布超过 1000 个消融模型。

**主要特性**

- 全自动：Optuna TPE 优化器自动搜索参数，无需人工干预
- 双目标优化：最小化拒绝率 + 最小化 KL 散度（保留模型能力）
- 参数化方向消融：direction_index、max/min_weight 等可学习参数
- 支持大多数稠密模型，含多模态模型，部分 MoE 架构
- HuggingFace 社区：已产出 1000+ Heretic 模型

**技术栈**

Python / PyTorch / Optuna / HuggingFace Transformers / RTX 5090 基准测试

**适用场景**

- 本地 LLM 安全限制研究
- 模型安全对齐机制学术研究
- 开放权重模型定制化

**推荐语**

> "Heretic 把'消融'从专家手艺变成了可重复的工程工具——1000+ 社区模型是最好的证明。"

---

### 09 HunxByts/GhostTrack

- 仓库：https://github.com/HunxByts/GhostTrack
- Stars：11,876 | Forks：1,611
- 语言：Python
- 许可：MIT
- 标签：osint, geolocation, phone-number, tracking, python
- 是否新上榜：**否（持续上榜）**

**核心摘要**

基于 Python 的 OSINT 地理位置追踪工具，支持通过手机号码进行信息查询与位置捕获，适合安全研究和信息安全意识教育场景。

**主要特性**

- 手机号码信息查询
- 地理位置捕获
- Python 实现，跨平台运行
- OSINT 工具链集成

**技术栈**

Python / OSINT / Geolocation APIs

**适用场景**

- 安全研究与渗透测试学习
- OSINT 信息搜集演练
- 信息安全意识教育

**推荐语**

> "OSINT 入门级工具，连续多日 Trending 说明安全类开源工具在 AI 工具链时代仍有持续关注度。"

---

### 10 ComposioHQ/awesome-codex-skills

- 仓库：https://github.com/ComposioHQ/awesome-codex-skills
- Stars：5,065 | Forks：311
- 语言：Markdown
- 许可：MIT
- 标签：codex, agent-skills, automation, workflow, composio
- 是否新上榜：**否（持续上榜）**

**核心摘要**

Composio 精选的 Codex Skills 实用合集，专注于通过 Codex CLI 和 API 实现跨应用工作流自动化。接入 1000+ 应用，涵盖 Linear、GitHub、Slack、Gmail 等常见开发工具，每个 skill 均可直接执行真实动作。

**主要特性**

- 1000+ 应用工具集成
- 每个 skill 可直接执行真实动作（非只读）
- 覆盖开发、运营、沟通常见场景
- Composio 官方维护，持续更新

**技术栈**

Markdown / Composio SDK / Codex CLI 格式

**适用场景**

- Codex 用户快速接入外部工具
- 企业工作流自动化构建
- Agent 工具集成参考

**推荐语**

> "Skills 生态的'工具集成层'——有了它，Codex 才能真的做事，而不只是写代码。"

---

### 11 lukilabs/craft-agents-oss

- 仓库：https://github.com/lukilabs/craft-agents-oss
- Stars：5,456 | Forks：730
- 语言：TypeScript
- 许可：Apache-2.0
- 标签：agent, claude, claude-agent-sdk, desktop-app, mcp, agent-native
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

Craft Agents 是 craft.do 团队基于 Claude Agent SDK + Pi SDK 构建的开源 Agent 原生桌面应用。核心理念是 Agent Native 软件：你告诉 agent 你想做什么，它自己搞定连接、配置、工具调用，无需手动配置 MCP。已发布 60 个版本，并用 Craft Agents 自身构建 Craft Agents（dogfood）。

**主要特性**

- 自然语言接入任意服务：告诉 agent "加 Linear 作为 source"，它自己找 API/MCP、读文档、配凭证
- 支持本地 MCP、OpenAPI 规格、自定义 API
- 32+ Craft 文档工具（block、collection、search、task）
- Multi-Session Inbox：会话管理 + 状态工作流 + 标记系统
- Multi-File Diff：VS Code 风格的变更预览
- 三级权限模式：Explore / Ask to Edit / Auto
- 远程服务器 headless 模式 + CLI 客户端

**技术栈**

TypeScript / Claude Agent SDK / Pi SDK / Electron / MCP / Google OAuth

**适用场景**

- 非 CLI 用户的 Agent 工作台
- 文档为中心的 Agent 工作流（区别于代码编辑器中心）
- 自定义 Agent 桌面工具开发基础

**推荐语**

> "Craft Agents 是第一批把'用 Agent 构建 Agent 工具'做到真正可用的产品之一，dogfood 战略让它的可信度远高于同类。"

---

### 12 1jehuang/jcode

- 仓库：https://github.com/1jehuang/jcode
- Stars：1,642 | Forks：147
- 语言：TypeScript
- 许可：MIT
- 标签：coding-agent, multi-session, swarm, oauth, browser-automation
- 是否新上榜：**是（今日新上榜）**

**核心摘要**

jcode 是下一代 Coding Agent Harness，专注于多会话工作流、极致可定制化和高性能。支持 Swarm 模式（并发子 agent）、OAuth 多 Provider、浏览器自动化、多 LLM Provider，已发布 51 个版本，是面向高级工程师的 Agent 框架工具。

**主要特性**

- Multi-Session 工作流：并发多会话管理
- Swarm 模式：并发子 agent 协同
- 性能优化：Time to first frame / first input 极低
- OAuth 多 Provider：内置登录流，支持自托管端点和 MCP
- 浏览器自动化：集成 browser automation
- iOS 应用（Native OpenClaw）计划中

**技术栈**

TypeScript / OAuth / MCP / Swarm / Browser Automation

**适用场景**

- 多 session、多 agent 并发工作场景
- 高定制化 coding agent 工具链构建
- Agent 框架研究与集成

**推荐语**

> "51 次发布背后是一个正在快速成长的 agent harness，Swarm 模式是它最值得关注的差异化方向。"

---

## Language Distribution

| 语言 | 项目数 | 代表项目 |
|---|---|---|
| Python | 5 | TradingAgents, daily_stock_analysis, GhostTrack, heretic, VibeVoice |
| TypeScript | 3 | mattpocock/skills, craft-agents-oss, jcode |
| Rust | 1 | warpdotdev/warp |
| Markdown/Shell | 2 | obra/superpowers, awesome-codex-skills |
| JavaScript | 1 | GitNexus |

---

## GitHub Explore Highlights

以下项目出现在 Python Trending 或全语言 Trending 后半段，未进入 Top 12，但具有关注价值：

1. **gorhill/uBlock**（64,150 ⭐）- uBlock Origin 浏览器扩展，Firefox/Chrome 128 配套更新推动本周再度回热，隐私工具常青树

2. **deepseek-ai/DeepSeek-V3**（103,309 ⭐）- Python Trending 持续在榜，社区集成实验和微调工作流活跃度仍在上升

3. **hugohe3/ppt-master**（9,820 ⭐）- AI 从任意文档生成原生可编辑 PPTX，使用真实 PowerPoint 形状 + 原生动画，而非图片嵌入，是办公场景 AI 应用的代表方向

4. **shaxiu/XianyuAutoAgent**（7,324 ⭐）- 闲鱼平台 AI 值守机器人，7×24 小时自动化响应 + 多专家协同决策 + 智能议价 + 上下文感知对话，LLM 在垂直电商场景的落地案例

5. **microsoft/PowerToys**（132,545 ⭐）- 微软 Windows 生产力工具集，近期 v0.90 更新后社区活跃度回升

---

## Rendering Notes

- 新上榜项目卡片需使用绿色边框 + "今日新上榜" badge 视觉标注
- 项目排名以 stars 综合排序，非原始 Trending 位置
- 所有项目卡片支持展开详情（features、tech-tags、recommend-quote）
- HTML 需使用固定 UI 模板（fixedBaseTemplate_2026-03-16.html），不得重新设计 UI
