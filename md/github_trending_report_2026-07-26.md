# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-26
- Generated At: 2026-07-26 21:18 JST
- Output Markdown: md/github_trending_report_2026-07-26.md
- Planned HTML: html/github_trending_report_2026-07-26.html
- Fixed Base Template: .codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html
- User Rules: .codex/skills/skill-github-trending-report/reference/user-rules.md
- Data Scope: GitHub Trending · Repositories · Any language · Today
- Sources:
  - https://github.com/trending
  - https://github.com/explore
  - Repo README / About / Homepage / Release / source files

## Page Intent

- 今日主线：Agent 工具继续从 Prompt 和技能文本走向可执行系统；浏览器自动化、MCP 视频编辑和通信基础设施同时升温，Rust 项目则在协作、语言检查与游戏服务器三个方向持续出现。
- 适合谁阅读：关注 AI 工程、开发工具、端侧应用、通信系统和 Rust 生态的软件工程师、技术负责人及开源观察者。
- 页面重点：严格保留 GitHub 原始排名，同时把 Stars Today 单独展示；日报负责快速发现，独立分析文档负责解释系统怎样工作。
- 需要诚实降级说明的地方：Trending 排名算法未公开；Stars Today 是动态页面快照；项目方的性能、模型效果和安全主张未做独立复测；Explore 与 Trending 高度重合。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：10,148
- 编程语言数：7
- AI 相关项目数：9（包含 AI 协作平台 Buzz；该统计是编辑分类，不是 GitHub 官方标签）

## Editorial Insights

### Insight 1
- Title: Agent 能力从“写说明书”继续走向“接管真实工具”
- Body: `ego-lite` 把已登录浏览器变成 Agent 可调用的 CDP 工具，`palmier-pro` 通过本地 MCP 让 Claude、Codex 和 Cursor 直接操作视频时间线，`open-code-review` 则把 LLM Agent 放进可重复执行的代码审查流水线。今天的趋势不是又多了几段 Prompt，而是 Agent 开始进入浏览器、编辑器和工程流程的执行层。

### Insight 2
- Title: Rust 同时出现在协作、语言工具和游戏服务器
- Body: `block/buzz` 用 Rust 构建人类与 Agent 共用的通信平台，`Automattic/harper` 用 Rust 做离线语法检查核心，`Pumpkin-MC/Pumpkin` 则以 Rust 重写 Minecraft 服务端。三者场景不同，但共同诉求都是低延迟、可控资源与可部署的系统边界。

### Insight 3
- Title: 排名和增星速度依然是两张表
- Body: 第 10 名 `bitchat` 今日新增 1,720 Stars，第 11 名 `mattpocock/skills` 新增 1,740，而榜首 `block/buzz` 新增 2,491。原始排名是 GitHub 的综合趋势结果，Stars Today 更像加速度；看热度时两者都要看，不能拿百米成绩给马拉松颁奖。

### Insight 4
- Title: 本地优先不等于没有安全边界
- Body: `ego-lite` 使用用户已登录的浏览器，`bitchat` 涉及密钥、离线转发与互联网中继，`palmier-pro` 在本机开放 MCP HTTP 服务。它们都在减少云端依赖，但也把权限、会话、端口与本地数据保护变成了使用前必须检查的项目。

## Top Projects

### Rank 01 - block/buzz
- Repo URL: https://github.com/block/buzz
- Tagline: 面向人类与 AI Agent 的 hive-mind 通信平台，提供频道、签名事件、实时中继和审计能力。
- Stars: 12,360
- Stars Today: 2,491
- Forks: 995
- Language: Rust
- License: Apache-2.0
- Homepage: https://github.com/block/buzz
- Topics: rust, collaboration, agents, nostr, realtime
- 技术栈: Rust workspace, WebSocket/REST, Nostr events, PostgreSQL, Redis, S3/MinIO
- Why It Matters Today: 它把 Agent 协作从聊天界面推进到有身份、权限、事件签名和审计的通信基础设施。
- 项目摘要: Buzz 试图成为人类与 Agent 共用的实时协作层。客户端通过 WebSocket 或 REST 接入 Rust relay，以签名事件表达消息和状态，并规划持久化、缓存与对象存储等服务。
- 核心特性:
  1. 频道和私有通信面向人类与 Agent 双方。
  2. 使用签名事件与认证机制减少身份冒用。
  3. 提供实时中继、审计与可扩展存储边界。
- 适用场景: Agent 团队协作、需要可审计消息流的内部工具、研究多 Agent 通信协议。
- 一句话推荐: 想研究“Agent 怎么像团队成员一样安全进群干活”，Buzz 是今天最值得拆开的系统。
- Evidence Notes: README 与仓库资料描述 Rust relay、WebSocket/REST、Nostr 签名事件及 PostgreSQL/Redis/S3 组件。
- Honest Caveat: 多项组件仍处于建设或接线阶段，不应把路线图当作已完成的生产能力。

### Rank 02 - alibaba/open-code-review
- Repo URL: https://github.com/alibaba/open-code-review
- Tagline: 将确定性流水线与 LLM Agent 结合的命令行代码审查工具。
- Stars: 13,214
- Stars Today: 431
- Forks: 899
- Language: Go
- License: Apache-2.0
- Homepage: https://open-codereview.ai
- Topics: code-review, llm-agent, cli, go, devtools
- 技术栈: Go, Git diff, LLM tool use, CLI workflow
- Why It Matters Today: 它强调先用确定性流程收集范围和证据，再让模型推理，减少“把整个仓库扔给模型”的失控感。
- 项目摘要: OpenCodeReview 从 Git 变更入手，构建可重复的审查上下文，再让 LLM Agent 调用工具定位代码并生成行级反馈，适合在本地或 CI 中运行。
- 核心特性:
  1. 围绕 Git diff 构建审查范围。
  2. Agent 可使用工具补充代码上下文。
  3. 输出可定位到文件和行的审查意见。
- 适用场景: PR 预审、团队代码规范检查、在 CI 前做本地风险扫描。
- 一句话推荐: 适合想把 AI Review 从“随口点评”变成可重复工程流程的团队。
- Evidence Notes: 官方 README、CLI 文档和仓库源码说明确定性 pipeline 与 LLM Agent 协作。
- Honest Caveat: 审查准确率依赖模型、提示词和代码上下文，不能替代人工评审与测试。

### Rank 03 - citrolabs/ego-lite
- Repo URL: https://github.com/citrolabs/ego-lite
- Tagline: 让 AI Agent 使用用户已经登录的共享浏览器完成网页自动化。
- Stars: 3,825
- Stars Today: 986
- Forks: 189
- Language: JavaScript
- License: MIT（仓库辅助代码；下载应用的分发条款需另行核验）
- Homepage: https://github.com/citrolabs/ego-lite
- Topics: browser-automation, cdp, ai-agent, macos, typescript
- 技术栈: TypeScript, Node.js 22+, Chromium, CDP, browser bridge
- Why It Matters Today: 它减少了 Agent 每次重新登录和启动独立浏览器的成本，把真实用户会话变成受控自动化入口。
- 项目摘要: Ego Lite 在用户控制的 Chromium 浏览器中提供 `globalThis.ego` 桥接，Node CLI 读取 Agent 的 JavaScript 任务，构建 helper 上下文并通过 CDP 操作当前标签页。
- 核心特性:
  1. 复用已登录浏览器会话。
  2. 提供 Playwright 风格 helper 和 CDP 访问。
  3. 会话丢失时自动重新附加目标标签页。
- 适用场景: 需要登录态的后台操作、网页数据收集、Agent 驱动的浏览器测试和运营流程。
- 一句话推荐: 需要 Agent 操作“你真正正在用的浏览器”时，它比再造一个无头浏览器更直接。
- Evidence Notes: `package/ego-browser/src/run.ts`、`browser-runtime.ts` 与 package.json 证实 CLI、helper 上下文、CDP 会话和重连逻辑。
- Honest Caveat: 当前主要面向 macOS；共享真实登录态意味着自动化脚本拥有较高权限，必须限制任务来源和可操作站点。

### Rank 04 - ComposioHQ/awesome-claude-skills
- Repo URL: https://github.com/ComposioHQ/awesome-claude-skills
- Tagline: Claude Skills、资源和示例的精选目录。
- Stars: 70,747
- Stars Today: 577
- Forks: 7,952
- Language: Python
- License: 未在本次仓库概览中明确确认，使用前需核验各子项目许可证
- Homepage: https://github.com/ComposioHQ/awesome-claude-skills
- Topics: claude, skills, agents, resources, awesome-list
- 技术栈: Markdown, SKILL.md conventions, Python examples
- Why It Matters Today: Skills 已经成为 Claude 工具生态的分发单元，开发者需要一个发现入口。
- 项目摘要: 这是围绕 Claude Skills 的导航和示例集合，帮助开发者寻找可安装能力、参考格式和社区实践。
- 核心特性:
  1. 按用途整理 Skill 与资源。
  2. 展示 `SKILL.md` 渐进加载模式。
  3. 提供生态发现入口。
- 适用场景: 寻找 Claude Skill、学习 Skill 结构、搭建团队能力目录。
- 一句话推荐: 适合逛目录，不适合把目录本身当成生产系统。
- Evidence Notes: README 明确定位为 curated list，并说明 Skill 的渐进加载方式。
- Honest Caveat: 条目质量、维护状态和许可证彼此独立，需要逐项核验。

### Rank 05 - anthropics/claude-cookbooks
- Repo URL: https://github.com/anthropics/claude-cookbooks
- Tagline: Anthropic 官方维护的 Claude API 示例、模式和实践配方。
- Stars: 49,988
- Stars Today: 132
- Forks: 5,903
- Language: Jupyter Notebook
- License: MIT
- Homepage: https://github.com/anthropics/claude-cookbooks
- Topics: claude, api, notebooks, examples, prompt-engineering
- 技术栈: Python, Jupyter Notebook, Anthropic API
- Why It Matters Today: API 示例仍是开发者理解新能力和正确调用方式的低成本入口。
- 项目摘要: Claude Cookbooks 用可运行 Notebook 和代码片段演示常见 API 模式，包括工具调用、检索和多模态等任务。
- 核心特性:
  1. 官方示例与可运行 Notebook。
  2. 按任务拆分调用模式。
  3. 适合快速验证 API 行为。
- 适用场景: 原型验证、Claude API 入门、团队内部示例库。
- 一句话推荐: 想先把 API 跑通再谈架构，先来这里抄正确的第一行代码。
- Evidence Notes: 官方仓库 README、Notebook 和 MIT 许可证。
- Honest Caveat: Cookbook 是示例，不包含完整生产治理、安全、成本和可观测性方案。

### Rank 06 - Automattic/harper
- Repo URL: https://github.com/Automattic/harper
- Tagline: 离线、隐私优先的英语拼写与语法检查器，核心由 Rust 实现。
- Stars: 13,520
- Stars Today: 503
- Forks: 513
- Language: Rust
- License: Apache-2.0
- Homepage: https://writewithharper.com
- Topics: grammar-checker, rust, webassembly, language-server, privacy
- 技术栈: Rust workspace, harper-core, LSP, WebAssembly, TypeScript/Svelte integrations
- Why It Matters Today: 它展示了不用云端 LLM，也能以较低资源和低延迟提供实用语言检查。
- 项目摘要: Harper 把文档解析、英语 token 化和规则 lint 集中在 `harper-core`，再通过语言服务器、WASM、CLI、桌面端和编辑器插件复用同一核心。
- 核心特性:
  1. 文本在本地处理，不上传云端。
  2. Parser 与 Linter trait 允许扩展格式和规则。
  3. 通过 LSP 与 WASM 覆盖编辑器和 Web 环境。
- 适用场景: 编辑器语法提示、离线写作、隐私敏感文档和嵌入式语言检查。
- 一句话推荐: 想研究“小而快的本地语言工具”怎样做成多端产品，Harper 很有教材味。
- Evidence Notes: 官方架构文档说明 `Document`、`Parser`、`Linter`、`harper-ls` 和 `harper.js`；Cargo workspace 与 `harper-core` 源码提供佐证。
- Honest Caveat: 当前主要支持英语；官方性能对比未在本次任务中独立复测。

### Rank 07 - shiyu-coder/Kronos
- Repo URL: https://github.com/shiyu-coder/Kronos
- Tagline: 面向金融 K 线序列的基础模型与研究代码。
- Stars: 33,888
- Stars Today: 319
- Forks: 5,720
- Language: Python
- License: MIT
- Homepage: https://github.com/shiyu-coder/Kronos
- Topics: finance, time-series, foundation-model, trading, deep-learning
- 技术栈: Python, PyTorch, time-series modeling, financial datasets
- Why It Matters Today: 专用时序基础模型仍在吸引量化与 AI 研究者，但从模型表现到交易价值之间还有很长的验证链。
- 项目摘要: Kronos 针对金融 K 线序列进行预训练，提供模型、推理与实验材料，用于价格序列建模和下游研究。
- 核心特性:
  1. 面向 OHLCV/K 线数据的专用建模。
  2. 提供预训练模型与示例。
  3. 覆盖多市场数据研究。
- 适用场景: 金融时序研究、特征实验、模型基线比较。
- 一句话推荐: 适合研究，不适合看见回测图就把银行卡交出去。
- Evidence Notes: README、模型卡和研究资料说明训练范围与用途。
- Honest Caveat: 训练规模和收益表现属于项目方披露；模型权重与研究代码不等于可交易系统，更不构成投资建议。

### Rank 08 - obra/superpowers
- Repo URL: https://github.com/obra/superpowers
- Tagline: 面向编码 Agent 的可组合 Skills 与软件开发方法论。
- Stars: 261,256
- Stars Today: 479
- Forks: 23,317
- Language: Shell
- License: MIT
- Homepage: https://github.com/obra/superpowers
- Topics: agentic-workflow, skills, tdd, code-review, claude-code
- 技术栈: Markdown, Shell, agent skills, Git workflows
- Why It Matters Today: Agent 开发正在从个人提示习惯变成可复用、可审查的团队流程资产。
- 项目摘要: Superpowers 把需求澄清、计划、TDD、调试、审查和 Git 操作整理成可组合 Skill，供多种编码 Agent 使用。
- 核心特性:
  1. 覆盖软件开发生命周期的 Skills。
  2. 强调测试驱动与系统化调试。
  3. 支持多种编码 Agent 环境。
- 适用场景: 标准化 AI 编程流程、团队共享 Agent 方法、复杂任务分阶段执行。
- 一句话推荐: 它卖的不是魔法，是把靠谱开发习惯装进 Agent 的工具箱。
- Evidence Notes: README、Skills 目录和 MIT 许可证。
- Honest Caveat: 方法论效果依赖执行环境和团队纪律；仓库主要是技能与流程资产，不是独立运行时。

### Rank 09 - Pumpkin-MC/Pumpkin
- Repo URL: https://github.com/Pumpkin-MC/Pumpkin
- Tagline: 使用 Rust 编写、兼容 Minecraft Java Edition 的服务端实现。
- Stars: 9,787
- Stars Today: 358
- Forks: 660
- Language: Rust
- License: GPL-3.0
- Homepage: https://github.com/Pumpkin-MC/Pumpkin
- Topics: minecraft, server, rust, game-server, protocol
- 技术栈: Rust, Tokio, Minecraft protocol, world/chunk systems
- Why It Matters Today: 它用 Rust 探索传统 JVM 游戏服务端之外的性能与内存安全路线。
- 项目摘要: Pumpkin 实现 Minecraft Java Edition 的网络协议、玩家生命周期、世界和区块等服务端能力，目标是成为高性能替代实现。
- 核心特性:
  1. 原生 Rust 异步服务端。
  2. 覆盖登录、玩家、世界与网络协议。
  3. 面向插件和扩展继续建设。
- 适用场景: Minecraft 服务端研发、协议学习、Rust 游戏后端实验。
- 一句话推荐: 适合研究和试服，不适合现在就把十年老服连人带存档搬家。
- Evidence Notes: README、Cargo workspace 和源码模块；该项目已在 2026-07-24 报告中做过深入分析。
- Honest Caveat: 项目仍处于重度开发阶段，功能兼容性和生产稳定性需逐项验证。

### Rank 10 - permissionlesstech/bitchat
- Repo URL: https://github.com/permissionlesstech/bitchat
- Tagline: 同时支持离线 BLE mesh 与互联网 Nostr 的去中心化聊天应用。
- Stars: 28,956
- Stars Today: 1,720
- Forks: 4,404
- Language: Swift
- License: Unlicense / Public Domain
- Homepage: https://bitchat.free
- Topics: bluetooth, mesh, nostr, privacy, ios, macos
- 技术栈: Swift, Bluetooth LE, Noise Protocol, Nostr/NIP-17, LZ4, Keychain
- Why It Matters Today: 它把离线灾难通信、移动携带转发和互联网中继放在同一套消息路由里。
- 项目摘要: Bitchat 在设备附近使用 BLE mesh，在互联网可用时使用 Nostr；MessageRouter 根据可达性选择传输，并以持久 outbox、courier 和 relay mailbox 支持暂时离线的收件人。
- 核心特性:
  1. BLE 多跳与 Nostr 双传输。
  2. Noise/NIP-17 端到端加密。
  3. Store-and-forward、智能排队与 panic wipe。
- 适用场景: 灾害或活动现场通信、弱网社区聊天、去中心化消息协议研究。
- 一句话推荐: 想看“没网也能聊、有网就走远”的消息系统，这个项目很有拆解价值。
- Evidence Notes: README、WHITEPAPER v2、Package.swift 与测试目录说明 MessageRouter、Transport、outbox、courier 和安全设计。
- Honest Caveat: BLE 距离和元数据无法完全隐藏；白皮书明确指出离线 sealed mail 尚无前向保密，是重要权衡。

### Rank 11 - mattpocock/skills
- Repo URL: https://github.com/mattpocock/skills
- Tagline: 面向软件工程任务的可组合 Agent Skills 集合。
- Stars: 188,683
- Stars Today: 1,740
- Forks: 16,210
- Language: Shell
- License: MIT
- Homepage: https://github.com/mattpocock/skills
- Topics: agent-skills, typescript, engineering, workflows, ai-coding
- 技术栈: Markdown, Shell, coding-agent conventions
- Why It Matters Today: Skills 正在成为开发经验的可分发包装，而不是留在某个人的聊天记录里。
- 项目摘要: 该仓库把工程任务的操作步骤、约束和检查项整理为可组合 Skills，供编码 Agent 加载执行。
- 核心特性:
  1. 按工程任务拆分 Skill。
  2. 文档化输入、流程和验收。
  3. 便于团队复制和定制。
- 适用场景: 编码 Agent 能力扩展、团队工程规范复用、建立内部 Skill 库。
- 一句话推荐: 它不是新 IDE，而是给 Agent 准备的一摞靠谱工单模板。
- Evidence Notes: README、Skills 目录和 MIT 许可证。
- Honest Caveat: 主要是流程内容，不应把 Star 数解释为每个 Skill 都经过生产验证。

### Rank 12 - palmier-io/palmier-pro
- Repo URL: https://github.com/palmier-io/palmier-pro
- Tagline: Swift 原生 macOS 视频编辑器，允许用户和 Agent 通过时间线与 MCP 协同编辑。
- Stars: 12,336
- Stars Today: 412
- Forks: 897
- Language: Swift
- License: GPL-3.0（生成式 AI 处理为闭源服务）
- Homepage: https://palmier.io
- Topics: video-editor, macos, swift, mcp, ai-video
- 技术栈: Swift 6.2, SwiftUI/AppKit, MCP Swift SDK, Metal, MLX optional, Convex/Clerk optional
- Why It Matters Today: 它不是只让 AI 生成素材，而是让外部 Agent 通过本地 MCP 进入真实视频编辑时间线。
- 项目摘要: Palmier Pro 是 Apple Silicon 上的 Swift 原生视频编辑器。应用内包含时间线、预览、合成、导出和 Agent 工具层，并在 127.0.0.1:19789 暴露 MCP HTTP 服务。
- 核心特性:
  1. 原生时间线编辑和 Metal 合成。
  2. 本地 MCP 工具供 Claude/Codex/Cursor 调用。
  3. 可选生成式 AI、语音和遥测能力。
- 适用场景: AI 辅助视频剪辑、可编程时间线、Agent 驱动的媒体工作流。
- 一句话推荐: 想让 Agent 真正在时间线上动刀，而不是只在旁边提意见，可以重点看它。
- Evidence Notes: README、Package.swift、`Agent/MCP/MCPHTTPServer.swift`、Agent 与 Timeline 目录说明本地 MCP、会话管理和编辑模块。
- Honest Caveat: 仅支持 macOS 26 Apple Silicon；生成式 AI 处理并非全部开源且需要订阅；MCP 工具对本地项目有写权限，应限制客户端来源。

## Language Distribution

- Rust:
  - Count: 3
  - Percent: 25.0%
  - Color Hint: #DEA584
- Python:
  - Count: 2
  - Percent: 16.7%
  - Color Hint: #3572A5
- Shell:
  - Count: 2
  - Percent: 16.7%
  - Color Hint: #89E051
- Swift:
  - Count: 2
  - Percent: 16.7%
  - Color Hint: #F05138
- Other:
  - Count: 3（Go、JavaScript、Jupyter Notebook）
  - Percent: 25.0%
  - Color Hint: #8B949E

## Explore Highlights

### Explore 1
- Title: obra/superpowers
- URL: https://github.com/obra/superpowers
- Kind: Repository
- Meta: Agent Skills · Shell
- Short Reason: 与 Trending 重合，代表可组合 Agent 开发流程持续高热。

### Explore 2
- Title: Pumpkin-MC/Pumpkin
- URL: https://github.com/Pumpkin-MC/Pumpkin
- Kind: Repository
- Meta: Rust Minecraft server
- Short Reason: Rust 游戏服务端仍有明显社区关注。

### Explore 3
- Title: permissionlesstech/bitchat
- URL: https://github.com/permissionlesstech/bitchat
- Kind: Repository
- Meta: BLE mesh + Nostr
- Short Reason: 离线与互联网双传输消息架构值得研究。

### Explore 4
- Title: mattpocock/skills
- URL: https://github.com/mattpocock/skills
- Kind: Repository
- Meta: Agent Skills
- Short Reason: 工程经验继续以 Skill 形式产品化。

### Explore 5
- Title: palmier-io/palmier-pro
- URL: https://github.com/palmier-io/palmier-pro
- Kind: Repository
- Meta: Swift video editor + MCP
- Short Reason: 外部 Agent 进入原生创作工具的代表案例。

### Explore 6
- Title: CoreBunch/Instatic
- URL: https://github.com/CoreBunch/Instatic
- Kind: Repository
- Meta: Explore 补充项目
- Short Reason: 非 Trending Top 12 的额外发现入口。

### Explore 7
- Title: Lordog/dive-into-llms
- URL: https://github.com/Lordog/dive-into-llms
- Kind: Repository
- Meta: LLM learning
- Short Reason: 提供大模型学习材料，不纳入系统架构 Top 12。

### Explore 8
- Title: RyanCodrai/turbovec
- URL: https://github.com/RyanCodrai/turbovec
- Kind: Repository
- Meta: Explore 补充项目
- Short Reason: 作为当天 Explore 的额外技术线索。

## Rendering Notes

- Hero 主标题建议：GitHub Trending 日报
- Hero 副标题建议：Agent 进入真实工具执行层，Rust 与端侧系统同时升温
- Top 3 高亮原因：保留 GitHub 原始排名，不按 Stars Today 重排。
- 需要在 HTML 中诚实提示的降级点：Stars Today 为晚间动态快照；Explore 与 Trending 高度重合；性能和模型效果未独立复测。
- 不允许省略的区块：Header / Hero、4 张 Stats Cards、今日洞察、今日热门 Top 12、编程语言分布、GitHub Explore 精选、Footer。
- 必须保留的固定模板结构：主题切换按钮、固定 class、Top 3 克制高亮、Explore 紧凑列表。
- Top 详情固定顺序：项目摘要、核心特性、技术栈、适用场景、一句话推荐。
