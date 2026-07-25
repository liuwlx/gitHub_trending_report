# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-25
- Generated At: 2026-07-25 21:18 JST
- Output Markdown: md/github_trending_report_2026-07-25.md
- Planned HTML: html/github_trending_report_2026-07-25.html
- Fixed Base Template: .codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html
- User Rules: .codex/skills/skill-github-trending-report/reference/user-rules.md
- Data Scope: GitHub Trending · Repositories · Any language · Today
- Sources:
  - https://github.com/trending
  - https://github.com/explore
  - Repo README / About / Homepage / License / Official Documentation / Source Files

## Page Intent

- 今日主线：榜单一头是 Buzz、World Monitor、ego-lite 这类“人和 Agent 共用工作空间”的新系统，另一头是 Harper、Superfile、Pumpkin 等强调本地性能和工程效率的工具。AI 正在从聊天框走进浏览器、协作平台和内容系统，但真正决定能否落地的仍是权限、状态隔离、发布链路与许可证。
- 适合谁阅读：关注 AI Agent 基础设施、Rust/TypeScript 工具链、自托管软件和开发者体验的工程师、架构师与技术负责人。
- 页面重点：严格保留 GitHub 原始排名，同时单列 Stars Today；对重复上榜项目继续提供扫读信息，对首次深挖的 Harper、ego-lite、Instatic 提供独立源码架构报告。
- 需要诚实降级说明的地方：Trending 是晚间动态快照；项目方公布的性能、模型效果和硬件感知准确率未独立复测；`awesome-claude-skills` 未发现标准 LICENSE 文件；Apollo-11 是历史源码转录档案，不宜按现代应用仓库评价成熟度。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：11,152
- 编程语言数：6
- AI 相关项目数：7

## Editorial Insights

### Insight 1
- Title: Agent 不再借你的浏览器，它开始有自己的“工位”
- Body: Buzz 把人和 Agent 放进同一协作房间，ego-lite 给每个 Agent 独立浏览器 Space，World Monitor 则把多源情报和 AI 分析收进一个态势界面。共同方向不是再造一个聊天框，而是给 Agent 明确的工作空间、状态边界和可观察结果。

### Insight 2
- Title: 本地优先重新成为卖点：快、私密、少一层服务费
- Body: Harper 把英文语法检查放进 Rust/WASM 本地执行，Superfile 把文件管理留在终端，Instatic 把编辑器、内容、发布和插件塞进一台自托管 Bun 服务。云服务不是坏人，但“数据不出门、请求不绕路、系统自己掌控”正重新变成产品竞争力。

### Insight 3
- Title: 今天最热的不等于今天涨得最快之外的唯一答案
- Body: Buzz 以 3,270 Stars Today 领跑，World Monitor 增加 2,184，RuView 增加 1,022；但 Harper、ego-lite、Instatic 的绝对体量更小，增长比例和技术新鲜度更值得单独观察。原始排名看综合热度，增星量看加速度，源码分析看有没有真东西，三把尺子别互相冒名顶替。

### Insight 4
- Title: “一体化”项目越来越多，边界检查也要跟着升级
- Body: Instatic 一台 Bun 服务承载编辑、内容、发布、插件与认证；Buzz 组合实时通信、数据库、对象存储和 Agent；RuView 横跨 WiFi 感知、边缘硬件与可视化。系统越一体化，安装越省心，但权限、备份、升级、故障域和许可证责任也更集中。

## Top Projects

### Rank 01 - block/buzz
- Repo URL: https://github.com/block/buzz
- Tagline: 面向人类与 AI Agent 的实时协作平台，把房间、消息、文件和自动化工作流放在同一套自托管系统中。
- Stars: 10,538
- Stars Today: 3,270
- Forks: 826
- Language: Rust
- License: Apache-2.0
- Homepage: https://github.com/block/buzz
- Topics: collaboration, agents, nostr, self-hosted, realtime
- 技术栈: Rust, WebSocket, REST, Nostr signed events, PostgreSQL, Redis Pub/Sub, S3/MinIO
- Why It Matters Today: 今日增星最高，代表 Agent 协作正在从单人 CLI 扩展到共享房间、消息和可审计事件流。
- 项目摘要: Buzz 是一个可自托管的实时协作工作区。人和 Agent 可以加入房间、发送签名事件、共享媒体并触发自动化；服务端负责连接管理、事件持久化与分发。
- 核心特性:
  1. 以签名事件组织消息和状态，便于验证来源与同步。
  2. WebSocket 实时分发，PostgreSQL 保存事件，Redis 负责跨实例发布订阅。
  3. 媒体可接 S3/MinIO，支持桌面端、CLI 与 Agent 接入。
- 适用场景: 自托管团队协作、Agent 运行看板、需要事件审计与实时反馈的自动化工作空间。
- 一句话推荐: 想研究“人和 Agent 怎么在同一间办公室里干活”，Buzz 是今天最直接的样本。
- Evidence Notes: 仓库说明与源码结构明确列出 relay、数据库、实时连接和对象存储边界；许可证为 Apache-2.0。
- Honest Caveat: 项目仍处于快速增长阶段；多实例一致性、权限模型和大规模房间压力需结合实际部署验证。

### Rank 02 - koala73/worldmonitor
- Repo URL: https://github.com/koala73/worldmonitor
- Tagline: 将新闻、地缘政治、基础设施与市场信号汇总到统一地图和态势面板的实时情报系统。
- Stars: 73,630
- Stars Today: 2,184
- Forks: 11,039
- Language: TypeScript
- License: AGPL-3.0-or-later
- Homepage: https://github.com/koala73/worldmonitor
- Topics: osint, geopolitics, news, monitoring, dashboard, ai, mcp
- 技术栈: TypeScript, Web frontend, API routes, data ingestion, maps, caching, AI summaries
- Why It Matters Today: 连续高位上榜，说明开发者对统一态势感知和多源信息聚合的需求仍在快速增长。
- 项目摘要: World Monitor 把多类公开数据和新闻信号投射到可交互地图与监控面板，为分析员提供全球事件、基础设施和市场变化的统一入口。
- 核心特性:
  1. 多源信息抓取、归一化和地图可视化。
  2. 支持 AI 摘要与情报辅助分析。
  3. 提供多种监控视图和自托管部署路径。
- 适用场景: OSINT、风险监控、供应链观察、新闻编辑室和全球运营态势看板。
- 一句话推荐: 不想在二十个网页之间来回搬砖，可以先看它怎样把信息收进一张图。
- Evidence Notes: 仓库目录含 API、数据、部署与 E2E；LICENSE 明确为 AGPLv3 或更高版本。
- Honest Caveat: 数据准确性和授权取决于上游源；AI 摘要不能替代原始材料核验。

### Rank 03 - ComposioHQ/awesome-claude-skills
- Repo URL: https://github.com/ComposioHQ/awesome-claude-skills
- Tagline: Claude Skills、Agent 工作流与工具资源的策展合集。
- Stars: 70,238
- Stars Today: 663
- Forks: 7,914
- Language: Python
- License: 未发现标准 LICENSE 文件
- Homepage: https://github.com/ComposioHQ/awesome-claude-skills
- Topics: claude, agent-skills, automation, mcp, developer-tools
- 技术栈: Markdown, Python utilities, skill packages, workflow examples
- Why It Matters Today: Skill 正在成为 Agent 能力复用的常见包装方式，资源合集因此获得强关注。
- 项目摘要: 该仓库汇总不同来源的 Claude Skills、自动化模板和工具连接方式，适合做生态导航和快速发现。
- 核心特性:
  1. 按场景整理 Skills 与工作流资源。
  2. 覆盖 Claude Code、Codex、MCP 与多种自动化用途。
  3. 部分目录包含可直接参考的 Skill 文件和产物构建示例。
- 适用场景: Agent 能力调研、Skill 设计参考、团队建立内部能力目录。
- 一句话推荐: 它像工具市场导购，不是发动机拆解图；适合逛，不适合直接当生产架构。
- Evidence Notes: GitHub 将其描述为 curated list，仓库主要由资源目录组成。
- Honest Caveat: 未发现标准 LICENSE 文件；收录项目质量、安全性和维护状态需要逐项核验。

### Rank 04 - Pumpkin-MC/Pumpkin
- Repo URL: https://github.com/Pumpkin-MC/Pumpkin
- Tagline: 用 Rust 编写的高性能 Minecraft 服务端实现。
- Stars: 9,441
- Stars Today: 473
- Forks: 634
- Language: Rust
- License: GPL-3.0
- Homepage: https://github.com/Pumpkin-MC/Pumpkin
- Topics: rust, minecraft, game-server, networking, minecraft-protocol
- 技术栈: Rust, Tokio, Minecraft protocol, async networking, Docker
- Why It Matters Today: Rust 在高并发游戏服务端领域继续吸引关注，项目强调效率和现代工程结构。
- 项目摘要: Pumpkin 从协议与服务端逻辑层重建 Minecraft 服务端，目标是降低资源消耗并提供可维护的模块化实现。
- 核心特性:
  1. 异步网络处理和协议状态机。
  2. 世界、玩家、实体和插件等模块化组织。
  3. 提供容器化与开发运行方式。
- 适用场景: Rust 游戏服务端研究、Minecraft 私服实验、协议实现学习。
- 一句话推荐: 想看 Rust 怎么接住一群方块世界玩家，Pumpkin 比南瓜灯更亮。
- Evidence Notes: LICENSE 为 GPL-3.0；仓库和 Explore 均明确定位为 Minecraft 服务端。
- Honest Caveat: 与官方服务端的功能兼容度和插件生态仍需按版本核验。

### Rank 05 - shiyu-coder/Kronos
- Repo URL: https://github.com/shiyu-coder/Kronos
- Tagline: 面向金融市场 K 线序列的基础模型与预测工具链。
- Stars: 33,591
- Stars Today: 499
- Forks: 5,683
- Language: Python
- License: MIT
- Homepage: https://github.com/shiyu-coder/Kronos
- Topics: time-series, finance, foundation-model, forecasting, trading
- 技术栈: Python, PyTorch, tokenizer, transformer, Gradio/Web UI, fine-tuning utilities
- Why It Matters Today: 金融时间序列基础模型继续升温，项目同时提供模型、推理和微调入口。
- 项目摘要: Kronos 将金融 K 线序列离散化并交给专用模型学习，用于市场序列建模、预测和下游微调研究。
- 核心特性:
  1. 面向 OHLCV 等金融序列的专用 tokenizer 和模型。
  2. 提供推理、微调、示例和 Web UI。
  3. 维护者披露使用多交易所数据训练。
- 适用场景: 金融时间序列研究、特征表示实验、模型微调与策略研究前置分析。
- 一句话推荐: 可以拿来做研究对象，别拿 README 的曲线直接去给账户上香。
- Evidence Notes: 仓库包含 model、finetune、examples、tests 与 webui；LICENSE 为 MIT。
- Honest Caveat: 模型效果、回测收益和跨市场稳定性未由本报告独立复测，不构成交易建议。

### Rank 06 - Automattic/harper
- Repo URL: https://github.com/Automattic/harper
- Tagline: Rust 驱动、离线运行、隐私优先的英文语法与拼写检查引擎。
- Stars: 13,137
- Stars Today: 876
- Forks: 487
- Language: Rust
- License: Apache-2.0
- Homepage: https://writewithharper.com
- Topics: grammar-checker, english-language, rust, webassembly, language-server, privacy
- 技术栈: Rust workspace, harper-core, Brill POS tagger, dictionary/FST, LSP, WebAssembly, editor integrations
- Why It Matters Today: 本地 AI/语言工具热度上升，Harper 用小型规则与语言处理管线而非云端大模型解决高频写作检查。
- 项目摘要: Harper 的核心先解析文本、生成 token 与词性/短语元数据，再执行拼写和语法 lint；同一核心通过 LSP、WASM、CLI、桌面和编辑器插件复用。
- 核心特性:
  1. 文本完全本地处理，适合隐私敏感写作。
  2. `harper-core` 作为统一引擎，向 LSP、WASM 与多编辑器暴露。
  3. 支持 Markdown、HTML、Typst 等多种文本载体的解析适配。
- 适用场景: 编辑器实时英文校对、离线写作、隐私敏感文档和嵌入式语法检查。
- 一句话推荐: 不想每敲一句话都寄到云端批改，Harper 值得拆开看。
- Evidence Notes: Cargo workspace、`Document` 解析流程和官方架构文档共同确认 core/LSP/WASM 分层；LICENSE 为 Apache-2.0。
- Honest Caveat: 当前主要支持英语；“毫秒级”和内存优势来自维护者说明，未在本报告环境独立复测。

### Rank 07 - likec4/likec4
- Repo URL: https://github.com/likec4/likec4
- Tagline: 用代码维护 C4 风格架构模型并生成可交互图表的 Architecture-as-Code 工具。
- Stars: 5,095
- Stars Today: 337
- Forks: 336
- Language: TypeScript
- License: MIT
- Homepage: https://likec4.dev
- Topics: architecture, diagrams, c4, architecture-as-code
- 技术栈: TypeScript, DSL parser, language server, layout engine, web renderer, VS Code tooling
- Why It Matters Today: 软件架构图持续性失真是常见痛点，代码化模型和即时校验提供了可维护路径。
- 项目摘要: LikeC4 让团队用 DSL 描述系统、关系和视图，工具链完成解析、校验、布局和交互式渲染。
- 核心特性:
  1. 架构模型与视图分离，支持复用和多层次展示。
  2. 编辑器实时诊断和预览。
  3. 可生成 Web 图表并接入文档流程。
- 适用场景: 架构文档、系统边界评审、团队共享 C4 模型和持续更新的技术地图。
- 一句话推荐: 架构图要活着，不能每次评审才从坟里刨出来。
- Evidence Notes: LICENSE 为 MIT；仓库明确定位为 architecture-as-code。
- Honest Caveat: 大型模型布局性能和协作治理需要按团队规模测试。

### Rank 08 - citrolabs/ego-lite
- Repo URL: https://github.com/citrolabs/ego-lite
- Tagline: 让人和 AI Agent 在同一浏览器内使用隔离 Space 并共享登录状态的浏览器自动化系统。
- Stars: 2,922
- Stars Today: 880
- Forks: 137
- Language: JavaScript
- License: MIT（仓库内容；浏览器二进制单独分发）
- Homepage: https://lite.ego.app
- Topics: browser, ai-agent, agent-skills, automation, chromium
- 技术栈: Chromium-based app, Node.js >=22, TypeScript, CDP harness, JavaScript tool facade, Agent Skill
- Why It Matters Today: 今日增长比例突出，击中了 Agent 浏览器自动化中登录态、标签争用和多任务隔离三个真实问题。
- 项目摘要: ego-lite 为 Agent 建立独立 Task Space，同时继承用户登录状态；`ego-browser` 通过 Node.js/TypeScript 运行时暴露 Playwright 风格页面能力和任务空间生命周期。
- 核心特性:
  1. 每个 Agent 使用独立 Space，避免与用户标签页互相抢控制权。
  2. Agent 可在一次 JavaScript 执行中组合导航、读取、填写、点击和验证。
  3. Task Space 提供创建、切换、交接和完成的生命周期。
- 适用场景: 已登录网站自动化、网页测试、数据采集、多 Agent 并行浏览器任务。
- 一句话推荐: 以前 Agent 借你浏览器像借车不还，如今给它单独停车位。
- Evidence Notes: README、Skill 与 `package/ego-browser/src/index.ts` 共同确认 Task Space、page/browser facade 与 CLI 运行方式；仓库 LICENSE 为 MIT。
- Honest Caveat: 当前浏览器应用主要支持 macOS；2.5×速度和 Token 优势为维护者基准，未独立复测；共享登录态意味着权限边界必须谨慎配置。

### Rank 09 - yorukot/superfile
- Repo URL: https://github.com/yorukot/superfile
- Tagline: 面向终端用户的现代 TUI 文件管理器。
- Stars: 19,751
- Stars Today: 338
- Forks: 606
- Language: Go
- License: MIT
- Homepage: https://superfile.netlify.app
- Topics: cli, golang, filemanager, tui, filesystem, bubbletea
- 技术栈: Go, Bubble Tea ecosystem, terminal UI, filesystem operations, themes/plugins
- Why It Matters Today: 开发者对键盘优先、跨平台和可定制本地工具的需求持续稳定。
- 项目摘要: Superfile 把多面板文件浏览、搜索、预览和常用文件操作放进终端交互界面。
- 核心特性:
  1. 键盘驱动的多面板文件管理。
  2. 主题、热键和插件式扩展配置。
  3. 跨平台分发和本地文件系统操作。
- 适用场景: 远程服务器、终端重度用户、开发环境文件整理。
- 一句话推荐: 鼠标不在手边，文件也不能装看不见。
- Evidence Notes: 仓库主题和目录明确为 Go TUI 文件管理器；LICENSE 为 MIT。
- Honest Caveat: 批量删除、移动等高风险操作仍需结合备份和权限策略使用。

### Rank 10 - ruvnet/RuView
- Repo URL: https://github.com/ruvnet/RuView
- Tagline: 利用普通 WiFi 信号推断空间占用、动作和生命体征的无线感知平台。
- Stars: 86,104
- Stars Today: 1,022
- Forks: 11,460
- Language: Rust
- License: MIT
- Homepage: https://github.com/ruvnet/RuView
- Topics: wifi, esp32, spatial-intelligence, presence-detection, home-assistant, rf
- 技术栈: Rust, ESP32/CSI, signal processing, edge processing, dashboard, Home Assistant integrations
- Why It Matters Today: 无摄像头空间感知继续吸引大量关注，项目把射频信号处理、边缘硬件和可视化放进同一仓库。
- 项目摘要: RuView 采集 WiFi CSI 等无线信号，经过处理后输出存在检测、动作或生命体征相关估计，并提供仪表盘与家居集成。
- 核心特性:
  1. 不依赖摄像头的空间与存在感知。
  2. 支持边缘硬件、信号处理和可视化链路。
  3. 提供 Home Assistant 等集成方向。
- 适用场景: 智能家居实验、隐私友好存在检测、无线感知研究。
- 一句话推荐: 墙上没摄像头，WiFi 也可能在“听脚步”，先研究再部署。
- Evidence Notes: LICENSE 为 MIT；仓库明确包含固件、dashboard、benchmarks 与多种感知组件。
- Honest Caveat: 准确率受硬件、布局和无线环境影响；医疗用途与安全结论未经独立认证。

### Rank 11 - CoreBunch/Instatic
- Repo URL: https://github.com/CoreBunch/Instatic
- Tagline: 把视觉编辑、内容管理、插件、认证和静态发布合并到一个 Bun 服务的自托管 CMS。
- Stars: 4,398
- Stars Today: 201
- Forks: 416
- Language: TypeScript
- License: MIT
- Homepage: https://instatic.com
- Topics: cms, visual-editor, self-hosted, static-site, bun, plugins
- 技术栈: Bun, TypeScript, React 19, Vite, SQLite/PostgreSQL, TypeBox, QuickJS-WASM, Docker
- Why It Matters Today: 自托管“一体化网站生命周期”重新获得关注，项目同时尝试干净静态输出和受限插件执行。
- 项目摘要: Instatic 在一个 Bun 进程内提供管理后台、视觉编辑器、CMS API、公开页面和媒体；发布器把页面树转为语义 HTML/CSS，并对静态、缓存和动态洞采用三层交付。
- 核心特性:
  1. 统一内容模型和可视化页面树。
  2. 静态文件原子切换、版本化内存缓存与按需动态洞。
  3. 插件后端在 QuickJS-WASM 沙箱与独立 Worker 中运行。
- 适用场景: 自托管品牌站、博客、小型内容团队、需要可视化编辑又希望输出干净 HTML 的项目。
- 一句话推荐: 它想把建站工具的“全家桶”装进一个箱子，值得看看箱盖怎么扣住的。
- Evidence Notes: 官方架构文档明确 Bun 单进程、两类 Worker、SQLite/Postgres、三层发布器和 TypeBox 边界；package.json 与 LICENSE 为 MIT。
- Honest Caveat: 当前版本仍早期；一体化架构减少运维组件，也会放大单进程故障域和升级风险。

### Rank 12 - chrislgarry/Apollo-11
- Repo URL: https://github.com/chrislgarry/Apollo-11
- Tagline: Apollo 11 指令舱与登月舱制导计算机源代码的数字转录档案。
- Stars: 71,449
- Stars Today: 409
- Forks: 7,933
- Language: Assembly
- License: 仓库未给出适用于现代复用的清晰标准许可证结论
- Homepage: https://github.com/chrislgarry/Apollo-11
- Topics: apollo, guidance-computer, assembly, history, nasa
- 技术栈: Apollo Guidance Computer assembly, Comanche 055, Luminary 099
- Why It Matters Today: 历史工程源码再次进入榜单，提醒开发者软件史和系统约束同样是技术学习材料。
- 项目摘要: 该仓库是 Apollo 11 AGC 源码的数字化转录，主要用于历史保存、阅读和研究，而不是可直接部署的现代软件。
- 核心特性:
  1. 保留指令舱与登月舱 AGC 程序文本。
  2. 提供历史注释和转录修正过程。
  3. 可用于计算机史、嵌入式约束和软件考古研究。
- 适用场景: 软件史教学、AGC 研究、汇编与受限计算环境学习。
- 一句话推荐: 这不是“老代码”，这是人类把代码写到月亮上的证物。
- Evidence Notes: GitHub 明确将其描述为 Apollo 11 AGC 原始源码数字转录。
- Honest Caveat: 不是现代构建项目；版权与再利用范围应单独核验，不应按普通开源库直接集成。

## Language Distribution

- Rust:
  - Count: 4
  - Percent: 33.3%
  - Color Hint: #DEA584
- TypeScript:
  - Count: 3
  - Percent: 25.0%
  - Color Hint: #3178C6
- Python:
  - Count: 2
  - Percent: 16.7%
  - Color Hint: #3572A5
- JavaScript:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #F1E05A
- Go:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #00ADD8
- Assembly:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #6E4C13

## Explore Highlights

### Explore 1
- Title: block/buzz
- URL: https://github.com/block/buzz
- Kind: Trending repository
- Meta: Rust · 人与 Agent 的实时协作平台
- Short Reason: 同时占据 Trending 与 Explore 首位，代表 Agent 协作空间热度。

### Explore 2
- Title: koala73/worldmonitor
- URL: https://github.com/koala73/worldmonitor
- Kind: Trending repository
- Meta: TypeScript · 全球态势监控
- Short Reason: 多源情报和地图可视化持续高热。

### Explore 3
- Title: Copilot vs. raw API access: What are you actually paying for?
- URL: https://github.blog
- Kind: GitHub Blog
- Meta: Agent 成本与工程 harness
- Short Reason: 讨论模型调用之外的工作流、策略与工具成本。

### Explore 4
- Title: Automattic/harper
- URL: https://github.com/Automattic/harper
- Kind: Trending repository
- Meta: Rust · 离线语法检查
- Short Reason: 本地隐私工具和 WASM 复用架构值得关注。

### Explore 5
- Title: ChartDB
- URL: https://github.com/chartdb/chartdb
- Kind: GitHub staff recommendation
- Meta: Web 数据库图表编辑器
- Short Reason: 通过查询快速可视化数据库 Schema。

### Explore 6
- Title: citrolabs/ego-lite
- URL: https://github.com/citrolabs/ego-lite
- Kind: Trending repository
- Meta: JavaScript · Agent 浏览器 Space
- Short Reason: 解决登录态共享与并行浏览器任务冲突。

### Explore 7
- Title: yorukot/superfile
- URL: https://github.com/yorukot/superfile
- Kind: Trending repository
- Meta: Go · 终端文件管理器
- Short Reason: 本地开发者工具继续保持稳定关注。

### Explore 8
- Title: Game Engines
- URL: https://github.com/collections/game-engines
- Kind: GitHub Collection
- Meta: 64 个跨平台游戏引擎项目
- Short Reason: 为游戏开发者提供体系化项目入口。

## Rendering Notes

- Hero 主标题建议：GitHub Trending 日报
- Hero 副标题建议：Agent 有了独立工位，本地工具和一体化自托管系统同时升温
- Top 3 高亮原因：严格按 GitHub 原始排名高亮 Buzz、World Monitor、awesome-claude-skills，不以编辑偏好重排。
- 需要在 HTML 中诚实提示的降级点：Trending 为动态晚间快照；项目性能与模型效果未独立复测；资源合集和历史档案不参与源码架构深挖。
- 不允许省略的区块：Header / Hero、4 张 Stats Cards、今日洞察、今日热门 Top 12、编程语言分布、GitHub Explore 精选、Footer。
- Top 详情固定顺序：项目摘要、核心特性、技术栈、适用场景、一句话推荐。
- 独立架构分析入口：analysis/2026-07-25/README.md
