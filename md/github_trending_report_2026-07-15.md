# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-15
- Generated At: 2026-07-15 21:01:52 JST
- Output Markdown: `md/github_trending_report_2026-07-15.md`
- Planned HTML: `html/github_trending_report_2026-07-15.html`
- Fixed Base Template: `.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html`
- User Rules: `.codex/skills/skill-github-trending-report/reference/user-rules.md`
- Sources:
  - https://github.com/trending?since=daily
  - https://github.com/explore
  - Top 项目的 GitHub 仓库页、README、About、Release、官方文档与源码

## Page Intent

- 今日主线：视频创作工具突然冲到榜首，而 Agent 工程正在从“会调用模型”继续向技能库、设计质量门禁和金融研究工作流细分。
- 适合谁阅读：想快速判断当天开源热点、寻找可落地工具，或准备深入研究工程架构的开发者与技术决策者。
- 页面重点：先看 Stars Today 的真实增速，再区分“可直接运行的软件系统”和“资源、技能、数据集合”。
- 需要诚实降级说明的地方：OpenCut 当前主分支是重写工程；ai-hedge-fund 与 Vibe-Trading 均明确不构成投资建议；SharpEmu 仍处于早期实验阶段；exercises-dataset 的媒体文件有独立使用条款。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：12,073
- 编程语言数：9
- AI 相关项目数：7

## Editorial Insights

### Insight 1
- Title: 🎬 OpenCut 一天新增 4,276 Stars，创作工具成了今天最响的一炮
- Body: OpenCut 的今日增星超过榜单总增量的三分之一。它吸引人的不只是“开源剪映替代品”，而是团队正在把编辑器重写为 Rust 核心、插件优先、可扩展的多端架构。不过当前主分支仍在设计和重写期，想马上用于生产剪辑，应先看 Classic 版本和成熟度说明。

### Insight 2
- Title: 🧩 Agent 竞争进入“技能与质量标准”阶段
- Body: mattpocock/skills、Hallmark 和 awesome-llm-apps 合计新增 3,800 Stars。信号很清楚：大家不再满足于一个通用聊天框，而是在争夺可复用技能、设计质量门禁和可复制应用范式。这里面既有工具，也有资源集合，挑项目时别把“资料多”误认成“系统架构成熟”。

### Insight 3
- Title: 📈 AI 交易工具热度高，风险提示也得跟上
- Body: Vibe-Trading 今日新增 1,256 Stars，显著高于 ai-hedge-fund 的 109。前者已经扩展到 FastAPI、React、MCP、回测、会话和实验性券商执行；后者仍强调教育与研究用途。两者都值得研究 Agent 工作流，但都不能拿回测图当提款机说明书。

### Insight 4
- Title: 🛠️ 榜单两头都在讲“可控性”
- Body: Win11Debloat 用脚本控制操作系统噪音，Penpot 用开放标准控制设计资产，grok2api 用路由、账号池和审计控制模型访问。今天真正有工程含量的共同点不是“用了 AI”，而是把复杂系统的入口、权限、状态和失败处理说清楚。

## Top Projects

### Rank 01 - Shubhamsaboo/awesome-llm-apps
- Repo URL: https://github.com/Shubhamsaboo/awesome-llm-apps
- Tagline: LLM 应用、AI Agent 与 RAG 示例集合，覆盖从入门 Demo 到多 Agent 工作流。
- Stars: 121,210
- Stars Today: 1,106
- Forks: 17,921
- Language: Python
- License: Apache-2.0
- Homepage: https://www.theunwindai.com
- Topics: python, agents, rag, llms, generative-ai, ai-agents
- 技术栈: Python, 多家 LLM SDK, RAG, 向量数据库, Agent 框架
- Why It Matters Today: 今日新增 1,106 Stars，说明“可复制的 AI 应用配方”仍有很强的学习需求。
- 项目摘要: 这是一个大型示例与教程集合，把常见 LLM 应用、RAG、语音、视觉和多 Agent 场景整理为可运行项目。它更像工具箱和教材，不是一个统一运行时或产品。
- 核心特性:
  1. 按 Agent、RAG、语音、视觉和业务场景组织示例，方便按问题找参考实现。
  2. 示例通常包含完整代码和依赖说明，适合快速验证技术路线。
  3. 覆盖多种模型与框架，便于比较不同组合，而不必从空项目起步。
- 适用场景: AI 应用原型学习、方案调研、寻找可复用 Demo；不适合直接作为统一生产平台部署。
- 一句话推荐: 想抄作业可以来，想找一套统一架构得另看——这是菜谱大全，不是一口锅。
- Evidence Notes: GitHub Trending 排名与增星；仓库 README、About、目录和 Apache-2.0 许可证。
- Honest Caveat: 仓库内容跨度很大，各示例的维护质量、安全性和生产成熟度不一致，使用前需要逐个验收。

### Rank 02 - mattpocock/skills
- Repo URL: https://github.com/mattpocock/skills
- Tagline: 面向 Claude Code、Codex 等编程 Agent 的小型、可组合工程技能集。
- Stars: 170,917
- Stars Today: 1,679
- Forks: 14,702
- Language: Shell
- License: MIT
- Homepage: https://aihero.dev
- Topics: agent-skills, claude-code, codex, software-engineering
- 技术栈: Markdown/Skill 定义, Shell, Agent Skill 安装器
- Why It Matters Today: 今日新增 1,679 Stars，排名第二，Agent Skill 正从个人提示词变成可分发工程资产。
- 项目摘要: Matt Pocock 整理的一组可组合编程技能，目标是给支持 Skills 的编码 Agent 增加更明确的软件工程工作流。它的价值主要在方法和指令资产，而不是运行一个独立后端系统。
- 核心特性:
  1. 通过 `npx skills@latest add mattpocock/skills` 等方式安装到兼容 Agent。
  2. 每个技能聚焦一个工程问题，便于组合而不是塞进超长总提示词。
  3. 同时提供 Claude 插件和通用 Skill 分发路径。
- 适用场景: 希望标准化 AI 编程流程的个人和团队；需要完整任务编排、审计或权限系统时，还要搭配具体 Agent 平台。
- 一句话推荐: 这是给编程 Agent 发的“岗位说明书”，不是再造一个 Agent 公司。
- Evidence Notes: GitHub Trending；仓库 README、安装说明、Skill 目录和 MIT 许可证。
- Honest Caveat: Skill 的实际效果依赖所用模型、宿主工具和项目上下文，Stars 不能替代任务级评测。

### Rank 03 - OpenCut-app/OpenCut
- Repo URL: https://github.com/OpenCut-app/OpenCut
- Tagline: 开源、跨平台的视频编辑器；当前主仓库正在进行插件优先的全新重写。
- Stars: 69,577
- Stars Today: 4,276
- Forks: 7,231
- Language: TypeScript
- License: MIT
- Homepage: https://opencut.app
- Topics: video-editor, open-source, react, rust, desktop
- 技术栈: TypeScript, React, Rust, Moonrepo, 桌面/网页应用
- Why It Matters Today: 今日新增 4,276 Stars，位列榜单增速第一，是今天最强的非模型类热点。
- 项目摘要: OpenCut 希望提供无水印、无订阅、可自托管的视频编辑体验。当前主仓库是新架构重写：团队公开提出 Editor API、插件优先、Rust 核心和多端共用代码等方向；Classic 版本仍是现阶段更可用的实现。
- 核心特性:
  1. 以开源和本地控制为核心，瞄准常见短视频与时间线剪辑需求。
  2. 新架构计划让 Web、桌面和未来自动化入口共享 Rust 编辑核心。
  3. 开发命令按 Web、API、Desktop 分开，仓库采用统一工作区管理。
- 适用场景: 关注开源视频编辑器、插件架构或 Rust 多端核心的开发者；需要稳定生产剪辑时先验证 Classic 或等待重写成熟。
- 一句话推荐: 热度像开演唱会，主分支还在搭舞台——值得盯，但别拿装修图当交付房。
- Evidence Notes: GitHub Trending；仓库 README 的 rewrite、Classic、开发命令与架构目标说明；MIT 许可证。
- Honest Caveat: MCP、headless、统一 Rust Core 等多项能力仍属于重写目标或进行中设计，不能全部当成现成功能。

### Rank 04 - virattt/ai-hedge-fund
- Repo URL: https://github.com/virattt/ai-hedge-fund
- Tagline: 用多位“投资风格 Agent”协作完成市场研究和组合判断的教育型实验项目。
- Stars: 62,011
- Stars Today: 109
- Forks: 10,920
- Language: Python
- License: MIT
- Homepage: https://www.aihedgefund.ai
- Topics: ai-agents, finance, hedge-fund, llm, python
- 技术栈: Python, LLM Agents, 金融数据接口, 组合分析
- Why It Matters Today: 总 Stars 很高且仍在上榜，说明多 Agent 金融研究仍有持续关注，但今日增速相对温和。
- 项目摘要: 项目让多个模拟投资风格的 Agent 分别给出观点，再由组合管理与风险角色汇总。官方明确将其定位为教育和研究概念验证，而不是自动赚钱或真实投顾系统。
- 核心特性:
  1. 多角色并行研究，同一标的可从价值、增长、宏观等角度给出判断。
  2. 将分析、风险和组合决策拆开，便于观察多 Agent 如何协作与冲突。
  3. 提供命令行和可视化使用路径，适合学习金融 Agent 的编排方法。
- 适用场景: 多 Agent 教学、金融研究原型和决策流程实验；不适合直接用于真实资金自动交易。
- 一句话推荐: 看它研究 Agent 怎么开投委会可以，拿它当基金经理身份证就过了。
- Evidence Notes: GitHub Trending；仓库 README、免责声明、代码目录、最新 Release 与 MIT 许可证。
- Honest Caveat: 项目明确不构成投资建议，输出质量依赖数据、模型和提示词，未提供可替代独立实盘验证的证据。

### Rank 05 - Nutlope/hallmark
- Repo URL: https://github.com/Nutlope/hallmark
- Tagline: 给编码 Agent 使用的网页设计质量 Skill，用规则和审计门禁减少“AI 味”界面。
- Stars: 6,409
- Stars Today: 1,015
- Forks: 360
- Language: CSS
- License: MIT
- Homepage: https://usehallmark.com
- Topics: agent-skill, web-design, ui, claude-code, cursor, codex
- 技术栈: Agent Skill, CSS/前端设计规则, Markdown
- Why It Matters Today: 今日新增 1,015 Stars，说明开发者开始认真治理 AI 生成 UI 的审美和可用性问题。
- 项目摘要: Hallmark 把常见 AI 生成页面的问题整理成一套设计 Skill 和质量门禁，让 Claude Code、Cursor、Codex 等工具在生成或审计界面时少犯套路化错误。
- 核心特性:
  1. 提供 build、audit、redesign、study 等明确工作模式。
  2. 用数十项质量门禁检查排版、色彩、层级、动效和常见“AI 模板味”。
  3. 可安装进多种编码 Agent，作为项目级设计约束复用。
- 适用场景: AI 辅助前端开发、设计审查和团队 UI 规范；不替代真实用户研究、品牌设计或可访问性专项测试。
- 一句话推荐: 给 AI 设计稿请了个嘴损但有用的监工，至少不让它满屏渐变大药丸。
- Evidence Notes: GitHub Trending；仓库 README、Skill 内容、官网与 MIT 许可证。
- Honest Caveat: 规则能减少常见问题，但审美效果仍需结合品牌、用户和实际可用性验证。

### Rank 06 - HKUDS/Vibe-Trading
- Repo URL: https://github.com/HKUDS/Vibe-Trading
- Tagline: 面向自然语言金融研究、回测、多 Agent 协作和实验性交易执行的 AI 原生工作台。
- Stars: 23,138
- Stars Today: 1,256
- Forks: 3,966
- Language: Python
- License: MIT
- Homepage: https://vibetrading.wiki
- Topics: python, trading, ai-agents, mcp, backtesting, multi-agent
- 技术栈: Python, FastAPI, React, MCP, 文件化运行产物, 多 Agent
- Why It Matters Today: 今日新增 1,256 Stars，且近期连续强化 MCP、认证、沙箱和 Docker 安全边界。
- 项目摘要: Vibe-Trading 把自然语言研究目标转成会话、工具调用、证据、回测产物和可视化结果。它既有 FastAPI/React 工作台，也有 MCP、计划任务、群体 Agent 和实验性券商通道，是榜单里最值得研究的完整软件系统之一。
- 核心特性:
  1. 会话式研究入口，可创建目标、追加证据并通过 SSE 观察 Agent 执行事件。
  2. 运行结果落到目录，包含状态、策略代码、指标、交易记录、验证结果和分析数据。
  3. 提供认证、CORS、SSE Ticket、路径校验、上传限制和受控 Shell 等安全措施。
- 适用场景: 金融研究 Agent、策略原型、回测工作流和 MCP 集成研究；真实资金执行前必须独立安全审查和风控验证。
- 一句话推荐: 这是个金融研究实验室，不是彩票站；工具链挺全，钱包得自己看住。
- Evidence Notes: GitHub Trending；README、`agent/api_server.py`、`agent/src/api/sessions_routes.py`、`agent/src/api/runs_routes.py`、测试与近期提交。
- Honest Caveat: 官方明确不构成投资建议；券商执行属于实验能力，回测结果也不能代表未来收益。

### Rank 07 - Raphire/Win11Debloat
- Repo URL: https://github.com/Raphire/Win11Debloat
- Tagline: 用 PowerShell 清理 Windows 11 预装应用、遥测和常见界面干扰项。
- Stars: 51,962
- Stars Today: 783
- Forks: 2,144
- Language: PowerShell
- License: MIT
- Homepage: https://github.com/Raphire/Win11Debloat
- Topics: windows-11, debloat, powershell, privacy, telemetry
- 技术栈: PowerShell, Windows Registry, Appx 管理, 系统策略
- Why It Matters Today: 今日新增 783 Stars，说明新装机、系统更新后的可控性和隐私清理仍是高频刚需。
- 项目摘要: Win11Debloat 通过交互式或预设 PowerShell 脚本删除常见预装应用、关闭部分遥测和广告建议，并调整资源管理器与任务栏等设置。
- 核心特性:
  1. 提供默认、精简和自定义执行方式，降低手工改注册表的成本。
  2. 将应用卸载、隐私设置和界面调整集中到一个可审阅脚本仓库。
  3. 支持参数化和配置化运行，便于重复用于新设备。
- 适用场景: 个人新装 Windows 11、实验室设备初始化；企业环境应先在测试机验证并结合组策略管理。
- 一句话推荐: 系统自带一桌子赠品，它负责问你哪些真不要——下手前先备份，别把桌腿也扔了。
- Evidence Notes: GitHub Trending；仓库 README、脚本、参数说明和 MIT 许可证。
- Honest Caveat: Windows 版本和策略会变化，某些调整可能影响系统功能、企业管理或后续更新，必须先测试。

### Rank 08 - hasaneyldrm/exercises-dataset
- Repo URL: https://github.com/hasaneyldrm/exercises-dataset
- Tagline: 面向健身应用的结构化动作数据与 GIF 媒体集合。
- Stars: 13,813
- Stars Today: 851
- Forks: 1,652
- Language: HTML
- License: Code MIT；媒体文件适用独立条款
- Homepage: https://github.com/hasaneyldrm/exercises-dataset
- Topics: fitness, exercises, dataset, gif, workout
- 技术栈: JSON/静态数据, GIF 媒体, 多语言字段
- Why It Matters Today: 今日新增 851 Stars，数据资产型项目在应用开发者中依然吃香。
- 项目摘要: 仓库提供按部位、器械、目标肌群等字段整理的健身动作数据，并配有大量动作 GIF，方便快速搭建训练计划、动作检索或健身内容产品。
- 核心特性:
  1. 动作条目数量大，字段适合搜索、筛选和应用端展示。
  2. README 声称支持 9 种语言，可用于多语言健身产品原型。
  3. 数据与媒体分开说明授权，提醒开发者不能只看代码许可证。
- 适用场景: 健身 App 原型、动作搜索和教学内容；商业发布前必须核对媒体归属、署名与分发条件。
- 一句话推荐: 数据能拿来练产品，GIF 不能闭眼搬家——代码免费不等于健身教练也白送。
- Evidence Notes: GitHub Trending；仓库 README、数据目录、MIT 代码许可及媒体归属说明。
- Honest Caveat: About 与 README 对语言数量的描述可能不同；媒体文件并非简单随 MIT 代码许可证自由使用。

### Rank 09 - penpot/penpot
- Repo URL: https://github.com/penpot/penpot
- Tagline: 基于开放 Web 标准的协作式设计与原型平台，可云端使用也可自托管。
- Stars: 56,315
- Stars Today: 395
- Forks: 3,697
- Language: Clojure
- License: MPL-2.0
- Homepage: https://penpot.app
- Topics: design, prototyping, clojure, clojurescript, open-source
- 技术栈: Clojure, ClojureScript, PostgreSQL, Redis, WebSocket, SVG, Docker
- Why It Matters Today: 今日新增 395 Stars；在大量 AI 项目中，它代表成熟、可自托管、标准驱动的协作软件。
- 项目摘要: Penpot 是面向设计师和开发者的开源设计平台，使用 SVG、CSS、HTML 和 JSON 等开放标准表达设计资产。它包含前端编辑器、后端 RPC、实时协作、导出器、存储和自托管部署能力。
- 核心特性:
  1. 矢量设计、原型、设计系统和开发者检查模式集中在同一平台。
  2. 通过前端本地变更队列、后端 revision 校验与 WebSocket 通知实现多人协作。
  3. 支持插件、API、Webhooks、设计 Token 和 Docker 自托管。
- 适用场景: 产品设计协作、开源/内网设计平台、设计与开发交接；大型团队迁移前应验证插件、字体和既有 Figma 工作流兼容性。
- 一句话推荐: 不想把设计资产锁在黑箱里，Penpot 是一条正经路，不是“开源版截图工具”。
- Evidence Notes: GitHub Trending；README、官方技术指南、`backend/src/app/main.clj`、前端 persistence、后端 files-update 与 MPL-2.0。
- Honest Caveat: 自托管需要 PostgreSQL、Redis、存储、升级和备份运维；复杂设计兼容性应以真实文件迁移测试为准。

### Rank 10 - AIEraDev/Clypra
- Repo URL: https://github.com/AIEraDev/Clypra
- Tagline: 基于 Tauri、React 与 Rust 的跨平台视频编辑器，强调轻量桌面体验和多轨时间线。
- Stars: 2,747
- Stars Today: 85
- Forks: 282
- Language: TypeScript
- License: MIT
- Homepage: https://clypra.abdulkabirmusa.com
- Topics: video-editor, tauri, react, rust, ffmpeg
- 技术栈: Tauri v2, React 19, TypeScript, Rust, FFmpeg
- Why It Matters Today: 虽然今日新增只有 85 Stars，但它和 OpenCut 同日上榜，说明开源视频编辑器赛道正在升温。
- 项目摘要: Clypra 是跨平台桌面/移动视频编辑器，采用 Tauri 作为应用壳，React 构建界面，Rust 负责原生侧能力，并通过 FFmpeg 执行媒体导出。
- 核心特性:
  1. 多轨时间线、剪切、分割、文本、音频和转场等常见编辑能力。
  2. 使用命令模式支持撤销/重做，适合研究编辑器状态设计。
  3. 支持本地导出并提供可选 AI 功能入口。
- 适用场景: 轻量桌面视频编辑、Tauri 多媒体应用学习；专业剪辑、色彩和大型工程需先实测性能与格式兼容性。
- 一句话推荐: 个头不大，零件不少；适合研究轻量编辑器，先别让它一口吞下院线工程。
- Evidence Notes: GitHub Trending；仓库 README、Tauri/React/Rust 配置、时间线与导出代码、MIT 许可证。
- Honest Caveat: 项目规模和成熟度低于成熟商业编辑器；AI 功能、移动端和复杂编解码支持需要按当前版本验证。

### Rank 11 - par274/sharpemu
- Repo URL: https://github.com/par274/sharpemu
- Tagline: 从零用 C# 开发的实验性 PlayStation 5 模拟器。
- Stars: 2,276
- Stars Today: 332
- Forks: 149
- Language: C#
- License: GPL-2.0
- Homepage: https://github.com/par274/sharpemu
- Topics: emulator, playstation-5, csharp, reverse-engineering
- 技术栈: C#, .NET, 本地 CPU 执行, 图形/系统模块实验
- Why It Matters Today: 今日新增 332 Stars，早期基础设施项目因“能加载真实 eboot.bin”获得开发者关注。
- 项目摘要: SharpEmu 是研究和教育用途的早期 PS5 模拟器，目前可加载 eboot.bin/ELF、执行部分原生 CPU 指令、读取元数据和处理部分内核及系统模块功能，主开发目标仍是 Windows。
- 核心特性:
  1. 聚焦 PS5，不以 PS4 兼容为目标。
  2. 已搭建可执行文件加载、系统模块和部分内核导出基础设施。
  3. 提供持续发布构建，方便开发者观察兼容性进展。
- 适用场景: 模拟器架构、C# 低层系统研究和逆向工程学习；不适合期待稳定运行商业游戏的普通用户。
- 一句话推荐: 这是发动机试车台，不是游戏机代购；看技术进展挺有意思，拿来通关还早。
- Evidence Notes: GitHub Trending；仓库 README、源码目录、测试、GPL-2.0 与 2026-07-15 最新构建。
- Honest Caveat: 项目明确处于早期，多个关键组件缺失；用户必须使用合法获得的游戏与系统资料。

### Rank 12 - chenyme/grok2api
- Repo URL: https://github.com/chenyme/grok2api
- Tagline: 将 Grok Build、Web 和 Console 多账号池统一成 OpenAI/Anthropic 兼容 API 的 Go 网关。
- Stars: 5,945
- Stars Today: 186
- Forks: 1,938
- Language: Go
- License: MIT
- Homepage: https://github.com/chenyme/grok2api
- Topics: grok, grok-imagine, api-gateway
- 技术栈: Go, Gin, React, SQLite/PostgreSQL, Memory/Redis, Docker
- Why It Matters Today: 今日新增 186 Stars并发布 v3.0.1，模型兼容网关和多账号调度需求依旧旺盛。
- 项目摘要: grok2api 把三类 Grok 认证来源做成独立 Provider 和账号池，对外暴露 Responses、Chat Completions、Anthropic Messages、图片与视频等接口，并提供模型、密钥、用量、代理和审计后台。
- 核心特性:
  1. 统一 OpenAI/Anthropic 风格接口，隐藏上游 Provider 差异。
  2. 支持优先级、并发、额度、会话粘滞、冷却、重试和账号故障切换。
  3. 提供凭据加密、客户端密钥哈希、日志脱敏、SSRF 与传输大小限制。
- 适用场景: 研究型模型网关、内部兼容层和多账号调度实验；生产使用前必须核对上游条款、凭据安全和合规责任。
- 一句话推荐: 它把三路 Grok 账号排成了公交调度站；车能发，票和路权得你自己合法解决。
- Evidence Notes: GitHub Trending；README、`backend/internal/transport/http/inference/handler.go`、gateway service、Docker 配置、MIT 与 v3.0.1 Release。
- Honest Caveat: 项目明确仅供学习研究并要求遵守 Grok 条款；使用 SSO/多账号代理可能涉及上游服务政策和账号风险。

## Language Distribution

- Python:
  - Count: 3
  - Percent: 25.0%
  - Color Hint: #3572A5
- TypeScript:
  - Count: 2
  - Percent: 16.7%
  - Color Hint: #3178C6
- Shell:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #89E051
- CSS:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #563D7C
- PowerShell:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #012456
- HTML:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #E34C26
- Clojure:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #DB5855
- C#:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #178600
- Go:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #00ADD8

## Explore Highlights

### Explore 1
- Title: OpenCut-app/OpenCut
- URL: https://github.com/OpenCut-app/OpenCut
- Kind: Repository
- Meta: 开源视频编辑器 · 今日 Trending #3
- Short Reason: 今日增速第一，重写架构值得持续观察。

### Explore 2
- Title: Nutlope/hallmark
- URL: https://github.com/Nutlope/hallmark
- Kind: Repository
- Meta: Agent 网页设计 Skill · 今日 Trending #5
- Short Reason: 把 AI 生成 UI 的常见毛病整理成可执行质量门禁。

### Explore 3
- Title: mattpocock/skills
- URL: https://github.com/mattpocock/skills
- Kind: Repository
- Meta: 编程 Agent Skills · 今日 Trending #2
- Short Reason: 小型可组合技能正在替代越来越长的通用提示词。

### Explore 4
- Title: moeru-ai/airi
- URL: https://github.com/moeru-ai/airi
- Kind: Repository
- Meta: 自托管 AI 伴侣与角色系统
- Short Reason: Explore 补充了榜单之外的实时语音、角色和多端 AI 产品方向。

### Explore 5
- Title: Dicklesworthstone/destructive_command_guard
- URL: https://github.com/Dicklesworthstone/destructive_command_guard
- Kind: Repository
- Meta: 危险命令防护工具
- Short Reason: 直接解决编码 Agent 和终端自动化中的高权限误操作问题。

### Explore 6
- Title: HKUDS/Vibe-Trading
- URL: https://github.com/HKUDS/Vibe-Trading
- Kind: Repository
- Meta: AI 原生金融研究与回测 · 今日 Trending #6
- Short Reason: 近期安全加固与 MCP 更新，让它比普通金融 Demo 更值得看源码。

### Explore 7
- Title: openinterpreter/openinterpreter
- URL: https://github.com/openinterpreter/openinterpreter
- Kind: Repository
- Meta: 本地自然语言计算机执行工具
- Short Reason: 经典本地执行 Agent 继续出现在 Explore，说明“模型操作电脑”的需求没有退潮。

### Explore 8
- Title: HKUDS/DeepTutor
- URL: https://github.com/HKUDS/DeepTutor
- Kind: Repository
- Meta: 深度推理与个性化学习 Agent
- Short Reason: 教育 Agent 从答题器向可规划、可检索、可讲解的学习工作流演进。

## Rendering Notes

- Hero 主标题建议：GitHub Trending 日报
- Hero 副标题建议：视频编辑器冲上增速榜首，Agent 工程转向技能、质量门禁与可控工作流
- Top 3 高亮原因：保留 GitHub 原始排名 01–03，不按总 Stars 或编辑偏好重新排序。
- 需要在 HTML 中诚实提示的降级点：OpenCut 重写未完成；金融项目非投资建议；SharpEmu 早期实验；exercise 媒体独立许可；grok2api 需遵守上游条款。
- 不允许省略的区块：Header / Hero、4 张 Stats Cards、今日洞察、今日热门 Top 12、编程语言分布、GitHub Explore 精选、Footer。
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

## Evidence Notes

- GitHub Trending 原始排名来自 `https://github.com/trending?since=daily` 在 2026-07-15（Asia/Tokyo）本次抓取结果。
- `Stars Today` 为 Trending 页面展示的当日增量；`Stars` 为累计 Stars，两者没有混用。
- Top 12 今日新增 Stars 合计为 12,073；语言数按 Trending 主语言去重为 9。
- 项目能力优先依据仓库源码、README、官方文档与 Release；无法独立验证的性能、收益和未来路线均保留 Caveat。

## Honest Caveat

- GitHub Trending 是动态页面，同一天不同抓取时刻的 Stars、Stars Today 和排序可能小幅变化；本报告保留本次抓取快照。
- Explore 是个性化和动态推荐入口，只作为补充，不参与 Top 12 排名或统计。
- 本报告不独立运行所有项目，也不替维护者验证性能、收益或兼容性；深度架构分析只对证据足够的项目继续展开。