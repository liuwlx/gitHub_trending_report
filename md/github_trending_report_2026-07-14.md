# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-14
- Generated At: 2026-07-14 21:00 JST
- Output Markdown: `md/github_trending_report_2026-07-14.md`
- Planned HTML: `html/github_trending_report_2026-07-14.html`
- Fixed Base Template: `.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html`
- User Rules: `.codex/skills/skill-github-trending-report/reference/user-rules.md`
- Sources:
  - [GitHub Trending · Repositories / Any language / Today](https://github.com/trending?since=daily)
  - [GitHub Explore](https://github.com/explore)
  - 各项目仓库 README、依赖清单、源码与许可证
- Data Note: 本次 GitHub Trending 官方页面只返回 11 个仓库。报告严格保留原始排名 01–11，不编造第 12 名；为维持固定页面的信息节奏，额外加入 1 条明确标注的 GitHub Explore 补位内容，它不属于 Trending 排名，也不计入 Trending 统计。

## Page Intent

- 今日主线：AI 开发工具正在同时向“更能干”和“更不容易闯祸”两头扩张；榜首增量由安全护栏、金融 Agent、知识图谱与设计技能共同推动。
- 适合谁阅读：AI 工程师、开发工具团队、开源项目研究者、希望快速判断新项目是否值得试用的开发者。
- 页面重点：先看 Stars Today 与项目类别，再决定是试用产品、研究源码，还是仅收藏观察。
- 需要诚实降级说明的地方：官方 Trending 今日只有 11 项；Explore 补位没有 Trending 星标数据。OpenCut 当前仓库是重写中的下一代版本，不能把规划中的能力当成已经稳定交付。

## Stats

- Trending 项目数：11
- 今日累计新增 Stars：8,051
- 编程语言数：7
- AI 相关项目数：8

## Editorial Insights

### Insight 1
- Title: 安全护栏比“再来一个 Agent”涨得更快
- Body: destructive_command_guard 以 1,295 Stars Today 位居增量第一。它不是替 Agent 做事，而是在 Bash 命令真正执行前拦截高风险操作。AI 编程开始进入真实工程后，团队关心的不再只是模型能否写代码，还包括误删文件、强制覆盖 Git 状态和危险云命令该由谁踩刹车。

### Insight 2
- Title: Agent 正从通用聊天框钻进具体业务
- Body: Vibe-Trading 把自然语言研究、市场数据、回测和报告组织到同一套金融工作流；airi 做虚拟角色；marketingskills 把营销方法沉淀成可调用技能。今天的热点不是“一个万能 Agent 包打天下”，而是让 Agent 在明确领域里拿到工具、流程和上下文。

### Insight 3
- Title: 上下文基础设施开始分成两派
- Body: Graphify 把代码、文档和多媒体材料转换成可查询知识图谱，强调关系与证据；spec-kit 则把需求、规范、计划和任务固化成开发流程。一个解决“系统里到底有什么、怎么连”，另一个解决“我们到底准备做什么、按什么顺序做”。

### Insight 4
- Title: 今日榜单只有 11 个，少一个也不能拿空气补
- Body: GitHub Trending 页面本次只给出 11 个仓库。报告保留原始排名，并用 GitHub Explore 的 Ranger 推荐补足固定页面的第 12 张阅读卡，但不会把它冒充 Trending 第 12 名。榜单可以少，证据不能虚胖。

## Top Projects

### Rank 01 - OpenCut-app/OpenCut
- Repo URL: https://github.com/OpenCut-app/OpenCut
- Tagline: 面向创作者的开源视频编辑器，目标是提供可自托管、跨平台、可扩展的 CapCut 替代方案。
- Stars: 67,650
- Stars Today: 1,229
- Forks: 7,107
- Language: TypeScript
- License: MIT
- Homepage: https://opencut.app/
- Topics: video-editor, open-source, creator-tools, timeline, desktop
- 技术栈: TypeScript、pnpm、Moon、Web 前端；下一代方案规划 Rust 核心与插件 API
- Why It Matters Today: 日增超过 1.2k Stars，说明“本地可控、无订阅锁定”的创作工具仍有强需求。
- 项目摘要: OpenCut 希望把常用剪辑能力做成开放、可自托管的视频编辑器。当前仓库是一次从头重写的新版本，README 明确把 Classic 版本视为目前可用产品，而新架构仍在开发。
- 核心特性:
  1. 公开源码并以 MIT 许可发布，目标覆盖浏览器、桌面和移动端。
  2. 新版本设计强调 Editor API、插件优先、脚本化与未来 MCP 接入。
  3. 采用 monorepo 工程方式组织协议、应用与构建任务。
- 适用场景: 想研究现代视频编辑器架构、需要可定制剪辑界面，或希望参与下一代开源创作工具建设的团队。
- 一句话推荐: 值得看，但要分清“今天能用的 Classic”和“正在重写的新 OpenCut”，别把施工图当精装房。
- Evidence Notes: Trending 原始排名与 Stars Today 来自 GitHub Trending；定位、许可证、重写状态与路线图来自仓库 README、About 与 LICENSE。
- Honest Caveat: Editor API、Rust 核心、MCP、插件生态等多项能力仍属于新版本方向，尚不能按成熟生产能力评价。

### Rank 02 - Dicklesworthstone/destructive_command_guard
- Repo URL: https://github.com/Dicklesworthstone/destructive_command_guard
- Tagline: AI 编程代理的命令执行前安全钩子，在危险 Shell 操作落地前给它踩刹车。
- Stars: 3,931
- Stars Today: 1,295
- Forks: 144
- Language: Rust
- License: MIT
- Homepage: https://github.com/Dicklesworthstone/destructive_command_guard
- Topics: ai-agent, cli, rust, safety, developer-tools, hook
- 技术栈: Rust、Clap、Regex/Aho-Corasick、tree-sitter/ast-grep、TOML/YAML、FrankenSQLite、MCP stdio
- Why It Matters Today: Stars Today 位居第一，开发者正在给高权限 Agent 补上命令执行的安全边界。
- 项目摘要: DCG 作为 Claude Code、Codex CLI、Gemini CLI、Copilot CLI、Cursor 等工具的 pre-execution hook，解析代理准备执行的命令，结合规则包、白名单、AST 与上下文判断，返回允许、警告或拒绝结果。
- 核心特性:
  1. 在命令执行前拦截危险 Git、文件系统、数据库、云平台与容器操作。
  2. 快速关键词预筛加正则/AST 深度匹配，兼顾每条命令都要经过的低延迟要求。
  3. 提供分层白名单、规则包、历史记录、一次性放行和不同 Agent 协议输出。
- 适用场景: 让 AI 编程代理接触真实代码库、CI 环境或开发机，同时需要降低误删和强制覆盖风险的个人与团队。
- 一句话推荐: Agent 是徒弟，DCG 像站在电闸旁边的老师傅——活儿可以干，砸总闸不行。
- Evidence Notes: 二进制入口、hook 输入、规则评估、history、deny/warn/log 分支均可在 `src/main.rs`、`src/hook.rs`、`src/evaluator.rs` 和 `Cargo.toml` 中定位。
- Honest Caveat: 规则系统只能降低已覆盖模式的风险，不能证明任意 Shell 命令都安全；默认若输入解析或预算异常存在 fail-open 路径，严格环境需要审查 fail-closed 配置。

### Rank 03 - HKUDS/Vibe-Trading
- Repo URL: https://github.com/HKUDS/Vibe-Trading
- Tagline: 用自然语言组织金融研究、数据分析、因子探索与回测的开源 AI Agent 平台。
- Stars: 22,156
- Stars Today: 1,153
- Forks: 3,824
- Language: Python
- License: MIT
- Homepage: https://vibetrading.wiki/
- Topics: finance, trading, backtesting, langgraph, agent, quantitative-research
- 技术栈: Python 3.11、LangChain/LangGraph、Pandas、DuckDB、FastAPI、WebSocket、FastMCP、多市场数据源
- Why It Matters Today: 把 AI Agent 从通用研究推进到“取数—分析—回测—报告”的完整金融任务链。
- 项目摘要: Vibe-Trading 面向金融研究与量化探索，允许用户通过自然语言发起研究任务，调用市场数据、统计计算、回测和文档生成能力，并通过 CLI、API、Web 与 MCP 等入口使用。
- 核心特性:
  1. 使用 LangGraph 组织多步骤 Agent 与状态流转。
  2. 集成 yfinance、AkShare、Tushare、CCXT 等多类市场数据源。
  3. 提供回测、因子分析、FastAPI/WebSocket 服务和多种消息渠道扩展。
- 适用场景: 研究型原型、教学、策略假设验证和内部分析助手；不适合未经验证直接接管真实资金交易。
- 一句话推荐: 它能帮你把研究桌面摆齐，不能替你把亏损责任也打包带走。
- Evidence Notes: 项目定位、MIT 许可、依赖、CLI/MCP 入口和数据源来自 `pyproject.toml` 与官方文档。
- Honest Caveat: 市场数据质量、回测偏差、模型幻觉和实时执行风险需要独立验证；仓库热度不等于策略有超额收益。

### Rank 04 - moeru-ai/airi
- Repo URL: https://github.com/moeru-ai/airi
- Tagline: 可自托管的 LLM 虚拟角色与数字伙伴工程，覆盖 Web、桌面、移动端、语音和动画场景。
- Stars: 42,125
- Stars Today: 78
- Forks: 4,231
- Language: TypeScript
- License: MIT
- Homepage: https://airi.moeru.ai/
- Topics: virtual-character, llm, live2d, voice, electron, vue
- 技术栈: TypeScript、Vue、pnpm、Turborepo、Electron/Tauri 类桌面能力、音频与视觉管线、Vitest
- Why It Matters Today: 它代表 AI 应用从文本窗口向长期角色、语音互动和多端陪伴体验迁移。
- 项目摘要: AIRI 是一个大型 TypeScript monorepo，用模块化应用、服务、引擎与插件构建可自托管的虚拟角色体验，目标包括网页舞台、桌面宠物、移动端和实时语音互动。
- 核心特性:
  1. 多应用、多包、多服务的 monorepo，支持 Web、移动端和桌面形态。
  2. 把角色状态、语音、视觉、场景和模型接入拆成可组合模块。
  3. 使用统一构建、测试与类型检查流程管理复杂前端工程。
- 适用场景: 虚拟角色原型、直播互动、桌面陪伴、语音 Agent 与多模态 UI 研究。
- 一句话推荐: 不是给聊天框换张头像，而是在搭一套“角色怎么活着”的工程底座。
- Evidence Notes: 项目描述、MIT 许可、workspace 划分、构建和测试命令来自根目录 `package.json` 与仓库结构。
- Honest Caveat: 多端和实时媒体链路较复杂，部署成本、模型费用、隐私与内容安全需要按实际配置单独评估。

### Rank 05 - Shubhamsaboo/awesome-llm-apps
- Repo URL: https://github.com/Shubhamsaboo/awesome-llm-apps
- Tagline: 收集并实现多类 LLM Agent、RAG、语音与多模态应用的可运行示例库。
- Stars: 120,002
- Stars Today: 996
- Forks: 17,806
- Language: Python
- License: Apache-2.0
- Homepage: https://www.theunwindai.com/
- Topics: llm, agents, rag, multi-agent, voice-agent, generative-ai
- 技术栈: Python、主流 LLM SDK、向量检索、RAG、Agent 框架与各类 API
- Why It Matters Today: 接近 1k 日增，说明开发者仍需要“能跑起来的参考实现”，而不只是概念介绍。
- 项目摘要: 这是一个按应用类型组织的示例集合，覆盖单 Agent、多 Agent、RAG、语音、MCP 和垂直业务案例。价值在于广度和上手参考，而不是一套统一生产架构。
- 核心特性:
  1. 按场景提供独立示例，方便学习不同模型和工具组合。
  2. 覆盖多种 Agent、检索和多模态模式。
  3. 大量案例适合做原型起点或技术选型对照。
- 适用场景: 学习、Demo、PoC 和内部技术调研；生产系统需要重新做安全、状态、成本、测试和可观测性设计。
- 一句话推荐: 菜谱很多，厨房得你自己建，消防验收也不能让 README 替你签字。
- Evidence Notes: Trending 数据来自 GitHub；Apache-2.0、项目分类、主页和仓库结构来自官方仓库元数据与 README。
- Honest Caveat: 这是案例集合，不应按单一系统架构分析；不同目录的质量、依赖和维护状态可能不一致。

### Rank 06 - Nutlope/hallmark
- Repo URL: https://github.com/Nutlope/hallmark
- Tagline: 给 AI 编程助手使用的设计技能，目标是减少模板化“AI 味”界面。
- Stars: 5,463
- Stars Today: 794
- Forks: 322
- Language: CSS
- License: MIT
- Homepage: https://github.com/Nutlope/hallmark
- Topics: design-skill, claude-code, cursor, codex, typography, oklch
- 技术栈: Markdown Skill、CSS 设计知识、Claude Code/Cursor/Codex 技能加载约定、Together AI
- Why It Matters Today: 近 800 日增说明开发者开始把注意力从“页面能生成”转向“页面别一眼像机器批发”。
- 项目摘要: Hallmark 把排版、色彩、层级和常见 AI 设计反模式整理成可被 AI 编程助手读取的技能与参考材料，让生成式前端在动手前先得到设计约束。
- 核心特性:
  1. 以可安装 Skill 的方式向多个 AI 编程工具注入设计方法。
  2. 聚焦字体、色彩、布局和反模板化的具体规则。
  3. 结构轻量，核心资产是 `skills/hallmark/SKILL.md` 与 references。
- 适用场景: AI 辅助前端、快速原型和团队希望统一生成界面审美底线的工作流。
- 一句话推荐: 它不是设计师替身，更像在 Agent 耳边提醒一句：别又把所有东西都做成三张渐变卡片。
- Evidence Notes: MIT 许可、技能入口、支持的 harness 与项目描述来自根目录 `package.json`。
- Honest Caveat: 设计质量具有主观性；技能可以改善约束和提示，但不能保证每次输出都达到专业设计评审标准。

### Rank 07 - Raphire/Win11Debloat
- Repo URL: https://github.com/Raphire/Win11Debloat
- Tagline: 用 PowerShell 批量清理 Windows 11 预装应用、遥测和界面干扰项的可配置脚本。
- Stars: 51,093
- Stars Today: 118
- Forks: 2,104
- Language: PowerShell
- License: MIT
- Homepage: https://github.com/Raphire/Win11Debloat
- Topics: windows-11, debloat, powershell, privacy, telemetry
- 技术栈: PowerShell、Windows 注册表、Appx 管理、系统策略与配置文件
- Why It Matters Today: Windows 设备初始化和隐私配置仍是高频刚需，脚本化比手动点几十个开关更可复现。
- 项目摘要: Win11Debloat 通过可选配置执行应用卸载、遥测限制、广告和推荐关闭、开始菜单与资源管理器调整，适合新机器初始化或批量标准化。
- 核心特性:
  1. 按选项执行多类 Windows 清理与隐私设置。
  2. 支持交互和预设方式，便于重复使用。
  3. 以 PowerShell 和系统原生命令为主，不依赖大型常驻程序。
- 适用场景: 个人电脑初始化、测试机模板和明确了解企业策略边界的运维脚本化。
- 一句话推荐: 省的是点鼠标的时间，动的是系统设置，下手前照样得看清菜单。
- Evidence Notes: MIT 许可来自仓库 LICENSE；功能定位和 Trending 数据来自官方仓库与 Trending 页面。
- Honest Caveat: Windows 版本和厂商策略会变化；执行前应审阅选项、建立还原点，并避免在受管企业设备上绕过组织策略。

### Rank 08 - Graphify-Labs/graphify
- Repo URL: https://github.com/Graphify-Labs/graphify
- Tagline: 把代码、文档、论文、图片和视频转换成可查询知识图谱，为 AI 编程助手提供结构化项目上下文。
- Stars: 85,212
- Stars Today: 1,095
- Forks: 8,414
- Language: Python
- License: MIT
- Homepage: https://github.com/Graphify-Labs/graphify
- Topics: knowledge-graph, code-analysis, tree-sitter, graph-rag, mcp, ai-coding
- 技术栈: Python 3.10、NetworkX、tree-sitter 多语言解析、RapidFuzz、可选 Neo4j/FalkorDB/MCP/LLM 适配
- Why It Matters Today: 日增超过 1k，说明“给 Agent 一个关系清楚、可验证的代码地图”正在成为上下文工程的重要方向。
- 项目摘要: Graphify 由 AI 工具 Skill 和可独立使用的 Python 库组成，按 detect → extract → build_graph → cluster → analyze → report → export 管线，把异构资料提取为节点和边，再输出报告、图文件、Obsidian Vault 或 MCP 查询服务。
- 核心特性:
  1. 使用 tree-sitter 解析多种编程语言，并给关系标记 EXTRACTED、INFERRED、AMBIGUOUS 证据等级。
  2. 通过 NetworkX 构图、社区发现与分析模块发现核心节点和结构问题。
  3. 支持多种导出格式和可选 MCP、图数据库、PDF、视频与模型扩展。
- 适用场景: 大型代码库熟悉、遗留系统梳理、架构评审准备、AI 编程上下文增强和技术尽调。
- 一句话推荐: 先给代码库画地图，再让 Agent 开车，至少不至于一脚油门扎进死胡同。
- Evidence Notes: 管线、模块职责、数据 Schema、置信标签和安全校验来自 `ARCHITECTURE.md`；依赖与入口来自 `pyproject.toml`。
- Honest Caveat: 解析关系包含推断，图越大越需要抽样核验；可选数据库和 LLM 能力不是默认运行的必需组件。

### Rank 09 - hasaneyldrm/exercises-dataset
- Repo URL: https://github.com/hasaneyldrm/exercises-dataset
- Tagline: 面向健身应用和计算机视觉研究的动作、肌群与示范素材数据集。
- Stars: 12,889
- Stars Today: 451
- Forks: 1,532
- Language: HTML
- License: 代码与数据 MIT；视觉媒体另有使用条款
- Homepage: https://github.com/hasaneyldrm/exercises-dataset
- Topics: fitness, exercise, dataset, computer-vision, biomechanics
- 技术栈: JSON/静态数据、HTML 浏览界面、图像与动作媒体资产
- Why It Matters Today: 健身应用、姿态识别和训练计划生成需要结构化动作数据，开源基础数据比再写一套空壳界面更稀缺。
- 项目摘要: 该仓库提供动作名称、目标肌群、器械和演示素材等数据，并带静态浏览入口，主要价值是数据资产而非复杂软件系统。
- 核心特性:
  1. 将多类健身动作和属性整理为可供应用消费的数据。
  2. 配套视觉素材帮助动作展示或训练数据研究。
  3. 可作为健身搜索、训练计划、姿态识别和内容应用的数据底座。
- 适用场景: 健身产品原型、动作检索、教学展示和计算机视觉数据研究。
- 一句话推荐: 这是原料库，不是健身教练；数据能喂应用，动作安全还得专业人士把关。
- Evidence Notes: Trending 数据与仓库定位来自 GitHub 页面；许可证需要区分代码/数据与视觉媒体条款。
- Honest Caveat: 这是数据集项目，未进入架构深度分析；视觉素材授权、数据准确性和医疗适用性必须单独核验。

### Rank 10 - github/spec-kit
- Repo URL: https://github.com/github/spec-kit
- Tagline: GitHub 推出的 Spec-Driven Development 工具包，把需求、规范、计划和任务变成可执行的 AI 开发流程。
- Stars: 120,831
- Stars Today: 543
- Forks: 10,747
- Language: Python
- License: MIT
- Homepage: https://github.github.io/spec-kit/
- Topics: spec-driven-development, ai-coding, cli, workflow, templates
- 技术栈: Python 3.11、Typer/Click、Rich、YAML/JSON5、模板与脚本资产、Agent integration 插件体系
- Why It Matters Today: 当 AI 能快速写代码后，瓶颈开始前移到需求是否清楚、约束是否稳定和任务是否可验证。
- 项目摘要: spec-kit 的 `specify` CLI 用内置模板、工作流、脚本、集成和 preset 初始化 SDD 项目，让团队先形成 constitution、spec、plan 和 tasks，再让支持的 AI 编程工具执行。
- 核心特性:
  1. `specify init` 离线安装随版本打包的模板、脚本、工作流和共享基础设施。
  2. 支持 Copilot、Claude、Codex、Gemini 等多类 Agent 集成，并记录安装 manifest。
  3. 通过 constitution、spec、plan、tasks 等固定产物把需求和实现过程连接起来。
- 适用场景: 新项目启动、复杂功能拆解、团队希望规范 AI 编程流程，以及需要留下决策与任务证据的工程。
- 一句话推荐: AI 写代码像手快的伙计，spec-kit 先把菜单、分工和验收单写明白，省得端上来一盆“差不多”。
- Evidence Notes: MIT 许可来自 LICENSE；CLI 入口、依赖和离线资产来自 `pyproject.toml`；初始化步骤来自 `src/specify_cli/commands/init.py`。
- Honest Caveat: 流程模板能减少歧义，但不会自动保证需求正确；过度套模板也可能增加小项目的仪式成本。

### Rank 11 - coreyhaines31/marketingskills
- Repo URL: https://github.com/coreyhaines31/marketingskills
- Tagline: 为 AI Agent 准备的营销技能集合，覆盖定位、文案、增长、SEO 与发布工作流。
- Stars: 38,864
- Stars Today: 299
- Forks: 6,224
- Language: JavaScript
- License: MIT
- Homepage: https://github.com/coreyhaines31/marketingskills
- Topics: marketing, ai-agent, skills, copywriting, seo, growth
- 技术栈: Markdown/Skill 文档、JavaScript 辅助工具、面向 Claude/Codex 等 Agent 的加载约定
- Why It Matters Today: Agent 技能市场正在从编程扩展到营销等知识工作，方法论开始被包装成可复用执行单元。
- 项目摘要: marketingskills 将常见营销任务拆成可供 AI Agent 读取的技能说明，帮助模型在执行定位、文案、SEO、发布和增长任务时遵循更具体的步骤与检查项。
- 核心特性:
  1. 按营销任务拆分技能，便于按需加载而不是塞进一个超长 Prompt。
  2. 提供结构化步骤、问题清单和输出要求。
  3. 适合与编程 Agent 结合，覆盖产品上线后的内容和增长工作。
- 适用场景: 创业团队的营销初稿、内容检查、SEO 工作流和内部方法沉淀；关键品牌与合规内容仍需人工审核。
- 一句话推荐: 它能给 Agent 一套营销手艺，不能给你的产品凭空变出市场需求。
- Evidence Notes: Trending 数据来自 GitHub；MIT 许可来自 LICENSE；项目定位来自仓库说明和技能目录。
- Honest Caveat: 营销效果依赖产品、渠道和市场环境；技能输出不能替代事实核验、法务审查和真实实验。

### Rank 12（Explore 补位，不属于 Trending 原始排名）- GitHub Explore / Ranger
- Repo URL: https://github.com/explore
- Tagline: GitHub Explore 的 Staff Recommendation：自动处理仓库合并、关闭、评论和分支清理的维护机器人。
- Stars: N/A（Explore 推荐，不是 Trending 仓库条目）
- Stars Today: N/A
- Forks: N/A
- Language: N/A
- License: 未在 Explore 卡片中提供
- Homepage: https://github.com/explore
- Topics: repository-automation, maintenance, pull-requests, issues
- 技术栈: GitHub App / 仓库自动化（Explore 卡片未公开具体实现栈）
- Why It Matters Today: 热榜里工具越来越多，仓库维护本身也需要自动化；它补充了“写代码之外，如何保持项目运转”的视角。
- 项目摘要: Ranger 是 GitHub Explore 的编辑推荐，介绍中包括在检查通过后自动合并、按标签和时间自动关闭 issue、标准化评论，以及删除已合并分支等仓库维护动作。
- 核心特性:
  1. 依据检查状态执行自动合并。
  2. 按标签和等待时间处理 issue 生命周期。
  3. 自动评论和清理已合并分支。
- 适用场景: 希望减少重复维护操作、且能够明确配置权限与合并规则的开源或内部仓库。
- 一句话推荐: 这是 Explore 加菜，不是 Trending 第十二名；能省杂活，权限菜单得先看清。
- Evidence Notes: 仅基于 GitHub Explore Staff Recommendation 卡片；没有把它计入 Trending 项目数、Stars Today 或语言统计。
- Honest Caveat: 本次 Explore 卡片没有提供可核验的仓库实现、Stars、许可证和技术栈，因此只作编辑补充，不进入架构分析。

## Language Distribution

- Python:
  - Count: 4
  - Percent: 36.4%
  - Color Hint: #3572A5
- TypeScript:
  - Count: 2
  - Percent: 18.2%
  - Color Hint: #3178C6
- Rust:
  - Count: 1
  - Percent: 9.1%
  - Color Hint: #DEA584
- JavaScript:
  - Count: 1
  - Percent: 9.1%
  - Color Hint: #F1E05A
- CSS:
  - Count: 1
  - Percent: 9.1%
  - Color Hint: #563D7C
- PowerShell:
  - Count: 1
  - Percent: 9.1%
  - Color Hint: #012456
- HTML:
  - Count: 1
  - Percent: 9.1%
  - Color Hint: #E34C26

## Explore Highlights

### Explore 1
- Title: Ranger · GitHub Staff Recommendation
- URL: https://github.com/explore
- Kind: GitHub App / Repository Automation
- Meta: 自动合并、自动关闭、标准化评论、合并后分支清理
- Short Reason: 适合关注开源仓库维护自动化的人；权限和合并条件必须先审查。

### Explore 2
- Title: Recurse ML · GitHub Staff Recommendation
- URL: https://github.com/explore
- Kind: CLI + GitHub App
- Meta: `rml` 检查 staged changes，GitHub App 审查 Pull Request
- Short Reason: 把代码审查前移到提交和 PR 两个节点，值得与传统 lint/test 工作流对照。

### Explore 3
- Title: GitHub Checkout · Copilot CLI updates
- URL: https://github.com/explore
- Kind: Video
- Meta: Chronicle、plugins、fleet mode
- Short Reason: 快速了解 Copilot CLI 新能力和 GitHub 对命令行 Agent 的产品方向。

### Explore 4
- Title: Database Topic
- URL: https://github.com/topics/database
- Kind: Popular Topic
- Meta: 数据库相关热门项目集合
- Short Reason: 当日主榜偏 AI 应用，Database Topic 可补充基础设施视角。

### Explore 5
- Title: Learn to Code Collection
- URL: https://github.com/collections/learn-to-code
- Kind: Collection
- Meta: 入门项目与学习资源
- Short Reason: 适合希望从可运行项目入手、而不是只看热门复杂仓库的学习者。

### Explore 6
- Title: Trending Developers
- URL: https://github.com/trending/developers
- Kind: Developer Ranking
- Meta: 当日活跃开发者补充视角
- Short Reason: 仓库热度之外，看看哪些维护者持续产出，常能更早发现后续项目。

## Rendering Notes

- Hero 主标题建议：AI Agent 一边加速，一边补刹车
- Hero 副标题建议：2026-07-14 · 官方 Trending 11 项 + Explore 补位 1 项，原始排名不掺水
- Top 3 高亮原因：DCG、OpenCut、Vibe-Trading 分别代表安全护栏、创作工具和垂直金融 Agent，且 Stars Today 均超过 1.1k。
- 需要在 HTML 中诚实提示的降级点：GitHub Trending 官方页面只返回 11 项；第 12 张为 Explore 补位，不得显示为原始 Trending 排名或纳入统计。
- 不允许省略的区块：Header / Hero、4 张 Stats Cards、今日洞察、今日热门、编程语言分布、GitHub Explore 精选、Footer。
- 必须保留的固定模板结构：
  - Header / Hero
  - 4 张 Stats Cards
  - 今日洞察
  - 今日热门 Trending 11 + Explore 补位 1
  - 编程语言分布
  - GitHub Explore 精选
  - Footer
- Top 详情固定顺序：
  1. 项目摘要
  2. 核心特性
  3. 技术栈
  4. 适用场景
  5. 一句话推荐

## Validation

- 官方 Trending 原始排名 01–11 已保留。
- 11 个 Trending 项目均区分总 Stars 与 Stars Today。
- 4 个统计指标已按 Trending 11 项计算，Explore 补位未混入。
- 每个阅读卡均包含项目摘要、核心特性、技术栈、适用场景、一句话推荐、Evidence Notes 和 Honest Caveat。
- Explore 缺口已明确说明，没有复用旧数据或虚构第 12 名。
