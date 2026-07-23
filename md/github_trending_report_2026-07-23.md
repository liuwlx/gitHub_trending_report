# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-23
- Generated At: 2026-07-23 21:06 JST
- Output Markdown: md/github_trending_report_2026-07-23.md
- Planned HTML: html/github_trending_report_2026-07-23.html
- Fixed Base Template: .codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html
- User Rules: .codex/skills/skill-github-trending-report/reference/user-rules.md
- Data Scope: GitHub Trending · Repositories · Any language · Today
- Sources:
  - https://github.com/trending
  - https://github.com/explore
  - Repo README / About / Homepage / Release / source files
  - GitHub 公开仓库元数据与官方文档

## Page Intent

- 今日主线：今天的榜单一头是 WiFi 空间感知、AI 语音、模型路由和金融基础模型，另一头是安全文件传输、架构即代码与 Apollo 11 历史源码。AI 仍占主场，但真正能长期留下来的项目，仍要靠协议、工具链和工程边界撑腰。
- 适合谁阅读：关注 AI 工程、开发工具、系统软件、架构治理与开源基础设施的软件工程师、架构师和技术负责人。
- 页面重点：严格保留 GitHub Trending 原始 Top 12 顺序，单独列出累计 Stars 与 Stars Today；日报负责扫读，3 个独立技术档案负责源码级深挖。
- 需要诚实降级说明的地方：Trending 排名算法未公开；Stars Today 是动态页面快照；RuView、OmniRoute、Kronos 等项目方公布的性能或效果数字没有在本次任务中独立复测；资源合集和模型研究仓库不按完整生产系统口径评价。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：12,290
- 编程语言数：5
- AI 相关项目数：8

## Editorial Insights

### Insight 1
- Title: WiFi 感知把“无线网络”变成了传感器
- Body: `RuView` 不把 WiFi 只当通信介质，而是读取 Channel State Information，推断存在、运动、呼吸与心率。它的高热度说明边缘感知正在从摄像头和可穿戴设备之外寻找新入口；不过涉及生命体征与安全判断时，项目自测数据和实际医疗、养老场景之间还有很长一段路。

### Insight 2
- Title: 越基础的工具，越容易穿过技术潮流
- Body: `croc` 解决的是一个不时髦但天天有人遇到的问题：两台电脑怎样不用端口转发、安全传文件，并在断线后继续。PAKE、Relay、端到端加密和断点续传，比一句“AI 原生”少了锣鼓，多了能干活的螺丝钉。

### Insight 3
- Title: 架构文档开始从“画图”变成“可执行模型”
- Body: `LikeC4` 把架构写成文本模型，再由语言服务、布局与前端工具生成实时图、静态站点、React 组件和多种导出格式。架构图不再只是会议前临时画一张，而可以跟代码一起版本化、校验和评审。

### Insight 4
- Title: 今日高增量项目的风险边界差异很大
- Body: `OmniRoute` 涉及账号配额与模型路由，`Kronos` 涉及金融模型，`voicebox` 涉及语音生成，`RuView` 涉及空间与生命体征推断。Stars Today 只能说明注意力在聚集，不能自动证明数据授权、隐私、安全、效果或生产稳定性已经过关。

## Top Projects

### Rank 01 - koala73/worldmonitor
- Repo URL: https://github.com/koala73/worldmonitor
- Tagline: 实时全球情报仪表盘，把地缘政治、市场、航空、海事、网络安全与气候数据整合进统一地图和专业面板。
- Stars: 70,039
- Stars Today: 4,139
- Forks: 10,642
- Language: TypeScript
- License: AGPL-3.0-only
- Homepage: https://worldmonitor.app
- Topics: agent, osint, news, ai, monitoring, dashboard, mcp, geopolitics
- 技术栈: TypeScript, Vite, MapLibre, deck.gl, globe.gl, Tauri 2, Vercel Edge, Railway, Redis, Protocol Buffers, Web Workers, ONNX
- Why It Matters Today: 连续高位并大幅增星，说明开发者对统一态势感知、多源数据组织和 Agent 可调用情报接口的需求仍在上升。
- 项目摘要: World Monitor 是一套浏览器与桌面端全球情报工作台。它把多种公开数据源经过边缘 API、Relay 与缓存整理后，展示在地图、三维地球和专业面板中，并通过 MCP、CLI、SDK 和结构化 API 向自动化分析流程开放。
- 核心特性:
  1. 统一展示新闻、冲突、市场、航班、船舶、基础设施和网络威胁等多域数据。
  2. 提供平面地图、三维地球、专业面板和桌面端运行形态。
  3. 通过边缘函数、Relay、Redis 与智能轮询缓冲外部数据源的延迟和抖动。
  4. 提供 MCP、CLI、SDK 与本地模型能力，便于接入 Agent 工作流。
- 适用场景: OSINT 与风险观察、企业态势看板、多源新闻和市场事件交叉分析、Agent 获取结构化全球事件上下文。
- 一句话推荐: 想研究“几十种外部数据怎样收进一张还能操作的地图”，它仍是今天最先该点开的系统。
- Evidence Notes: 仓库 `ARCHITECTURE.md`、前端入口、Edge Functions、Relay、Redis、Tauri、Proto/RPC 与数据播种说明共同支持其多层架构；该项目已在此前日报完成独立架构解析。
- Honest Caveat: 外部数据源的授权、覆盖、延迟和准确性并不一致；统一界面不能消除源数据偏差，项目列出的功能数量也未做独立全量核验。

### Rank 02 - ruvnet/RuView
- Repo URL: https://github.com/ruvnet/RuView
- Tagline: 把 ESP32 采集的 WiFi CSI 信号转成存在、运动、姿态和生命体征估计的边缘空间感知平台。
- Stars: 84,352
- Stars Today: 741
- Forks: 11,280
- Language: Rust
- License: MIT；Rust workspace 包声明 MIT OR Apache-2.0
- Homepage: https://github.com/ruvnet/RuView
- Topics: wifi, csi, sensing, edge-ai, densepose, esp32, smart-home
- 技术栈: Rust, Tokio, Axum, UDP, WebSocket, MQTT, ESP32 CSI, rustfft, ndarray, Candle/ORT, Web UI, Home Assistant/Matter
- Why It Matters Today: 它把低成本 WiFi 硬件、实时信号处理、边缘推理和智能家居集成装进同一系统，是今日最值得追源码的数据采集—推理—发布链路。
- 项目摘要: RuView 通过 ESP32 采集 WiFi Channel State Information，由 Rust sensing server 在本地解析、处理和推断，再通过 WebSocket、REST、MQTT 或智能家居桥接输出存在、运动、呼吸、心率等状态。核心 sensing path 被明确设计为实时系统，不依赖数据库持久化。
- 核心特性:
  1. UDP 接收 ESP32 CSI 帧，结合信号处理、模型推理和追踪生成实时 sensing update。
  2. WebSocket 向本地 UI 推送结果，并可选通过 MQTT/Home Assistant 与 Matter 暴露状态。
  3. 支持模拟数据、真实 ESP32、模型容器、校准、多节点融合与边缘模块。
  4. 采用 Rust workspace 拆分 core、signal、NN、hardware、vitals、server 和 desktop 等能力。
- 适用场景: 非摄像头房间占用检测、边缘传感研究、智能家居状态输入、WiFi CSI 算法验证；医疗或安全关键用途只能在严格验证后尝试。
- 一句话推荐: 它把“路由器旁边那团看不见的电波”做成了一条可读、可推送、可集成的实时数据管线。
- Evidence Notes: `v2/Cargo.toml` 明确列出 workspace crates，并说明 sensing server 提供 REST/WS、当前实时路径无持久状态；`v2/crates/wifi-densepose-sensing-server/src/main.rs` 明确写出 UDP 5005、WS 8765、UI 8080 和 Axum/Tokio 广播链路。
- Honest Caveat: 呼吸、心率、姿态和穿墙范围等结果高度依赖环境、硬件、校准和数据分布；README 中的准确率、速度和规模数字属于项目方报告，本次未独立复测，不应直接当作医疗或安防认证。

### Rank 03 - ayghri/i-have-adhd
- Repo URL: https://github.com/ayghri/i-have-adhd
- Tagline: 为 Claude Code、Codex 等编码 Agent 提供“先行动、少绕弯、步骤编号”的输出风格 Skill。
- Stars: 8,722
- Stars Today: 1,699
- Forks: 398
- Language: Python
- License: MIT
- Homepage: https://github.com/ayghri/i-have-adhd
- Topics: coding-agent, skill, claude-code, codex, accessibility, productivity
- 技术栈: Markdown Skill, Claude Code plugin, Codex plugin, Agent instruction rules
- Why It Matters Today: 高增星说明用户对 AI 助手的痛点已经从“能不能回答”转向“回答能不能立刻执行、别把结论埋在棉花里”。
- 项目摘要: 这是一个编码 Agent 输出规范 Skill，而不是独立运行时。它通过十条规则约束回答顺序、列表长度、错误表达、状态复述和下一步动作，让长篇、客套和支线更少。
- 核心特性:
  1. 先给下一步行动，再补必要解释。
  2. 多步骤任务编号，并以一个明确下一步收尾。
  3. 限制支线与列表长度，强调错误和进展的可见性。
- 适用场景: 容易被长回答淹没的编码会话、团队统一 Agent 沟通风格、无障碍与注意力友好输出实验。
- 一句话推荐: 它不是给 Agent 加新脑子，而是教它少铺垫、先把扳手递过来。
- Evidence Notes: README 提供 Claude Code 与 Codex 安装路径、十条规则及前后对比；规则正文位于 `skills/i-have-adhd/SKILL.md`。
- Honest Caveat: 这是提示与交互规范，不是完整软件架构；“ADHD-friendly”是一种输出设计取向，不构成医学诊断或临床有效性声明。

### Rank 04 - schollz/croc
- Repo URL: https://github.com/schollz/croc
- Tagline: 使用 Relay 与 PAKE，在两台电脑之间完成端到端加密、跨平台、可断点续传的文件或目录传输。
- Stars: 37,934
- Stars Today: 739
- Forks: 1,503
- Language: Go
- License: MIT
- Homepage: https://getcroc.schollz.com
- Topics: file-transfer, encryption, p2p, relay, cli, cross-platform
- 技术栈: Go, TCP relay, PAKE, x/crypto, chunk transfer, reconnect/resume, peer discovery, proxy support
- Why It Matters Today: 它解决的不是新概念，而是跨网络安全传文件的高频难题；Relay、密钥协商、分块和重连状态让它具备很清楚的系统主线。
- 项目摘要: Croc 是一个 CLI 文件传输工具。发送端生成或指定短语，收发双方通过 Relay 会合并使用 PAKE 建立共享密钥，随后交换文件元数据、按块加密传输，并在中断时按缺失范围继续。
- 核心特性:
  1. 无需本地服务器和端口转发，通过 Relay 让任意两台电脑会合。
  2. 使用密码认证密钥交换建立端到端加密通道，Relay 不需要拿到明文密钥。
  3. 支持多文件、目录、文本、管道、代理、自托管 Relay 和中断续传。
- 适用场景: 临时跨网络传文件、远程支持、跨平台设备交换数据、自托管安全传输；长期大规模分发仍应评估专用对象存储和权限体系。
- 一句话推荐: 想看一个“小工具怎样把密码学、网络会合和断点续传串成一条完整业务链”，Croc 很适合下刀解剖。
- Evidence Notes: README 明确描述 Relay、PAKE、E2E 加密、续传与自托管；`src/croc/croc.go` 的 `Client` 显式维护安全通道、元数据、请求、传输、关闭五阶段以及 chunk/reconnect 状态。
- Honest Caveat: 安全仍依赖短语强度、终端环境和 Relay 配置；在类 Unix 系统中把短语直接放进进程参数可能泄漏，README 已建议使用 `CROC_SECRET` 环境变量。

### Rank 05 - likec4/likec4
- Repo URL: https://github.com/likec4/likec4
- Tagline: 用可版本化文本模型描述软件架构，并生成实时图、静态站点、React 组件和多种导出格式。
- Stars: 4,465
- Stars Today: 80
- Forks: 308
- Language: TypeScript
- License: MIT
- Homepage: https://likec4.dev
- Topics: architecture-as-code, c4-model, diagrams, dsl, vscode, mcp
- 技术栈: TypeScript, Langium, language server, Vite, React, Graphviz/Dagre, Chokidar, CLI, VS Code, MCP
- Why It Matters Today: 它把架构文档从静态图片升级成可解析、可校验、可热更新和可复用的工程资产，适合团队治理和代码评审场景。
- 项目摘要: LikeC4 是一门架构建模语言和配套工具链。CLI 递归查找 `.c4`/`.likec4` 文件，语言服务解析并验证模型，布局与前端组件生成交互图；同一模型还可构建静态站点、导出多种格式、生成 React 组件或通过 MCP/API 查询。
- 核心特性:
  1. 自定义元素类型、关系和任意嵌套层级，不被固定 C4 层次绑死。
  2. 本地 serve 模式支持源码变更后浏览器热更新。
  3. 可输出静态网站、PNG、JSON、Mermaid、Dot、D2、PlantUML 和 DrawIO。
  4. 提供 VS Code、Vite Plugin、React codegen、API 与 MCP server。
- 适用场景: 架构即代码、系统景观图、评审和审计、文档站点、在产品或内部平台中嵌入架构视图。
- 一句话推荐: 它想让架构图像代码一样能 diff、能校验、能跑起来，而不是会议结束后躺进 PPT 冰箱。
- Evidence Notes: `packages/likec4/README.md` 明确描述扫描、解析、热更新、构建与导出；`packages/likec4/package.json` 指向 `src/cli/index.ts`、language services、core、layouts、React、Vite 与 MCP 依赖。
- Honest Caveat: 图是否“始终最新”仍依赖团队维护模型和 CI 约束；它不会自动从所有真实运行依赖中无损反推出架构。

### Rank 06 - chrislgarry/Apollo-11
- Repo URL: https://github.com/chrislgarry/Apollo-11
- Tagline: Apollo 11 指令舱 Comanche055 与登月舱 Luminary099 的原始 AGC 汇编源码转录归档。
- Stars: 70,795
- Stars Today: 768
- Forks: 7,897
- Language: Assembly
- License: Public domain
- Homepage: https://www.ibiblio.org/apollo
- Topics: apollo, nasa, agc, assembly, history, space
- 技术栈: AGC Assembly, yaYUL assembler, Virtual AGC tooling
- Why It Matters Today: 历史源码重新上榜，说明开发者仍愿意从真实、资源极度受限的系统中学习工程取舍，而不只追最新框架。
- 项目摘要: 该仓库保存 Apollo 11 指令舱和登月舱 Guidance Computer 的原始源码转录。它的重点是历史保存、校对和研究；编译与模拟通常借助 Virtual AGC 项目完成。
- 核心特性:
  1. 收录 Comanche055 与 Luminary099 两套任务源码。
  2. 依据 MIT Museum 扫描件进行转录和差异校对。
  3. 提供多语言 README、历史审批信息和 Virtual AGC 编译入口。
- 适用场景: 计算机历史研究、航天软件教育、汇编与受限计算环境学习、数字保存。
- 一句话推荐: 这不是“复古皮肤”，是人类真的靠它去了月球的代码档案。
- Evidence Notes: README 明确说明两套 AGC 源码、数字化来源、yaYUL assembler 与 Public domain 状态。
- Honest Caveat: 这是历史源码归档，不按现代依赖管理、安全更新和生产部署标准维护；不能直接把其工程模式搬到今天系统。

### Rank 07 - jamiepine/voicebox
- Repo URL: https://github.com/jamiepine/voicebox
- Tagline: 开源 AI 语音工作室，用于语音克隆、文本转语音、项目管理和本地或远程推理工作流。
- Stars: 46,039
- Stars Today: 557
- Forks: 5,618
- Language: TypeScript
- License: MIT
- Homepage: https://github.com/jamiepine/voicebox
- Topics: text-to-speech, voice-cloning, ai-audio, studio, local-ai
- 技术栈: TypeScript, desktop/web UI, TTS model adapters, audio pipeline, local/remote inference
- Why It Matters Today: 生成式语音从脚本和 Demo 走向可管理项目、素材和多模型后端的工作台，说明用户开始要求完整制作流程。
- 项目摘要: Voicebox 面向需要生成、管理和编辑 AI 语音内容的用户，把模型调用、声音配置、文本项目和音频输出集中在统一工作室界面中。
- 核心特性:
  1. 管理语音、文本和生成项目，而不是只提供单次 API 调用。
  2. 支持语音克隆和多种推理后端的工作流整合。
  3. 通过可视界面降低音频模型的安装、参数和素材管理负担。
- 适用场景: 播客和视频配音、游戏原型、无障碍朗读、语音模型评估；涉及他人声音时必须处理授权和标识。
- 一句话推荐: 它把“跑一次 TTS”扩展成了真正能整理素材和反复制作的语音工作台。
- Evidence Notes: 仓库 About、README 与发布物将项目定位为开源 AI voice studio，并公开 MIT 许可证。
- Honest Caveat: 声音克隆可能涉及肖像、版权、欺诈和平台政策；模型质量、延迟与硬件要求因后端而异，本次未独立测试。

### Rank 08 - diegosouzapw/OmniRoute
- Repo URL: https://github.com/diegosouzapw/OmniRoute
- Tagline: 为多种 AI Provider 统一请求、账号配额、故障切换和上下文压缩的本地网关。
- Stars: 25,949
- Stars Today: 1,651
- Forks: 3,410
- Language: TypeScript
- License: MIT
- Homepage: https://github.com/diegosouzapw/OmniRoute
- Topics: ai-gateway, proxy, llm, rate-limit, failover, context-compression
- 技术栈: TypeScript, local gateway, provider adapters, account pool, retry/failover, streaming, context compression
- Why It Matters Today: 当开发者同时使用多个模型和账号时，真正痛点变成配额、兼容、流式返回和失败切换，OmniRoute 正好站在这个控制面上。
- 项目摘要: OmniRoute 在客户端和多个模型提供方之间提供统一入口，负责请求适配、目标选择、账号状态、速率限制、故障切换与可选上下文压缩，使上层工具不必分别处理每个 Provider 的差异。
- 核心特性:
  1. 统一不同 AI Provider 的调用接口和流式响应。
  2. 根据配额、冷却和错误状态切换账号或备用模型。
  3. 提供上下文压缩与请求路由，降低重复上下文成本。
- 适用场景: 多 Provider 开发环境、本地 AI 网关、模型可用性实验；企业生产使用需审查凭据和上游条款。
- 一句话推荐: 模型越来越多，它做的是总机：哪条线忙、哪张卡没额度，先别让业务跟着一起掉线。
- Evidence Notes: README、配置和源码公开了 Provider adapters、账号池、冷却、流式代理与压缩路径；此前独立解析已追踪 429 后切换流程。
- Honest Caveat: Provider 数量、免费额度与压缩比例属于项目方口径；账号聚合和自动切换可能触及上游服务条款，生产使用前应进行合规与密钥管理评估。

### Rank 09 - shiyu-coder/Kronos
- Repo URL: https://github.com/shiyu-coder/Kronos
- Tagline: 面向金融 K 线序列的基础模型与研究工具，尝试从历史市场数据学习通用表示并支持预测任务。
- Stars: 32,749
- Stars Today: 137
- Forks: 5,622
- Language: Python
- License: MIT
- Homepage: https://github.com/shiyu-coder/Kronos
- Topics: finance, foundation-model, time-series, forecasting, quantitative-research
- 技术栈: Python, PyTorch, Transformer/time-series model, financial datasets, pretrained weights, evaluation notebooks
- Why It Matters Today: 金融时间序列基础模型仍有强关注度，但它的价值必须通过时间切分、交易成本和跨市场验证，而不是看一次回测图。
- 项目摘要: Kronos 是金融市场序列建模研究项目，提供预训练模型、推理和评估工具，目标是让同一表示适配多类 K 线或市场预测任务。
- 核心特性:
  1. 面向 OHLCV 等金融序列训练通用模型表示。
  2. 提供预训练权重、推理接口和研究示例。
  3. 支持不同市场、周期和下游任务的实验比较。
- 适用场景: 金融时间序列研究、特征提取、预测基线与模型比较；不适合作为未经验证的自动交易信号直接上线。
- 一句话推荐: 可以把它当研究发动机，别把 README 的马力表直接当明天的收益曲线。
- Evidence Notes: 仓库 README、代码与模型发布资料将其定位为金融市场基础模型，并提供 Python 推理与研究流程。
- Honest Caveat: 预测效果对数据泄漏、市场阶段、手续费和执行延迟极敏感；本次未复现实验，也不构成投资建议。

### Rank 10 - ComposioHQ/awesome-claude-skills
- Repo URL: https://github.com/ComposioHQ/awesome-claude-skills
- Tagline: Claude Skills 的精选目录、模板和使用资料，帮助用户发现可复用的 Agent 工作流。
- Stars: 69,028
- Stars Today: 163
- Forks: 7,824
- Language: Python
- License: Apache-2.0（目录内第三方 Skill 可能采用不同许可证）
- Homepage: https://github.com/ComposioHQ/awesome-claude-skills
- Topics: claude, skills, agents, awesome-list, automation, composio
- 技术栈: Markdown catalog, Python examples, Claude Skills, Agent integrations
- Why It Matters Today: Agent 能力分发正在形成“插件目录”，但目录的价值在筛选和发现，不等同于每个条目都经过安全审核。
- 项目摘要: 这是 Claude Skills 的资源集合和入口索引，按用途整理可安装或参考的技能、模板与集成示例，更接近目录而非统一运行时。
- 核心特性:
  1. 按场景收录和分类 Claude Skills。
  2. 提供安装、示例和第三方项目入口。
  3. 帮助团队快速比较可复用 Agent 工作流。
- 适用场景: Skill 发现、Agent 工作流调研、团队能力目录建设；不适合作为“全部已审计”的安全白名单。
- 一句话推荐: 这是工具市场的地图，不是每家店都替你验过后厨。
- Evidence Notes: 仓库结构和 README 明确属于 curated awesome list，因此本次不纳入源码架构深挖。
- Honest Caveat: 第三方 Skill 的权限、依赖、维护状态和许可证各不相同，安装前应逐项审阅源码和配置。

### Rank 11 - oblien/openship
- Repo URL: https://github.com/oblien/openship
- Tagline: 把仓库识别、构建、容器部署、域名、证书、数据库与备份整合进自托管控制面。
- Stars: 7,556
- Stars Today: 1,302
- Forks: 558
- Language: TypeScript
- License: Apache-2.0
- Homepage: https://github.com/oblien/openship
- Topics: self-hosted, deployment, paas, docker, devops, desktop
- 技术栈: TypeScript, desktop/web UI, CLI, containers, build queue, SSE, deployment orchestration
- Why It Matters Today: 高增星说明开发者仍希望把零散脚本和云平台费用收拢成一条可控、自托管的交付链路。
- 项目摘要: Openship 是面向开发者的自托管部署平台，尝试从代码仓库识别项目、生成构建与运行配置，管理容器、环境变量、域名、证书、数据服务和部署状态，并通过桌面端、Web 与 CLI 统一操作。
- 核心特性:
  1. 从仓库到构建、容器启动和域名接入形成连续部署流程。
  2. 提供桌面端、Web 控制台与 CLI 多入口。
  3. 通过任务状态和 SSE 反馈构建、部署及失败信息。
- 适用场景: 小团队自托管 PaaS、内网工具部署、个人服务器和开发测试环境；关键生产负载需先验证升级、备份和故障恢复。
- 一句话推荐: 它想把“SSH 上去敲一晚命令”改成一条能重复、能看状态的流水线。
- Evidence Notes: README、命令入口和源码已在前日报解析中追踪创建部署、排队构建、容器操作和 SSE 状态路径。
- Honest Caveat: 平台覆盖面不等于每种数据库、云环境和故障模式都成熟；生产使用需验证权限隔离、备份恢复、滚动升级和供应链安全。

### Rank 12 - agegr/pi-web
- Repo URL: https://github.com/agegr/pi-web
- Tagline: 为 Pi coding agent 提供浏览器界面，让用户在 Web 中管理会话、工具调用和编码任务。
- Stars: 2,175
- Stars Today: 314
- Forks: 315
- Language: TypeScript
- License: MIT
- Homepage: https://github.com/agegr/pi-web
- Topics: coding-agent, web-ui, ai, developer-tools, pi
- 技术栈: TypeScript, Web UI, agent session integration, streaming events, tool-call rendering
- Why It Matters Today: CLI Agent 开始向可视化会话、远程访问和结构化工具状态扩展，Web UI 正成为编码 Agent 的第二入口。
- 项目摘要: Pi Web 是 Pi coding agent 的 Web 前端和会话入口，把消息、流式输出、工具调用及任务状态从终端搬到浏览器，适合希望在不同设备或更可视界面中使用 Agent 的开发者。
- 核心特性:
  1. 在浏览器中展示 Agent 消息、流式内容和工具调用。
  2. 管理编码会话与任务状态，减少对单一终端窗口的依赖。
  3. 复用 Pi Agent 能力，而不是重新实现模型和工具执行核心。
- 适用场景: 可视化编码 Agent、远程或多设备访问、演示和会话观察；暴露到公网前必须做好认证和执行权限隔离。
- 一句话推荐: 它给终端里的 Agent 开了一扇窗，窗户好看不难，锁得牢才是真功夫。
- Evidence Notes: 仓库 About、README 和源码结构将其定位为 Pi coding agent Web UI，许可证为 MIT。
- Honest Caveat: Web 暴露会扩大本地文件、工具和凭据的攻击面；本次未验证其认证、沙箱和多用户隔离是否满足公网生产要求。

## Language Distribution

- TypeScript:
  - Count: 6
  - Percent: 50.0%
  - Color Hint: #3178C6
- Python:
  - Count: 3
  - Percent: 25.0%
  - Color Hint: #3572A5
- Rust:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #DEA584
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
- Title: koala73/worldmonitor
- URL: https://github.com/koala73/worldmonitor
- Kind: Repository
- Meta: 全球情报仪表盘 · Trending #1
- Short Reason: 多源实时数据、地图与 Agent 接口继续获得集中关注。

### Explore 2
- Title: ruvnet/RuView
- URL: https://github.com/ruvnet/RuView
- Kind: Repository
- Meta: WiFi CSI 空间感知 · Trending #2
- Short Reason: 边缘感知、生命体征和智能家居集成让它具备完整系统研究价值。

### Explore 3
- Title: ayghri/i-have-adhd
- URL: https://github.com/ayghri/i-have-adhd
- Kind: Repository
- Meta: Agent 输出风格 Skill · Trending #3
- Short Reason: 用户开始主动治理 AI 回答的信息密度和可执行性。

### Explore 4
- Title: schollz/croc
- URL: https://github.com/schollz/croc
- Kind: Repository
- Meta: 安全文件传输 · Trending #4
- Short Reason: Relay、PAKE、E2E 和续传组成清晰、成熟的工程链路。

### Explore 5
- Title: likec4/likec4
- URL: https://github.com/likec4/likec4
- Kind: Repository
- Meta: Architecture as Code · Trending #5
- Short Reason: 可版本化架构模型和实时图适合团队治理与评审。

### Explore 6
- Title: CSS
- URL: https://github.com/topics/css
- Kind: Topic
- Meta: GitHub Explore Topic
- Short Reason: 作为当天 Explore 的主题补充入口，不参与 Trending 排名。

## Rendering Notes

- Hero 主标题建议：GitHub Trending 日报
- Hero 副标题建议：WiFi 感知、加密传输和架构即代码一起上桌：今天不只看谁火，还看谁的系统真能跑
- Top 3 高亮原因：保持 GitHub 原始排名 1–3 的固定高亮，不按照 Stars Today 重排。
- 需要在 HTML 中诚实提示的降级点：Stars Today 为 2026-07-23 晚间动态快照；性能、准确率、金融效果和 Provider 能力均未独立复测。
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
- 当日深度解析候选：ruvnet/RuView、schollz/croc、likec4/likec4。
