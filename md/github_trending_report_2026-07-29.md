# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-07-29
- Generated At: 2026-07-29 晚间（Asia/Tokyo）
- Output Markdown: `md/github_trending_report_2026-07-29.md`
- Planned HTML: `html/github_trending_report_2026-07-29.html`
- Fixed Base Template: `.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html`
- User Rules: `.codex/skills/skill-github-trending-report/reference/user-rules.md`
- Sources:
  - [GitHub Trending · Repositories · Any language · Today](https://github.com/trending?since=daily)
  - [GitHub Explore](https://github.com/explore)
  - Top 12 仓库 README、About、许可证与公开源码
- Ranking Rule: 严格保留 GitHub Trending 页面原始顺序；累计 Stars 与 Stars Today 分开记录。

## Page Intent

- 今日主线：AI Agent 的“能做事”继续向“能说话、能被治理、能处理多媒体”扩展，同时浏览器端专业工具和成熟 CI 平台仍占有一席之地。
- 适合谁阅读：想快速发现开源项目的开发者、技术负责人、AI 工程师、工具链与平台工程团队。
- 页面重点：先看 Top 12 原始榜单和 Stars Today，再按需展开项目定位、适用场景与证据边界。
- 需要诚实降级说明的地方：Stars Today 是动态快照；AI 相关项目数是编辑分类；项目方性能、安全、兼容性与生产可用性主张未做独立复测。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：5,278（Stars Today 合计）
- 编程语言数：5
- AI 相关项目数：7（编辑分类，非 GitHub 官方标签）

## Editorial Insights

### Insight 1
- Title: 🎙️ Agent 从文字框走向实时语音与多媒体
- Body: `moeru-ai/airi`、`huggingface/speech-to-speech` 与 `bradautomates/claude-video` 分别覆盖实时语音伴侣、模块化语音代理后端和视频理解工作流。今天的共同信号不是“又多了几个聊天机器人”，而是 Agent 的输入输出边界正在从文本扩展到音频、视频和实时交互。

### Insight 2
- Title: 🛡️ 会调用工具之后，治理开始补课
- Body: `microsoft/agent-governance-toolkit` 把策略执行、身份、沙箱与审计放到模型之外的确定性代码路径中。Agent 连接数据库、邮件和系统工具之后，真正难的不是让它“更敢干”，而是让不该干的事在结构上干不了。

### Insight 3
- Title: 🏗️ 浏览器正在接管更重的专业工作
- Body: 排名第 1 的 `pascalorg/editor` 用 React Three Fiber 与 WebGPU 构建 3D 建筑编辑器；`opengeos/GeoLibre` 则把 GIS 可视化和分析带到浏览器、桌面、移动端和 Jupyter。浏览器不再只负责看页面，正逐渐承担 CAD、GIS 这类过去更依赖厚客户端的工作。

### Insight 4
- Title: 📈 今日热度高度集中，但老牌工程平台仍在场
- Body: Stars Today 前五名 `claude-video`、`airi`、`superfile`、`ECC`、`GeoLibre` 合计 3,690，占 Top 12 当日新增约 69.9%。与此同时，Jenkins 仍以原始第 2 名出现，说明热榜虽被 AI 和新工具抢镜，成熟自动化基础设施并没有退场。

## Top Projects

### Rank 01 - pascalorg/editor
- Repo URL: https://github.com/pascalorg/editor
- Tagline: 在浏览器中创建和分享 3D 建筑项目的编辑器。
- Stars: 19,196
- Stars Today: 341
- Forks: 2,560
- Language: TypeScript
- License: MIT
- Homepage: https://editor.pascal.app
- Topics: 3d-editor, architecture, webgpu, react-three-fiber, building-design
- 技术栈: React 19, Next.js 16, Three.js/WebGPU, React Three Fiber, Zustand, Zod, Zundo, Turborepo, Bun
- Why It Matters Today: 原始排名第 1；它把节点化建筑模型、增量几何更新和插件机制组合成浏览器内的专业 3D 编辑系统。
- 项目摘要: Pascal Editor 是一个面向建筑空间建模的 3D 编辑器。场景数据由节点构成，编辑器负责工具与选择交互，Viewer 负责渲染，系统组件只处理被标记为 dirty 的节点，减少不必要的几何重算。
- 核心特性:
  1. 用统一节点模型描述 Site、Building、Level、Wall、Slab、Zone、Item 等对象。
  2. 通过 scene registry 将节点 ID 映射到 Three.js 对象，几何系统可直接增量更新。
  3. IndexedDB 持久化与 Zundo 撤销/重做，配合插件接口扩展节点、渲染器、工具和面板。
- 适用场景: 浏览器端建筑概念设计、空间方案原型、可嵌入的 3D 建筑查看器，以及需要自定义节点插件的垂直工具。
- 一句话推荐: 想研究“浏览器如何扛起专业 3D 编辑器”，它比一摞宣传稿更有嚼头。
- Evidence Notes: README 明确给出 monorepo 分包、三套 Zustand Store、节点模型、registry、dirty-node 系统、事件总线和插件机制；根 `package.json` 给出 Turborepo/Bun 构建入口。
- Honest Caveat: 本次没有运行大型建筑模型，也没有独立验证 WebGPU 兼容性、复杂 CSG 性能和跨浏览器稳定性。

### Rank 02 - jenkinsci/jenkins
- Repo URL: https://github.com/jenkinsci/jenkins
- Tagline: 长期维护的可扩展自动化服务器与 CI/CD 平台核心。
- Stars: 26,181
- Stars Today: 180
- Forks: 9,704
- Language: Java
- License: MIT
- Homepage: https://www.jenkins.io
- Topics: ci, cd, automation-server, plugins, devops
- 技术栈: Java, Maven, Stapler, Jetty/Servlet, Plugin Architecture
- Why It Matters Today: 在一众 AI 新项目之间保持原始第 2，显示成熟工程基础设施仍有持续关注度。
- 项目摘要: Jenkins 通过核心服务加插件生态承载构建、测试、发布和运维自动化。它的优势不是“开箱即新”，而是长年积累的插件、权限、任务编排和部署经验。
- 核心特性:
  1. Pipeline 与任务执行模型覆盖从代码提交到发布的自动化链路。
  2. 插件机制连接 SCM、构建工具、云环境、通知和凭据系统。
  3. 支持控制器与代理节点分工，适配异构构建环境。
- 适用场景: 已有 Jenkins 资产的企业 CI/CD、需要大量历史插件集成的工程平台、受控内网自动化。
- 一句话推荐: 它不是热榜里的新面孔，但很多公司的发布按钮后面，还真站着这位老伙计。
- Evidence Notes: Trending 提供原始排名和动态指标；项目定位以 Jenkins 官方仓库与官网为准。
- Honest Caveat: 插件质量、升级路径和控制器安全边界差异很大，不能用核心项目成熟度替代具体部署审计。

### Rank 03 - moeru-ai/airi
- Repo URL: https://github.com/moeru-ai/airi
- Tagline: 可自托管、由用户掌控的实时语音 AI 伴侣与虚拟角色平台。
- Stars: 45,090
- Stars Today: 797
- Forks: 4,465
- Language: TypeScript
- License: MIT
- Homepage: https://airi.moeru.ai
- Topics: ai-companion, realtime-voice, virtual-character, self-hosted, desktop
- 技术栈: TypeScript, Web/Desktop Clients, Realtime Voice, LLM Integrations
- Why It Matters Today: Stars Today 位居全榜第二，说明“可拥有、可自托管的 AI 角色”仍是高热方向。
- 项目摘要: AIRI 试图把虚拟角色从聊天窗口带入实时语音、桌面和游戏互动。仓库自述支持 Web、macOS 与 Windows，并探索 Minecraft、Factorio 等环境中的交互。
- 核心特性:
  1. 面向实时语音的持续对话体验，而非一次一问一答。
  2. 强调自托管与用户拥有角色数据和运行环境。
  3. 将角色表现扩展到桌面和游戏交互场景。
- 适用场景: 虚拟主播原型、个人 AI 伴侣实验、实时语音角色应用与游戏交互研究。
- 一句话推荐: 想看 AI 伴侣怎么从“会聊天”长出声音、形象和行动能力，可以从这里下手。
- Evidence Notes: Trending 与仓库 About 确认实时语音、自托管、桌面平台和游戏交互定位；许可证文件为 MIT。
- Honest Caveat: 角色长期记忆、实时延迟、资源消耗与游戏控制可靠性未独立测试，不宜直接当作生产 SLA。

### Rank 04 - andrewyng/aisuite
- Repo URL: https://github.com/andrewyng/aisuite
- Tagline: 用统一接口调用多家生成式 AI 提供商。
- Stars: 15,785
- Stars Today: 62
- Forks: 1,663
- Language: Python
- License: MIT
- Homepage: https://github.com/andrewyng/aisuite
- Topics: llm, generative-ai, providers, python-sdk, unified-api
- 技术栈: Python, Provider Adapters, OpenAI-style Interface
- Why It Matters Today: 当模型供应商越来越多，减少调用层切换成本依旧是开发者的刚需。
- 项目摘要: aisuite 用相近的调用方式封装多家模型提供商，让应用在不重写上层业务代码的情况下切换模型或做对比实验。
- 核心特性:
  1. 统一客户端与消息结构，降低多供应商接入摩擦。
  2. 通过 provider adapter 隔离不同 SDK 与认证方式。
  3. 适合在同一实验脚本中快速比较模型输出。
- 适用场景: LLM 原型、模型 A/B 测试、多供应商容灾的前期验证和教学示例。
- 一句话推荐: 模型接口各唱各的调，它负责先把谱子翻到同一页。
- Evidence Notes: Trending 与官方仓库描述确认多提供商统一接口；许可证文件为 MIT。
- Honest Caveat: 统一接口通常只覆盖公共能力，供应商特有参数、工具调用细节、流式事件和错误语义仍需单独处理。

### Rank 05 - affaan-m/ECC
- Repo URL: https://github.com/affaan-m/ECC
- Tagline: 面向 Claude Code、Codex、OpenCode、Cursor 等 Agent 工具的技能、记忆、安全与研究优先工作体系。
- Stars: 235,184
- Stars Today: 636
- Forks: 35,822
- Language: JavaScript
- License: MIT
- Homepage: https://github.com/affaan-m/ECC
- Topics: agent-harness, skills, memory, security, developer-tools
- 技术栈: JavaScript, Markdown Skills, Agent Configuration, MCP-oriented Workflows
- Why It Matters Today: 累计 Stars 和当日增量都很高，反映开发者正把注意力从单次提示词转向可复用的 Agent 工作规范。
- 项目摘要: ECC 更接近一套 Agent harness 优化知识与配置体系，覆盖技能、记忆、安全和研究优先的开发方法，目标是让不同 AI 编程代理遵循更稳定的工程流程。
- 核心特性:
  1. 将常见开发流程沉淀为可复用技能和行为规范。
  2. 强调记忆管理、安全边界与研究后再实现。
  3. 面向多种编程 Agent，而非绑定单一客户端。
- 适用场景: 想标准化 AI 编程工作流的个人或团队、Agent 配置研究、技能库管理。
- 一句话推荐: 它更像一套“怎么带好 Agent 干活”的班规，不是另一个编译器或运行时。
- Evidence Notes: Trending 与 Explore 对其定位表述一致；许可证文件为 MIT。
- Honest Caveat: 仓库的高 Star 数不能直接证明技能对所有项目都有效；其主要价值偏方法、配置与资料组织，系统架构深度有限。

### Rank 06 - huggingface/speech-to-speech
- Repo URL: https://github.com/huggingface/speech-to-speech
- Tagline: 用开源模型搭建低延迟、可替换组件的实时语音代理后端。
- Stars: 7,545
- Stars Today: 227
- Forks: 978
- Language: Python
- License: Apache-2.0
- Homepage: https://github.com/huggingface/speech-to-speech
- Topics: voice-agent, vad, stt, llm, tts, realtime-api
- 技术栈: Python, PyTorch, Transformers, FastAPI/Uvicorn, WebSocket, OpenAI Realtime-compatible API
- Why It Matters Today: 它不是简单 Demo，而是把 VAD、STT、LLM、TTS 拆成可更换后端，并提供标准化实时接口。
- 项目摘要: Speech-to-Speech 是一个 VAD → STT → LLM → TTS 的级联语音管线。各阶段运行在线程中并通过队列连接，客户端可通过兼容 OpenAI Realtime 的 WebSocket 协议接入，也可使用本地音频、原始 WebSocket 或 TCP 模式。
- 核心特性:
  1. VAD、识别、语言模型和语音合成后端均可替换。
  2. 提供 `/v1/realtime` 接口、流式文本/音频事件和中断处理。
  3. 可接托管模型，也可连接 vLLM、llama.cpp 或本地 Transformers/MLX 后端。
- 适用场景: 机器人语音后端、实时语音助手、开源模型语音实验和 OpenAI Realtime 客户端的自托管替代。
- 一句话推荐: 语音 Agent 想换耳朵、换脑子、换嗓子，它把插槽都给你留好了。
- Evidence Notes: README 明确说明四段管线、线程与队列、运行模式和默认后端；`src/speech_to_speech/s2s_pipeline.py` 给出队列、PipelineUnit、RealtimeServer、CancelScope 与后端构建逻辑。
- Honest Caveat: 端到端延迟高度受模型、硬件、量化与网络影响；项目方生产使用说明不等同于本次独立压测。

### Rank 07 - virgiliojr94/book-to-skill
- Repo URL: https://github.com/virgiliojr94/book-to-skill
- Tagline: 把技术书 PDF 转成 Claude Code 可调用的 Skill。
- Stars: 12,051
- Stars Today: 423
- Forks: 1,376
- Language: Python
- License: 本次未确认
- Homepage: https://github.com/virgiliojr94/book-to-skill
- Topics: pdf, claude-code, skills, knowledge-extraction, developer-learning
- 技术栈: Python, PDF Processing, LLM-assisted Extraction, Claude Code Skills
- Why It Matters Today: 它把“读一本技术书”转换成可在工作流中随用随查的技能资产，符合 Agent 上下文工程趋势。
- 项目摘要: book-to-skill 面向技术 PDF，提取结构化知识并生成 Claude Code Skill，使书中概念能在开发过程中被检索和引用。
- 核心特性:
  1. 从 PDF 中提取章节与关键知识。
  2. 按 Skill 结构整理可引用内容。
  3. 将学习资料放进实际编码工作流，而不是停在阅读笔记里。
- 适用场景: 技术书学习、团队内部手册转 Skill、离线资料辅助编码。
- 一句话推荐: 书还是得读，它只是把“翻哪一页”这件事少折腾几回。
- Evidence Notes: Trending 与仓库公开描述确认 PDF → Claude Code Skill 的主路径。
- Honest Caveat: PDF 版权、扫描质量、图表/公式抽取和生成内容准确性需要用户自行核验。

### Rank 08 - opengeos/GeoLibre
- Repo URL: https://github.com/opengeos/GeoLibre
- Tagline: 可在浏览器、桌面、移动端和 Jupyter 运行的轻量云原生 GIS。
- Stars: 3,657
- Stars Today: 607
- Forks: 409
- Language: TypeScript
- License: MIT
- Homepage: https://geolibre.org
- Topics: gis, geospatial, browser, desktop, jupyter, cloud-native
- 技术栈: TypeScript, Web GIS, Desktop/Mobile Packaging, Jupyter Integration
- Why It Matters Today: 以 607 Stars Today 进入热度前五，浏览器内地理数据处理持续升温。
- 项目摘要: GeoLibre 试图用一套轻量 GIS 体验覆盖网页、桌面、移动设备和 Notebook，帮助用户可视化、探索与分析地理空间数据。
- 核心特性:
  1. 多运行形态共享地理数据查看和分析能力。
  2. 面向云端数据与浏览器交互，降低传统桌面 GIS 的使用门槛。
  3. 可嵌入 Jupyter 工作流，连接代码分析和交互地图。
- 适用场景: 教学、轻量空间分析、Notebook 可视化、跨设备地理数据浏览。
- 一句话推荐: GIS 不一定先装一大套桌面软件，先在浏览器里把地图摊开也能办正事。
- Evidence Notes: Trending 与仓库公开资料确认多端运行和 GIS 定位；此前同日报仓库已完成源码深度解析，本日不重复分析。
- Honest Caveat: 大数据集性能、坐标系覆盖、空间算法完整性与离线能力需按真实任务验证。

### Rank 09 - paperswithbacktest/awesome-systematic-trading
- Repo URL: https://github.com/paperswithbacktest/awesome-systematic-trading
- Tagline: 系统化交易的库、策略、书籍、博客与教程资源合集。
- Stars: 10,039
- Stars Today: 309
- Forks: 1,322
- Language: Python
- License: 本次未确认
- Homepage: https://github.com/paperswithbacktest/awesome-systematic-trading
- Topics: systematic-trading, quantitative-finance, resources, backtesting
- 技术栈: Markdown/Python ecosystem references
- Why It Matters Today: 量化交易学习与工具导航仍有稳定需求，但它是资源索引，不是一个可执行交易系统。
- 项目摘要: 该仓库整理系统化交易相关库、软件包、策略、书籍、博客和教程，适合做领域入口和资料筛选。
- 核心特性:
  1. 按主题聚合量化交易工具和阅读材料。
  2. 帮助新手快速建立术语和工具地图。
  3. 便于研究者发现回测、数据和策略资源。
- 适用场景: 量化交易资料导航、课程准备、工具选型前的信息搜集。
- 一句话推荐: 它是书架和路标，不是替你下单的交易员。
- Evidence Notes: Trending 明确将其描述为 curated list。
- Honest Caveat: 收录不代表背书；策略收益、数据质量和许可证必须逐项核验，不能把资源列表当投资建议。

### Rank 10 - microsoft/agent-governance-toolkit
- Repo URL: https://github.com/microsoft/agent-governance-toolkit
- Tagline: 在 Agent 工具调用前执行策略、身份、沙箱和审计控制的治理工具包。
- Stars: 5,392
- Stars Today: 46
- Forks: 854
- Language: Python
- License: MIT
- Homepage: https://microsoft.github.io/agent-governance-toolkit
- Topics: agent-governance, policy-engine, zero-trust, sandbox, compliance, ai-safety
- 技术栈: Python, Rust policy runtime, YAML/OPA/Cedar policies, SDKs for TypeScript/.NET/Rust/Go, MCP integrations
- Why It Matters Today: Agent 接入高权限工具后，确定性策略执行和可追责记录已从“加分项”变成上线门槛。
- 项目摘要: Agent Governance Toolkit 在模型意图抵达外部工具之前拦截动作，以策略引擎给出 allow、deny 或 require approval 决策。工具包还提供身份、执行隔离、可靠性与合规组件，但各层可按风险逐步启用。
- 核心特性:
  1. `govern()` 包装工具函数，每次调用前执行 YAML 策略并拒绝违规动作。
  2. Agent Control Specification 提供无状态、确定性、fail-closed 的策略决策运行时。
  3. 支持多语言 SDK、MCP 集成、合规验证和审计证据路径。
- 适用场景: 连接邮件、数据库、代码执行或企业 API 的 Agent；需要权限边界、审批和审计的多 Agent 系统。
- 一句话推荐: 提示词可以劝 Agent 讲规矩，治理层负责把门真锁上。
- Evidence Notes: README 给出官方 `govern()`、策略 YAML 和拒绝示例；`policy-engine` 文档说明 Rust 核心、Python bridge、主机快照与 fail-closed 语义。
- Honest Caveat: 项目处于 Public Preview，包整合与兼容层仍可能变化；同进程中间件不能替代操作系统级隔离。

### Rank 11 - yorukot/superfile
- Repo URL: https://github.com/yorukot/superfile
- Tagline: 面向终端的现代 TUI 文件管理器。
- Stars: 21,740
- Stars Today: 662
- Forks: 713
- Language: Go
- License: MIT
- Homepage: https://superfile.netlify.app
- Topics: cli, tui, file-manager, golang, terminal
- 技术栈: Go, Bubble Tea ecosystem, Terminal UI, Filesystem APIs
- Why It Matters Today: 662 Stars Today 位列全榜第三，说明本地效率工具仍能在 AI 热潮中抢到头排。
- 项目摘要: superfile 用终端界面提供多面板浏览、文件操作、搜索和快捷键工作流，目标是让重度命令行用户少在 `cd`、`cp`、`mv` 与脚本之间来回折腾。
- 核心特性:
  1. 多面板和键盘优先的文件浏览。
  2. 复制、移动、删除、搜索等常用文件操作集中在 TUI 中。
  3. 支持主题与配置，面向跨平台终端使用。
- 适用场景: 远程服务器、终端重度用户、开发环境中的快速文件整理。
- 一句话推荐: 命令行不等于只能盯着黑框背路径，它也能把文件收拾得挺利索。
- Evidence Notes: Trending 与 Explore 定位一致；该项目已在 2026-07-28 完成源码架构分析，本日不重复创建。
- Honest Caveat: 文件冲突、符号链接、权限和跨盘移动语义受操作系统影响，生产数据操作前应先备份并验证。

### Rank 12 - bradautomates/claude-video
- Repo URL: https://github.com/bradautomates/claude-video
- Tagline: 为 Claude 提供 `/watch` 视频下载、抽帧、转写和内容交接工作流。
- Stars: 12,448
- Stars Today: 988
- Forks: 1,237
- Language: Python
- License: MIT
- Homepage: https://github.com/bradautomates/claude-video
- Topics: claude-code, video, transcription, frames, skill
- 技术栈: Python, Video Downloading, Frame Extraction, Speech Transcription, Claude Code Skill
- Why It Matters Today: 988 Stars Today 为全榜最高，视频理解进入编程 Agent 工作流的需求十分直接。
- 项目摘要: claude-video 通过 `/watch` 命令获取视频，提取关键帧并转写音轨，再把整理后的视觉和文本材料交给 Claude 分析。
- 核心特性:
  1. 将视频下载、抽帧和转写串成一条可调用工作流。
  2. 把长视频转成模型更容易消费的图像与文本上下文。
  3. 面向 Claude Code 的 Skill 使用方式，降低手工预处理成本。
- 适用场景: 技术演示总结、课程视频笔记、产品录屏分析和故障录像初筛。
- 一句话推荐: 让 Claude 看视频之前，先有人把片子拆成它吃得下的盘子。
- Evidence Notes: Trending 与仓库公开描述确认 `/watch` 的下载、抽帧、转写和交接链路。
- Honest Caveat: 视频站点条款、版权、转写语言准确率、关键帧采样遗漏和大文件成本需逐项评估。

## Language Distribution

- Python:
  - Count: 6
  - Percent: 50.0%
  - Color Hint: #3572A5
- TypeScript:
  - Count: 3
  - Percent: 25.0%
  - Color Hint: #3178C6
- Java:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #B07219
- JavaScript:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #F1E05A
- Go:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #00ADD8

## Explore Highlights

### Explore 1
- Title: pascalorg/editor
- URL: https://github.com/pascalorg/editor
- Kind: Trending repository
- Meta: TypeScript · 3D 建筑编辑器
- Short Reason: 今日原始第 1，浏览器专业 3D 工具值得源码研究。

### Explore 2
- Title: moeru-ai/airi
- URL: https://github.com/moeru-ai/airi
- Kind: Trending repository
- Meta: TypeScript · 实时语音 AI 伴侣
- Short Reason: 当日增星 797，代表 AI 角色从文本向实时交互扩展。

### Explore 3
- Title: huggingface/speech-to-speech
- URL: https://github.com/huggingface/speech-to-speech
- Kind: Trending repository
- Meta: Python · 开源语音 Agent 后端
- Short Reason: VAD、STT、LLM、TTS 可替换，兼容 OpenAI Realtime API。

### Explore 4
- Title: microsoft/agent-governance-toolkit
- URL: https://github.com/microsoft/agent-governance-toolkit
- Kind: Trending repository
- Meta: Python/Rust · Agent 治理
- Short Reason: 把工具调用策略从提示词移到确定性执行层。

### Explore 5
- Title: React Native
- URL: https://github.com/topics/react-native
- Kind: Popular topic
- Meta: GitHub Explore 热门主题
- Short Reason: 作为跨平台移动开发生态补充，不参与 Trending 排名。

### Explore 6
- Title: Made in Brazil
- URL: https://github.com/collections/made-in-brazil
- Kind: GitHub Collection
- Meta: GitHub 官方精选集合
- Short Reason: 提供地域开源项目发现入口，不与 Top 12 混排。

### Explore 7
- Title: GitHub Checkout / The Download
- URL: https://github.com/explore
- Kind: GitHub editorial video
- Meta: GitHub 开发者与开源新闻
- Short Reason: 补充社区动态和 GitHub 产品更新。

### Explore 8
- Title: Explore staff recommendations
- URL: https://github.com/explore
- Kind: Staff recommendations
- Meta: PullFlow、Deploybot 等应用推荐入口
- Short Reason: 保留 Explore 的编辑精选属性，不把它包装成第二套榜单。

## Rendering Notes

- Hero 主标题建议：GitHub Trending 日报
- Hero 副标题建议：Agent 会说话、会看视频，也得先学会守规矩
- Top 3 高亮原因：严格按 GitHub Trending 原始排名高亮，不按累计 Stars 或 Stars Today 重新排序。
- 需要在 HTML 中诚实提示的降级点：Stars Today 为晚间动态快照；AI 项目数为编辑分类；性能与生产主张未独立复测。
- 不允许省略的区块：主题切换、Header/Hero、4 张 Stats Cards、今日洞察、Top 12、语言分布、Explore、Footer。
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

- Trending 数据直接来自 2026-07-29 晚间（Asia/Tokyo）的 GitHub Trending `Repositories / Any language / Today` 页面。
- 原始顺序从 `pascalorg/editor` 到 `bradautomates/claude-video`，未按累计 Stars 或 Stars Today 二次排序。
- 累计 Stars 与 Forks 是仓库累计指标；Stars Today 是 GitHub 页面给出的当日动态值。
- Explore 获取成功，内容与 Trending 有较高重合，故作为紧凑补充列表处理。
- Top 项目定位以仓库 README、About、许可证和公开源码为证据；证据不足处已在各项目 Honest Caveat 中说明。

## Honest Caveat

- GitHub Trending 是动态页面，同一日期不同时刻的 Stars、Stars Today 和顺序可能发生变化。
- GitHub 不公开完整排名算法，原始排名不能等同于质量、安全性或生产成熟度评分。
- “AI 相关项目数 7”是编辑分类，不是 GitHub 官方标签。
- 项目方披露的性能、兼容性、生产使用、安全覆盖或效果指标均未在本次任务中独立复测。
- 本日报用于技术观察和项目发现，不构成安全审计、投资建议或生产选型结论。
