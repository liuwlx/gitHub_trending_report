# GitHub Trending 日报内容底稿

## Meta

- Report Date: 2026-08-02
- Generated At: 2026-08-02 21:08:00 Asia/Tokyo
- Output Markdown: `md/github_trending_report_2026-08-02.md`
- Planned HTML: `html/github_trending_report_2026-08-02.html`
- Fixed Base Template: `.codex/skills/skill-github-trending-report/reference/fixedBaseTemplate_2026-03-16.html`
- User Rules: `.codex/skills/skill-github-trending-report/reference/user-rules.md`
- Sources:
  - GitHub Trending — Repositories / Any language / Today
  - GitHub Explore
  - Repo README / About / dependency manifests / official documentation
- Ranking rule: 以下 Top 12 严格保留抓取时 GitHub Trending 的原始顺序。
- Metric rule: `Stars` 是累计收藏数，`Stars Today` 是 GitHub 当日趋势页展示的新增收藏数，两者不得混用。

## Page Intent

- 今日主线：教育内容、AI 工具与成熟基础设施同时上榜；增速冠军是安全技能路由包，但真正适合源码深挖的项目集中在 CLI、Web 服务和本地多媒体流水线。
- 适合谁阅读：想快速判断项目价值的开发者、技术负责人、开源项目研究者。
- 页面重点：先看原始排名和 Stars Today，再看项目是否是可运行系统、课程资源还是模型研究代码。
- 需要诚实降级说明的地方：GitHub Trending 会在一天内动态变化；Explore 与 Trending 高度重合；项目性能、安全和生产可用性均未独立复测。

## Stats

- Trending 项目数：12
- 今日累计新增 Stars：4,920
- 编程语言数：7
- AI 相关项目数：7（编辑分类，不是 GitHub 官方标签）

## Editorial Insights

### Insight 1
- Title: 教程内容仍有强大的“入口效应”
- Body: `AI-For-Beginners` 与 `generative-ai-for-beginners` 都进入 Top 5。它们的优势不是新模型，而是把复杂知识拆成可以连续学习的课程。热榜说明很多读者今天需要的不是再来一个框架，而是一张能走得通的地图。

### Insight 2
- Title: 今日增速第一不是应用，而是工作流路由包
- Body: `reverse-skill` 获得 1,320 Stars Today，明显高于其他项目。它把逆向、安全研究的流程、工具检查和证据记录整理成可供 AI 编程客户端使用的技能路由；价值主要在方法编排，不应把它误解为一个自动完成所有安全任务的独立平台。

### Insight 3
- Title: 开发协作工具正在把“隐性流程”产品化
- Body: `gh-stack` 把堆叠分支、逐层 PR、重定基和远端同步做成 GitHub CLI 扩展；`Kaneo` 则强调轻量、自托管项目管理。前者治理代码变更链，后者治理工作项，都是在减少团队靠口头约定维持秩序的成本。

### Insight 4
- Title: 本地 AI 的门槛正在从模型转向工程集成
- Body: `speech-to-speech` 与 `voice-pro` 都把语音识别、模型调用、语音合成或翻译串成可操作流程。真正的难点不只在模型精度，还包括显存、驱动、音视频编解码、错误恢复和跨平台依赖；功能菜单很热闹，部署账单可不能装没看见。

## Top Projects

### Rank 01 - microsoft/AI-For-Beginners
- Repo URL: https://github.com/microsoft/AI-For-Beginners
- Tagline: 12 周、24 课的人工智能入门课程，包含概念、实验、测验与 Notebook。
- Stars: 58,021
- Stars Today: 949
- Forks: 11,450
- Language: Jupyter Notebook
- License: MIT
- Homepage: https://microsoft.github.io/AI-For-Beginners/
- Topics: artificial-intelligence, machine-learning, deep-learning, computer-vision, nlp, curriculum
- 技术栈: Jupyter Notebook、Python、PyTorch、TensorFlow、OpenCV
- Why It Matters Today: 位居榜首，说明系统化课程依旧是开发者进入 AI 领域的重要入口。
- 项目摘要: Microsoft 维护的初学者课程，覆盖符号 AI、神经网络、计算机视觉、自然语言处理、遗传算法和多智能体等主题，并提供 PyTorch/TensorFlow 示例与实验。
- 核心特性:
  1. 24 课渐进课程，兼顾概念、代码和实验。
  2. 支持多语言翻译，并提供 Binder 等在线运行入口。
  3. 明确列出课程覆盖范围和不覆盖范围，适合制定学习路径。
- 适用场景: AI 入门、自学计划、学校或团队内部训练营。
- 一句话推荐: 想学 AI 不知道先翻哪本砖头，这套课程先把路标立好了。
- Evidence Notes: README 明确说明 12 周 24 课、TensorFlow/PyTorch、实验和伦理内容。
- Honest Caveat: 这是课程仓库，不是生产 AI 平台；部分内容也明确提示可能不是最新 SOTA。

### Rank 02 - paperswithbacktest/awesome-systematic-trading
- Repo URL: https://github.com/paperswithbacktest/awesome-systematic-trading
- Tagline: 系统化交易的论文、软件、策略、书籍、视频和课程导航。
- Stars: 12,410
- Stars Today: 523
- Forks: 1,522
- Language: Python
- License: 未发现明确 LICENSE 文件
- Homepage: https://paperswithbacktest.com/
- Topics: awesome-list, quantitative-trading, backtesting, strategies, finance
- 技术栈: Markdown 资源索引；所收录项目涉及 Python、回测框架、券商 API 与数据分析工具
- Why It Matters Today: 量化交易学习与工具选型需求升温，但它本质上是导航集合，不是统一交易系统。
- 项目摘要: 收集系统化交易研究与实盘相关资源，README 声明包含 97 个库和包、40 多个策略、55 本书以及视频、博客和课程。
- 核心特性:
  1. 按回测、实盘、数据源、风险、机器学习等类别整理工具。
  2. 同时覆盖策略、论文、书籍和课程，便于建立研究清单。
  3. 提供中文 README 入口。
- 适用场景: 量化学习资料检索、工具初筛、研究主题导航。
- 一句话推荐: 它是地图册，不是自动提款机；找资料好使，收益率还得自己负责。
- Evidence Notes: README 明确自称 curated list，并列出资源数量。
- Honest Caveat: 未对收录项目质量、策略收益或数据授权逐项验证；不应把列表收录视为投资建议。

### Rank 03 - usekaneo/kaneo
- Repo URL: https://github.com/usekaneo/kaneo
- Tagline: 强调简洁、自托管和快速体验的开源项目管理工具。
- Stars: 5,815
- Stars Today: 760
- Forks: 494
- Language: TypeScript
- License: MIT
- Homepage: https://kaneo.app/
- Topics: react, typescript, project-management, kanban, self-hosted, hono
- 技术栈: TypeScript、React、Hono、PostgreSQL、Docker Compose
- Why It Matters Today: 今日新增 760 Stars，说明团队仍在寻找比大型协作套件更轻的自托管替代品。
- 项目摘要: Kaneo 提供看板、任务和项目管理能力，主打少而必要的功能，并允许团队自行部署以控制数据。
- 核心特性:
  1. 面向日常任务管理的清爽界面。
  2. 支持 Docker Compose 和一键部署工具。
  3. 自托管部署使用 PostgreSQL 保存业务数据。
- 适用场景: 小型产品团队、内部项目跟踪、希望数据自持的组织。
- 一句话推荐: 不想让项目管理工具反过来管理你，Kaneo 的“少点按钮”路线值得看。
- Evidence Notes: README 给出自托管定位、MIT 许可、Docker Compose 与 PostgreSQL 示例。
- Honest Caveat: 性能宣传未独立压测；升级、备份、权限治理仍需部署方自行验证。

### Rank 04 - zhaoxuya520/reverse-skill
- Repo URL: https://github.com/zhaoxuya520/reverse-skill
- Tagline: 为 AI 编程客户端提供逆向工程与授权安全测试的技能路由和工具链检查流程。
- Stars: 12,236
- Stars Today: 1,320
- Forks: 1,841
- Language: PowerShell
- License: MIT
- Homepage: https://github.com/zhaoxuya520/reverse-skill
- Topics: reverse-engineering, security-research, pentest, agent-skills, tool-routing
- 技术栈: PowerShell、Bash、Python、Node.js、Java、MCP、IDA/Ghidra/radare2 等外部工具
- Why It Matters Today: 以 1,320 Stars Today 成为今日增速第一，反映 AI Agent 的专业工作流资产正在被单独打包。
- 项目摘要: 项目通过规则、主路由、场景技能和操作契约，让 AI Agent 在处理 APK、二进制、前端加密或授权测试任务时先确定方法、权限和工具，而不是随机猜命令。
- 核心特性:
  1. 主路由按任务类型分配方法和工具。
  2. 在执行目标操作前要求初始化案例、范围与网络权限。
  3. 强调时间线、Evidence→Finding→Path 与现场日志。
- 适用场景: 已获授权的逆向分析、安全研究、CTF 环境和内部工具链标准化。
- 一句话推荐: 它先教 Agent 看路再踩油门，安全活儿里这顺序不能反。
- Evidence Notes: README 给出完整路由链和 Java/Node/Python 等前置工具。
- Honest Caveat: 它是技能与方法路由包，不是隔离沙箱；使用者必须自行确保授权、环境安全与工具合规。

### Rank 05 - microsoft/generative-ai-for-beginners
- Repo URL: https://github.com/microsoft/generative-ai-for-beginners
- Tagline: 21 课生成式 AI 应用开发课程，提供 Python 与 TypeScript 示例。
- Stars: 114,388
- Stars Today: 108
- Forks: 61,245
- Language: Jupyter Notebook
- License: MIT
- Homepage: https://microsoft.github.io/generative-ai-for-beginners/
- Topics: generative-ai, llm, prompt-engineering, rag, python, typescript
- 技术栈: Jupyter Notebook、Python、TypeScript、OpenAI API、Microsoft Foundry、Foundry Local
- Why It Matters Today: 累计 Stars 为榜单最高，继续承担生成式 AI 的入门入口角色。
- 项目摘要: Microsoft Cloud Advocates 维护的 21 课课程，分为概念学习与应用构建，覆盖模型调用、提示工程、搜索、RAG 等基础主题。
- 核心特性:
  1. 每课包含说明、示例和继续学习材料。
  2. 尽可能同时提供 Python 与 TypeScript 实现。
  3. 支持云端模型和 Foundry Local 等本地路径。
- 适用场景: 生成式 AI 入门、团队训练营、从概念过渡到小型应用原型。
- 一句话推荐: 课程像楼梯，不能替你上楼，但至少不让你抱着模型 API 在一楼转圈。
- Evidence Notes: README 明确 21 课、Python/TypeScript 示例和多种模型服务路径。
- Honest Caveat: 课程示例不是生产架构模板；云服务名称、配额和 API 可能变化，使用前需核对最新文档。

### Rank 06 - github/copilot-sdk
- Repo URL: https://github.com/github/copilot-sdk
- Tagline: 将 Copilot CLI 的 Agent Runtime 嵌入应用和服务的多语言 SDK。
- Stars: 10,313
- Stars Today: 142
- Forks: 1,389
- Language: Java（Trending 展示；仓库同时提供多语言 SDK）
- License: MIT
- Homepage: https://github.com/github/copilot-sdk
- Topics: copilot, agent, sdk, json-rpc, tool-calling
- 技术栈: TypeScript、Python、Go、.NET、Java、Rust、JSON-RPC、Copilot CLI
- Why It Matters Today: 它把成熟 Agent 运行时变成应用可调用组件，减少团队自行搭建编排循环的成本。
- 项目摘要: 各语言 SDK 通过 JSON-RPC 与 Copilot CLI 的 server mode 通信，SDK 管理进程生命周期，并暴露会话、工具、权限和模型能力。
- 核心特性:
  1. 六种语言 SDK 共用 Copilot CLI Agent 引擎。
  2. 支持 GitHub 身份验证和 BYOK。
  3. 应用可以定义自有工具、技能和权限处理器。
- 适用场景: 在开发工具、企业内部应用或自动化服务中嵌入 Agent 工作流。
- 一句话推荐: 想要 Agent 引擎，不想从零手搓规划、工具和文件编辑循环，可以从这里下手。
- Evidence Notes: README 给出 SDK→JSON-RPC→Copilot CLI 的官方架构和各语言安装方式。
- Honest Caveat: 标准使用需要 Copilot 订阅或配置 BYOK；工具权限与密钥安全仍由集成应用负责。

### Rank 07 - github/gh-stack
- Repo URL: https://github.com/github/gh-stack
- Tagline: 管理堆叠分支与逐层 Pull Request 的 GitHub CLI 扩展。
- Stars: 878
- Stars Today: 46
- Forks: 38
- Language: Go
- License: MIT
- Homepage: https://gh.io/stacks
- Topics: github-cli, stacked-prs, git, code-review, developer-tools
- 技术栈: Go、Cobra、GitHub CLI/go-gh、GraphQL、Bubble Tea、Git
- Why It Matters Today: 它把大型改动拆成小 PR 的协作方式落成可执行 CLI，而不是停留在团队规范文档里。
- 项目摘要: `gh stack` 维护有序分支链，自动推送分支、设置每层 PR 的 base、同步远端 Stack，并用本地 `.git/gh-stack` JSON 保存状态。
- 核心特性:
  1. init/add/submit/sync/rebase 等命令覆盖完整堆叠 PR 生命周期。
  2. submit 按从底到顶顺序推送并创建或更新 PR。
  3. 本地状态写入采用锁与乐观并发检查，避免并发命令覆盖。
- 适用场景: 大型功能拆分、依赖式代码评审、需要保持小 PR 的团队。
- 一句话推荐: 大改动别端一锅上桌，`gh stack` 帮你一盘一盘出菜。
- Evidence Notes: README、`cmd/submit.go`、`internal/stack/stack.go` 和 `go.mod` 可互相验证。
- Honest Caveat: 强依赖 Git 分支纪律和 GitHub 远端能力；冲突解决、权限和异常网络仍需开发者处理。

### Rank 08 - huggingface/speech-to-speech
- Repo URL: https://github.com/huggingface/speech-to-speech
- Tagline: 可替换组件的低延迟语音 Agent 管线，并暴露 OpenAI Realtime 兼容 WebSocket API。
- Stars: 10,313
- Stars Today: 442
- Forks: 1,260
- Language: Python
- License: Apache-2.0
- Homepage: https://github.com/huggingface/speech-to-speech
- Topics: voice-agent, speech-to-text, text-to-speech, realtime, local-ai
- 技术栈: Python、Silero VAD、STT、OpenAI-compatible LLM、Qwen3-TTS、WebSocket、线程与队列
- Why It Matters Today: 442 Stars Today 表明本地可控、协议兼容的语音 Agent 仍是高热度方向。
- 项目摘要: 系统把 VAD、STT、LLM 和 TTS 分成独立线程并用队列连接，每个阶段可以替换后端，客户端通过 Realtime 兼容接口接入。
- 核心特性:
  1. 四阶段可插拔语音流水线。
  2. 可连接托管模型、HF Inference、vLLM 或 llama.cpp。
  3. 提供实时 WebSocket 服务和本地试听脚本。
- 适用场景: 本地语音助手、机器人对话后端、可控的实时语音原型。
- 一句话推荐: 想换模型不用拆整台机器，这条语音流水线把接口先留好了。
- Evidence Notes: README 明确四阶段线程/队列架构、默认端点和本地运行方式。
- Honest Caveat: 端到端延迟与效果高度依赖硬件、模型和网络后端；未独立复现生产规模声明。

### Rank 09 - abus-aikorea/voice-pro
- Repo URL: https://github.com/abus-aikorea/voice-pro
- Tagline: 集成下载、音频分离、ASR、翻译、TTS 和声音克隆的 Gradio 多媒体工作台。
- Stars: 11,887
- Stars Today: 58
- Forks: 1,732
- Language: Python
- License: GPL-3.0（仓库 LICENSE；README 元数据中的 LGPL 表述与之不一致）
- Homepage: https://github.com/abus-aikorea/voice-pro
- Topics: whisper, gradio, subtitles, dubbing, voice-cloning, translation, yt-dlp
- 技术栈: Python 3.12、Gradio 6、PyTorch、Whisper/Faster-Whisper、FFmpeg、Demucs、yt-dlp、F5-TTS、CosyVoice、Kokoro
- Why It Matters Today: 它代表把多种语音模型和音视频工具组合成创作者可操作界面的工程路线。
- 项目摘要: Voice-Pro 将媒体输入、音轨提取、降噪/人声分离、字幕生成、翻译和语音合成放进一个本地 WebUI，偏向 Windows 与 NVIDIA GPU 环境。
- 核心特性:
  1. 支持文件、麦克风或 YouTube URL 作为输入。
  2. 可选择多种 Whisper 引擎生成 SRT，并把字幕回挂到视频预览。
  3. 集成多种 TTS、声音克隆和翻译后端。
- 适用场景: 视频字幕、播客转录、多语言配音与本地语音实验。
- 一句话推荐: 像把一桌语音工具装进同一个控制台，方便是方便，显卡也得有座位。
- Evidence Notes: `pyproject.toml`、`app/tab_subtitle.py` 与 `app/gradio_asr.py` 证明依赖和字幕链路。
- Honest Caveat: README 明确称当前维护可能暂停，且主要验证 Windows + NVIDIA；许可证表述存在冲突，应以 LICENSE 文件和法律审查为准。

### Rank 10 - iv-org/invidious
- Repo URL: https://github.com/iv-org/invidious
- Tagline: 不依赖 YouTube 官方 API 的开源替代前端。
- Stars: 21,700
- Stars Today: 435
- Forks: 2,435
- Language: Crystal
- License: AGPL-3.0-only
- Homepage: https://invidious.io/
- Topics: youtube, privacy, alternative-frontend, crystal, video
- 技术栈: Crystal、Kemal、PostgreSQL、SQLite、HTTP、ECR、Docker Compose
- Why It Matters Today: 成熟隐私前端重新上榜，说明去广告、少追踪和自托管访问仍有稳定需求。
- 项目摘要: Invidious 提供视频观看、订阅、历史记录、评论和开发者 API；服务端自行请求并解析 YouTube 数据，再渲染轻量页面或返回 API 响应。
- 核心特性:
  1. 无广告、无追踪，并可在不启用 JavaScript 时使用主要页面。
  2. 支持独立订阅、历史记录、数据导入导出。
  3. 提供公共实例与自托管部署方式。
- 适用场景: 隐私友好的视频浏览、自托管 YouTube 前端、第三方客户端 API。
- 一句话推荐: 它没把 YouTube 变没，只是给你换了个少些喇叭和跟踪器的门口。
- Evidence Notes: README、`src/invidious.cr`、`routes/watch.cr`、`shard.yml` 与 Compose 文件形成完整证据链。
- Honest Caveat: 上游接口变化会直接影响可用性；公共实例还涉及容量、滥用治理和合规风险。

### Rank 11 - ansible/ansible
- Repo URL: https://github.com/ansible/ansible
- Tagline: 使用 Playbook 和无 Agent 连接方式执行配置、部署与编排的自动化平台。
- Stars: 70,154
- Stars Today: 30
- Forks: 24,271
- Language: Python
- License: GPL-3.0-or-later
- Homepage: https://www.ansible.com/
- Topics: automation, configuration-management, deployment, ssh, orchestration
- 技术栈: Python、YAML Playbook、SSH、插件系统、模块执行框架
- Why It Matters Today: 当日增速不高，但它是榜单里最成熟的基础设施工具之一，代表长期工程价值而非短期新鲜感。
- 项目摘要: Ansible 通过人可读的 Playbook 描述期望操作，由控制端连接目标机器并执行模块，用于配置管理、应用部署、云资源和网络自动化。
- 核心特性:
  1. 默认利用 SSH 等现有通道，无需在远端常驻 Agent。
  2. 支持并行管理与多节点编排。
  3. 模块和插件体系覆盖多种基础设施目标。
- 适用场景: 服务器配置、应用部署、网络设备管理、重复运维流程自动化。
- 一句话推荐: 老工具不靠喊新口号吃饭，Ansible 靠的是你第二百次部署还不想手敲命令。
- Evidence Notes: 官方 README 明确设计原则、无 Agent 模式和自动化范围。
- Honest Caveat: 大规模资产、密钥管理、幂等性和变更审计需要额外治理；仓库 devel 分支不等于稳定发布版。

### Rank 12 - microsoft/TRELLIS.2
- Repo URL: https://github.com/microsoft/TRELLIS.2
- Tagline: 使用 O-Voxel 与结构化潜变量从图像生成高保真 3D 资产的研究系统。
- Stars: 10,021
- Stars Today: 107
- Forks: 1,204
- Language: Python
- License: MIT
- Homepage: https://microsoft.github.io/TRELLIS.2
- Topics: image-to-3d, generative-model, sparse-voxel, pytorch, cuda
- 技术栈: Python、PyTorch、CUDA、Diffusion Transformer、Sparse 3D VAE、O-Voxel
- Why It Matters Today: 3D 生成继续从“能生成”向复杂拓扑、PBR 材质和更高分辨率推进。
- 项目摘要: TRELLIS.2 是 40 亿参数图像到 3D 模型，使用 O-Voxel 表达开放表面、非流形和内部结构，并生成带基础色、粗糙度、金属度与透明度的资产。
- 核心特性:
  1. Sparse 3D VAE 将资产压缩到结构化潜空间。
  2. O-Voxel 处理复杂拓扑和多种表面属性。
  3. 提供推理、训练代码、预训练权重和最小示例。
- 适用场景: 3D 内容原型、游戏与设计资产研究、生成式 3D 算法评估。
- 一句话推荐: 画一张图就想长出 3D，TRELLIS.2 给了代码；显存这位门神也没下班。
- Evidence Notes: README 给出 O-Voxel、4B 模型、安装条件、示例与官方性能口径。
- Honest Caveat: 需要 Linux、CUDA 与至少 24GB NVIDIA GPU；H100 性能数据来自项目方，未独立复测。

## Language Distribution

- Python:
  - Count: 5
  - Percent: 41.7%
  - Color Hint: #3572A5
- Jupyter Notebook:
  - Count: 2
  - Percent: 16.7%
  - Color Hint: #DA5B0B
- TypeScript:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #3178C6
- PowerShell:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #012456
- Java:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #B07219
- Go:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #00ADD8
- Crystal:
  - Count: 1
  - Percent: 8.3%
  - Color Hint: #000100

## Explore Highlights

GitHub Explore 获取成功。其主体与 Trending 高度重合，以下内容仅作发现入口，不参与原始排名和 Stars Today 统计。

### Explore 1
- Title: microsoft/AI-For-Beginners
- URL: https://github.com/microsoft/AI-For-Beginners
- Kind: Trending repository
- Meta: 12 周 24 课 AI 课程
- Short Reason: 今日 Trending 第一，同时被 Explore 推荐。

### Explore 2
- Title: usekaneo/kaneo
- URL: https://github.com/usekaneo/kaneo
- Kind: Trending repository
- Meta: TypeScript · Updated 2026-08-02
- Short Reason: 自托管项目管理工具，今日增速第二梯队。

### Explore 3
- Title: github/gh-stack
- URL: https://github.com/github/gh-stack
- Kind: Trending repository
- Meta: Go · GitHub CLI extension
- Short Reason: 把堆叠 PR 协作流程落实成 CLI。

### Explore 4
- Title: huggingface/speech-to-speech
- URL: https://github.com/huggingface/speech-to-speech
- Kind: Trending repository
- Meta: Python · Local voice agents
- Short Reason: 可替换组件的实时语音 Agent 管线。

### Explore 5
- Title: iv-org/invidious
- URL: https://github.com/iv-org/invidious
- Kind: Trending repository
- Meta: Crystal · Updated 2026-08-02
- Short Reason: 成熟隐私前端重回热榜。

### Explore 6
- Title: GitHub Copilot SDK Reddit Contest Winners
- URL: https://github.com/collections
- Kind: Collection
- Meta: GitHub Explore collection
- Short Reason: 提供 Copilot SDK 应用案例补充，不改变今日榜单。

### Explore 7
- Title: TencentCloud/TencentDB-Agent-Memory
- URL: https://github.com/TencentCloud/TencentDB-Agent-Memory
- Kind: Explore/Trending continuation
- Meta: TypeScript · Agent memory hub
- Short Reason: 展示 Agent 记忆基础设施的另一个方向，但位于本报告 Top 12 之外。

### Explore 8
- Title: bytedance/deer-flow
- URL: https://github.com/bytedance/deer-flow
- Kind: Explore/Trending continuation
- Meta: Python · Long-horizon agent harness
- Short Reason: 作为长任务 Agent 工程的补充阅读入口。

## Rendering Notes

- Hero 主标题建议：GitHub 热榜日报 · 2026-08-02
- Hero 副标题建议：课程资源领跑，安全技能路由增速第一；CLI、隐私前端与本地语音工作台更值得源码深挖。
- Top 3 高亮原因：严格按 GitHub 原始排名高亮，不按编辑偏好改名次。
- 需要在 HTML 中诚实提示的降级点：Explore 与 Trending 高度重合；动态榜单为抓取快照；性能和生产能力未独立验证；Voice-Pro 许可证表述冲突。
- 不允许省略的区块：Header / Hero、4 张 Stats Cards、今日洞察、今日热门 Top 12、编程语言分布、GitHub Explore 精选、Footer。
- Top 详情固定顺序：项目摘要 → 核心特性 → 技术栈 → 适用场景 → 一句话推荐。
- 必须保留 `toggleDetail(btn)` 与 `toggleTheme()`。

## Markdown Gate 验收记录

- [x] 报告日期为 Asia/Tokyo 的 2026-08-02。
- [x] Top 12 原始顺序完整，累计 Stars 与 Stars Today 分开。
- [x] 12 个项目均包含摘要、特性、技术栈、适用场景、推荐语、Evidence Notes 与 Honest Caveat。
- [x] 语言分布数量合计 12，百分比合计约 100%。
- [x] Explore 成功并明确不参与排名。
- [x] 所有项目能力均以公开证据为边界，未把维护者性能声明写成独立验证结论。
