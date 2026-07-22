# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-22
- Generated At: 2026-07-22 21:18 JST
- Output Markdown: md/github_trending_report_2026-07-22.md
- Planned HTML: html/github_trending_report_2026-07-22.html
- Fixed Base Template: .codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html
- User Rules: .codex/skills/skill-github-trending-report/reference/user-rules.md
- Data Scope: GitHub Trending · Repositories · Any language · Today
- Sources:
  - https://github.com/trending
  - https://github.com/explore
  - Repo README / About / Homepage / Release / source files
  - GitHub 公开仓库元数据与官方文档

## Page Intent

- 今日主线：AI 开发工具仍然占据主舞台，但热点从单纯聊天助手扩展到实时情报、代码图谱、CAD、部署平台、交易数据接入和本地模型选型；同时 Hyprland 与 Apollo 11 说明底层系统和历史源码依然能吸引大规模关注。
- 适合谁阅读：希望快速发现 AI 工程、开发工具、基础设施和系统软件变化的软件工程师、架构师、技术负责人和开源观察者。
- 页面重点：严格保留 GitHub Trending 原始 Top 12 顺序，单列累计 Stars 与 Stars Today，并为具备实际系统实现的项目提供进一步架构解析。
- 需要诚实降级说明的地方：Trending 排名算法未公开；Stars Today 是动态页面快照；项目方性能或效果数字未独立复测；Apollo 11 是历史源码转录归档，不应按现代生产项目口径评价。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：13,341
- 编程语言数：6
- AI 相关项目数：9

## Editorial Insights

### Insight 1
- Title: 实时情报平台从“多开网页”走向统一操作台
- Body: 榜首 `worldmonitor` 把新闻、地缘事件、市场、航空、海事、网络安全和气候数据汇入同一地图与面板系统，并进一步提供 MCP、CLI 与 SDK。它的热度反映出一种更明确的需求：开发者和分析人员不只缺数据，更缺把多源数据组织成可操作情境的系统。

### Insight 2
- Title: AI 编程工具开始争夺“上下文入口”
- Body: `code-review-graph` 用本地代码图谱减少模型无效阅读，`jcode` 把代码编辑、工具调用和工作流放进 Rust CLI，`text-to-cad` 把 Agent Skills 延伸到 CAD 与硬件设计。大家都在解决同一个问题：模型会说话已经不稀奇，能否拿到正确上下文并可靠执行才是下一道门槛。

### Insight 3
- Title: 自托管平台继续吃“云平台太贵、脚本太碎”的红利
- Body: `openship` 试图把仓库识别、构建、容器部署、数据库、域名、证书、备份与监控收进同一控制面，并同时提供桌面端、Web 和 CLI。它不是发明容器，而是把常见但分散的运维工作重新包装成一条可重复的交付链路。

### Insight 4
- Title: 高热度并不等于低风险
- Body: `tradingview-mcp` 涉及市场数据与桌面端自动化，`AstrBot` 和多个 Agent 项目可能接触消息、插件、模型凭据或本地执行能力，`worldmonitor` 聚合大量外部数据源。真正落地前仍要看数据授权、密钥管理、插件权限、速率限制和故障隔离；星标是敲门声，不是安全审计报告。

## Top Projects

### Rank 01 - koala73/worldmonitor
- Repo URL: https://github.com/koala73/worldmonitor
- Tagline: 实时全球情报仪表盘，把地缘政治、市场、航空、海事、网络安全与气候数据整合到统一地图和专业面板。
- Stars: 66,535
- Stars Today: 1,295
- Forks: 10,301
- Language: TypeScript
- License: AGPL-3.0-only
- Homepage: https://worldmonitor.app
- Topics: agent, osint, news, ai, monitoring, dashboard, mcp, geopolitics
- 技术栈: TypeScript, Vite, deck.gl, MapLibre, globe.gl, Tauri 2, Vercel Edge Functions, Railway, Upstash Redis, Protocol Buffers, Web Workers, ONNX
- Why It Matters Today: 它既是高信息密度前端，也是包含 API 网关、缓存、数据种子任务、桌面端和 Agent 接口的完整系统，今日增量显示开发者对“统一态势感知”工具兴趣强烈。
- 项目摘要: World Monitor 是一个实时全球情报平台。前端通过平面地图、三维地球和可组合面板展示多域数据；后端 Edge Functions、Relay 服务和 Redis 负责代理、缓存、播种与聚合外部数据。它既能作为浏览器或桌面端使用，也暴露 MCP、CLI、SDK 和结构化 API，适合进一步接入自动化分析流程。
- 核心特性:
  1. 统一展示新闻、冲突、市场、航班、船舶、基础设施、网络威胁与气候事件。
  2. 提供平面地图与三维地球两套渲染系统，以及按场景切换的专业面板布局。
  3. 通过边缘 API、Railway Relay、Redis 缓存和智能轮询减少多上游数据源的延迟与抖动。
  4. 内置本地 ONNX 推理、语义搜索与新闻聚类，并提供 MCP、CLI 和多语言 SDK。
- 适用场景: OSINT 与风险观察、企业态势看板、新闻与市场事件交叉分析、Agent 获取结构化全球事件上下文、需要自托管情报界面的团队。
- 一句话推荐: 想研究“多源实时数据怎样变成一张能操作的全球态势图”，今天先看它，料足得像把整个自助餐搬进了浏览器。
- Evidence Notes: `ARCHITECTURE.md` 明确记录 SPA、Edge Functions、Railway Relay、Upstash Redis、Tauri、Proto/RPC、Web Workers 和数据播种流程；`src/main.ts` 与 `src/App.ts` 是前端初始化主线；README 与 Explore 描述一致。
- Honest Caveat: 65+ 上游数据源的可用性、授权、延迟和覆盖范围并不一致；地图上的“统一视图”不能消除源数据误差。项目方关于功能数量和数据能力的统计来自仓库自身 CI，未做独立全量验证。

### Rank 02 - bojieli/ai-agent-book
- Repo URL: https://github.com/bojieli/ai-agent-book
- Tagline: 《深入理解 AI Agent：设计原理与工程实践》的开源正文、PDF 与逐章实验代码。
- Stars: 15,948
- Stars Today: 4,624
- Forks: 1,512
- Language: Python
- License: Apache-2.0
- Homepage: https://bojieli.github.io/ai-agent-book
- Topics: agent, reinforcement-learning, book, mcp, multi-agent, rag, coding-agent, context-engineering
- 技术栈: Python, Jupyter/示例代码, LLM APIs, MCP, RAG, Multi-Agent, Reinforcement Learning
- Why It Matters Today: 今日增星最高，说明开发者不仅想用 Agent，也在系统补课其规划、记忆、工具、强化学习和多智能体机制。
- 项目摘要: 这是一本以原理和工程实践为主线的开源 AI Agent 教材仓库，包含正文、可下载版本以及按章实验代码。它更适合作为学习路径和团队共识材料，而不是直接部署的 Agent 产品。
- 核心特性:
  1. 从 Agent 基础范式逐步讲到规划、记忆、工具、上下文工程和多智能体。
  2. 通过按章代码实验把抽象概念落到可运行示例。
  3. 同时提供在线阅读、PDF 和源码，方便个人学习或内部培训。
- 适用场景: AI Agent 系统学习、工程师培训、架构评审前建立共同词汇、为自研 Agent 选型补齐理论背景。
- 一句话推荐: 这是今日最热的“系统补课本”，适合认真读，不适合下载后问一句“服务怎么启动”。
- Evidence Notes: README 将仓库定义为开源图书主仓库，包含全书正文、编译 PDF 和配套代码；仓库许可证为 Apache-2.0。
- Honest Caveat: 教材与示例不能替代具体项目的安全、性能和生产验证；不同章节的实验复杂度与维护状态可能不同。

### Rank 03 - tirth8205/code-review-graph
- Repo URL: https://github.com/tirth8205/code-review-graph
- Tagline: 本地优先的代码智能图谱，为 MCP 和 CLI 建立持久代码关系图，让 AI 只读取真正相关的上下文。
- Stars: 24,853
- Stars Today: 1,925
- Forks: 2,366
- Language: Python
- License: MIT
- Homepage: https://github.com/tirth8205/code-review-graph
- Topics: python, tree-sitter, mcp, static-analysis, knowledge-graph, code-review, graphrag, ai-coding
- 技术栈: Python, Tree-sitter, SQLite/本地存储, MCP, CLI, Static Analysis, Knowledge Graph
- Why It Matters Today: 大型代码库的主要问题已经不是模型不会写，而是上下文太多、影响关系太难追。持久化代码图谱正成为 AI Code Review 和仓库理解的重要基础设施。
- 项目摘要: Code Review Graph 扫描代码仓库，抽取符号、依赖和调用关系，形成可增量更新的本地知识图谱。CLI 或 MCP 客户端可以查询改动影响、相关测试和关键依赖，从而减少把整个仓库塞给模型的成本。
- 核心特性:
  1. 用 Tree-sitter 做多语言语法分析，构建符号与依赖关系图。
  2. 支持增量更新，避免每次代码变化都全量重新索引。
  3. 通过 MCP 与 CLI 暴露影响分析、代码审查和上下文检索能力。
- 适用场景: 大型仓库代码审查、AI Coding Agent 上下文检索、改动影响分析、测试选择和代码知识图谱研究。
- 一句话推荐: 当模型看代码像进仓库找一颗螺丝，这个项目想先给它一张货架地图。
- Evidence Notes: README 与 Explore 均明确描述 local-first、persistent map、MCP/CLI、Tree-sitter 和上下文缩减；许可证为 MIT。
- Honest Caveat: 上下文缩减与召回质量依赖语言支持、索引质量和查询类型；维护者基准结果未在本次报告中独立复测。

### Rank 04 - earthtojake/text-to-cad
- Repo URL: https://github.com/earthtojake/text-to-cad
- Tagline: 面向 CAD、机器人和硬件设计的 Agent Skills 集合，把自然语言设计任务映射到专业工具工作流。
- Stars: 9,356
- Stars Today: 291
- Forks: 1,036
- Language: JavaScript
- License: MIT
- Homepage: https://cadskills.xyz
- Topics: cad, robotics, hardware, agent-skills, design-automation
- 技术栈: JavaScript, Agent Skills, CAD tool integrations, structured prompts/workflows
- Why It Matters Today: Agent Skills 正从软件开发扩展到工程设计，CAD 与机器人场景需要的不只是文本生成，而是约束、几何和专业工具链协同。
- 项目摘要: Text-to-CAD 是一组为编码 Agent 准备的 CAD、机器人和硬件设计技能。它通过结构化指令和工具工作流帮助 Agent 理解设计任务、生成或修改几何与工程文件，并连接相关设计工具。
- 核心特性:
  1. 按专业设计任务组织可复用 Agent Skills。
  2. 覆盖 CAD、机器人和硬件工作流，而非只生成概念图。
  3. 便于在支持 Skills 的 Agent 环境中安装和组合。
- 适用场景: 工程设计原型、CAD 自动化试验、机器人结构设计辅助、硬件团队探索自然语言工作流。
- 一句话推荐: 它不是“说句话就造火箭”，更像给 Agent 发了一本车间操作手册。
- Evidence Notes: 仓库 About 与 Explore 将其定义为 CAD、robotics、hardware design 的 Agent Skills 集合；主页为 cadskills.xyz，许可证为 MIT。
- Honest Caveat: 该仓库以技能与工作流为主，不等同于独立 CAD 内核；具体可用性取决于目标工具、Agent 平台和人工工程审查。

### Rank 05 - 1jehuang/jcode
- Repo URL: https://github.com/1jehuang/jcode
- Tagline: 用 Rust 编写的终端 AI 编程 Agent，围绕代码检索、编辑、工具调用和可扩展工作流组织开发任务。
- Stars: 10,488
- Stars Today: 843
- Forks: 1,149
- Language: Rust
- License: MIT
- Homepage: https://jcode.sh
- Topics: rust, coding-agent, cli, llm, developer-tools
- 技术栈: Rust, CLI/TUI, LLM APIs, tool calling, file operations, process execution
- Why It Matters Today: Rust 编写的 Coding Agent 继续获得关注，体现出开发者既要模型能力，也看重终端交互、资源控制和单文件工具的可部署性。
- 项目摘要: Jcode 是一个终端 AI 编程助手。它接收开发任务，读取项目上下文，调用文件与命令工具，生成修改并根据测试结果迭代，目标是在本地开发环境中形成完整闭环。
- 核心特性:
  1. 终端优先，适合直接在代码仓库中工作。
  2. 支持模型驱动的文件读取、编辑、搜索和命令执行。
  3. Rust 实现便于构建单一可执行程序并控制并发与资源。
- 适用场景: 本地代码修改、测试驱动修复、终端自动化、研究 Rust Agent Runtime 和工具调用边界。
- 一句话推荐: 喜欢在终端干活、又不想给 AI 单独盖办公楼的开发者，可以看看这位“随身工友”。
- Evidence Notes: 仓库 README、依赖与入口表明其为 Rust Coding Agent；MIT 许可证与 jcode.sh 主页已确认。
- Honest Caveat: 自动执行命令与修改文件具有高权限风险；应在版本控制、沙盒或明确审批策略下使用。本次未独立复测复杂任务成功率。

### Rank 06 - oblien/openship
- Repo URL: https://github.com/oblien/openship
- Tagline: 开源自托管部署平台，内置 CI/CD，通过桌面端、Web、CLI、REST API 和 MCP 管理构建、容器与基础设施。
- Stars: 6,527
- Stars Today: 1,562
- Forks: 471
- Language: TypeScript
- License: Apache-2.0
- Homepage: https://openship.io
- Topics: self-hosted, deployments, devops, ci-cd, docker, agents, infrastructure
- 技术栈: TypeScript, Bun, Turbo, Hono, Better Auth, Drizzle, BullMQ, Redis, Docker, Electron/Desktop, Next.js dashboard, REST, MCP
- Why It Matters Today: 它试图把从代码仓库到可访问服务的常见环节收进一个自托管控制面，直接回应团队在 CI/CD、证书、数据库、日志和回滚之间来回拼工具的痛点。
- 项目摘要: Openship 是一个开源部署控制面。用户可以从 CLI、桌面端或 Web 连接项目，系统识别技术栈、创建部署记录、排队执行构建和容器运行，并统一管理域名、SSL、数据服务、备份和部署历史。它既能运行在个人电脑上通过 SSH 管理服务器，也能作为团队共享的常驻服务。
- 核心特性:
  1. 内置 Push-to-deploy、预览环境、分阶段发布、部署历史和回滚。
  2. 支持多种语言、Docker Compose、数据库、Worker、WebSocket 和持久卷。
  3. 同时提供桌面端、Web Dashboard、CLI、REST API 与 MCP。
  4. API 服务采用 Hono，使用数据库仓储、BullMQ/Redis 任务队列和运行时适配器组织部署状态。
- 适用场景: 自托管 PaaS、个人或小团队统一管理 VPS、减少手写 CI/CD 与反向代理配置、需要可迁移 Docker 交付链的团队。
- 一句话推荐: 云平台嫌贵、部署脚本像祖传菜谱的团队，可以研究它怎么把厨房收拾成一条流水线。
- Evidence Notes: README 给出 `openship init/deploy`、桌面/Web/CLI 和自托管模式；根 `package.json` 显示 Bun + Turbo Monorepo；API 包使用 Hono、Better Auth、Drizzle、BullMQ、Redis；部署服务实现组织隔离、部署状态、回滚与资源清理。
- Honest Caveat: README 称核心生产可用，但多节点、负载均衡 UI、私有网络和高级监控仍在路线图；自托管部署平台拥有服务器与密钥高权限，生产使用前必须审查权限、备份和升级路径。

### Rank 07 - AstrBotDevs/AstrBot
- Repo URL: https://github.com/AstrBotDevs/AstrBot
- Tagline: 多平台 LLM Chatbot 与 Agent 开发框架，连接常见即时通信平台、模型、插件、MCP、知识库和 Web 管理界面。
- Stars: 37,596
- Stars Today: 416
- Forks: 2,624
- Language: Python
- License: AGPL-3.0-or-later
- Homepage: https://astrbot.app
- Topics: ai-agent, chatbot, im, llm, mcp, plugins, knowledge-base, multi-platform
- 技术栈: Python 3.12, asyncio, FastAPI, SQLModel/SQLAlchemy, aiosqlite, FAISS, OpenAI/Anthropic/Google SDKs, MCP, IM platform SDKs, Vue dashboard, Docker/Kubernetes
- Why It Matters Today: 它把多个聊天渠道、模型供应商、插件和 Agent 能力统一到一套运行时里，是观察“多渠道 Agent 平台”工程复杂度的好样本。
- 项目摘要: AstrBot 是面向个人与开发者的多渠道 Agent 平台。运行时加载配置、数据库、插件、模型 Provider、即时通信适配器和 Web Dashboard；外部消息进入后经过事件管线与插件处理，再调用模型、工具、知识库或 MCP，并把结构化结果送回原平台。
- 核心特性:
  1. 集成 Telegram、Slack、Discord、飞书、钉钉、QQ 等消息平台。
  2. 支持多家 LLM、工具调用、MCP、知识库、插件与沙盒能力。
  3. 提供 WebUI、CLI、Docker、Kubernetes 和桌面打包等多种运行方式。
  4. 以异步事件和插件机制组织消息处理，便于扩展命令、过滤器和业务逻辑。
- 适用场景: 多渠道企业或个人机器人、Agent 插件开发、统一模型接入、知识库问答、消息平台自动化。
- 一句话推荐: 不想给每个聊天平台各养一套机器人，这个项目试图把它们请到同一张桌子上吃饭。
- Evidence Notes: `pyproject.toml` 确认 Python 3.12、FastAPI、SQLModel、FAISS、MCP 与多平台 SDK；`main.py` 创建运行目录并通过 `InitialLoader.start()` 启动生命周期；仓库包含 `astrbot/`、dashboard、k8s、samples 和 tests。
- Honest Caveat: 多平台、多插件和多模型意味着攻击面与运维复杂度同步扩大；插件、消息权限、模型密钥和用户数据隔离需要单独评估。AGPL 也会影响网络服务修改版的发布义务。

### Rank 08 - every-app/open-seo
- Repo URL: https://github.com/every-app/open-seo
- Tagline: 开源 SEO 研究与站点分析工具，通过 CLI 与 MCP 提供关键词、审计、竞品和外链工作流。
- Stars: 6,721
- Stars Today: 849
- Forks: 723
- Language: TypeScript
- License: MIT
- Homepage: https://github.com/every-app/open-seo
- Topics: mcp, seo, site-audit, keyword-research, backlink-analysis, cli
- 技术栈: TypeScript, Node.js, CLI, MCP, HTTP clients, SEO data providers
- Why It Matters Today: SEO 工作流正被封装成 Agent 可调用的工具，而不再只依赖网页控制台和人工复制数据。
- 项目摘要: Open SEO 把站点审计、关键词研究、竞品观察和外链分析组织成开源 CLI 与 MCP 工具。它可以被人直接调用，也能成为 Coding Agent 或研究 Agent 的结构化数据入口。
- 核心特性:
  1. 面向关键词、站点、排名和外链的统一命令接口。
  2. 暴露 MCP 工具，便于 Agent 组合多步 SEO 研究。
  3. 支持批量处理并保留部分成功结果，减少单个请求失败拖垮整批任务。
- 适用场景: 内容团队研究、技术 SEO 审计、Agent 自动化报告、关键词与竞品批量分析。
- 一句话推荐: 它想把 SEO 从“开十个后台抄表”改成“让工具把账本递过来”。
- Evidence Notes: 仓库 About 与 README 明确 CLI、MCP、site audit、keyword research 和 backlink analysis；许可证为 MIT。
- Honest Caveat: 数据完整度、费用和使用许可取决于外部 SEO 数据源；工具输出不等同于搜索引擎官方排名承诺。

### Rank 09 - tradesdontlie/tradingview-mcp
- Repo URL: https://github.com/tradesdontlie/tradingview-mcp
- Tagline: 把 Claude Code 与 TradingView Desktop 连接起来的 MCP 服务，为 Agent 提供图表、市场数据和交易研究上下文。
- Stars: 4,945
- Stars Today: 114
- Forks: 2,183
- Language: JavaScript
- License: MIT
- Homepage: https://github.com/tradesdontlie/tradingview-mcp
- Topics: tradingview, mcp, claude-code, market-data, trading-tools
- 技术栈: JavaScript, Node.js, MCP, TradingView Desktop integration, desktop automation
- Why It Matters Today: 金融图表工具正成为 Agent 的外部工作台，但数据授权和自动化边界也比普通开发工具更敏感。
- 项目摘要: TradingView MCP 为支持 MCP 的客户端提供与 TradingView Desktop 交互的工具，使模型能够查询图表上下文、市场信息或执行桌面端研究动作。它更像桥接层，而不是独立交易系统。
- 核心特性:
  1. 把 TradingView 桌面环境封装为 MCP 工具。
  2. 让 Claude Code 等客户端在研究对话中调用图表与市场上下文。
  3. 采用本地桥接方式，减少重新搭建整套行情前端的成本。
- 适用场景: 个人市场研究、图表解释辅助、MCP 桌面自动化实验、非自动下单的策略讨论。
- 一句话推荐: 它给 Agent 搬来一块行情屏，但看屏和替你挣钱中间，还隔着一整条街。
- Evidence Notes: 仓库说明明确其连接 Claude Code 与 TradingView Desktop；主要实现语言为 JavaScript，许可证为 MIT。
- Honest Caveat: 应核对 TradingView 条款、数据源授权和桌面自动化稳定性；报告不把它视为自动交易或投资建议工具，也未验证实时行情准确性。

### Rank 10 - AlexsJones/llmfit
- Repo URL: https://github.com/AlexsJones/llmfit
- Tagline: 本地 LLM 选型与硬件适配工具，根据设备资源判断模型能否运行，并比较量化、速度与内存需求。
- Stars: 30,324
- Stars Today: 129
- Forks: 1,845
- Language: Rust
- License: MIT
- Homepage: https://llmfit.app
- Topics: rust, local-llm, hardware, quantization, benchmarking, cli
- 技术栈: Rust, CLI, hardware probing, model metadata, quantization estimates
- Why It Matters Today: 本地模型选择越来越像容量规划问题，开发者需要在下载数十 GB 权重之前先知道设备扛不扛得住。
- 项目摘要: LLMFit 检测设备 CPU、内存和 GPU 等资源，并将其与模型规模和量化配置匹配，给出可运行性、预估资源占用和候选模型建议。它帮助用户缩小本地模型选型范围，而非直接充当推理引擎。
- 核心特性:
  1. 探测本机硬件并形成资源画像。
  2. 根据模型参数量和量化方式估算内存与运行适配度。
  3. 提供 CLI 形式的模型筛选和比较结果。
- 适用场景: 本地 LLM 选型、边缘设备容量评估、量化方案预筛、教学和实验环境规划。
- 一句话推荐: 下载模型前先让它量量家里的门框，省得大沙发搬到楼道才发现进不去。
- Evidence Notes: 仓库 README 与 About 将其定义为本地模型硬件适配和推荐工具；Rust 实现与 MIT 许可证已确认。
- Honest Caveat: 估算不能替代真实推理测试；驱动、后端、上下文长度、KV Cache 和并发都会改变实际资源占用与速度。

### Rank 11 - hyprwm/Hyprland
- Repo URL: https://github.com/hyprwm/Hyprland
- Tagline: 高度可定制的动态平铺 Wayland Compositor，强调动画、插件、现代协议和桌面工作流控制。
- Stars: 37,117
- Stars Today: 58
- Forks: 1,862
- Language: C++
- License: BSD-3-Clause
- Homepage: https://hypr.land
- Topics: wayland, compositor, linux, desktop, tiling-window-manager
- 技术栈: C++, Wayland, wlroots-related protocols, OpenGL/Vulkan ecosystem, CMake/Meson tooling
- Why It Matters Today: 在几乎被 AI 项目包围的榜单里，Hyprland 仍持续上榜，说明 Linux 桌面和底层图形系统拥有稳定、真实的开发者需求。
- 项目摘要: Hyprland 是 Wayland 上的动态平铺合成器，负责窗口布局、输入、渲染、动画和协议交互。它面向希望深度定制 Linux 桌面行为与视觉效果的用户，并提供插件和丰富配置接口。
- 核心特性:
  1. 动态平铺、浮动窗口和多工作区管理。
  2. 丰富动画、窗口规则、快捷键和显示器配置。
  3. Wayland 协议支持与插件扩展机制。
- 适用场景: Linux 高度定制桌面、Wayland 合成器研究、键盘驱动工作流和系统图形开发。
- 一句话推荐: 别的项目教 AI 干活，它负责把你的桌面工位排得明明白白。
- Evidence Notes: 仓库 About、官方站点和源码表明其为 C++ Wayland compositor；许可证为 BSD-3-Clause。
- Honest Caveat: 桌面体验高度依赖显卡驱动、发行版、协议支持与配置；滚动版本更新可能带来兼容变化，生产工作站应谨慎升级。

### Rank 12 - chrislgarry/Apollo-11
- Repo URL: https://github.com/chrislgarry/Apollo-11
- Tagline: Apollo 11 指令舱与登月舱制导计算机源码的转录归档，是计算机历史与嵌入式工程的重要文献。
- Stars: 70,099
- Stars Today: 1,235
- Forks: 7,851
- Language: Assembly
- License: 仓库页面存在 License 文件入口，但本次未确认其现代 SPDX 标识
- Homepage: https://github.com/chrislgarry/Apollo-11
- Topics: apollo, nasa, guidance-computer, assembly, computer-history
- 技术栈: AGC Assembly, rope-memory-era tooling, historical embedded guidance software
- Why It Matters Today: 一个六十年前的制导程序在现代 AI 工具热榜中获得上千新增 Star，说明可读、可搜索的历史源码仍具有教育和文化价值。
- 项目摘要: 该仓库转录并整理 Apollo 11 Guidance Computer 的指令舱和登月舱源码，目标是尽量忠实保存原始代码、注释和排版。它不是现代可直接部署的软件，而是理解早期实时嵌入式系统、资源约束和任务关键软件工程的历史材料。
- 核心特性:
  1. 保存 Apollo Guidance Computer 的关键飞行软件源码与注释。
  2. 以可搜索、可协作校对的 Git 仓库形式呈现历史材料。
  3. 为嵌入式、航天软件和计算机历史研究提供第一手代码文本。
- 适用场景: 计算机历史教学、汇编语言研究、任务关键嵌入式软件史、数字人文和源码保存。
- 一句话推荐: 榜单前面都在讨论未来，它负责提醒大家：几十 KB 的机器，当年也真把人送上了月球。
- Evidence Notes: 仓库公开说明将内容定位为 Apollo 11 Guidance Computer 源码转录；主要语言为 Assembly，历史归档性质明确。
- Honest Caveat: 该仓库不是现代构建、测试或生产项目；许可证和原始 NASA 材料的法律状态需按仓库文件与适用司法辖区单独核对，不能仅凭历史来源推定。

## Language Distribution

- TypeScript:
  - Count: 3
  - Percent: 25.0%
  - Color Hint: #3178C6
- Python:
  - Count: 3
  - Percent: 25.0%
  - Color Hint: #3572A5
- JavaScript:
  - Count: 2
  - Percent: 16.7%
  - Color Hint: #F1E05A
- Rust:
  - Count: 2
  - Percent: 16.7%
  - Color Hint: #DEA584
- C++:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #F34B7D
- Assembly:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #6E4C13

## Explore Highlights

### Explore 1
- Title: koala73/worldmonitor
- URL: https://github.com/koala73/worldmonitor
- Kind: Trending repository
- Meta: TypeScript · 67k+ Stars · Updated 2026-07-22
- Short Reason: 今日榜首，同时展示了从前端地图、数据网关到 Agent 接口的完整系统形态。

### Explore 2
- Title: bojieli/ai-agent-book
- URL: https://github.com/bojieli/ai-agent-book
- Kind: Trending repository
- Meta: Python · 16k+ Stars · Updated 2026-07-22
- Short Reason: 今日新增 Star 最多，适合作为 AI Agent 原理与工程实践的系统学习入口。

### Explore 3
- Title: tirth8205/code-review-graph
- URL: https://github.com/tirth8205/code-review-graph
- Kind: Trending repository
- Meta: Python · 25k Stars
- Short Reason: 以本地代码图谱解决 AI Coding 的上下文选择问题。

### Explore 4
- Title: React Native
- URL: https://github.com/topics/react-native
- Kind: Popular topic
- Meta: JavaScript mobile framework
- Short Reason: GitHub Explore 当日推荐主题，适合补充移动端开源生态观察。

### Explore 5
- Title: ayghri/i-have-adhd
- URL: https://github.com/ayghri/i-have-adhd
- Kind: Trending repository
- Meta: Python · 7.5k Stars
- Short Reason: 用 Agent Skill 约束输出结构，关注信息可读性而不是再堆一层功能。

### Explore 6
- Title: earthtojake/text-to-cad
- URL: https://github.com/earthtojake/text-to-cad
- Kind: Trending repository
- Meta: JavaScript · 9.5k Stars
- Short Reason: Agent Skills 从编码扩展到 CAD、机器人和硬件设计。

## Rendering Notes

- Hero 主标题建议：GitHub Trending 日报
- Hero 副标题建议：实时情报、代码图谱与自托管交付齐升温，历史源码也来抢镜
- Top 3 高亮原因：保持 GitHub 原始前三名，不按总 Stars 或 Stars Today 重新排序。
- 需要在 HTML 中诚实提示的降级点：Trending 是动态快照；性能与效果主张未独立复测；Apollo 11 为历史源码归档；金融和外部数据工具需要额外核对授权与风险。
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
